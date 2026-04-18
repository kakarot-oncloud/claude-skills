# 📄 Resume Tailor

> Rewrite your resume for a specific job — without making anything up. Improves match score, mirrors job-description language, flags honest gaps.

## Why this skill exists
Generic resumes get ignored. Tailored ones get callbacks — but tailoring takes hours and most people don't bother. This skill does it in one paste, ATS-aware, and stays honest (no invented experience).

## When to use it
- Applying to a specific role and want maximum match
- Pivoting to a new function — needs reframing
- Updating an old resume to read modern
- Want to know which keywords you're missing

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


## What you give it
- **Your current resume** (text or markdown)
- **The job description** you're targeting

## What it gives back
- A **match analysis** — current vs tailored estimated match %
- The **rewritten resume** in plain text / markdown (ATS-safe)
- A **change log** — what was rewritten, what was added, what was cut
- **Suggested additions** — things the JD asks for that you might have but didn't list (phrased as questions, not assumptions)
- **Red flags & gaps** — honest issues a recruiter will spot

## Example flow

```
[paste current resume]
[paste job description]
```

→ Skill returns a tailored resume with:
- JD keywords woven into your real bullets
- Reordered sections (most relevant first)
- Quantified bullets where missing (with `[X%]` placeholders for you to fill in)
- A list of things to ask yourself ("Did you ever lead a team? The JD wants this.")

## Tips
- **Be honest in placeholders.** When the skill puts `[X%]` for a metric, fill in real numbers — don't guess.
- **Run it once per role.** Don't try to make one resume for 10 jobs.
- **Keep your "master resume" long.** Then let this skill cut it down per role.
- **Pair with a cover letter prompt** for a complete application.

## What it won't do
- Invent jobs, dates, certifications, or metrics
- Force a match for a totally different career track (it'll flag that honestly)
- Use tables or columns (ATS systems break on those)
