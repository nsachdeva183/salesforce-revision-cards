# Salesforce Daily Revision Cards

A daily spaced-repetition flashcard deck for Salesforce Senior Developer / Lead interview prep, covering Apex, Security & Sharing, 2026 security mandates, Integration & APIs, LWC, Sales Cloud, Service Cloud, Experience Cloud, Agentforce, Industries/OmniStudio, 2026 features & renaming, Architecture, and Leadership.

**Live deck:** enable GitHub Pages on this repo (Settings > Pages > Deploy from branch `main` / root) to get a shareable link, or just open `index.html` locally.

## How it works

- Every day the app picks up to 10 cards: overdue reviews first, then new cards to fill the rest.
- After revealing an answer, rate it **Easy** / **Medium** / **Difficult**:
  - Difficult -> resurfaces tomorrow.
  - Medium -> resurfaces every ~2-14 days (grows slowly if you keep getting it).
  - Easy -> resurfaces every ~4-60 days (grows fastest).
- Progress is stored in your browser's `localStorage` — nothing is sent to a server.
- `questions.json` holds the card bank (196 cards to start). A scheduled task adds a handful of new questions to it weekly.

## Files

- `index.html` — the app (self-contained, fetches `questions.json`).
- `questions.json` — the card bank. Each card: `{ id, domain, type, question, answer, code, added }`.
