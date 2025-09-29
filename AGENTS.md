# Repository Guidelines

## Project Structure & Module Organization
- `README.md` introduces the Human-in-the-Loop implementation protocol.
- `PLAN.md` hosts the active implementation plan; keep it authoritative for current work.
- `IMPLEMENTATION_PLAN_TEMPLATE.md` provides the per-step scaffold (statuses: `pending → in-progress → committed`).
- Add new source, test, or asset directories under the root and document them in `PLAN.md` as they appear.

## Build, Test, and Development Commands
- No universal build pipeline exists yet. Each implementation plan step must specify the exact commands it requires (e.g., `npm run test`, `pytest`, `cargo fmt`).
- Before coding, verify tooling availability and record command outcomes in the step log or plan notes.
- Use `git status -sb` to ensure the working tree only contains the planned changes.

## Coding Style & Naming Conventions
- Default to ASCII, 2- or 4-space indentation matching the language ecosystem you introduce; document deviations in the plan.
- Follow language-standard style guides (e.g., PEP8 for Python, eslint-config-standard for JavaScript). Configure formatters/linters in the plan’s Best Practices.
- Name files and directories descriptively; prefer `kebab-case` for docs/assets and the conventional casing for code languages.

## Testing Guidelines
- Define the test framework per project area (e.g., `pytest`, `jest`, `go test`) and record expectations in the plan’s Best Practices.
- Require targeted tests for every behavioral change. Include regression coverage when fixing bugs.
- Keep test artifacts near their modules (`tests/`, `__tests__/`, etc.) and describe new suites in `PLAN.md`.

## Commit & Pull Request Guidelines
- Use Conventional Commits: `<type>(optional-scope): imperative subject` (≤72 chars). Example: `feat(api): add project summary endpoint`.
- Body bullets should list key changes and validations, including test commands run.
- PRs must reference plan steps, summarize functional impact, note risk/roll-back, and attach evidence (logs, screenshots) when relevant.

## Agent Workflow Expectations
- Always follow the describe-before-code protocol, await human approval, and update plan statuses promptly.
- When tasks broaden, split the plan before coding to keep commits tightly scoped.
- After the final step is committed, request a plan review confirmation from the human collaborator.
