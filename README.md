# Claude Code Multi-Agent Workflow

Ready-to-use Claude Code CLI setup with 11 specialized agents.

## Installation

```bash
# 1. Copy to your project
cp -r claude-setup/.claude your-project/
cp claude-setup/.claude.json your-project/
cp claude-setup/CLAUDE.md your-project/

# 2. Navigate and run
cd your-project
claude .
```

**Requirements:**
- [Claude Code CLI](https://code.claude.com)
- Claude Max subscription (for Opus/Sonnet)

## Agents

| Agent | Model | Purpose |
|-------|-------|---------|
| 📋 planner | sonnet | Break down features into tasks |
| 📐 architect | opus | System design decisions |
| 💻 coder | sonnet | Write production code |
| 🧪 tdd-guide | sonnet | Test-driven development |
| 🔍 code-reviewer | sonnet | Code quality review |
| 🔒 security-reviewer | opus | Security audit |
| 🔧 bugfixer | sonnet | Fix review issues |
| ⚡ build-error-resolver | sonnet | Fix build/runtime errors |
| 🎭 e2e-runner | sonnet | End-to-end testing |
| 🧹 refactor-cleaner | sonnet | Remove dead code, simplify |
| 📝 doc-updater | haiku | Keep docs in sync |

## Commands

```bash
/start <task>       # Full development workflow
/tdd                # Test-driven development
/review             # Code review
/security-review    # Security audit
/refactor-clean     # Clean up code
/e2e                # E2E tests
/continue           # Resume from saved state
/status             # Show current state
```

## Workflow

```
/start "create REST API"
         ↓
   📋 Planner → break into tasks
         ↓
   📐 Architect → design system
         ↓
   👤 APPROVE → your confirmation
         ↓
   🧪 TDD → tests first
         ↓
   💻 Coder → implement
         ↓
   🔍 Review → check quality
         ↓
   🔒 Security → audit
         ↓
   🧹 Clean → refactor
         ↓
   📝 Docs → update
         ↓
   ✅ Done
```

## Structure

```
.claude/
├── agents/          # 11 agents
├── commands/        # 8 slash commands
├── rules/           # Rules (always applied)
├── skills/          # Workflows
├── templates/       # Templates
└── hooks.json       # Automation

.claude.json         # Project config + MCP
CLAUDE.md            # Quick reference
```

## MCP Servers

Included:
- **github** — GitHub integration
- **firecrawl** — Web page parsing
- **memory** — Cross-session memory
- **sequential-thinking** — Step-by-step reasoning

## Tips

| Action | Command |
|--------|---------|
| Show thinking | `Tab` |
| Compress context | `/compact` |
| Parallel work | `/fork` |
| Long-running commands | Use `tmux` |

## Customization

**Add agent:**
1. Create `.claude/agents/my-agent.md`
2. Add to `.claude.json` → `agents`

**Add command:**
1. Create `.claude/commands/my-command.md`

**Add rule:**
1. Create `.claude/rules/my-rule.md`

## License

MIT
