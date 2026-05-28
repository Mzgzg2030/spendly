# Spendly — Personal Expense Tracker

A web application for logging and categorizing personal expenses. Track where your money goes with category breakdowns, monthly summaries, and date-range filters.

## Features

- User registration and login
- Add, edit, and delete expenses
- Category-based spending breakdown (Bills, Food, Health, Transport, etc.)
- Monthly summaries and date-range filtering
- Clean, responsive UI
- Terms and Conditions and Privacy Policy pages
- YouTube demo modal on the landing page

## Screenshots

> Screenshots coming soon.

## Tech Stack

| Layer | Technology |
|---|---|
| Backend | Python 3.9 + Flask 3.1 |
| Database | SQLite |
| Templating | Jinja2 |
| Frontend | Vanilla HTML / CSS / JavaScript |
| Testing | pytest + pytest-flask |

## Project Structure

```
expense-tracker/
├── app.py              # Flask application and route definitions
├── requirements.txt    # Python dependencies
├── database/
│   ├── __init__.py
│   └── db.py           # Database helpers: get_db(), init_db(), seed_db()
├── templates/
│   ├── base.html       # Shared layout (navbar, footer)
│   ├── landing.html    # Marketing landing page
│   ├── login.html      # Login form
│   ├── register.html   # Registration form
│   ├── terms.html      # Terms and Conditions page
│   └── privacy.html    # Privacy Policy page
└── static/
    ├── css/style.css
    └── js/main.js
```

## Getting Started

### Prerequisites

- Python 3.9+

### Installation

1. Clone the repository:
   ```bash
   git clone <repo-url>
   cd expense-tracker
   ```

2. Create and activate a virtual environment:
   ```bash
   python3 -m venv venv
   source venv/bin/activate   # Windows: venv\Scripts\activate
   ```

3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```

4. Run the app:
   ```bash
   python3 app.py
   ```

5. Open your browser at `http://localhost:5001`

## Running Tests

```bash
pytest
```

## Routes

| Method | Path | Description |
|---|---|---|
| GET | `/` | Landing page |
| GET | `/terms` | Terms and Conditions |
| GET | `/privacy` | Privacy Policy |
| GET/POST | `/register` | Create a new account |
| GET/POST | `/login` | Sign in |
| GET | `/logout` | Sign out |
| GET | `/profile` | User profile |
| GET/POST | `/expenses/add` | Add a new expense |
| GET/POST | `/expenses/<id>/edit` | Edit an expense |
| GET/POST | `/expenses/<id>/delete` | Delete an expense |
