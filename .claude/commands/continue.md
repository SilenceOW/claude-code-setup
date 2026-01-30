# /continue Command

Resume an interrupted workflow from saved state.

## Usage

```
/continue
```

## What It Does

1. Reads `.task_state.json`
2. Determines current phase from `status`
3. Loads appropriate agent
4. Resumes workflow

## Status Mapping

| Status | Resumes As |
|--------|------------|
| `ANALYZING` | Orchestrator |
| `DESIGNING` | Architect |
| `AWAITING_ARCH_APPROVAL` | Architect (ask approval) |
| `CODING` | Coder (from last incomplete file) |
| `REVIEWING` | Reviewer |
| `FIXING` | Bugfixer |
| `COMPLETED` | Shows summary |
| `FAILED` | Shows failure reason |

## Example Output

```
═══════════════════════════════════════════════════════════════
📂 Resuming Task: a1b2c3d4
═══════════════════════════════════════════════════════════════

Status: CODING
Progress: 3/6 files completed
Last completed: src/feature/model.py

Continuing from: src/feature/repository.py
═══════════════════════════════════════════════════════════════
```
