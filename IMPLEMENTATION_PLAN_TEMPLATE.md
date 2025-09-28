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
- Do not execute the plan until I explicitly ask.
- One logical change per commit (small steps).
- Describe-before-code, wait for approval.
- Human can annotate with `# HUMAN:` (code) or `<!-- HUMAN: -->` (plan).
- Respect edits but critically evaluate.
- Track each step’s **Status** using only `not-started`, `in-progress`, `in-review`, or `committed`.
- Switch a step to `in-progress` when implementation begins; if work pauses or scope changes, align the status (e.g., back to `not-started`).
- Move a step to `in-review` when it is handed to the human for review; if rework is required, move it back to `in-progress`.
- After a successful commit, update the status to `committed` and add the commit reference.

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

**Acceptance criteria:**
- Behavior: …
- Tests: …
- Must pass all Best Practices defined in the global Implementation Plan

**Review**
- Commit msg: `feat: …`
- Questions: …

**Status:** not-started / in-progress / in-review / committed
