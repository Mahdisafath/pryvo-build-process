# How I build Pryvo with AI

**Vibe coding with security checks.**

**Status: Pryvo is an unaudited prototype on Polygon Amoy testnet. It is not on mainnet and is not for real funds.**

I'm Safath, the founder of [Pryvo](https://pryvo.io). I'm building an escrow and payments prototype with AI assistance: Claude helps me plan; Codex helps me implement and check the work. I define the requirements, make the trade-offs and review the evidence.

This repository shares my method, reusable writing templates and lessons from the build. The Pryvo product implementation is kept separately. You can reuse the materials here for your own project.

## Funds locked by agreed rules

In the prototype, each funded job keeps its payment in its own fixed smart-contract escrow. That escrow has no privileged admin withdrawal or override function. Pryvo's founder and admins cannot choose a new destination for an existing job's funds or rewrite its agreed payout rules.

Funds leave through the defined payment, refund, mutual settlement, dispute or timeout routes, including any agreed fee. A permitted caller can trigger a route only under those rules; triggering it does not give the caller an arbitrary withdrawal right.

My ambition is to build payment agreements people can understand and trust. I work toward that through explicit requirements, tests and careful review. The prototype is still unaudited, and software and its dependencies can still fail.

> A useful AI request explains the problem, the limits and what would count as a checked result.

## Start here

| You want to… | Read |
|---|---|
| Understand my approach in two minutes | [How I work](HOW_I_WORK.md) |
| See the reasoning behind decisions | [Decision log](DECISION_LOG.md) |
| See problems and how they were checked | [Problem solving](PROBLEM_SOLVING.md) |
| Understand the evidence and its limits | [Evidence](EVIDENCE.md) |
| Learn from the section-by-section build | [Practical guide](GUIDE.md) |
| Copy a complete section packet | [Section brief](templates/SECTION_BRIEF.md) · [Checklist](templates/SECTION_CHECKLIST.md) |
| See a worked section packet | [Synthetic walkthrough](examples/SECTION_WALKTHROUGH.md) |
| Try the method on your project | [Synthetic task-board example](examples/SHARED_TASK_BOARD.md) |

The working sequence is **problem → spec → questions → build → checks → review**.

## Reuse the method

Start with the [build-spec template](templates/BUILD_SPEC.md). Resolve the builder's questions with the [review-response template](templates/REVIEW_RESPONSE.md), then request the [result report](templates/RESULT_REPORT.md). My general [working rules](rules/WORKING_RULES.md) explain the standards behind these steps.

“Security checks” describes a working practice. It does not mean that the prototype is secure, independently audited or ready for real payments.

Follow the build on [X](https://x.com/MahdiSafath). Suggestions about the teaching materials are welcome; see [Contributing](CONTRIBUTING.md).

Licensed under the MIT License. Unaudited prototype; do not use with real funds.
