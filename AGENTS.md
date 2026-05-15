# Agent Instructions for Oficina_GithubCopilot

## Dev checklist (mandatory)
- `uv sync`
- `uv run ruff check .`
- `uv run pytest`

## What this app is
FastAPI + Jinja2 + HTMX social bingo for live mixers.

## Key workflows
- `uv run uvicorn app.main:app --reload --host 0.0.0.0 --port 8000`
- `uv run soc-ops`

## Key files
- `app/main.py` — routes, sessions, HTMX endpoints
- `app/game_service.py` — session/game state helpers
- `app/game_logic.py` — bingo board and rules
- `tests/test_api.py` / `tests/test_game_logic.py`

## Agent rules
- Prefer tests first: add/update tests, run `uv run pytest`, then implement.
- Keep UI logic in templates and HTMX fragments, not in Python route handlers.
- Do not change `.solutions/`; they are sample content.
- Use `.github/instructions/` and `README.md` for additional project conventions.
