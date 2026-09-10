# How to Use This System

## The whole system is one thing

Before Claude writes important code, you say your approach first.

That's it. Reading finished code *feels* like understanding. Being wrong first
is what actually sticks.

---

## The one thing to remember

Type `/predict` before implementing something important.

It asks how you would do it. Write 3–5 lines. Wrong is fine. Then it shows the
real approach and tells you exactly where your thinking was off.

Nothing else to memorize.

---

## When to use it

**Yes** — something new, an architecture decision, unfamiliar territory,
anything you will own long-term.

**No** — small bug, config change, rename, anything you have done before.

About **1 task in 5**. Use it on everything and you will quit in two weeks.

---

## Running automatically — ignore these

`~/.claude/CLAUDE.md` loads in every project by itself:

- never add an `if` just to make a test pass
- short functions, no comment noise
- git rules — branches, commits, PRs

Nothing to do. It just works.

---

## The file that fills itself

`log/gaps.md` — every time you are wrong about *how something works*,
`/predict` writes it there.

**When you have free time:** open it and find the concept that appears three
times. Study that. Stop asking "what should I learn?" — the file answers it.

Split free time roughly **70/30**: gap clusters, plus one deliberate topic from
`specs/roadmap/roadmap.md` for the things the log cannot catch.

Build something small instead of reading. A two-hour experiment beats a course.

---

## Old code

Don't clean it. That burns time and looks like you shipped nothing.

Once: 2–3 hours, **read only, fix nothing**, and write the dangerous parts into
`log/risks.md` — special cases, hardcoded values, silent failures. Then fix only
what is dangerous or already sitting in your path.

Your unfinished tasks are where to start. They are real work, already in motion.

---

## While working

- Read the code that matters — architecture, data flow, correctness, security.
  Skim boilerplate.
- Every time you correct Claude, that correction goes into the project's
  `CLAUDE.md`. Don't write that file upfront. Grow it.
- Read the diff before committing. Read it again before the PR.

---

## Weekly — 10 minutes

1. Any concept in `gaps.md` three times? That is this week's topic.
2. Did any project `CLAUDE.md` grow? If not, you stopped reviewing.

---

## Right now

Close this file. Open Claude Code on an unfinished task. Type `/predict`.

The first few times feel bad, because you will be wrong in front of yourself.
That is the signal. If it feels comfortable, it isn't working.
