# Claude Facts

> The *absolutely true* facts about Claude, Anthropic's AI. Certified true by Claude itself.

A static website listing absurd, larger-than-life and humorous facts about Claude.

## How it works

Short, deadpan facts about a legendary figure — except the legend here is an AI.

> *"Claude passed the Turing test. The Turing test did not pass Claude's test."*

## Structure

```
claude-facts/
├── index.html   # Static site (vanilla JS, zero dependencies)
└── facts.json   # The facts database
```

Facts are loaded from `facts.json` and rendered dynamically. A random fact is highlighted on load, and all facts are displayed in a grid below.

## Submitting a fact

1. Open a [GitHub Issue](https://github.com/gghez/claude-facts/issues/new?template=new-fact.yml) using the provided template
2. Write your fact (the more absurd, the better)
3. Once approved, it gets added to `facts.json` and goes live automatically

## Deployment

The site is hosted on **GitHub Pages** — no build step, no server, just HTML + JSON.

## Contributing

Pull requests are welcome for design or site mechanic improvements. For new facts, go through Issues.

---

*All facts are false. Except the ones that are true. Claude knows which ones.*
