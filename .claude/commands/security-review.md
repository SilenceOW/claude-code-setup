# /security-review Command

Perform security audit on the codebase.

## Usage

```
/security-review              # Audit entire project
/security-review src/auth/    # Audit specific module
```

## What It Does

1. Loads `.claude/agents/security-reviewer.md`
2. Switches to Opus model (deep analysis)
3. Checks for vulnerabilities and security issues

## Checks Performed

- Hardcoded secrets
- SQL injection risks
- XSS vulnerabilities
- Input validation
- Authentication/authorization
- Dependency vulnerabilities

## Output

```
═══════════════════════════════════════════════════════════════
🔒 SECURITY REVIEW
═══════════════════════════════════════════════════════════════

Risk Level: MEDIUM
Issues Found: 2

[1] HIGH: Hardcoded JWT secret
    File: src/auth/config.py:15
    Fix: Use environment variable

[2] MEDIUM: Missing input validation
    File: src/api/routes.py:42
    Fix: Add Pydantic validation
═══════════════════════════════════════════════════════════════
```
