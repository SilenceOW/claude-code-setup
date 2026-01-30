# Multi-Agent Development Workflow

## Quick Start

```bash
/start Create a REST API for user management   # Full workflow
/tdd                                           # Test-driven dev
/review                                        # Code review
/security-review                               # Security audit
/refactor-clean                                # Clean up code
/e2e                                           # E2E tests
```

## Agents (11)

| Agent | Model | Purpose |
|-------|-------|---------|
| 📋 planner | sonnet | Break down features into tasks |
| 📐 architect | opus | System design decisions |
| 💻 coder | sonnet | Write production code |
| 🧪 tdd-guide | sonnet | Test-driven development |
| 🔍 code-reviewer | sonnet | Quality review |
| 🔒 security-reviewer | opus | Vulnerability analysis |
| 🔧 bugfixer | sonnet | Fix review issues |
| ⚡ build-error-resolver | sonnet | Fix build/runtime errors |
| 🎭 e2e-runner | sonnet | End-to-end testing |
| 🧹 refactor-cleaner | sonnet | Remove dead code |
| 📝 doc-updater | haiku | Keep docs in sync |

## Commands (8)

| Command | Description |
|---------|-------------|
| `/start <task>` | Full feature workflow |
| `/tdd` | Test-driven development |
| `/review` | Code review |
| `/security-review` | Security audit |
| `/refactor-clean` | Clean up code |
| `/e2e` | E2E tests |
| `/continue` | Resume saved state |
| `/status` | Show state |

## Workflow

```
/start "feature"
       ↓
📋 Planner → tasks
       ↓
📐 Architect → design
       ↓
👤 APPROVE
       ↓
🧪 TDD → tests first
       ↓
💻 Coder → implement
       ↓
🔍 Review → quality
       ↓
🔒 Security → audit
       ↓
🧹 Clean → refactor
       ↓
📝 Docs → update
       ↓
✅ Done
```

## Tips

- `Tab` — toggle thinking
- `/compact` — compress context
- `/fork` — parallel experiments
- Keep ≤10 MCP enabled
- Use `tmux` for long commands

# Additional

 - Always read .claude.json at the start of a conversation