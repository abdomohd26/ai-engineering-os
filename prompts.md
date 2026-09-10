# Prompts

Paste-able. If you use one three times, turn it into a skill.

---

## Starting or continuing a task

Use as the **first** message. Do not run `/predict` before this — Claude has no
context yet, so the prediction would be meaningless.

```
I'm working on [task]. Business goal: [what it's actually for].

Done so far: [...]
Missing: [...]

Read the existing code first and tell me:
- how you understand the system works
- what looks missing or wrong
- the most dangerous thing in it

Don't write any code yet.
```

Then discuss, agree on the next concrete piece, and **only then** run `/predict`.

---

## Auditing old code

Read-only. Once per project, 2–3 hours.

```
Audit the existing code in this project. Read only — fix nothing.

Look for:
- special cases and conditionals added to make one specific case pass
- hardcoded values
- places where errors are swallowed silently
- missing error handling
- anything that will fail in production without an obvious cause

Write the results to log/risks.md, ranked by blast radius — what hurts most
if it fails.

For each one: where it is, what the problem is, what could go wrong.

Fix nothing. If you don't understand something, say so instead of guessing.
```

---

## Free learning time

```
I have [X] hours free.

Read log/gaps.md and find which concept appears more than once.

Tell me:
1. What to study now, and why
2. What depth I need — use it / modify it / design with it / master it
3. One small thing to build in that time that will actually make it stick
4. What NOT to study right now

Pick one. Not a list.
```
