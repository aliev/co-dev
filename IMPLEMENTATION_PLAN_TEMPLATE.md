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
- Track each step’s **Status** using only `pending`, `review`, or `committed`.
- When a step is submitted for review (plan or code), set its status to `review`; if rework is required, move it back to `pending`.
- After a successful commit, update the corresponding step’s status to `committed` and add the commit reference.

## Step Log
| ID | Title | Status | Commit |
|---:|-------|--------|--------|
| 01 | …     | pending| —      |

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

**Status:** pending / review / committed
