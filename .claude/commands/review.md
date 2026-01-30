# /review Command

Run code review on specified files or recent changes.

## Usage

```
/review                    # Review all changed files
/review src/users/         # Review specific path
/review src/api/routes.py  # Review specific file
```

## What It Does

1. Loads `.claude/agents/code-reviewer.md`
2. Reviews code against architecture and guidelines
3. Produces verdict: APPROVED | NEEDS_CHANGES

## Output

```
═══════════════════════════════════════════════════════════════
🔍 REVIEW: src/users/service.py
═══════════════════════════════════════════════════════════════

Score: 8/10
Verdict: APPROVED

Issues: none

Positive:
  • Clean separation of concerns
  • Good error handling
  • Type hints complete
═══════════════════════════════════════════════════════════════
```
