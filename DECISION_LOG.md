# Decision log

These are selected design and process decisions, rewritten at a general level. They show the problem, alternatives and reasoning. They do not expose the product implementation.

## 1. A bounded pause instead of stopping every action

**Problem:** “Stop the system” was too broad a requirement. Starting new work and finishing an existing agreement are different actions.

**Options considered:** stop everything together; stop only the relevant new intake; leave every action available.

**Decision:** define a bounded pause around new intake while preserving the existing agreement's completion paths.

**Why:** the intended stop should not silently change an agreement that people already accepted. Writing the distinction down also gives the builder a specific behavior to check.

**Limit:** this is a technical design requirement, not a claim that the complete prototype is secure.

## 2. Keep agreed terms fixed for an existing job

**Problem:** future improvements could be confused with permission to change an existing agreement.

**Options considered:** update all jobs together; apply new rules to future jobs; require a new agreement for changed terms.

**Decision:** an existing job keeps its agreed rules. Future versions apply to newly created jobs.

**Why:** people should be able to understand the terms they accepted without following every later product change.

**Limit:** fixed terms do not eliminate software defects. The implementation still needs review and testing.

## 3. Separate local results from testnet results

**Problem:** a local walkthrough can look convincing while leaving real wallet behavior untested.

**Options considered:** describe every successful demonstration as equivalent; label the environment and evidence separately.

**Decision:** report local simulations and actual Amoy actions as different evidence categories.

**Why:** a result is useful only when a reader can tell what it establishes.

**Limit:** a testnet result still does not establish a production payment service or an independent audit.

## 4. Resolve questions in one written response

**Problem:** individual replies can leave the builder with several versions of the requirements.

**Options considered:** answer each question in isolation; provide one consolidated response with the final choices.

**Decision:** collect the questions, make the choices and return one current response.

**Why:** it makes contradictions easier to find before implementation continues.

**Limit:** later discoveries can still require a revision. When a choice changes, the written spec should change with it.
