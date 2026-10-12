# Evidence and limits

Snapshot: **12 October 2026**. Pryvo is an unaudited Polygon Amoy testnet prototype, not a mainnet payment service and not for real funds.

## Selected build results

| Date | Setting | Recorded result | What it establishes |
|---|---|---|---|
| 6 October 2026 | Local simulation | Browser job journeys and the associated integration check passed | The local participant flow was exercised; this was not a real testnet wallet journey |
| 8 October 2026 | Actual Amoy wallet journey | Six actions completed one job; the final job was terminal with zero principal locked | One complete test-wallet happy path was exercised and read back |
| 9 October 2026 | Actual Amoy wallet journeys | Thirteen actions completed refund, silent-client and unfunded-expiry cases; each finished with zero principal locked | Those stated testnet paths were exercised |
| 11 October 2026 | Local regression | 128 Foundry checks passed, zero failed; three historical or optional fork checks were skipped | The stated local suite passed; skipped checks are not counted as passes |
| 12 October 2026 | Isolated Amoy fork | A remaining 56-action route passed with 34 expected rejection checks | A simulated continuation was exercised; it does not claim the corresponding public actions happened |

The tests above are from different dates and scopes. The regression count is not a count of public transactions. The fork route is not another completed public deployment.

## The fund-control claim

The reviewed job-escrow implementations have no privileged admin withdrawal or override function. Existing jobs keep their destinations and agreed rules. This claim concerns the designed authority boundary: valid payment, refund, settlement, dispute and timeout actions can still move funds under those rules, including any agreed fee.

It is not a claim that funds are inaccessible under every circumstance or that bugs and dependency failures are impossible. The prototype remains unaudited.

## How to interpret this page

These are maintainer-reported summaries checked against the project's build records. The product source, deployment scripts and raw records are not part of this teaching repository. Deployment addresses and explorer links are also omitted from this version. Readers cannot independently reproduce or audit the product from these files.

Passing tests, recorded walkthroughs and tool checks do not establish independent audit completion, real customer use or production readiness. Testnet work uses test assets only.

## A result report worth asking for

For your own project, record the date, setting, requested behavior, observed result, failed or skipped checks and unresolved limits. The [result-report template](templates/RESULT_REPORT.md) is a reusable starting point.
