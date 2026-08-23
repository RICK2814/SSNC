# Siksha Sahayak

A Django-based e-learning platform for students in Classes 5–10, offering structured study
material, chapter-wise practice questions, timed quizzes, and progress tracking across six
core subjects.

**Live demo:** https://ssnc-8qqp.onrender.com

> Hosted on Render's free tier — the app may take 30–60 seconds to wake up on the first
> request after a period of inactivity.

## Features

- **Student accounts** — registration and login tied to a class level, with an editable
  profile (including a profile picture).
- **Structured curriculum** — Class → Subject → Chapter → Study Material hierarchy covering
  Mathematics, Science, English, History, Geography, and Computer Science.
- **Practice mode** — chapter-wise multiple-choice questions with instant feedback and
  explanations, tagged by difficulty (Easy / Medium / Hard).
- **Timed quizzes** — a full quiz engine with per-question marks, scoring, and a results
  breakdown after each attempt.
- **Progress tracking** — students can review their quiz and practice history over time.
- **Admin panel** — Django's built-in admin for managing curriculum content and monitoring
  student data.

## Tech stack

| Layer            | Technology                                  |
|-------------------|----------------------------------------------|
| Backend           | Django 5.2                                   |
| Database          | PostgreSQL (production) / SQLite (local dev) |
| Static files      | WhiteNoise                                   |
| WSGI server       | Gunicorn                                     |
| Image handling    | Pillow                                       |
| Hosting           | Render                                       |

## Project structure

```
siksha_sahayak/     Project settings, root URLconf, WSGI entry point
accounts/           Registration, login, profile management
materials/          Curriculum models (ClassLevel, Subject, Chapter, StudyMaterial)
                     + the seed_curriculum management command
assessments/        Questions, quizzes, attempts, dashboard, and progress views
templates/          HTML templates, organized per app
static/             CSS and images
```

## Getting started locally

### Prerequisites

- Python 3.12+
- pip

### Setup

```bash
# Clone the repository
git clone https://github.com/RICK2814/SSNC.git
cd SSNC

# Create and activate a virtual environment
python -m venv .venv
.venv\Scripts\activate      # Windows
source .venv/bin/activate   # macOS/Linux

# Install dependencies
pip install -r requirements.txt

# Apply migrations
python manage.py migrate

# Seed the curriculum (classes, subjects, chapters, questions, quizzes)
python manage.py seed_curriculum

# Create an admin account
python manage.py createsuperuser

# Run the development server
python manage.py runserver
```

The app will be available at `http://127.0.0.1:8000/`, and the admin panel at
`http://127.0.0.1:8000/admin/`.

### Environment variables (optional for local dev)

The app runs out of the box locally with sensible defaults (SQLite, `DEBUG=True`). For a
production-like setup, set:

| Variable       | Purpose                                              | Default                        |
|----------------|-------------------------------------------------------|---------------------------------|
| `SECRET_KEY`   | Django's cryptographic signing key                    | insecure dev key (change this) |
| `DEBUG`        | Enables/disables debug mode                            | `False`                        |
| `ALLOWED_HOSTS`| Comma-separated list of allowed hostnames               | `*`                             |
| `DATABASE_URL` | Full database connection string (e.g. `postgres://...`)| local `db.sqlite3`             |

## Deployment

This project is configured to deploy on [Render](https://render.com) as a Python web
service, using `build.sh` as the build command and Gunicorn as the WSGI server:

- **Build command:** `./build.sh` — installs dependencies, runs `collectstatic`, applies
  migrations, and seeds curriculum data.
- **Start command:** `gunicorn siksha_sahayak.wsgi:application`

A managed PostgreSQL instance is expected via the `DATABASE_URL` environment variable; the
app falls back to SQLite when it isn't set, which is only suitable for local development.

## Curriculum coverage

`seed_curriculum` currently seeds **Classes 5 through 10**, each with six subjects
(Mathematics, Science, English, History, Geography, Computer Science), six chapters per
subject, one detailed study material per chapter, and a 20-question quiz with mixed
difficulty. The class range is defined in
`materials/management/commands/seed_curriculum.py` and can be extended to cover Classes
1–4 or 11–12.

## License

MIT — see [LICENSE](LICENSE) for details.
