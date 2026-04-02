# CLAUDE.md

## Project overview

Static website listing humorous, absurd facts about Claude, Anthropic's AI. No build step, no framework — just `index.html` and `facts.json`.

## Language

All code, comments, commit messages, and documentation must be written in **English**.

## Repository structure

```
claude-facts/
├── index.html   # The entire frontend (HTML + CSS + vanilla JS)
├── facts.json   # Array of fact objects
└── CLAUDE.md
```

## Facts format

Each entry in `facts.json` follows this schema:

```json
{
  "id": 1,
  "text": "The fact text.",
  "approved_at": "YYYY-MM-DD"
}
```

- `id` must be unique and sequential
- `text` must be a single sentence, humorous and self-contained
- `approved_at` is the approval date in ISO 8601 format

## Deployment

The site is deployed automatically via GitHub Pages on every push to `main`. No build step required.
