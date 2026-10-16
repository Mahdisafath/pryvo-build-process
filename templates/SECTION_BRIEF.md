# Section brief and handoff template

Copy for one bounded section. Replace every bracketed field. This is a blank teaching template, not a Pryvo implementation specification. Keep a complete internal version where appropriate; author a separate sanitized version for public sharing.

## 1. Outcome and starting point

- Section name and date: [name; date; time zone if relevant]
- Responsible reviewer: [role]
- User problem: [one concrete situation]
- Intended outcome: [what the person can do]
- Current verified behavior: [observation and date]
- Reviewed starting version: [artifact or revision]
- Status: [planned / in progress / blocked / complete with stated scope]

## 2. Scope and authority

- Included: [specific actions and deliverables]
- Excluded: [work reserved for another section]
- Existing behavior to preserve: [observable behavior]
- Builder may proceed with: [authorized actions]
- Additional decision required for: [scope changes or external actions]
- Limits: [environment, time, cost or other applicable bound]
- Stop if: [concrete condition]
- Open choices: [question; responsible role; what can continue meanwhile]

Do not put passwords, account recovery material or access tokens in this brief. Refer to an approved access process without copying its sensitive contents.

## 3. Acceptance and check plan

| Criterion | Check or user task | Required setting | Expected observation | Evidence location |
|---|---|---|---|---|
| [normal outcome] | [steps] | [local/device/external] | [specific result] | [safe reference] |
| [failure or cancellation] | [steps] | [setting] | [specific result] | [safe reference] |
| [repetition, timing or existing behavior, if relevant] | [steps] | [setting] | [specific result] | [safe reference] |

For interface work, include what the person should understand before acting. Choose meaningful checks proportional to the change. A rehearsal does not satisfy a criterion requiring actual external execution.

## 4. Decision record

- Problem or discovery: [what changed our understanding]
- Options: [real alternatives]
- Choice and reason: [decision; why it fits]
- Trade-off or remaining risk: [limit]
- Effect on agreed scope: [unchanged / exact amendment and decision]
- Current source of truth updated: [safe reference]

## 5. Result and verification

- Implemented change: [what changed and why]
- Reviewed final version: [artifact or revision]

| Criterion | Date and setting | Observed result | Passed / failed / skipped / unverified | Limit |
|---|---|---|---|---|
| [criterion] | [actual date; environment] | [observed fact] | [status] | [what remains unknown] |

- Final state: [what is true after the action]
- Remaining obligation: [unfinished work, if any]
- Repetition behavior, if relevant: [observed response]
- Checks not rerun: [which; why they are outside this change]

Report what happened, including failures. Do not turn an expected result into an observed result. A scan is not an independent audit; a testnet result is not production readiness.

## 6. Acceptance and next action

- Reviewer decision: [pending / accepted / changes requested]
- Accepted limitations: [exact limitation, deciding role and date, or none]
- Missing checks remain labelled: [unverified items]
- Current focus and session record saved and read back: [reference; verified / pending]
- Proposed next section: [name and bounded outcome]
- Next section authority: [already authorized / awaiting decision]
- Immediate next action: [specific action within existing authority]

## 7. Publication record, when applicable

- Audience and destination: [private/public; repository or other destination]
- Exact file allowlist: [paths of reviewed files]
- Withheld material: [categories and reasons; no sensitive values]
- Content and disclosure review: [what was inspected; outcome]
- Secret scan scope and result: [files; history if public; tool/version; outcome]
- Links and claim checks: [what was checked; outcome]
- Authority to publish this content: [current instruction or decision]
- Reviewed revision: [identifier]
- Uploaded revision and remote file comparison: [verified / pending]
- Visibility and unpublished-work check: [result]
- Running deployment, if applicable: [separate verification or not applicable]

Keep approval records and sensitive verification details in the appropriate private store. A successful upload establishes publication of that revision, not deployment of a working service.
