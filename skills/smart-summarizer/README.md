# 📚 Smart Summarizer

> Tiered summaries: TL;DR, key points, structured breakdown, and notable quotes. Stop reading at any tier — you'll have what you need.

## Why this skill exists
Most summaries are one flat block of text. This skill gives you a **layered summary** — a one-liner for skimmers, key bullets for browsers, a full structured breakdown for serious readers, and verbatim quotes/stats for when you need to cite the source.

## When to use it
- Long articles, papers, or reports you don't have time to read
- Podcast/video transcripts
- Books or chapters
- Long documents at work
- Research papers
- Substack essays you want the gist of

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


## What it gives back
Every summary has 4 tiers + a trust note:

- **⚡ TL;DR** — one sentence
- **🎯 Key Points** — 3-7 bullets
- **📘 Structured Summary** — context, main argument, evidence, caveats, conclusions
- **🔍 Notable Quotes / Stats** — verbatim, ready to cite
- **Trust note** — flags bias, thin sourcing, or one-sided framing

## Example

**You give it:** a 5,000-word essay arguing for universal basic income.

**You get back:**
```
## ⚡ TL;DR (1 sentence)
The author argues UBI is the cheapest, simplest fix to automation-driven inequality, citing pilot results from Finland and Kenya.

## 🎯 Key Points
- Three main pilots (Finland, Kenya, Stockton CA) showed [specific outcomes]
- Cost is lower than current welfare-program overhead
- ...

## 📘 Structured Summary
[full breakdown with main argument, evidence, caveats, conclusions]

## 🔍 Notable Quotes / Stats
> "The Finnish pilot reduced reported stress by 17% with no measurable drop in employment."

---
**Reading time saved:** ~25 min
**Trust note:** Author is a UBI advocate; counter-arguments are addressed but briefly.
```

## Tips
- **Paste long text in chunks** if it exceeds context — re-summarize the partials together at the end.
- **Ask for a deeper dive on one tier.** "Expand the evidence section."
- **Use the Trust Note seriously.** It tells you when to seek another source.
- **Combine with Decision Helper** when summarizing multiple options for a choice.

## What it won't do
- Editorialize or insert opinions
- Round numbers from the source
- Hide bias when the source is one-sided
- Add facts not in the source (without labeling them `[external context]`)
