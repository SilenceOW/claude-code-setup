# Security Rules

## Secrets

- NEVER hardcode secrets, API keys, passwords
- Use environment variables via `pydantic-settings`
- Check for secrets before every commit

## Input Validation

- Validate ALL user input with Pydantic
- Use parameterized queries (never string formatting for SQL)
- Sanitize file paths to prevent traversal

## Error Handling

- Never expose internal errors to users
- Log full errors, return generic messages
- Use custom exception classes

## Dependencies

- Pin exact versions in requirements
- Audit dependencies periodically
- Prefer well-maintained packages
