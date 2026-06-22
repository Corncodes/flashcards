# Flashcards

A Django app for studying anatomy and physiology through flashcard-style review, organized by body system.

**Status:** In progress. Project scaffolded, apps created, no models or views implemented yet.

---

## Tech Stack

- Python / Django
- SQLite (default Django DB)

---

## Structure

Each body system is its own Django app:

- `circulatory` — circulatory system cards (app created, models and views empty)
- `heart` — heart-specific cards (app created, models and views empty)

---

## How to Run

```bash
python -m venv venv && source venv/bin/activate
pip install django
python manage.py migrate
python manage.py runserver
```

---

## Roadmap

- Define flashcard models (question, answer, topic, difficulty)
- Build views and templates for card review
- Add more body systems
- Spaced repetition logic

---

## What I Learned / Key Decisions

**One app per body system.** Keeping each system in its own Django app means adding a new system is just scaffolding a new app — no existing code changes. The tradeoff is that shared flashcard logic (if any) needs to live somewhere central rather than in each app.
