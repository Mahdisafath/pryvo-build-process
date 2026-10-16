# Build with AI in sections: a practical guide

For founders and small teams who want useful progress they can explain and check. This guide turns lessons from Pryvo's prototype work into a method you can reuse on an unrelated project.

As of **16 October 2026**, our first eight prototype sections are recorded complete. The ninth, interface and direct-access review, is accepted for the demonstration scope with explicit limitations: independent participant tasks, a new current-interface external reviewer trial and detailed device/accessibility coverage remain unverified. These lessons include corrections and unfinished learning. This guide does not establish final prototype completion. Pryvo remains unaudited, on Polygon Amoy testnet and unsuitable for real funds.

## Start in five minutes

Copy the [section brief](templates/SECTION_BRIEF.md). Write one user outcome, the limits and three observable checks. Agree what the builder can do, then work through the [section checklist](templates/SECTION_CHECKLIST.md). The [synthetic example](examples/SECTION_WALKTHROUGH.md) shows a complete written packet.

The loop is **define → build → check → record → review → choose the next section**. A section is small enough to review and has a clear finishing condition. It need not equal one chat or one day.

## 1. Define the responsibility before the mechanism

We learned to separate what an operator may do from what an existing agreement permits. Broad phrases such as “manage the system” hide important differences.

For any project, name the actor, action and limit. In a shared task board, a coordinator might stop new task creation while people can still finish existing tasks. Write both behaviors before choosing an implementation.

**Put in the brief:** who can act, what changes, and what existing behavior must remain available.

## 2. Check readiness before starting the journey

A correct feature can still be impossible to exercise if the test environment or required role is unavailable. Readiness work deserves its own result rather than being assumed.

For your project, confirm the intended environment, disposable test data and required access. An account being available does not prove every later action works.

**Put in the brief:** prerequisites, how they will be checked, and the point at which work must stop if they fail. Keep actual credentials out of the document.

## 3. Rehearse, then describe the rehearsal accurately

An isolated rehearsal helped uncover problems before external execution. It established simulated behavior, within that rehearsal's limits.

Use local or disposable environments where appropriate. Then ask what changes when a real browser, device or external service is involved. Keep that separate check visible.

**Put in the report:** the setting for every result. A local test, an isolated fork, an actual testnet action and a physical-device observation answer different questions.

## 4. Keep changes within the agreed scope

During external testing, observed conditions sometimes differed from rehearsal. We paused when a bound no longer matched and reviewed the specific change before continuing.

Agree the actions, destination, time or cost limits and exclusions. If one limit needs changing, describe that change and its reason. Keep authorization for an unchanged section usable; seek a new decision when its scope or limits change.

**Put in the brief:** what the builder may do now, what requires another decision, and which conditions require a pause. A completed section does not authorize the next external action.

## 5. Check the final state after the successful action

A successful click was only part of the evidence. We also checked the resulting state and whether an action could accidentally finish twice.

For a task board, verify that a completed task stays completed after refresh and that repeating completion does not create another history entry. Define the result in terms a user can observe.

**Put in the acceptance criteria:** the expected final state, any remaining obligation, and the expected response to a duplicate action.

## 6. Include absence, cancellation and late actions

A normal journey does not explain what happens when someone never responds or an operation cannot finish. Refund, silence and expiry testing made those omissions visible in the prototype.

For another app, consider cancellation, an unanswered request, a missing permission and a deadline. Decide what each should do before calling the feature complete.

**Put in the check plan:** at least one normal path, one failure or cancellation path, and one timing or repetition case when relevant. Choose checks for the behavior and risk; avoid tests that only restate the implementation.

## 7. Write ambiguous decisions down

Disagreement and changing proposals revealed why the current accepted choice needs a clear record. “We discussed it” is difficult for the next session to use.

Record the choice, the reason and the alternative you declined. If a later discovery changes the choice, update the current specification and preserve a dated explanation. Check that older accepted items still behave as promised when that matters to the product.

**Put in the decision record:** problem, options, chosen behavior, trade-off and effect on existing work. Keep confidential reasoning private.

## 8. Define completion with evidence and limitations

The governance and isolation work required reconciliation across multiple checks. A green summary alone would have hidden skipped or unavailable evidence.

Use a small table mapping each acceptance criterion to an observation, setting and limitation. Mark incomplete work as incomplete. If a limitation is acceptable for a demonstration, the responsible person must explicitly accept it; that does not turn the missing check into a pass.

**Put in the report:** passed, failed, skipped and unverified items; where the evidence is retained; and the next concrete action. Tool scans are scoped checks, not an independent audit.

## 9. Simplify when the interface teaches the wrong thing

Our interface work exposed a confusing demonstration: example actions could be mistaken for real wallet-funded actions. The participant experience was simplified into a clearly labelled wallet-free example, while actual testnet tools remained separate.

For your app, ask a person to explain what the next action will do before they use it. If they misunderstand, fix the wording or flow and try again. A pleasant screenshot does not establish understanding. An emulated phone viewport and a general physical-device report do not establish independent participant task success.

**Put in the check plan:** a short user task, expected understanding and the observed outcome. Keep early positive feedback distinct from acceptance. This remains an open learning area even though the ninth section was accepted for its demonstration scope.

## Keep a record another session can use

At meaningful milestones, record the requirement, decision and reason, reviewed artifact version, checks, limits and next action. Update the current focus when it changes. Retain a concise handoff rather than a raw conversation dump, and verify the file was saved before reporting it saved.

A useful handoff lets another builder answer: What is true now? What is unfinished? What can I do next? What needs a decision?

## Publish the lesson deliberately

Write a fresh explanation and synthetic example for public readers. List the exact files being published, read every changed line, scan both those files and the history being pushed, then verify the remote version and intended visibility.

Keep product source, private notes, confidential plans, personal data and operating details in their appropriate private stores. Credentials and recovery material do not belong in any repository. A clean secret scan cannot decide whether a business detail is appropriate to disclose; that needs a content review.

After uploading, compare the published files with the reviewed version. Distinguish a local commit, a remote upload, a merged change and a running deployment in your report.

## What this guide can establish

These are maintainer-reported process lessons checked against private build records. This repository supplies reusable teaching materials, not product source or an independently reproducible audit. See [Evidence and limits](EVIDENCE.md). Adapt the method to your project's risks; the method cannot guarantee correctness, security or successful user adoption.
