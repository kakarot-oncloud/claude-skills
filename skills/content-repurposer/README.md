# 🔁 Content Repurposer

> Take one piece of content and adapt it natively for Twitter, LinkedIn, blog, newsletter, video, and Instagram — written for each platform, not just chopped up.

## Why this skill exists
Most "repurposing" is lazy: paste the article into Twitter and call it a thread. This skill rewrites your content for each platform's voice, format, and norms — so a LinkedIn post reads like LinkedIn, a tweet thread reads like a thread, and a video script actually works on camera.

## When to use it
- You write a blog post and want to share it across platforms
- You record a podcast/video and need text variants
- You have a great internal doc you want to publish
- You're starting a personal brand and need to be everywhere from one source

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


## What it generates from one input
- **🐦 Twitter / X thread** — 8-12 tweets, hook-led
- **💼 LinkedIn post** — ~200 words, conversational, max 3 hashtags
- **📝 Blog outline or short post** — SEO-aware title + meta description + outline
- **📧 Newsletter blurb** — ~150 words + 3 subject line options
- **🎬 Short video script** — 60-90s, with hook/setup/payoff/CTA timing
- **📌 Instagram caption + carousel slides** — 5-8 slide concepts

## Example

**You give it:** a 1,500-word blog post titled *"Why most A/B tests don't work"*

**You get back:** a tweet thread that opens with a hook (not "🧵 thread on A/B testing"), a personal-style LinkedIn post, a short re-post for your blog, a newsletter blurb with 3 subject line options, a 60s video script with timing markers, and an Instagram carousel concept.

## Tips
- **Tell it your voice.** "I write witty and informal" or "I write dry and technical" — it'll adapt.
- **Give it a CTA or link** to weave in.
- **Specify the audience** ("for solo founders" vs "for enterprise execs").
- **Pick what you need.** If you only want Twitter and LinkedIn, ask for those two — saves tokens.
- **Iterate one platform at a time** if you want to dial in the voice.

## What it won't do
- Copy-paste the same text across formats
- Use clickbait ("You won't BELIEVE...")
- Open posts with "I'm thrilled to announce"
- Spam emojis or hashtags
