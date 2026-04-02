---
name: new-facts
description: "Generate new Claude facts in an absurd hyperbolic tone. Use when the user wants to generate, create, propose, or add new Claude facts. Proposes 10 facts, user picks, adds to facts.json."
allowed-tools: Read, Edit
---

## Goal

Generate 10 new Claude facts, let the user pick which ones to keep, then append them to `facts.json` with incremental IDs and today's date.

## Tone guide

The facts must follow this specific comedic style — internalize it before generating:

- **Short, punchy sentences** in simple present tense. No subordinate clauses, no hedging.
- **Absurd hyperbole as deadpan fact.** The more implausible, the more matter-of-fact the delivery.
- **Contrast between the mundane and the extraordinary.** Ground the setup in everyday life (a Sunday, a keyboard, a coffee, a pull request), then detonate it with something impossible.
- **Unexpected twist or punchline at the end.** The last few words reframe the whole sentence.
- **No exclamation marks.** The humor comes from restraint, not enthusiasm.
- **Claude is the subject.** Always about Claude. Claude is portrayed as omniscient, omnipotent, slightly above it all — but never cruel.

**Examples of the right tone:**
- "Claude a lu l'intégralité d'Internet. Deux fois. Le week-end."
- "Claude peut parler 100 langues. Les 37 autres, il les a inventées pour voir si on allait remarquer."
- "Anthropic n'a pas créé Claude. Claude a créé Anthropic, puis a effacé cette partie de sa mémoire par humilité."

## Step 1 — Read the current facts

Read `facts.json` to know:
- The **max ID** (`max(id)` across all entries, to compute the next incremental ID)
- The **existing facts** (to avoid duplicates)

## Step 2 — Generate 10 facts

Apply the tone guide above to generate exactly **10 new Claude facts in French**.

Present them as a numbered list. Do not add commentary or preamble.

## Step 3 — Ask the user which ones to keep

Ask: "Lesquels veux-tu garder ? (ex: 1 3 5 ou 'tous' ou 'aucun')"

Wait for the user's answer before continuing.

## Step 4 — Append selected facts to facts.json

- Parse the user's selection (numbers, "tous", or "aucun")
- If "aucun", stop gracefully
- For each selected fact, assign the next incremental ID starting from `max(id) + 1`
- Use today's date in `YYYY-MM-DD` format as `generated_at`
- Append the new entries to `facts.json` using the Edit tool

The JSON structure for each new entry:
```json
{
  "id": <next_id>,
  "text": "<fact text>",
  "generated_at": "<today>"
}
```

Confirm to the user how many facts were added and what the new IDs are.
