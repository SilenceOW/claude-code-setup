# Agent Coordination Rules

## When to Use Subagents

Delegate to subagent when:
- Task is well-defined and scoped
- Task can run independently
- Main context is getting large

## Agent Selection

| Task | Agent | Model |
|------|-------|-------|
| Analyze request | orchestrator | haiku |
| Design architecture | architect | opus |
| Write code | coder | sonnet |
| Review code | code-reviewer | sonnet |
| Fix issues | bugfixer | sonnet |
| Write tests | tdd-guide | sonnet |

## Handoff Protocol

1. Save current state to `.task_state.json`
2. Create clear task description for subagent
3. Specify expected output format
4. Include relevant context only (not full history)

## Context Management

- Keep subagent context minimal
- Pass only necessary files
- Limit tool access per agent
- Use `/compact` before long operations
