# Worked example: a shared task board

**Entirely synthetic teaching example.** This is not a Pryvo feature, actual customer story or implemented project. No result below is presented as a test that has been run.

## Initial request

“Let people archive a finished task.”

That request leaves several decisions open. Does archive mean delete? Can the task be restored? What happens to existing activity notes?

## A clearer spec

**Problem:** finished tasks crowd the board, but people still need to find their history.

**Outcome:** move a finished task out of the active view while keeping its contents available.

**Required behavior:** archive keeps the title and activity notes; the archived view can show the task; restore moves it back; a failed request leaves the current task visible.

**Outside this task:** permanent deletion, bulk actions and changes to notifications.

## Consolidated answers

| Question | Choice | Reason |
|---|---|---|
| Does archive delete the task? | No | The goal is a quieter active view while retaining history |
| Is restoring allowed? | Yes | An accidental archive should be reversible |
| What happens if the request fails? | Keep the current view and explain the failure | The interface should reflect what actually happened |

## Verification to request

Ask the builder to exercise archive, restore and the failed-request case. Compare the resulting view with the stored task state. Record the setting and any case that was not exercised.

## How to report it honestly

An example report might say: “Archive and restore were exercised locally; a failed request left the task visible. Shared-user behavior has not been checked.”

That sentence is illustrative, not a result obtained for this example. Its purpose is to show how the scope of a claim can stay narrow.
