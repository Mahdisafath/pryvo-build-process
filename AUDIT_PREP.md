# Preparing for a security review with AI

Before paying for an independent audit, I worked through a security self-assessment checklist of about a hundred questions, using Claude Code as the builder and reviewer. This page shares the method and the lessons. It doesn't share Pryvo's code or its private findings.

**A self-assessment is not an audit.** It helps you arrive at an audit with fewer surprises, clearer scope and evidence an auditor can reuse. It doesn't prove a contract is safe.

## The loop for one check

1. **Read the exact question**, including what the checklist says to look for. Shorten it in your notes, but don't change what it asks.
2. **Find the code it concerns.** List the functions, loops, external calls or roles involved. If nothing applies, write down why.
3. **Write a test that tries to break it.** Write the test the attacker would want to run, not one that only confirms the happy path.
4. **Prove the test can fail.** Temporarily break the contract on purpose (remove a check, reorder two lines). The test must go red. Restore the code and confirm its fingerprint (hash) matches the reviewed version.
5. **Give a verdict with a reason:** Pass, Pass with a note, Fail, or Not applicable. Each comes with one or two sentences an auditor can check.
6. **Save the evidence and the next step** before moving on.

Why: a verdict without a test is an opinion, and a test that never fails proves nothing. Step 4 is the cheapest way to tell them apart.

## Lessons that changed how I test

### Attack as the trusted party, not only as a stranger

My first reentrancy test had a malicious token call back into the escrow. That proved little, because the token held no role and was rejected by the ordinary permission check. The stronger test turns the **paid party itself** (the freelancer or client) into an attacker contract that re-enters every function **with its valid role** while being paid. That test actually tests the reentrancy protection.

### Test every caller against every function, in every state

One table did more than many single tests: every possible caller × every state-changing function × every lifecycle state. Assert that each unauthorised caller is rejected with the **expected** error, and that each authorised caller always gets past the role check. A few hundred calls in one test cover most access-control questions at once.

### Look for "one failure blocks everyone"

If one transaction pays several people and any single payment can fail, the whole payout can fail. A stablecoin that can freeze addresses, or a recipient contract that refuses tokens, are typical causes. Ask what happens to the **other** people. A common fix is a fallback: pay everyone you can, and hold the failed share for that same address to claim later. Don't let anyone redirect it.

### Check the edges of time

For every deadline, test one second before, exactly at, and one second after. Make sure there's no moment when two contradictory actions are both allowed, and no moment when nothing is allowed.

### Check minimums as well as maximums

It's easy to cap the largest value and forget the smallest. Ask whether a value of 1 (one second, one unit) makes sense for every period and amount.

### Small, honest Fails are useful

When a check fails, write the issue in plain language, list two or three fix options with their trade-offs, and let the owner choose. In my case, approved fixes go into the **next version for new agreements only**, because terms already agreed in a funded escrow are never changed.

## Lessons about AI-written tests

- **The test can be wrong too.** Twice, a failing test was the test's fault: a "this call should fail" expectation was attached to a harmless lookup instead of the real call. Investigate before blaming the contract, and before "fixing" the contract.
- **Measure, then set limits.** A guessed gas limit failed. The real cost was higher for a known reason (a safety lock taken before the permission check). Record the measured number and the reason instead of loosening the test silently.
- **Know your tool's naming rules.** One test framework refuses test names that start with a reserved word. Rename it; don't skip it.

## Lessons about entering answers in a web checklist

- **Check what keyboard shortcuts do.** The checklist used number keys as answer shortcuts. Typing a note without the text box focused quietly changed an earlier answer. Fix: click the answer buttons, confirm the text box has focus (or set the text directly), then **reload and recount every section**.
- **Verify after a reload.** The screen you just clicked isn't proof. Reload, read the totals and compare them with what you expected.
- **Don't quote generated text as evidence.** Summary reports can add generic praise about features your project doesn't have.

## Working inside a usage limit

I work on a small AI plan, so the checklist was split into **numbered parts**. Each part was small and finished completely: read, test, verdict, save. Each one ended by recording "what's done, the evidence, the next part" in a resume note. I could stop at any moment and continue in a fresh session without re-explaining anything.

## What to give the auditor

- The exact reviewed commit and file hashes, plus which files are in and out of scope.
- Each check's verdict, reason and test name.
- Open findings with their chosen fix and status (planned, built, retested).
- Plain limits: what was not tested, which tools were not rerun, and anything simulated.

Use the [security check template](templates/SECURITY_CHECK.md) for one check at a time.
