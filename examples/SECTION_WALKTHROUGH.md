# Synthetic walkthrough: completing a shared task

**Entirely illustrative.** This task-board project, its decisions and its results are invented to demonstrate the writing method. Nothing on this page is a Pryvo feature, executed test or observed participant result.

## The brief

**Section:** complete one shared task. **User problem:** a teammate cannot tell whether pressing Complete actually saved the change. **Outcome:** an authorized teammate can complete an open task once and still see it completed after refresh.

**Starting point:** assume a disposable local task-board prototype with one open task and an existing permission rule. **Included:** completion feedback, persistence and repeat-click handling. **Excluded:** notifications, task reassignment and production deployment. **Preserve:** people without edit permission cannot change the task.

**Authority:** local editing and disposable test data only. Stop if the work requires production access or a new external service. Ask the reviewer about a changed scope, while continuing independent documentation.

## Acceptance plan

| Criterion | Check | Setting | Expected result |
|---|---|---|---|
| Complete an open task | Authorized person presses Complete, then refreshes | Local prototype | Task remains completed; one completion entry |
| Repeat completion | Repeat the request | Local prototype | No second completion entry |
| Preserve permission | Person without edit permission tries completion | Local prototype | Task unchanged; clear refusal |
| Handle a failed save | Simulate a failed response, then inspect saved state | Local prototype | UI does not claim success without evidence; recovery guidance is clear |
| Explain the action | Ask a participant what Complete will do before pressing it | Participant session | They explain the task change and persistence in their own words |

## An illustrative discovery and decision

**Discovery:** the screen says Done before the save response arrives. **Options:** leave the optimistic message; add a pending state with failure recovery. **Choice:** show Saving until success is confirmed, then show Completed. **Reason:** the status should describe what is known. **Trade-off:** an extra visible state needs clear wording.

## An illustrative result report

Suppose the builder observes completion persistence, one history entry after a repeat request, permission refusal and correct failure feedback in local checks. Report those four local outcomes separately from the participant criterion.

Suppose no participant has tried it. The report should say **participant understanding unverified**, with section acceptance still pending. Four local passes do not satisfy five criteria. The reviewer could later accept the local demonstration with that explicit limitation; the participant result would still remain unverified.

Do not use the suppositions above as real test evidence. In a real report, add actual dates, the reviewed version and evidence references.

## Handoff and public lesson

The next authorized action is to prepare the short participant task. Sending invitations needs the relevant authorization. Production deployment remains outside this section.

A public lesson could explain why a pending state matters using newly authored wording and fake tasks. Keep participant identities, internal board records, access information and private source out of the public packet. Review and scan the exact files/history, then verify the uploaded revision.

Copy the [section brief](../templates/SECTION_BRIEF.md) and [checklist](../templates/SECTION_CHECKLIST.md) to write your own packet. Return to the [practical guide](../GUIDE.md) for the reasons behind each step.
