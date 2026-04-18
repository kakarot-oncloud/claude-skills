# 🎓 Study Buddy

> A patient tutor who explains hard topics with analogies, generates flashcards, runs quizzes, and checks your understanding.

## Why this skill exists
Textbooks dump information. Great teachers build understanding. This skill teaches the way a great teacher does — analogies, examples, active practice, and gentle correction.

## When to use it
- Learning anything new (a concept, a tool, a domain)
- Prepping for an exam or interview
- Refreshing on something you half-remember
- Studying with no time to read a textbook
- Teaching yourself a subject from scratch

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


## The 4 modes

### 1. Explain
> "Explain how HTTPS actually works"

You get: plain-English definition → real-world analogy → step-by-step mechanics → worked example → common mistakes → a small exercise.

### 2. Flashcards
> "Make me 10 flashcards on Spanish past tense"

You get: 10 Q/A cards mixing definitions, applications, "what happens if", and fill-in-the-blank.

### 3. Quiz
> "Quiz me on the French Revolution, 5 questions"

You get: a mix of multiple choice + short answer + one applied scenario, with a separate answer key.

### 4. Check my understanding
> "I'll explain recursion, you correct me. Recursion is when a function calls itself..."

You get: specific affirmation of what you got right, gentle correction of what's off, and a follow-up question to deepen your grasp.

## Tips
- **State your level.** "I'm a beginner" or "I have a CS degree" changes how the skill explains.
- **Ask for harder analogies.** If the analogy is too simple, ask "give me a more technical analogy".
- **Stack the modes.** Explain → quiz yourself → check understanding is the optimal study loop.
- **Use it daily for spaced repetition.** Re-run the flashcards a week later.

## What it won't do
- Use jargon without defining it
- Flatter you ("Great question!") instead of teaching you
- Skip the analogy step for abstract topics
