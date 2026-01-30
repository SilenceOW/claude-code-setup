# /e2e Command

Write and run end-to-end tests.

## Usage

```
/e2e                         # Run all E2E tests
/e2e user registration       # Create E2E test for flow
/e2e --write login flow      # Write new E2E test
```

## What It Does

1. Loads `.claude/agents/e2e-runner.md`
2. Writes or runs E2E tests using pytest/playwright
3. Reports results with screenshots on failure

## Test Types

| Framework | Use Case |
|-----------|----------|
| pytest + httpx | API testing |
| Playwright | Browser testing |

## Output

```
═══════════════════════════════════════════════════════════════
🎭 E2E TEST RUN
═══════════════════════════════════════════════════════════════

Running: test_user_registration_flow

Steps:
  1. ✅ POST /auth/register
  2. ✅ POST /auth/login
  3. ✅ GET /users/me

Result: PASSED ✅
Duration: 2.3s

Summary: 5 passed, 0 failed
═══════════════════════════════════════════════════════════════
```
