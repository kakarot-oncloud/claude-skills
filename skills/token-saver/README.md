# 💰 Token Saver

> Compress prompts and text into the smallest token footprint without losing meaning. Built for free-tier and budget-conscious Claude users.

## Why this skill exists
Free-tier Claude users hit message and context limits fast. Most prompts are 30-60% larger than they need to be — full of polite fluff, redundant context, and verbose phrasing. This skill rewrites them into the tightest version that still does the job.

## When to use it
- You're on Claude's free plan and want to fit more into each message
- You're paying per-token via the API and want to cut bills
- You're building a system prompt and want it as compact as possible
- You're hitting context-window limits with long inputs

## How to install

  This skill follows Claude's official **Agent Skills** format.

  **Option A — Upload to Claude.ai (Pro/Team/Enterprise):**
  1. Download [`SKILL.md`](./SKILL.md) (or grab the prebuilt zip from `dist/` in the repo root)
  2. In Claude.ai → **Settings → Capabilities → Skills → Upload skill**
  3. Select the file or folder. Done — Claude will use it automatically when relevant.

  **Option B — Claude Code:**
  Copy this folder into `~/.claude/skills/` (global) or your project's `.claude/skills/` directory.

  **Option C — Free-tier fallback:**
  Open `SKILL.md`, copy everything **after** the `---` frontmatter block, paste at the top of a new Claude conversation, then add your request below.


## Example

**You give it:**
> Could you please help me write a really nice and friendly email to my boss letting them know that I won't be able to make it to the meeting tomorrow because I'm feeling sick?

**It gives back:**
```
COMPRESSED:
Write a friendly email to my boss: I'll miss tomorrow's meeting — I'm sick.

ORIGINAL TOKENS (est): 38
COMPRESSED TOKENS (est): 16
SAVED: 58%
```

## Tips
- **Compress your system prompts first.** Those run on every message — savings compound.
- **Don't compress code or quoted text.** The skill preserves these automatically, but double-check.
- **Use it on long source material** before pasting it into another Claude conversation.
- For massive savings, run this on your custom system prompts once and save the compressed version.

## What it won't do
- Drop instructions or constraints
- Rewrite code, URLs, file paths, or quoted strings
- Compress text that's already efficient (it'll tell you so)
