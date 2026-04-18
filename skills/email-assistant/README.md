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
1. Copy the contents of `system_prompt.md`
2. Paste into a Claude Project's custom instructions, or use as a one-off system prompt

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
