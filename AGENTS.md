## Python Development Rules

All Python code in this repository must follow these conventions.

### Naming Conventions

| Thing | Convention | Example |
|---|---|---|
| Variables & functions | `snake_case` | `user_name`, `get_balance()` |
| Classes | `PascalCase` | `BankAccount`, `AudioBook` |
| Constants | `UPPER_SNAKE_CASE` | `MAX_RETRIES = 3` |
| "Private" attributes | `_single_underscore` | `self._balance` |
| Name-mangled (truly private) | `__double_underscore` | `self.__secret` |

### Pythonic Idioms

- Use `in` / `not in` for membership checks instead of `.index()`.
- Use `not items` for falsy/empty checks instead of `len(items) == 0`.
- Swap variables with `a, b = b, a`.
- Return multiple values as tuples: `return min(nums), max(nums)`.
- Use iterable unpacking: `first, *rest = [1, 2, 3, 4]`.
- Prefer list/dict/set comprehensions over manual loops for building collections.

### Functions

- Use default arguments instead of method overloading.
- Use `*args` and `**kwargs` for flexible signatures.
- Prefer keyword arguments at call sites for clarity.
- Use type hints (recommended): `def summarize(nums: list[int]) -> dict:`.

### Classes & OOP

- Always call `super().__init__()` in subclasses.
- Implement `__str__` for human-readable output and `__repr__` for debug output.
- Use `@property` instead of Java-style getters/setters.

### Error Handling

- Raise early and be specific with exception types.
- Catch specific exceptions — never use bare `except:`.
- Prefer `ValueError`, `TypeError`, `KeyError`, `IndexError`, `AttributeError`, `NotImplementedError` as appropriate.

### String Formatting

- Always prefer f-strings over `.format()` or `%` formatting.

### Imports

- Order: standard library → third-party → local modules (separated by blank lines).
- Never use wildcard imports (`from math import *`). Import specific names.

### Common Gotchas

- Use `is None` / `is not None`, never `== None`.
- Boolean literals are `True` / `False` (capitalized).
- Logical operators are `and` / `or` / `not` (words, not symbols).
- `self` must be an explicit first parameter in every instance method.
- Use `isinstance(x, Type)` instead of `type(x) == Type`.

---

## Cursor Cloud specific instructions

This repository (`prototyping`) is currently an empty scaffold. There are no source files, dependencies, services, build tools, or tests yet.

- **No package manager or lock file** — no dependency installation is needed.
- **No services to run** — there is no backend, frontend, database, or other service.
- **No lint, test, or build commands** — none are configured.
- **Git** is the only tool required to work in this repo.

When code is added to this repository, update this section with relevant setup, lint, test, build, and run instructions.
