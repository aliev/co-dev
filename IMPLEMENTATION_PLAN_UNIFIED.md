# Task: Generate Implementation Plan

**Input:** PRD at `{path/to/PRD.md}`
**Output:** `implementation_plan.md` next to PRD

**Additional context for PRD:**
{Optional: clarifications, scope adjustments, focus areas, exclusions, etc.}

## Process
1. Read PRD
2. **Analyze project**: Discover tooling (package.json scripts, Makefile, pytest.ini, etc.) and fill Checks section with actual commands
3. Fill ALL template sections
4. Create small, atomic steps (1 step = 1 commit)
5. Save plan, DO NOT commit
6. Request review

**Status:** Waiting for PRD path

# Implementation Plan Template

**PRD:** `{path/to/PRD.md}`
**Goal:** {one-line summary}
**Success Metric:** {measurable outcome}

## Working Instructions

### 1. Collaboration & Scope
- **Describe before code**: Summarize changes and wait for approval
- **Stay in scope**: If scope grows beyond the step, stop and consult with human
- **Wait for go-ahead**: Never start without explicit approval

### 2. Execution
- **Update status first**: Change both Step Log table and step status to `in-progress` BEFORE coding
- **Stay in scope**: Implement only what's planned for this step
- **Run checks iteratively**: Use Checks section commands during implementation

### 3. Review & Commit
- **Propose commit message**: Use format from Commit section
- **Wait for finalization**: Keep `in-progress` until human says "commit"
- **Mark committed**: Set `committed`, record commit hash, ask "Proceed to next?"

### 4. Progress Tracking
- **Status flow**: `pending` → [approval] → `in-progress` → [commit] → `committed`
- **Update immediately**: Never batch status updates
- **One step at a time**: Complete current before starting next

## Checks
```bash
# Run during implementation for quick feedback, MUST pass all before commit:
test: {test command}
lint: {lint command}
type: {type-check command}
build: {build command if applicable}
```

## Steps

| # | Task | Status | Commit |
|---|------|--------|--------|
| 1 | {task} | pending | - |
| 2 | ... | pending | - |

---

### Step 1: {Task Title}

**Why:** {reason for this step}
**What:** {specific changes}

#### Changes
- [ ] File: `path/to/file.ext` - {what changes}
- [ ] Test: `path/to/test.ext` - {test coverage}

#### Acceptance Criteria
- [ ] {specific behavior requirement}
- [ ] {performance requirement}
- [ ] {edge case handled}
- [ ] All Checks pass (see Checks section above)

#### Commit
```
type(scope?): short description

- Added/Fixed/Updated {what}
- Tests: {what was tested}
```

**Status:** pending → in-progress → committed

---

## Workflow States
- **pending** - Awaiting approval to start
- **in-progress** - Currently implementing
- **committed** - Done and committed