---
# Implementation Plan — DO NOT COMMIT
metadata:
  prd_path: {path/to/PRD.md}
---

## Context & Goal
- Summary: …
- KPI / outcome: …

## Best Practices
- Tests: …
- Lint: …
- Format: …
- Type-check: …
- …

## Working Rules

### Collaboration & Scope
- Act as a collaborator executing the plan; wait for an explicit go-ahead before starting any step.
- For every step, describe-before-code: summarize intended changes, wait for approval, and keep the step at `not-started` until approval or requested revisions are addressed. If the scope balloons beyond a tightly-scoped commit, pause and split the plan first.
- Keep one logical change per step—never bundle large, unrelated modifications.

### Execution
- Once approved, implement only the changes for that single step and keep the scope small.
- Before touching code, update both the Step Log row and the step’s **Status** field to `in-progress`; never write code while the step is still `not-started`.
- Apply the plan’s Best Practices and confirm acceptance criteria are met (tests, lint, type-checks, migrations, etc.) before handing the step off.

### Review & Commit
- Run a review cycle for each step: request review, move the status to `in-review`, and move it back to `in-progress` if rework is required.
- Propose a Conventional Commits-style message with each hand-off: `<type>(scope?): imperative subject` (≤72 chars) plus a body that captures the key changes and validations (e.g., tests). Human feedback may appear as `# HUMAN:` in code or `<!-- HUMAN: -->` in the plan; evaluate suggestions critically and offer alternatives when trade-offs exist.
- When the human signals finalization (e.g., `# HUMAN: final — please commit this step`), update the step status to `committed`, record the commit reference when available, commit the changes, and ask “Do you agree to proceed to the next step?”

### Progress Tracking & Closeout
- Track statuses using only `not-started`, `in-progress`, `in-review`, and `committed`; never skip updating the Step Log after completing work.
- Do not start the next step until the review cycle closes, the plan is updated, and the previous commit is created.
- After all steps are committed, ask the human to review the implementation plan and confirm completion.

## Step Log
| ID | Title | Status | Commit |
|---:|-------|--------|--------|
| 01 | …     | not-started | — |

## Steps

### Step {ID}: {Concise title}
**Rationale:** …
**Scope:** …

**Planned changes:**
- Files: …
- API/Data: …
- Observability: …
- …

**Acceptance criteria:**
- Behavior: …
- Tests: …
- Must pass all Best Practices defined in the global Implementation Plan
- …

**Review**
- Commit msg: `type(scope?): imperative summary` (≤72 chars)
- Commit body:
  ```
  - detail …
  - tests: …
  ```
- Questions: …

**Status:** not-started / in-progress / in-review / committed — update to `in-progress` before implementation begins
