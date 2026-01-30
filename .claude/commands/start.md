# /start Command

Begin a new multi-agent development workflow.

## Usage

```
/start <task description>
```

## What It Does

1. Switches to `/model haiku`
2. Loads `.claude/agents/orchestrator.md`
3. Analyzes the task
4. Creates `.task_state.json`
5. Proceeds through workflow phases

## Example

```
/start Create a REST API for managing products with CRUD operations
```

## Workflow Triggered

```
Orchestrator → Architect → [APPROVAL] → Coder → Reviewer → [Bugfixer if needed]
```
