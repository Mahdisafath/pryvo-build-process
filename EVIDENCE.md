# Evidence and limits

Snapshot: **16 October 2026**. Pryvo is an unaudited Polygon Amoy testnet prototype, not a mainnet payment service and not for real funds.

## Selected build results

| Date | Setting | Recorded result | What it establishes |
|---|---|---|---|
| 6 October 2026 | Local simulation | Browser job journeys and the associated integration check passed | The local participant flow was exercised; this was not a real testnet wallet journey |
| 8 October 2026 | Actual Amoy wallet journey | Six actions completed one job; the final job was terminal with zero principal locked | One complete test-wallet happy path was exercised and read back |
| 9 October 2026 | Actual Amoy wallet journeys | Thirteen actions completed refund, silent-client and unfunded-expiry cases; each finished with zero principal locked | Those stated testnet paths were exercised |
| 11 October 2026 | Local regression | 128 Foundry checks passed, zero failed; three historical or optional fork checks were skipped | The stated local suite passed; skipped checks are not counted as passes |
| 12 October 2026 | Isolated Amoy fork | A remaining 56-action route passed with 34 expected rejection checks | A simulated continuation was exercised; it does not claim the corresponding public actions happened |
| 14 October 2026 | Actual Amoy acceptance | The bounded eighth section finished its recorded governance, pause and isolation route; final accounting was reconciled | The stated testnet section completed; it does not establish production readiness. Exact historical timing replay was unavailable for some checks; local boundary checks remained separately labelled |
| 16 October 2026 | Local participant interface and founder feedback | The participant demonstration uses examples without a wallet; local browser checks and general Mac/iPhone feedback are recorded | General device feedback is distinct from independent participant tasks; broader device coverage and current-interface external reviewer acceptance remain unverified |

The first eight prototype sections are recorded complete. Section 9 was subsequently accepted on 16 October for the demonstration scope with the three evidence gaps above retained as unverified follow-up work. Final prototype completion is not claimed by this documentation release. The new [guide](GUIDE.md) teaches lessons from both completed work and unfinished learning. This update reviews existing records; no contract tests, chain checks or independent audit were performed for the documentation release.

The tests above are from different dates and scopes. The regression count is not a count of public transactions. The fork route is not another completed public deployment.

## The fund-control claim

The reviewed job-escrow implementations have no privileged admin withdrawal or override function. Existing jobs keep their destinations and agreed rules. This claim concerns the designed authority boundary: valid payment, refund, settlement, dispute and timeout actions can still move funds under those rules, including any agreed fee.

It is not a claim that funds are inaccessible under every circumstance or that bugs and dependency failures are impossible. The prototype remains unaudited.

## How to interpret this page

These are maintainer-reported summaries checked against the project's build records. The product source, deployment scripts and raw records are not part of this teaching repository. Deployment addresses and explorer links are also omitted from this version. Readers cannot independently reproduce or audit the product from these files.

Passing tests, recorded walkthroughs and tool checks do not establish independent audit completion, real customer use or production readiness. Testnet work uses test assets only.

## A result report worth asking for

For your own project, record the date, setting, requested behavior, observed result, failed or skipped checks and unresolved limits. The [result-report template](templates/RESULT_REPORT.md) is a reusable starting point.
