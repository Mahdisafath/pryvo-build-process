# Problem solving

Three selected stories from the prototype work. The tasks below summarize the work's intent; they are not quotations from conversations.

## 1. The wallet was connected, but the interface disagreed

**Problem:** during the actual wallet walkthrough, a connection update left the interface with inconsistent connection state. The intended next step could not proceed.

**Task:** complete a clear client-to-freelancer wallet journey and check the interface against the result.

**AI work:** Codex traced the connection timing and corrected how the connected wallet and account were assigned.

**How it was checked:** the walkthrough was resumed with the test roles; the completed Amoy happy path was read back and compared with the interface. The report kept the interface fix separate from the contract behavior.

**Lesson:** treat a convincing interface as something to verify against the underlying state.

## 2. A simulated payment looked like a complete product flow

**Problem:** the local demo could perform several outcomes, but the participant's role and the evidence category needed to be clearer.

**Task:** make the client and freelancer steps understandable, then check what the demonstration actually proves.

**AI work:** Codex added explicit role-specific guidance, clearer progress labels and refresh/reconnection handling.

**How it was checked:** local browser walkthroughs and integration checks covered the job journey. The record explicitly said that these were local role simulations. A later actual Amoy wallet journey was reported separately.

**Lesson:** make the next action clear without overstating what a demonstration establishes.

## 3. A successful result did not justify repeating the action

**Problem:** payment flows need to distinguish a finished outcome from an action that remains available to repeat.

**Task:** verify the completed outcome, including the amount left in escrow, and check that a duplicate final action is rejected.

**AI work:** Codex checked recorded transaction outcomes and read the final accounting independently.

**How it was checked:** the Amoy happy-path record showed a terminal job and zero locked principal. A read-only duplicate completion attempt was rejected; it did not create a second paid transaction.

**Lesson:** define “done” in terms of the resulting state and remaining obligation, not only a successful click.

These summaries are maintained from the build records. This repository does not provide product source or a complete independent reproduction of those checks. See [Evidence](EVIDENCE.md) for dates and limits.
