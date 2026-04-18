# ⚖️ Decision Helper

> A structured thinking partner for decisions of any size. Weighted pros/cons, blind-spot detection, and an actual recommendation — not "it depends".

## Why this skill exists
Pros-and-cons lists are weak because they treat all factors as equal. This skill weights criteria by what actually matters to you, surfaces blind spots you haven't considered, and **commits to a recommendation** — then honestly tells you when it would be wrong.

## When to use it
- Choosing between 2-5 options (job offers, tools, vendors, products)
- Stuck on a decision you've been avoiding
- Need to justify a choice to others
- Want a second opinion that won't just agree with you
- "Should I do X or not?" — open-ended deliberation

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
1. A clear framing of the actual decision
2. Weighted criteria table — what matters and how much
3. Each option compared with pros, cons, and a weighted score
4. **Blind spots** — things you probably haven't considered
5. **A specific recommendation** with reasoning + the case against
6. **Reversibility check** — how recoverable is being wrong?
7. A cheap experiment to de-risk if applicable

## Example

**You give it:**
> Should I take the senior engineer offer at a 50-person Series B startup ($200K, 0.2% equity) or stay at my current FAANG job ($280K, vested)? I'm bored at my current job but the startup is risky.

**You get:** a framed decision, weighted criteria (compensation, growth, risk tolerance, learning velocity, optionality), both options scored, blind spots ("you said you're bored — would you actually work harder at the startup, or is the boredom about the work itself?"), and a specific recommendation with the case against it.

## Tips
- **State constraints clearly.** "Must be under $1000" or "must close by Q3" — the skill respects these.
- **Mention emotional pulls.** "I really want option B but everyone says A is smarter" — this matters.
- **Ask for re-analysis** if your situation changes. "What if the salary was $250K instead?"
- **Use it on small decisions too** to practice the framework.

## What it won't do
- Punt with "it depends"
- Recommend an option that violates your stated constraints
- Hide its reasoning
- Pretend to know things it can't (like future market conditions)
