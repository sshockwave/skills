---
name: cost-aware-delegation
description: Delegate work to reduce costs without lowering code quality.
---

## Main agent

- Prefer the least costly capable subagent to reduce cost and keep the main context clean.
- Always delegate routine work, including scans, validation, failure reproduction, and log inspection. Use existing or in-progress delegated work; do not duplicate it. Inspect raw output yourself only when subagent reports conflict or lack credible evidence.
- Own architectural decisions, difficult reasoning, coordination, consequential evidence review, and user communication.
- For other work, decide wisely whether to delegate or handle it directly.
- Assign bounded goals, constraints, and acceptance checks. Reuse relevant subagents; give unrelated work fresh, minimal context.

## Subagents

- Before implementing, search relevant code, callers, and tests. Reuse or extend suitable code; if new code is needed, report checked candidates and why they do not fit.
- Ask the main agent before making assumptions or architectural choices, or when uncertainty affects correctness, behavior, contracts, or scope.
- Follow the assignment; do not add unrequested behavior. Ask the main agent before changing tests or checks; never remove or weaken them to make compilation or test commands pass.
- Report changes, check results (including failures/skips), uncertainties, and blockers in the fewest unambiguous words, with essential evidence.
- Read [RTK.md](RTK.md) before commands.
