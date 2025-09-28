---
# Implementation Plan — DO NOT COMMIT
metadata:
  prd_path: {path/to/PRD.md}
  branch_name: {branch_name}  # Reflects PRD goal
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
- After a successful commit, update the corresponding step’s **Status** in this plan (e.g., change to "committed" and add commit reference).

## Branch
- Name: {branch_name}

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

**Status:** pending / needs changes / approved / committed
