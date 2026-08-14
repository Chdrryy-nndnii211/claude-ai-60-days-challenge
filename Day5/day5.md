# Prompt A vs Prompt B: Does Context Actually Matter?

A side-by-side test of two ways to ask an AI for a 30-day learning roadmap — one with no context, one with context filled in — plus an analysis of what changed and why.

---

## The Two Prompts

**Prompt A (no context):** "Create a 30-day learning roadmap. Include weekly milestones, daily tasks, resources, projects, final outcome. Make it practical and beginner-friendly."

**Prompt B (with context):** Same ask, but with six variables filled in first — current situation, existing skills, goal, hours/day available, experience level, and preferred learning style.

For this comparison, Prompt B was filled in as:
> Freelancer · Knows basic Excel, no coding · Goal: learn Python for data automation · 2 hrs/day · Beginner · Prefers hands-on projects over videos/reading

---

## Output A — What You Get Without Context

Since the AI has no idea *who* you are, it has to guess. It usually defaults to the most statistically common request in its training data — which for "30-day roadmap" is almost always **generic web development or "programming basics."**

| Week | Milestone | Sample Daily Task |
|---|---|---|
| 1 | Learn fundamentals | "Watch intro videos, take notes" |
| 2 | Practice basics | "Complete exercises" |
| 3 | Build a small project | "Apply what you've learned" |
| 4 | Polish & review | "Build a portfolio project" |

**Resources:** generic — "freeCodeCamp, YouTube tutorials, official docs"
**Final outcome:** vague — "You'll have a solid foundation and a project to show for it."

It's not *wrong*. It's just not about you. It's a roadmap for an imaginary average learner who may not share your goal, your skill level, your time budget, or your learning style.

---

## Output B — What You Get With Context

With the same six blanks filled in, the roadmap reorganizes around the actual constraint that matters most: **2 hrs/day, project-first, Python for automation, starting from Excel-level logic.**

| Week | Milestone | Sample Daily Task |
|---|---|---|
| 1 | Python syntax + replace an Excel habit with code | "45 min: variables/loops. 45 min: rewrite one Excel formula as a Python script. 30 min: run/debug it." |
| 2 | File & data handling (`pandas`, `csv`) | "Automate a real task: read a CSV you actually use, clean it, export results." |
| 3 | Automate a recurring freelance task | "Build a script that does one thing you currently do by hand weekly." |
| 4 | Package it into a deliverable | "Turn Week 3's script into a small tool with error handling; write a 1-page usage doc." |

**Resources:** matched to stated style — project-based courses (e.g., Automate the Boring Stuff, hands-on notebooks) instead of long video lectures.
**Final outcome:** specific — "A working Python script that automates a real freelance task, plus the skills to build the next one yourself."

Every week ties back to *your* goal (automation), *your* time budget (2 hrs), and *your* preference (build, don't just watch).

---

## Comparison

### 1. Which roadmap feels more personalized?
Output B, clearly. Output A is a template; Output B is a plan. The difference shows up in three places: the **subject matter** (Python-for-automation vs. generic "learn to code"), the **pacing** (tasks sized to 2 hrs, not an assumed 4-6 hrs), and the **learning format** (projects front-loaded instead of videos-first).

### 2. Which roadmap would you actually follow?
Output B — because it removes the two biggest reasons roadmaps get abandoned:
- **Mismatched time load** (A assumes free time you may not have; B respects the stated 2 hrs/day)
- **Mismatched relevance** (A's project might have nothing to do with your actual work; B's project *is* your actual work)

A generic roadmap that "sounds right" is easy to start and easy to quit by day 4. A roadmap built around your real week has a reason to survive contact with your actual schedule.

### 3. What role did context play in improving the result?
Context didn't just add detail — it **changed the decisions**, not just the wording:
- **Goal** narrowed the entire subject from "programming" to "Python for automation."
- **Current skills** set the true starting point (skip "what is a variable" 101 stuff, start from Excel-logic parallels).
- **Available time** determined task size and pacing (2 hrs/day tasks vs. open-ended "study" blocks).
- **Learning style** changed the *type* of resources recommended (projects over lecture videos).
- **Experience level + situation** (freelancer) shaped the final outcome to be something monetizable/usable immediately, not just a portfolio piece.

In short: **without context, the AI optimizes for "plausible."** With context, it optimizes for "usable by this specific person, this week."

---

## Takeaway: A Reusable Context Template

For any roadmap, curriculum, or study-plan prompt, filling in these six fields before you ask tends to be the highest-leverage thing you can do:

```
Current Situation: [Student / Professional / Freelancer / etc.]
Current Skills: [What you already know, even loosely]
Goal: [The specific outcome — not "learn X" but "do Y with X"]
Available Time: [Realistic hours/day, not aspirational]
Experience Level: [Beginner / Intermediate / Advanced]
Preferred Learning Style: [Videos / Projects / Reading / Mixed]
```

The more specific the **Goal** and **Available Time** fields especially, the more the plan shifts from "generic curriculum" to "actual schedule you could start tomorrow."
