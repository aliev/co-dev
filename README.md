# co-dev

Human-in-the-Loop Implementation Protocol for pairing domain experts with LLM collaborators on tightly scoped engineering tasks.

## Overview
`co-dev` captures a battle-tested workflow for guiding language models through incremental software delivery. The protocol keeps humans in control—approving scope, reviewing diffs, and gating commits—while the LLM executes small, auditable steps. Use this repository as the control plane for engagements with autonomous or semi-autonomous coding agents.

## Why This Exists
- **Safety:** Prevents runaway changes by enforcing describe-before-code approvals and single-purpose commits.
- **Traceability:** Every decision, command, and status update is documented in the plan, making handoffs and audits painless.
- **Repeatability:** Standard templates let any contributor (human or model) join mid-stream and immediately understand expectations.

## Repository Layout
- `PLAN.md` – live implementation plan for the current milestone or ticket; update statuses (`pending → in-progress → committed`) as work progresses.
- `IMPLEMENTATION_PLAN_TEMPLATE.md` – scaffold for new plans, including collaboration rules, status vocabulary, acceptance criteria blocks, and Conventional Commit guidance.
- `AGENTS.md` – contributor handbook summarizing structure, coding style expectations, test policy, and commit/PR rules for LLM agents and humans alike.
- `LICENSE` – MIT license.

## Getting Started
1. Fork or clone this repo and create a working branch for the initiative.
2. Duplicate `IMPLEMENTATION_PLAN_TEMPLATE.md` into a new plan file (or update `PLAN.md`) with project-specific context, best practices, and step log entries.
3. Share the plan with your LLM collaborator. Require them to follow the describe-before-code loop, request approvals, and record status transitions before touching code.
4. During implementation, mirror results back into the plan (tests run, commits made) and keep `AGENTS.md` handy for process reminders.

## Execution Workflow
1. **Describe:** LLM outlines the intended changes for one step and awaits human approval (`Status: pending`).
2. **Implement:** After approval, the LLM switches the step to `in-progress`, edits code, and runs the plan’s mandated checks.
3. **Review:** LLM proposes a Conventional Commit message (`type(scope?): subject`) with a short body documenting key changes and validations. Human reviews diffs and either requests revisions or grants final approval.
4. **Commit:** When instructed (e.g., `# HUMAN: final — please commit this step`), the LLM commits, updates the plan to `committed`, and asks to proceed to the next step.
5. **Closeout:** Once all steps are committed, the human reviews the plan, confirms completion, and merges using standard GitHub/Git tooling.

## Best Practices
- Keep steps bite-sized—favor additional plan entries over broad commits.
- Capture every test, lint, or build command in the plan so future runs are reproducible.
- Maintain ASCII-only files unless the project explicitly requires Unicode elements.
- When scope expands, split the plan before writing code to preserve reviewability.

## Contributing
Refer to `AGENTS.md` for coding standards, testing expectations, and Conventional Commit conventions. External contributions should open a PR referencing the relevant plan section, summarize functional impact, list risk mitigations, and attach evidence (logs, screenshots) when useful.

## License
`co-dev` is distributed under the MIT License. See `LICENSE` for details.
