# Architecture: {Project Name}

> Generated: {date}
> Status: {Draft | Approved}

## Overview

{Brief description}

## Design Pattern

**Primary:** {Pattern name}

**Why:** {Reasoning}

## Project Structure

```
src/
├── {feature}/
│   ├── __init__.py
│   ├── model.py          # {description}
│   ├── repository.py     # {description}
│   ├── service.py        # {description}
│   ├── routes.py         # {description}
│   └── exceptions.py     # {description}
├── shared/
│   ├── __init__.py
│   ├── config.py
│   ├── database.py
│   └── exceptions.py
└── main.py
```

## Components

### {Feature}

#### model.py

**Entities:**
- `{Entity}`: {description}
  - `id: str`
  - `field: type` — {description}

**DTOs:**
- `Create{Entity}DTO`: {fields}
- `Update{Entity}DTO`: {fields}

#### repository.py

```python
class {Entity}Repository(Protocol):
    def find_by_id(self, id: str) -> {Entity} | None: ...
    def find_all(self, limit: int, offset: int) -> list[{Entity}]: ...
    def save(self, entity: {Entity}) -> {Entity}: ...
    def delete(self, id: str) -> bool: ...
```

#### service.py

```python
class {Entity}Service:
    def __init__(self, repository: {Entity}Repository) -> None: ...
    def create(self, data: Create{Entity}DTO) -> {Entity}: ...
    def get_by_id(self, id: str) -> {Entity}: ...
    def update(self, id: str, data: Update{Entity}DTO) -> {Entity}: ...
    def delete(self, id: str) -> None: ...
```

#### routes.py

| Method | Path | Description |
|--------|------|-------------|
| POST | /{entities} | Create |
| GET | /{entities}/{id} | Get by ID |
| GET | /{entities} | List |
| PUT | /{entities}/{id} | Update |
| DELETE | /{entities}/{id} | Delete |

## Dependencies

| Package | Version | Purpose |
|---------|---------|---------|
| fastapi | ^0.109 | Web framework |
| pydantic | ^2.5 | Validation |
| sqlalchemy | ^2.0 | ORM |

## Implementation Order

1. `src/shared/exceptions.py`
2. `src/shared/config.py`
3. `src/shared/database.py`
4. `src/{feature}/exceptions.py`
5. `src/{feature}/model.py`
6. `src/{feature}/repository.py`
7. `src/{feature}/service.py`
8. `src/{feature}/routes.py`
9. `src/main.py`

## Error Handling

| Exception | HTTP | When |
|-----------|------|------|
| NotFoundError | 404 | Entity missing |
| ValidationError | 422 | Invalid input |
| Unexpected | 500 | Server error |

## Notes

{Additional considerations}
