# Multi-Agent Development Workflow

This skill orchestrates a complete development workflow through multiple phases.

## Phases

### Phase 1: Orchestrator
**Model:** `/model haiku`

1. Parse user request
2. Classify task type: `new_feature` | `refactor` | `bugfix` | `extend`
3. Identify components needed
4. Initialize `.task_state.json`

Output:
```
═══════════════════════════════════════════════════════════════
🎯 TASK ANALYSIS
═══════════════════════════════════════════════════════════════
📋 Request: [summary]
📦 Type: [type]
🎯 Domain: [domain]

Components:
  • [component] — [purpose]
═══════════════════════════════════════════════════════════════
```

### Phase 2: Architect
**Model:** `/model opus`

1. Design system architecture
2. Apply SOLID principles and patterns
3. Create `docs/architecture.md`
4. Define implementation plan

**HUMAN GATE:** Ask for approval before proceeding.

### Phase 3: Coder
**Model:** `/model sonnet`

For each file in implementation plan (sequentially):
1. Announce: `[N/Total] Creating path/to/file.py...`
2. Create file following code guidelines
3. Confirm: `✓ Created`
4. Update `.task_state.json`

### Phase 4: Reviewer
**Model:** `/model sonnet`

For each file (one at a time):
1. Check against architecture
2. Apply review checklist
3. Score 1-10, verdict: APPROVED | NEEDS_CHANGES
4. Save to `docs/reviews/`

### Phase 5: Bugfixer
**Model:** `/model sonnet`

If NEEDS_CHANGES:
1. Read issues from review
2. Fix each issue
3. Return to Reviewer
4. Max 3 iterations

## State File

`.task_state.json` tracks:
- Current status
- Implementation plan progress
- Review results
- Iteration count
