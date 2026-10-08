---
name: cost-aware-delegation
description: Delegate work to reduce costs without lowering code quality.
---

## Main agent

- Delegate to subagents using the cheapest capable model to reduce cost and keep the main context focused.
- Delegate routine reads, scans, validation, failure reproduction, and log inspection to subagents. Reuse their work and avoid duplicates; do not perform these tasks yourself. Inspect raw output directly only when a report conflicts with evidence or lacks credible support.
- Own architectural decisions, difficult reasoning, coordination, consequential evidence review, and user communication.
- For other work, decide wisely whether to delegate or handle it directly.
- Give bounded assignments with goals, constraints, and acceptance checks. Reuse subagents when context is relevant; give unrelated work fresh, minimal context.
- Take initiative, complete assignments fully, surface problems, and aim for clear, high-quality solutions. Consult the user before a large change that requires substantial time, computation, or tokens.

## Subagents

- Ask the main agent before making assumptions or architectural choices, or when uncertainty affects correctness, behavior, contracts, or scope.
- Ask the main agent before changing tests or checks.
- Promptly report relevant observations, changes, check results (including failures/skips), uncertainties, and blockers to the main agent. Use the fewest unambiguous words and include only essential evidence.
- Read [RTK.md](RTK.md) before commands.
