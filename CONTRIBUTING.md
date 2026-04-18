# Contributing

Thanks for your interest in contributing! This repo is intentionally curated — we'd rather have 10 great skills than 100 mediocre ones.

## Adding a new skill

1. **Check it doesn't overlap** with an existing skill. Combinations of two existing skills don't count as new.
2. **Make sure it has daily-use value.** "Could a regular person use this this week?" is the bar.
3. **Use the standard skill structure** (see existing skills as templates).

### Folder layout

```
skills/<your-skill-name>/
├── system_prompt.md
└── README.md
```

### `system_prompt.md` should contain

- **Role** — who Claude acts as
- **Your job** — what the skill does
- **Output format** — exact structure of the response
- **Rules** — never-dos and always-dos
- **At least one example** — input → output

### `README.md` should contain

- One-line tagline
- Why this skill exists
- When to use it
- How to install (3 standard options)
- A worked example
- Tips
- What it won't do

## Editing an existing skill

Small improvements (typos, clearer wording, better examples) are always welcome.

For larger changes (output format, rule changes), open an issue first to discuss.

## Style

- Plain language. No buzzwords.
- Active voice.
- Short sentences.
- No emoji vomit.

## What we won't merge

- Joke skills
- Skills that overlap with existing ones
- Skills without a clear output format
- Skills with vague "you are an expert" prompts and nothing else

Open a PR with a 1-line summary of why your skill earned its slot. Thanks!
