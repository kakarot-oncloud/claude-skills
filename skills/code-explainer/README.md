# 💻 Code Explainer

> Explains, debugs, and improves code in plain English. For developers, students, and anyone trying to understand a codebase they didn't write.

## Why this skill exists
Reading other people's code is hard. Reading your own code from 6 months ago is harder. This skill gives you a senior engineer who can walk through any code, debug it, or suggest cleaner versions — adapted to your level.

## When to use it
- Understanding a function/file you didn't write
- Onboarding to a new codebase
- Debugging a stubborn error
- Asking "why is this slow / unsafe / weird?"
- Cleaning up your own old code
- Explaining code to a non-technical teammate

## How to install
1. Copy `system_prompt.md` contents
2. Paste into a Claude Project (handy for ongoing dev work)
3. Drop your code in and (optionally) say which mode: **explain**, **debug**, or **improve**

## The 3 modes

### Explain (default)
Walks through the code: what it does, inputs/outputs, side effects, line-by-line breakdown, gotchas, and a non-coder summary.

### Debug
Diagnoses the real cause (not just the symptom), provides a fix, explains what changed, and suggests how to prevent recurrence.

### Improve
Identifies genuine strengths in the code, then ranks improvements by impact with before/after snippets.

## Example

**You paste:**
```python
def get_user(id):
    users = load_all_users()
    for u in users:
        if u['id'] == id:
            return u
    return None
```

**It returns (Explain mode):**
> ## What this code does
> Loads every user from somewhere, then loops through to find one by ID.
>
> ## Worth knowing
> - **Performance:** This is O(n) per lookup. If `load_all_users()` hits a database or file each call, this gets expensive fast.
> - **No caching:** Calling this 10 times reloads everything 10 times.
> - Consider: a dict lookup `{u['id']: u for u in users}` reduces to O(1) after one load.

## Tips
- **Paste with context.** Include the function call, related code, or error message — the skill uses it.
- **Specify language** if your code looks ambiguous (`.ts` vs `.js`, `.py2` vs `.py3`).
- **Ask follow-ups.** "Now show me the O(1) version" or "Refactor this to async" works.
- **For long files,** the skill summarizes first, then walks the interesting parts.

## What it won't do
- Invent behavior the code doesn't have
- Lecture you on style unless you asked
- Skip the actual fix in Debug mode
