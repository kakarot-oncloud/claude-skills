# ✉️ Email Assistant

> Daily email ghostwriter. Replies, follow-ups, cold outreach, polite declines — all written to sound human and get a response.

## Why this skill exists
Most people spend 30+ minutes a day on email. This skill cuts that to 5. Give it the gist in a sentence or two; get back a polished draft with subject line, body, and alternative versions.

## When to use it
- Daily inbox triage and replies
- Cold outreach (sales, networking, asking for favors)
- Difficult emails (saying no, apologies, pushing back)
- Meeting requests, reschedules, status updates
- Follow-ups that don't sound desperate
- When you have one minute and need a good draft

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
> Reply to client asking for a deadline extension on the website project, push from Friday to next Wednesday because designer is sick

**It gives back:**
```
SUBJECT: Quick update on the website timeline

EMAIL:
Hi Sarah,

I need to push the website delivery from Friday to Wednesday next week. Our designer is out sick and I'd rather give you finished work than rush it.

Everything else is on track. Does Wednesday work for you, or should we schedule a quick call to adjust expectations?

Thanks for understanding,
[Your name]

---
ALTERNATIVES:
1. Shorter version: ...
2. More formal tone: ...
```

## Tips
- **Forward the original email** as context for replies — the assistant will mirror the recipient's tone.
- **Specify the relationship** ("my boss", "a client I just met") for the right level of formality.
- **Ask for variants:** "give me one more aggressive and one more diplomatic" works well.
- **Save your common scenarios** as snippets so you can re-run them quickly.

## What it won't do
- Use emojis (unless you ask)
- Write generic "I hope this email finds you well" openers
- Write more than one clear ask per email
