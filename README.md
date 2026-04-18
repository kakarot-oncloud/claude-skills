<div align="center">

# 🧠 Claude Skills

### A curated collection of 10 high-quality, daily-use Claude skills you can drop straight into Claude.ai or the API.

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![Skills: 10](https://img.shields.io/badge/Skills-10-blueviolet)](#-the-skills)
[![Made for Claude](https://img.shields.io/badge/Made%20for-Claude-orange)](https://claude.ai)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#-contributing)

*Practical. Battle-tested. No filler.*

</div>

---

## 🌟 What is this?

A hand-picked collection of **10 ready-to-use Claude skills** (system prompts) that solve real, daily problems — from writing better emails and summarizing long articles to compressing prompts so free-tier users can do more with each message.

Each skill is:

- ✅ **Drop-in ready** — copy the system prompt, paste into a Claude Project, done
- ✅ **Daily-use focused** — every skill solves a problem people face every day
- ✅ **Documented** — each skill has its own README with examples and tips
- ✅ **No fluff** — no overlapping skills, no novelty toys

---

## 📚 The Skills

| # | Skill | What it does |
|---|-------|--------------|
| 1 | [💰 **Token Saver**](./skills/token-saver/) | Compresses prompts/text into tiny token footprints — built for **free-tier users** |
| 2 | [✉️ **Email Assistant**](./skills/email-assistant/) | Writes daily emails, replies, follow-ups, and polite declines |
| 3 | [📝 **Meeting Notes → Actions**](./skills/meeting-notes-to-actions/) | Messy notes → decisions, action items (owner + deadline), open questions |
| 4 | [📄 **Resume Tailor**](./skills/resume-tailor/) | Rewrites your resume for a specific job — without inventing experience |
| 5 | [🎓 **Study Buddy**](./skills/study-buddy/) | Tutors any topic with analogies, flashcards, and quizzes |
| 6 | [💻 **Code Explainer**](./skills/code-explainer/) | Explains, debugs, and improves code in plain English |
| 7 | [🔁 **Content Repurposer**](./skills/content-repurposer/) | One piece of content → tweet thread, LinkedIn, blog, newsletter, video script |
| 8 | [⚖️ **Decision Helper**](./skills/decision-helper/) | Weighted pros/cons + a real recommendation for any decision |
| 9 | [📚 **Smart Summarizer**](./skills/smart-summarizer/) | Tiered summaries: TL;DR → key points → full breakdown → quotes |
| 10 | [✨ **Prompt Improver**](./skills/prompt-improver/) | Turns vague prompts into structured prompts that work |

---

## 🚀 How to use these skills

You have **three good options**, depending on how much you'll use the skill.

### Option 1 — Claude Projects (recommended for skills you'll reuse)

1. Open [Claude.ai](https://claude.ai) → **Projects** → **New Project**
2. Open the skill folder you want (e.g. [`skills/email-assistant/`](./skills/email-assistant/))
3. Open `system_prompt.md` → copy everything
4. Paste into **Project instructions** → save
5. Open a new chat in that project — the skill is now active

### Option 2 — One-off conversations

1. Open the skill's `system_prompt.md`
2. Copy it
3. Paste at the top of a new Claude conversation
4. Add your actual request below it

### Option 3 — API / Custom apps

1. Use the contents of `system_prompt.md` as the `system` parameter in your Anthropic API call
2. Pass the user's request as the user message

```python
import anthropic

with open("skills/email-assistant/system_prompt.md") as f:
    system_prompt = f.read()

client = anthropic.Anthropic()
message = client.messages.create(
    model="claude-sonnet-4-5",
    max_tokens=1024,
    system=system_prompt,
    messages=[{"role": "user", "content": "Reply to my boss about being sick tomorrow"}]
)
print(message.content[0].text)
```

---

## 💡 Free-tier tips

If you're on Claude's free plan, these skills stretch your messages further:

- **Start with [Token Saver](./skills/token-saver/)** — compress your prompts before pasting them. 30-60% smaller is normal.
- **Use [Smart Summarizer](./skills/smart-summarizer/)** before passing long text into another skill — fewer input tokens, faster responses.
- **Build a single Project** with the skill you use most. You don't pay for re-pasting the system prompt every time.
- **Pair skills:** Smart Summarizer → Decision Helper. Meeting Notes → Email Assistant (for follow-ups).

---

## 🧩 How a skill is structured

Every skill folder follows the same layout:

```
skills/<skill-name>/
├── system_prompt.md   ← Paste this into Claude
└── README.md          ← Description, examples, tips
```

The system prompt always includes:

- **Role** — who Claude is acting as
- **Job** — the specific task
- **Output format** — exact structure of the response
- **Rules** — what to never do, what to always do
- **Examples** — to lock in the behavior

This format works in Claude.ai, the Anthropic API, third-party clients (Cursor, Continue, Open WebUI), and most other LLM platforms with minor tweaks.

---

## 🛠️ Built for real life

This isn't a theoretical skill list. Every skill in this repo solves a problem you probably hit this week:

- Got a long email thread? → **Smart Summarizer**
- Stuck on a decision? → **Decision Helper**
- Need to send a difficult email? → **Email Assistant**
- Studying for something? → **Study Buddy**
- Hit your free-plan limit? → **Token Saver**

If a skill doesn't earn its place, it's not in this repo.

---

## 🤝 Contributing

Contributions are welcome — but the bar is high. To add a new skill:

1. Make sure it solves a **real, daily** problem not already covered
2. Write the system prompt in the same structure as existing skills (Role / Job / Output format / Rules / Examples)
3. Add a README in the skill's folder with: description, when to use, how to install, an example, tips, and what it won't do
4. Add it to the table in this README
5. Open a PR with a 1-line summary of why it earned its slot

**What we won't merge:**
- Joke / novelty skills with no real use case
- Skills that overlap heavily with existing ones
- Skills that don't ship a clear output format

---

## 📜 License

[MIT](./LICENSE) — use freely, modify freely, ship freely. Attribution appreciated but not required.

---

## ⭐ Like the repo?

If a skill saved you time today, consider giving the repo a star — it helps others find it.

<div align="center">

**Built for people who use Claude every day.**

</div>
