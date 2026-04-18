<div align="center">

# 🧠 Claude Skills

### 10 high-quality, daily-use Claude Skills in the official `SKILL.md` format — download and upload directly to Claude.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Skills: 10](https://img.shields.io/badge/Skills-10-blueviolet)](#-the-skills)
[![Format: Claude Skills](https://img.shields.io/badge/Format-Claude%20Skills-orange)](https://docs.claude.com/en/docs/agents-and-tools/agent-skills)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](./CONTRIBUTING.md)

*Practical. Battle-tested. No filler.*

</div>

---

## 🌟 What is this?

A curated collection of **10 ready-to-upload Claude Skills** that solve real, daily problems — from compressing prompts for free-tier users, to writing better emails, summarizing long articles, and tailoring resumes.

Every skill follows **Claude's official Agent Skills format**: a `SKILL.md` file with YAML frontmatter (`name`, `description`) and the skill's instructions. Drop the folder (or zip) into Claude.ai or pass it to the Claude API/Claude Code, and Claude will autonomously use the skill when relevant.

---

## 📚 The Skills

| # | Skill | What it does | Download |
|---|-------|--------------|----------|
| 1 | [💰 **token-saver**](./skills/token-saver/) | Compresses prompts/text into tiny token footprints — built for **free-tier users** | [📦 zip](./dist/token-saver.zip) |
| 2 | [✉️ **email-assistant**](./skills/email-assistant/) | Writes daily emails, replies, follow-ups, polite declines | [📦 zip](./dist/email-assistant.zip) |
| 3 | [📝 **meeting-notes-to-actions**](./skills/meeting-notes-to-actions/) | Messy notes → decisions, action items, owners, deadlines | [📦 zip](./dist/meeting-notes-to-actions.zip) |
| 4 | [📄 **resume-tailor**](./skills/resume-tailor/) | Rewrites resume to match a job — without inventing experience | [📦 zip](./dist/resume-tailor.zip) |
| 5 | [🎓 **study-buddy**](./skills/study-buddy/) | Tutors any topic with analogies, flashcards, and quizzes | [📦 zip](./dist/study-buddy.zip) |
| 6 | [💻 **code-explainer**](./skills/code-explainer/) | Explains, debugs, and improves code in plain English | [📦 zip](./dist/code-explainer.zip) |
| 7 | [🔁 **content-repurposer**](./skills/content-repurposer/) | One source → tweet, LinkedIn, blog, newsletter, video script | [📦 zip](./dist/content-repurposer.zip) |
| 8 | [⚖️ **decision-helper**](./skills/decision-helper/) | Weighted pros/cons + a real recommendation for any decision | [📦 zip](./dist/decision-helper.zip) |
| 9 | [📚 **smart-summarizer**](./skills/smart-summarizer/) | Tiered summaries: TL;DR / key points / full / quotes | [📦 zip](./dist/smart-summarizer.zip) |
| 10 | [✨ **prompt-improver**](./skills/prompt-improver/) | Turns vague prompts into structured prompts that work | [📦 zip](./dist/prompt-improver.zip) |

**👉 [Download all 10 as a single bundle (`all-skills.zip`)](./dist/all-skills.zip)**

---

## 🚀 How to use these skills

These skills follow Claude's official **Agent Skills** format. There are several ways to use them, depending on your setup.

### ✅ Option 1 — Upload to Claude.ai (Pro / Team / Enterprise)

1. **Get the skill** — either:
   - Download the individual `.zip` from the table above, **or**
   - Download all skills via the bundle: [`dist/all-skills.zip`](./dist/all-skills.zip)
2. In Claude.ai, open **Settings → Capabilities → Skills**
3. Click **Upload skill** and select the `.zip` file (or the unzipped folder)
4. Claude will now use the skill automatically when your message matches its description

> If you're on Claude **Free**, skill upload may not be available — use Option 4 instead.

### ✅ Option 2 — Use with Claude Code

1. Clone this repo or download the skill folder you want
2. Place it in your project's `.claude/skills/` directory (or globally in `~/.claude/skills/`)
3. Run Claude Code in that project — the skills are auto-loaded

```bash
git clone https://github.com/kakarot-oncloud/claude-skills.git
mkdir -p ~/.claude/skills
cp -r claude-skills/skills/* ~/.claude/skills/
```

### ✅ Option 3 — Use with the Claude API

Pass the skill folder when configuring your agent. See [Anthropic's Agent Skills docs](https://docs.claude.com/en/docs/agents-and-tools/agent-skills) for the latest API specifics.

### ✅ Option 4 — Free-tier fallback (any Claude account)

Even without skill upload, you can use these manually:

1. Open the skill folder (e.g. `skills/email-assistant/SKILL.md`)
2. Copy everything **after** the `---` frontmatter block (just the body)
3. Paste at the top of a new Claude conversation, then add your request below
4. (Optional) Save as a Claude Project's custom instructions for one-click reuse

---

## 🧩 Skill format

Every skill folder follows Claude's official structure:

```
skills/<skill-name>/
├── SKILL.md      ← name + description in YAML frontmatter, instructions in markdown
└── README.md     ← human-friendly docs (when to use, examples, tips)
```

A `SKILL.md` looks like this:

```markdown
---
name: skill-name
description: "What this skill does and when Claude should invoke it. This is what Claude reads to decide whether to use the skill."
---

# Instructions

(The full skill behavior, output format, rules, and examples go here.)
```

The **`description`** field is critical — Claude uses it to decide *when* to invoke the skill. Each skill in this repo has a tightly-written description that triggers reliably on the right requests.

---

## 💡 Free-tier tips

If you're on Claude Free:

- Start with [`token-saver`](./skills/token-saver/) — copy-paste it manually and use it to compress every long prompt before sending. 30-60% smaller is normal.
- Pair [`smart-summarizer`](./skills/smart-summarizer/) with anything else — summarize first, analyze second.
- Save your most-used skill as a **Claude Project's** custom instructions so you don't re-paste it on every chat.
- **Best combos:** `smart-summarizer → decision-helper`, `meeting-notes-to-actions → email-assistant`.

---

## 🛠️ Built for real life

This isn't a theoretical skill list. Every skill solves a problem you probably hit this week:

| Situation | Use this |
|-----------|----------|
| Got a long article you don't want to read | `smart-summarizer` |
| Stuck on a decision | `decision-helper` |
| Need to send a difficult email | `email-assistant` |
| Studying for an exam or interview | `study-buddy` |
| Hit your free-plan limit | `token-saver` |
| Trying to understand legacy code | `code-explainer` |
| Just wrote a blog post | `content-repurposer` |
| Job hunting | `resume-tailor` |
| Just finished a meeting | `meeting-notes-to-actions` |
| Your prompts keep returning bad answers | `prompt-improver` |

If a skill doesn't earn its place, it's not in this repo.

---

## 🤝 Contributing

Contributions welcome — bar is high. See [CONTRIBUTING.md](./CONTRIBUTING.md) for the rules.

To add a new skill:

1. Create `skills/<your-skill-name>/SKILL.md` with proper YAML frontmatter (`name`, `description`)
2. Create `skills/<your-skill-name>/README.md` with human docs
3. Build a zip: `cd skills/<your-skill-name> && zip ../../dist/<your-skill-name>.zip SKILL.md`
4. Add it to the table in this README
5. Open a PR with a 1-line summary of why it earned its slot

---

## 📜 License

[MIT](./LICENSE) — use freely, modify freely, ship freely. Attribution appreciated but not required.

---

## ⭐ Like the repo?

If a skill saved you time today, give the repo a star — it helps others find it.

<div align="center">

**Built for people who use Claude every day.**

[Skills](./skills/) · [Downloads](./dist/) · [Contributing](./CONTRIBUTING.md) · [License](./LICENSE)

</div>
