# Contributing

Thanks for your interest in contributing! This repo is intentionally curated — we'd rather have 10 great skills than 100 mediocre ones.

## Adding a new skill

1. **Check it doesn't overlap** with an existing skill. Combinations of two existing skills don't count as new.
2. **Make sure it has daily-use value.** "Could a regular person use this this week?" is the bar.
3. **Use Claude's official skill format** (see existing skills as templates).

### Folder layout

```
skills/<your-skill-name>/
├── SKILL.md      ← Claude Skills format (YAML frontmatter + instructions)
└── README.md     ← Human-friendly docs
```

### `SKILL.md` should contain

The official Claude Skills format:

```markdown
---
name: your-skill-name
description: "What this skill does and exactly when Claude should invoke it. Be specific — Claude uses this to decide whether to load the skill. Mention trigger phrases the user is likely to say."
---

# Skill instructions

## Your job
...

## Output format
...

## Rules
...

## Examples
...
```

**The `description` field is critical.** It's how Claude decides when to use the skill. Bad description = the skill never gets invoked. Include trigger phrases the user would actually say.

### `README.md` should contain

- One-line tagline
- Why this skill exists
- When to use it
- How to install (link to the standard upload guide)
- A worked example
- Tips
- What it won't do

### Build the downloadable zip

After adding the skill, build its zip:

```bash
cd skills/<your-skill-name>
zip ../../dist/<your-skill-name>.zip SKILL.md
```

Then rebuild the bundle:

```bash
cd skills
zip -r ../dist/all-skills.zip . -x "*/README.md"
```

### Update the table

Add a row to the table in the root `README.md`.

## Editing an existing skill

Small improvements (typos, clearer wording, better examples) are always welcome.

For larger changes (output format, rule changes, description rewrites), open an issue first to discuss.

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
- Skills with a weak `description` field that won't trigger reliably

Open a PR with a 1-line summary of why your skill earned its slot. Thanks!
