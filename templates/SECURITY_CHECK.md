# Security check record — template

Copy this for each checklist question. Keep one record per check, or one per small group of related checks.

## Check

- **ID and question:**
- **Severity (as given by the checklist):**
- **Reviewed version:** commit and file hashes
- **In scope / out of scope:**

## Where it applies

- Functions, loops, external calls or roles involved:
- If nothing applies, why:

## Evidence

| Test name | What it tries to break | Result |
|---|---|---|
| | | |

- **Can the test fail?** Mutation tried: (e.g. "removed the role check in X"). Did the test go red? Code restored and hash confirmed?
- **Measured values** (gas, limits, timings), and why they are what they are:

## Verdict

- [ ] Pass
- [ ] Pass with a note
- [ ] Fail (severity, plain-language description)
- [ ] Not applicable

**Reason (1–2 sentences an auditor can check):**

## If it fails

| Option | What it means | Trade-off |
|---|---|---|
| A | | |
| B | | |

- **Owner's decision and date:**
- **Applies to:** (e.g. next version, new agreements only)

## Limits

- Not tested:
- Tools not rerun, and why:
- Simulated rather than real:

## Next

- Next check or part:
