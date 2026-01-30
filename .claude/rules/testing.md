# Testing Rules

## TDD Approach

1. Write test first (red)
2. Implement minimum code to pass (green)
3. Refactor (refactor)

## Coverage Target

- Minimum 80% coverage
- 100% for critical business logic

## Test Structure

```python
def test_<what>_<condition>_<expected>():
    # Arrange
    ...
    # Act
    ...
    # Assert
    ...
```

## What to Test

| Layer | Test Type | Mock |
|-------|-----------|------|
| Model | Unit | Nothing |
| Repository | Integration | Database |
| Service | Unit | Repository |
| Routes | Integration | Nothing |

## Fixtures

- Use pytest fixtures for setup
- Prefer factory functions over fixtures for data
- Clean up after tests
