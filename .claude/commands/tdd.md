# /tdd Command

Activate test-driven development mode.

## Usage

```
/tdd
/tdd Create user validation
```

## What It Does

1. Loads `.claude/agents/tdd-guide.md`
2. Switches to TDD workflow: Red → Green → Refactor
3. Writes test FIRST, then implementation

## TDD Cycle

```
1. RED    → Write failing test
2. GREEN  → Minimum code to pass
3. REFACTOR → Clean up
```

## Example

```
/tdd Create email validation

→ Writing test first...
→ Test fails (expected)
→ Implementing validation...
→ Test passes ✅
→ Refactoring...
→ Done!
```
