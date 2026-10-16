# How I work

I use AI for planning and implementation. My job is to make the intended behavior clear, resolve trade-offs and decide whether the reported result answers the original request.

## 1. Explain the problem before choosing the implementation

With Claude, I describe who needs the feature, what goes wrong today and what a useful result would look like. I ask about alternatives and unclear assumptions.

Why: a fast implementation of an unclear request can create more work later.

## 2. Turn the discussion into a written spec

I write the expected behavior, constraints, exclusions and acceptance criteria. I distinguish required outcomes from suggestions about how to build them.

Why: the builder needs a stable target. A conversation alone is easy to interpret differently.

## 3. Give Codex a bounded task

Codex inspects what already exists, identifies gaps and implements the agreed part. I ask it to make the result reviewable and state what remains unverified.

Why: a smaller change is easier to understand and check.

## 4. Answer review questions together

When the builder raises several questions, I work through them and return one consolidated response. Each answer names the choice, its reason and anything it changes in the original spec.

Why: scattered answers can contradict each other. A single response makes the current decision easier to follow.

## 5. Check behavior in the right setting

Local checks come first. For the prototype's blockchain flows, a testnet walkthrough is a separate step. I expect the report to distinguish simulated behavior from actions that actually happened on Amoy.

Why: a local simulation cannot establish that a real wallet journey worked.

## 6. Review results and retain the lesson

I compare the result with the acceptance criteria, review any limits and record what changed. I use that record when choosing the next bounded task.

Why: progress is easier to build on when the reasoning and evidence survive the session.

## What this method establishes

The method helps me direct and review AI-assisted work. It does not make AI output automatically correct or replace independent expertise. Passing checks are evidence about their stated scope, not a guarantee about the whole product.

The [example](examples/SHARED_TASK_BOARD.md) shows how to apply this method without needing the Pryvo implementation.

## Apply this section by section

The [practical guide](GUIDE.md) expands this loop into nine practices learned during the prototype build. Copy its [section brief](templates/SECTION_BRIEF.md) to define one bounded outcome, record decisions as work progresses and hand off an honestly qualified result. Use the [checklist](templates/SECTION_CHECKLIST.md) to keep incomplete checks visible.
