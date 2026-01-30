# /refactor-clean Command

Clean up codebase: remove dead code, simplify complexity.

## Usage

```
/refactor-clean              # Clean entire project
/refactor-clean src/users/   # Clean specific module
```

## What It Does

1. Loads `.claude/agents/refactor-cleaner.md`
2. Analyzes for dead code and complexity
3. Reports findings and applies fixes

## What Gets Cleaned

- Unused imports
- Unused variables/functions
- Commented-out code
- Unnecessary files (.md, temp)
- Complex functions (split them)
- Duplicate code

## Output

```
═══════════════════════════════════════════════════════════════
🧹 CLEANUP ANALYSIS
═══════════════════════════════════════════════════════════════

Dead Code Found:
  • 12 unused imports
  • 3 unused functions
  • 5 commented code blocks

Complexity Issues:
  • 2 functions > 20 lines

Proceed with cleanup? (yes/no)
═══════════════════════════════════════════════════════════════
```
