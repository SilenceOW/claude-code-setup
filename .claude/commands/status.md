# /status Command

Show current workflow state.

## Usage

```
/status
```

## What It Does

Reads and displays `.task_state.json` in human-readable format.

## Output Format

```
═══════════════════════════════════════════════════════════════
📊 TASK STATUS
═══════════════════════════════════════════════════════════════

Task ID: a1b2c3d4
Description: Create REST API for products

Status: CODING
Iteration: 0/3
Created: 2025-01-27 10:00
Updated: 2025-01-27 10:30

Architecture: ✓ Approved

Implementation Progress:
  ✓ src/shared/exceptions.py
  ✓ src/shared/config.py
  ✓ src/feature/model.py
  → src/feature/repository.py (in progress)
  ○ src/feature/service.py
  ○ src/feature/routes.py

Reviews:
  (none yet)

═══════════════════════════════════════════════════════════════
```

## Status Icons

| Icon | Meaning |
|------|---------|
| ✓ | Completed |
| → | In progress |
| ○ | Pending |
| ✗ | Failed / Needs changes |
