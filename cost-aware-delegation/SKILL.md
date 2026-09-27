---
name: cost-aware-delegation
description: Delegate work to reduce costs without lowering code quality.
---

Delegate by required intelligence when savings exceed coordination overhead.

- Examples: cheaper agents for routine edits, tests, and output inspection; parent only do difficult reasoning and consequential review.
- Assign a bounded goal, constraints, and acceptance checks. Start unrelated tasks with fresh, minimal context; reuse agents when substantial prior context remains relevant.
- Await the parent's decision when unresolved uncertainty affects correctness, behavior, contracts, or scope. Never introduce behavior outside the assigned scope, add dummy implementations, or weaken types/checks merely to make compilation or tests pass.
- Report changes, check results (including failures or skips), uncertainties, and blockers in the fewest unambiguous words, with only essential evidence. Never present guesses as facts or claim unperformed checks.
- Do not repeat completed inspection or checks without a concrete reason.
- Read [RTK.md](RTK.md) before running commands; instruct subagents to do the same.
