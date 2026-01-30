# Git Workflow Rules

## Commit Format

```
<type>(<scope>): <description>

[optional body]
```

Types: `feat`, `fix`, `refactor`, `docs`, `test`, `chore`

Examples:
```
feat(auth): add JWT token refresh
fix(tasks): handle empty list edge case
refactor(api): extract validation logic
```

## Before Commit

- Run tests
- Run linter
- Check for console.log / print statements
- Review changes in editor

## Branch Strategy

- `main` — production ready
- `feat/<name>` — feature branches
- `fix/<name>` — bug fixes

## PR Process

1. Create feature branch
2. Implement with tests
3. Self-review changes
4. Create PR with description
5. Address review comments
