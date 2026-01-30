# Coding Style Rules

## Python Standards

- Python 3.11+
- Type hints on ALL functions
- Use `from __future__ import annotations` for forward refs

## Naming

| Type | Convention | Example |
|------|------------|---------|
| Classes | PascalCase | `TaskService` |
| Functions | snake_case | `get_task_by_id` |
| Constants | UPPER_SNAKE | `MAX_RETRIES` |
| Private | _prefix | `_validate` |

## Structure

- By-feature organization (not by-layer)
- Max 200 lines per file
- Max 20 lines per function
- Max 3 parameters (use dataclass for more)

## Imports Order

```python
# 1. Future
from __future__ import annotations

# 2. Standard library
import os
from typing import TYPE_CHECKING

# 3. Third party
from pydantic import BaseModel

# 4. Local
from src.shared.exceptions import BaseError
```

## Comments

- Explain WHY, not WHAT
- No commented-out code
- Docstrings for public functions only
