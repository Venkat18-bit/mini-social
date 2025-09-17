# Twister (Django)

A tiny social media app with profiles, posts & comments, likes, and follow/unfollow.

## Quick Start (Windows, macOS, Linux)

1) **Create a project folder & enter it**  
```bash
# Windows (PowerShell)
mkdir Twister && cd Twister

# macOS / Linux
mkdir -p Twister && cd Twister
```

2) **Create & activate a virtual environment**  
```bash
# Windows (PowerShell)
python -m venv .venv
.\.venv\Scripts\activate

# macOS / Linux
python3 -m venv .venv
source .venv/bin/activate
```

3) **Install dependencies**  
```bash
pip install -r requirements.txt
```

4) **Run database migrations**  
```bash
python manage.py migrate
```

5) **(Optional) Create a superuser**  
```bash
python manage.py createsuperuser
```

6) **(Optional) Load demo data** (creates users alice/bob/charlie/diana/eve, password `pass1234`)  
```bash
python manage.py seed_demo
```

7) **Start the server**  
```bash
python manage.py runserver
```

8) Open http://127.0.0.1:8000 in your browser.  
- Register a new user or log in with a demo user (e.g. alice / pass1234).  
- Create posts (text + optional image URL).  
- Like posts, add comments, follow/unfollow users, edit your profile avatar/bio.

## Project Structure
```
minisocial/        # Django project (settings, urls, wsgi)
core/              # App: models, views, forms, urls, admin
templates/         # HTML (Bootstrap via CDN)
static/            # CSS/JS
manage.py
requirements.txt
```

## Notes
- Uses SQLite by default — no setup required.
- Images are provided via **URL** fields (no media uploads required).
- For production: set `DEBUG=False` and update `ALLOWED_HOSTS`.
