# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Commands

```bash
# Setup
python3 -m venv venv && source venv/bin/activate
pip install -r requirements.txt

# Run dev server (http://localhost:5001)
python3 app.py

# Tests
pytest
```

## Architecture

**Spendly** is a Flask server-side rendered expense tracker. No build step — vanilla HTML/CSS/JS with Jinja2 templates.

- **`app.py`** — all routes and Flask app setup. Routes return `render_template()` calls or plain strings for stubs.
- **`database/db.py`** — stub for `get_db()`, `init_db()`, `seed_db()`. SQLite backend, not yet implemented.
- **`templates/base.html`** — shared layout via Jinja2 `{% block %}` inheritance. All pages extend this.
- **`static/css/style.css`** — single stylesheet using CSS custom properties for the design system (colors, spacing, typography).

## Stub Routes

Several routes are placeholder stubs awaiting implementation (logout, profile, expense CRUD). They return plain strings indicating which step they belong to. When implementing, add `GET/POST` methods and wire up the database via `get_db()`.

## Database

SQLite accessed via `database/db.py`. The `get_db()` helper is expected to return a connection; `init_db()` creates the schema; `seed_db()` populates test data. Schema is not yet defined — design it around users and expenses with categories (Bills, Food, Health, Transport, etc.).
