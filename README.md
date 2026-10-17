# Secure Login System

A beginner-friendly Flask web app demonstrating registration, login, password hashing, parameterized SQL queries, session-based access control, and logout.

## Features
- User registration and login
- Passwords stored as hashes (Werkzeug's password hashing helpers)
- Input validation
- Parameterized SQL queries to reduce SQL injection risk
- Login-protected dashboard and logout
- SQLite database created automatically

## Run locally
1. Install Python 3.10 or newer.
2. Open a terminal in this folder.
3. Create and activate a virtual environment (recommended):
   - Windows: `python -m venv .venv` then `.venv\Scripts\activate`
   - macOS/Linux: `python3 -m venv .venv` then `source .venv/bin/activate`
4. Install dependencies: `pip install -r requirements.txt`
5. Set a strong secret key in your environment before deployment. For local practice, the app has a development-only fallback:
   - PowerShell: `$env:SECRET_KEY = "replace-with-a-long-random-secret"`
6. Run: `python app.py`
7. Visit `http://127.0.0.1:5000`

## Security notes
- The fallback secret key is for local practice only. Set `SECRET_KEY` to a long random value for any deployment.
- This is an educational starter project. Before production use, add CSRF protection, HTTPS-only cookie settings, rate limiting, secure deployment configuration, and tests.
- Do not commit real user data or secrets. The SQLite database is generated locally and is not included in the repository.
