# Flashcards

Studying anatomy and physiology is a lot of memorization. Building a flashcard app for it instead of using Anki because I wanted the practice and I wanted it organized the way I think about it, by body system.

**Status:** In progress. Project and apps scaffolded, models and views not implemented yet.

---

## Tech Stack

- Python / Django
- SQLite (default Django DB)

---

## Structure

Each body system gets its own Django app:

- `circulatory` — circulatory system cards (scaffolded, models and views empty)
- `heart` — heart-specific cards (scaffolded, models and views empty)

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

**One app per body system.** Adding a new system is just scaffolding a new app with no existing code touched. If shared flashcard logic becomes necessary it needs a central home, but that's a problem for when there's actually shared logic to share.
