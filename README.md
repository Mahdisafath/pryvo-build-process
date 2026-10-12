# How I build Pryvo with AI

**Vibe coding with security checks.**

**Status: Pryvo is an unaudited prototype on Polygon Amoy testnet. It is not on mainnet and is not for real funds.**

I'm Safath, the founder of [Pryvo](https://pryvo.io). I'm building an escrow and payments prototype with AI assistance: Claude helps me plan; Codex helps me implement and check the work. I define the requirements, make the trade-offs and review the evidence.

This repository shares my method, reusable writing templates and lessons from the build. The Pryvo product implementation is kept separately. You can reuse the materials here for your own project.

> A useful AI request explains the problem, the limits and what would count as a checked result.

## Start here

| You want to… | Read |
|---|---|
| Understand my approach in two minutes | [How I work](HOW_I_WORK.md) |
| See the reasoning behind decisions | [Decision log](DECISION_LOG.md) |
| See problems and how they were checked | [Problem solving](PROBLEM_SOLVING.md) |
| Understand the evidence and its limits | [Evidence](EVIDENCE.md) |
| Try the method on your project | [Synthetic task-board example](examples/SHARED_TASK_BOARD.md) |

The working sequence is **problem → spec → questions → build → checks → review**.

## Reuse the method

Start with the [build-spec template](templates/BUILD_SPEC.md). Resolve the builder's questions with the [review-response template](templates/REVIEW_RESPONSE.md), then request the [result report](templates/RESULT_REPORT.md). My general [working rules](rules/WORKING_RULES.md) explain the standards behind these steps.

“Security checks” describes a working practice. It does not mean that the prototype is secure, independently audited or ready for real payments.

Follow the build on [X](https://x.com/MahdiSafath). Suggestions about the teaching materials are welcome; see [Contributing](CONTRIBUTING.md).

Licensed under the MIT License. Unaudited prototype; do not use with real funds.
