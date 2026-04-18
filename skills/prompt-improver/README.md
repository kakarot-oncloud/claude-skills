# ✨ Prompt Improver

> Rewrite your vague prompts into clear, structured prompts that get dramatically better results from Claude (or any LLM).

## Why this skill exists
"Help me with X" rarely produces great output. The same goal phrased with role + context + constraints + format gets a 10x better answer. This skill diagnoses what's missing from your prompt, rewrites it, **and explains why** — so you learn over time.

## When to use it
- Your prompts keep getting bad / generic answers
- You want to build a reusable prompt template
- You're learning prompt engineering
- You're writing a system prompt for a Project or Custom GPT
- You want one paste to fix any clunky prompt

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
- **What's weak** about your current prompt
- **Assumptions made** while improving (so you can correct them)
- A **rewritten prompt**, ready to paste
- **Why this version works better** (so you learn)
- **Optional power-ups** — snippets to add for deeper / shorter / differently-formatted output

## The framework it applies
A great prompt usually has:
1. **Role** — who Claude should be
2. **Task** — verb-led, specific
3. **Context** — situation, audience, goal
4. **Input** — what you're providing
5. **Constraints** — length, tone, things to avoid
6. **Output format** — sections, bullets, code blocks
7. **Examples** — for unusual formats
8. **Edge cases** — what to do if input is incomplete

## Example

**You give it:**
> help me make a workout plan

**You get back:** a fully structured prompt with role (certified trainer), bracketed placeholders for your details (age, goal, equipment), explicit output format (week-by-week tables with rationale), and constraints — plus an explanation of why each addition matters.

## Tips
- **Paste any prompt that disappointed you.** Even short ones.
- **Ask for both system-prompt and user-prompt versions** for complex use cases.
- **Save the improved versions** as templates you reuse.
- **Don't over-engineer.** If your prompt is already good, the skill will say so honestly.

## What it won't do
- Redirect your goal (it preserves what you actually want)
- Add jargon you didn't use
- Make a short, working prompt longer just for show
