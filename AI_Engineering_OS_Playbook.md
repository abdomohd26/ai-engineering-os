# AI Engineering OS --- Operating Playbook

This document is the practical playbook for using the AI Engineering OS
during work and learning.

The goal is **not** to add process for the sake of process. The goal is
to: - deliver high-quality work on time, - build genuine engineering
judgment, - reduce blind dependence on AI, - turn real work into a
learning curriculum, - keep the roadmap adaptive.

## Core Rule

**Delivery comes first, learning compounds through delivery.**

Do not turn every task into a study project.

Use the lightest workflow that is appropriate for the task size and
risk.

------------------------------------------------------------------------

# 1. A New Work Task

Use this whenever a new task arrives.

This is the default workflow for work involving AI, backend,
infrastructure, scraping, testing, or other technical areas.

## Step 1 --- Start in Claude Code

Open the repository where the task will be implemented.

If the AI Engineering OS is available in the same workspace, tell Claude
Code to use it.

Send:

``` text
I have a new task.

Before implementing anything, help me work through the task using my AI Engineering OS.

First:
1. Understand the business goal and expected outcome.
2. Identify ambiguities and ask me the questions that actually matter.
3. Identify constraints, dependencies, deadline risks, and important edge cases.
4. Estimate the scope: small, medium, or large.
5. Identify the technical areas involved.
6. Identify my knowledge gaps that could affect my ability to make good decisions.
7. Separate what I must understand before implementation from what I can learn while implementing.
8. Propose the simplest reasonable approach that can meet the requirements.
9. Tell me what could be overengineering for this task.

Do NOT start coding yet.

Challenge my assumptions when necessary. Do not agree with me automatically.
Keep delivery quality and the deadline in mind.
```

### Then discuss

Do not blindly accept the plan.

Discuss: - business requirements, - scope, - architecture, -
trade-offs, - risks, - unknowns, - what you need to learn, - what can be
postponed.

For a small task, this discussion may take only a few minutes.

For a large task, spend more time here.

------------------------------------------------------------------------

## Step 2 --- Decide the Learning Depth

After the task is understood, ask:

``` text
Based on this task and my current level:

1. What do I need to understand deeply enough to make and review the engineering decisions?
2. What do I only need to understand at a practical level?
3. What can I safely defer?
4. Is there anything I am about to study that is unnecessary for this task?

Be opinionated. Optimize for both delivery and long-term skill growth.
```

### Rule

If learning a topic would block delivery and the topic is not
fundamental to the decision:

**learn the minimum required, deliver, then deepen later if it proves
valuable.**

If the missing knowledge directly affects architecture, correctness,
security, reliability, or a major technical decision:

**stop and learn enough before implementation.**

------------------------------------------------------------------------

## Step 3 --- Approve the Plan

Once you understand and agree with the approach:

``` text
I approve the approach.

Now create the implementation plan.

The plan should:
- be broken into practical steps,
- identify dependencies,
- identify tests,
- identify important failure and edge cases,
- avoid unnecessary architecture,
- keep the deadline in mind.

Do not implement yet.
```

Review the plan.

Then tell Claude Code to implement it.

------------------------------------------------------------------------

## Step 4 --- Implement

Use Claude Code as an implementation partner, not as an unquestioned
programmer.

During implementation:

``` text
Implement the approved plan.

While working:
- Follow the existing repository conventions.
- Do not introduce unnecessary architectural changes.
- Explain important technical decisions.
- Flag uncertainty instead of guessing.
- Keep correctness, reliability, security, and deadline in mind.
- Ask me when a decision requires business judgment.
```

You should still inspect the important code and understand the system
flow.

Do not accept code just because tests pass.

------------------------------------------------------------------------

## Step 5 --- Review Before Delivery

After implementation:

``` text
The implementation is complete.

Review it critically before I deliver it.

Check:
1. Correctness
2. Business requirements
3. Edge cases
4. Failure handling
5. Error handling
6. Security
7. Performance
8. Concurrency / async behavior where relevant
9. Maintainability
10. Tests
11. Integration risks
12. Observability / logging where relevant
13. Unnecessary complexity

Do not just tell me that it looks good.
Try to find problems and challenge the implementation.

Separate:
- must fix before delivery
- should fix if time allows
- safe to postpone
```

Then review the findings yourself.

------------------------------------------------------------------------

## Step 6 --- Delivery Check

Before committing / PR:

``` text
Do a final delivery check.

Given the original task and deadline, verify:
- Is the business requirement actually satisfied?
- Is anything important missing?
- Are there obvious edge cases?
- Could this break existing behavior?
- Are tests sufficient?
- Is the implementation more complex than necessary?
- Is there anything that should block the PR?

Give me a concise final checklist.
```

Then you make the final decision and deliver.

------------------------------------------------------------------------

## Step 7 --- Knowledge Capture

Only do this for meaningful tasks.

Do NOT do it for every tiny bug.

After the task is complete:

``` text
The task is complete.

Help me extract reusable knowledge from it.

Identify:
1. What I learned.
2. What I misunderstood.
3. What I should now be able to explain without AI.
4. Important engineering decisions and why they were made.
5. Mistakes or weak reasoning I showed.
6. Any recurring weakness this task exposed.
7. Whether this should change my learning priorities or roadmap.

Be selective.
Do not recommend roadmap changes unless the evidence is strong.
```

### After this

If the result reveals a real recurring gap:

-   record it in the Personal OS,
-   do not immediately create a huge study plan,
-   let multiple tasks confirm whether it is actually important.

------------------------------------------------------------------------

# 2. I Have Free Time and Want to Study

Use this when you have dedicated learning time and do not already have
an urgent work-driven topic.

The objective is to avoid random learning.

## Step 1 --- Ask the Personal OS

Use the Personal OS / planning conversation:

``` text
I have [X] hours available for learning this week.

Review my:
- current goals,
- current roadmap,
- recent work,
- recent knowledge gaps,
- weaknesses,
- current career direction.

Recommend what I should study this week.

Be strongly opinionated.

Choose the highest-leverage topic(s), not a long list.

For each recommendation, tell me:
1. Why now?
2. What competency am I trying to build?
3. What depth do I need?
4. What should I actually do?
5. How does it connect to my work?
6. What is the expected outcome?
7. What should I explicitly NOT study right now?

Optimize for becoming a strong AI engineer who can understand AI systems deeply, build production systems, make engineering decisions, and work independently.
```

------------------------------------------------------------------------

## Step 2 --- Choose the Learning Mode

Prefer a combination of:

-   mental models,
-   targeted theory,
-   implementation,
-   reading documentation,
-   small experiments,
-   reviewing real systems,
-   papers when appropriate.

Do not automatically start a full course or book.

Ask:

``` text
For this topic, design the most effective learning approach for me.

I prefer practical understanding, but I also want enough theory to understand why systems work.

Tell me:
- what to learn first,
- what resource(s) to use,
- what to build or experiment with,
- how to test whether I actually understand it.

Avoid giving me multiple competing resources unless there is a clear reason.
```

------------------------------------------------------------------------

## Step 3 --- Learn Actively

While studying, periodically ask:

``` text
Do not just explain this to me.

Teach me through reasoning.

After explaining a concept, ask me questions that test whether I actually understand it.
Prefer questions that require me to make engineering decisions rather than repeat definitions.
```

For important topics, aim to reach this level:

> I can explain the mental model, reason about trade-offs, recognize the
> concept in a production system, and make a reasonable engineering
> decision.

You do **not** need to master every topic mathematically before using
it.

------------------------------------------------------------------------

## Step 4 --- Apply It

Whenever possible:

``` text
Show me how this concept appears in a real production AI system.

Give me one realistic engineering scenario and let me reason about it before you give me the answer.
```

Then compare your reasoning with the correct approach.

This is especially important for: - LLM systems, - RAG, - agents, -
inference, - evaluation, - system architecture, - distributed systems, -
databases, - backend design.

------------------------------------------------------------------------

## Step 5 --- End the Study Session

Do not end with "I watched a course."

End with:

``` text
Let's close this learning session.

Test me on the most important concepts.

Then tell me:
1. What I genuinely understand.
2. What I only partially understand.
3. What I misunderstood.
4. What I should practice.
5. Whether I should continue this topic or move on.

Keep the next step small and concrete.
```

If the topic is sufficiently understood, **move on**.

Do not keep studying just because there is more material.

------------------------------------------------------------------------

# 3. Weekly Review

Do this approximately once per week.

Time: about 20--30 minutes.

Use the Personal OS rather than a work repository.

Start with:

``` text
Let's do my weekly engineering review.

Review this week's progress with me.

Ask me about:
- important tasks I worked on,
- difficult problems,
- what I learned,
- mistakes,
- decisions I made,
- things I relied on AI for,
- things I still cannot explain,
- recurring problems,
- learning I completed,
- learning I planned but did not complete.

Then evaluate:
1. What improved?
2. What did I avoid?
3. Where am I still weak?
4. Where am I overusing AI?
5. What knowledge gaps appeared repeatedly?
6. What should I focus on next week?
7. What should I stop doing?
8. Did anything happen that should change my roadmap?

Be honest and opinionated.
Do not create work just to make the review look productive.
```

### After the review

Update the Personal OS only when something meaningful changed.

Examples:

-   a recurring weakness became clear,
-   a competency improved significantly,
-   work direction changed,
-   a new responsibility appeared,
-   a topic became much more important,
-   a previous priority is no longer relevant.

Do not update the roadmap because of one isolated bad day.

------------------------------------------------------------------------

# 4. Monthly Review

Do this approximately every 4 weeks.

Time: 45--60 minutes.

This is more strategic than the weekly review.

Start with:

``` text
Let's do my monthly engineering and career review.

Evaluate the last month against my long-term goals.

Review:
- work I actually performed,
- competencies I used,
- technical problems I solved,
- knowledge gaps,
- mistakes,
- AI dependence,
- learning progress,
- architecture and system-design exposure,
- ability to work independently,
- delivery quality,
- deadlines,
- new responsibilities,
- changes in the AI industry or my work environment that are relevant.

Then evaluate:

1. What meaningful progress did I make?
2. What is currently my biggest weakness?
3. What competency should become a higher priority?
4. What am I spending time on that has low leverage?
5. What should I stop, start, continue, increase, or decrease?
6. Is my current roadmap still appropriate?
7. Should any roadmap item be postponed or removed?
8. What should be my top 3 priorities for the next month?
9. What would make the next month successful?

Be opinionated.
Optimize for long-term compounding skills, but respect my current job responsibilities and delivery requirements.

Do not change the roadmap automatically.
Propose changes first and wait for my approval.
```

------------------------------------------------------------------------

# 5. When a New Technical Topic Appears During Work

Sometimes a task exposes a topic that is too large to learn immediately.

Use this:

``` text
This task exposed a knowledge gap around [TOPIC].

Help me decide how to handle it.

Classify it as:
A. Must understand before continuing
B. Learn the minimum now and deepen later
C. Understand conceptually now, defer implementation details
D. Not important enough to study right now

Explain why.

If it is worth learning, define the smallest useful learning target.
Do not create a full roadmap unless the topic is strategically important.
```

This prevents every unfamiliar concept from becoming a new rabbit hole.

------------------------------------------------------------------------

# 6. When the Task Is Tiny

Do not use the full workflow.

Use:

``` text
Quick task.

Understand the requirement, identify obvious risks, propose the simplest solution, and implement it.

Do not overengineer.
After implementation, do a brief correctness and edge-case review.
```

The AI Engineering OS should reduce friction, not create it.

------------------------------------------------------------------------

# 7. When the Task Is Large or Ambiguous

Use the full workflow.

Start with:

``` text
This is a large / ambiguous task.

Do not jump into implementation.

Help me first establish:
- business goal,
- scope,
- constraints,
- dependencies,
- architecture,
- risks,
- milestones,
- knowledge gaps,
- deadline strategy.

If the full solution is too large, propose a smaller version that delivers value first and can be extended safely.
```

------------------------------------------------------------------------

# 8. Rules for Using AI

These rules apply everywhere.

## Rule 1 --- Do not outsource judgment

Claude can: - explain, - research, - generate, - review, - challenge, -
implement.

You remain responsible for: - business understanding, - priorities, -
architecture decisions, - trade-offs, - correctness, - final delivery.

## Rule 2 --- Do not accept unexplained AI output

For important code or architecture, ask:

> "Can I explain why this works and why we chose this approach?"

If not, learn enough to answer it.

## Rule 3 --- Use AI to increase your thinking, not replace it

Prefer:

``` text
Here is my reasoning. Challenge it.
```

over:

``` text
What should I do?
```

when you are capable of forming an initial opinion.

## Rule 4 --- Do not study everything

Your career direction is broad, but your time is limited.

Prioritize: 1. Modern AI / LLM systems 2. AI system architecture 3.
Production engineering 4. Software/system design 5. Strong engineering
fundamentals 6. Supporting areas required by your actual work

For secondary areas such as frontend, DevOps, or testing:

> Learn enough to perform the responsibility professionally unless the
> area becomes strategically important.

## Rule 5 --- Optimize for compounding

Prefer skills that repeatedly improve your ability to: - understand
systems, - make decisions, - solve difficult problems, - build
production systems, - review AI-generated work, - operate independently.

------------------------------------------------------------------------

# 9. The Overall Loop

The entire system can be reduced to:

``` text
WORK
  ↓
Encounter a problem
  ↓
Understand
  ↓
Decide what matters
  ↓
Learn only what is necessary
  ↓
Build
  ↓
Review
  ↓
Deliver
  ↓
Extract knowledge
  ↓
Weekly review
  ↓
Monthly review
  ↓
Update priorities
  ↓
Repeat
```

The purpose of the AI Engineering OS is not to make this process
complicated.

The purpose is to make sure that **your real work continuously turns
into better engineering judgment and deeper AI understanding.**
