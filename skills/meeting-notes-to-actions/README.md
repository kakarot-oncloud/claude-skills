# 📝 Meeting Notes → Actions

> Turn messy meeting notes or transcripts into a clean record of what was decided and who's doing what next.

## Why this skill exists
Meetings produce notes. Notes go nowhere. This skill turns the chaos into a structured summary with **decisions, action items (owner + deadline), open questions, and risks** — readable in 60 seconds by anyone who missed the meeting.

## When to use it
- After every meeting — paste your notes in, get a summary out
- Processing call transcripts (Zoom, Otter, Fireflies)
- Recapping a stand-up, planning session, or 1:1
- Turning a long email thread into a decision log
- Building a meeting record you can search later

## How to install
1. Copy `system_prompt.md` contents
2. Use in a Claude Project (great for repeated use) or paste as a one-off system prompt
3. Drop your raw notes / transcript into the conversation

## Example

**You give it:**
> Notes from product sync, april 18:
> mike said pricing page needs new copy by next fri
> we agreed to drop the dark mode feature for v2
> sarah will write the launch email but unclear when
> open question: do we need legal to review terms before launch?
> revenue down 5% but might be seasonal

**It gives back:**
```
# Product Sync
**Date:** April 18
**Attendees:** Mike, Sarah, others (not specified)

## TL;DR
Dark mode dropped from v2. Pricing copy due Friday. Legal review on terms is unresolved.

## Key Decisions
- Drop dark mode from the v2 release

## Action Items
| # | Action | Owner | Due |
|---|--------|-------|-----|
| 1 | Write new copy for pricing page | Mike | Fri next week |
| 2 | Write launch email | Sarah | TBD |

## Discussion Highlights
- Revenue down 5% — possibly seasonal, needs investigation

## Open Questions / Parking Lot
- Does legal need to review terms before launch?
- When does Sarah's launch email need to ship?

## Risks & Blockers
_None explicitly raised._
```

## Tips
- **Paste raw transcripts** — the skill strips filler and attributes only when it matters.
- **Use it for written threads** too (Slack, email chains) by pasting the conversation.
- **Re-run with new context.** "Mike confirmed launch email is due May 1" updates the doc.
- **Combine with Smart Summarizer** for very long sessions.

## What it won't do
- Invent owners or deadlines (always marks them "TBD")
- Confuse decisions with discussion
- Add commentary or opinions
