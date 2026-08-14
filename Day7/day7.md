# Claude Usage Strategy Prompt — README

A documentation guide for the "Claude AI Expert / Productivity Consultant" prompt: what it does, what's actually true about Claude's model and effort settings, and how to use the output well.

---

## What This Prompt Does

This prompt turns the AI into a **personal Claude-usage consultant**. Instead of jumping straight to advice, it:

1. Interviews you first (situation, primary activities, usage frequency, output type needed)
2. Reasons step-by-step through your profile before recommending anything
3. Outputs a fixed, scannable strategy document — not a conversation

It's a "gather → analyze → prescribe" pattern, which is the right shape for this kind of question: model/effort choice genuinely depends on *your* mix of tasks, not on general best practices alone.

---

## Background You Should Know Before Using the Output

The prompt assumes two real, current Claude features — here's what's actually true about them as of mid-2026, so you can sanity-check whatever the AI recommends:

### Model tiers
Claude currently ships three main tiers, roughly fast-to-deep:
- **Haiku** — fastest and cheapest, best for quick lookups, simple formatting, high-volume/low-complexity tasks
- **Sonnet** — the balanced default for most day-to-day work: writing, coding, research, analysis
- **Opus** — the deepest reasoning tier, best for hard/ambiguous problems, complex coding, and high-stakes analysis where quality matters more than speed or cost

(There's also a newer "Mythos" tier above Opus, but it's not in general public use yet, so it's not part of a normal daily workflow.)

### Effort levels
"Effort" is a real, separate setting from which model you pick — it controls *how thoroughly* Claude reasons before answering, independent of which tier you're using. It sits right next to the model selector in the Claude app. The levels are **Low, Medium, High, xHigh, and Max**, and Claude defaults to **High**.

- **Low/Medium** — faster, cheaper, less internal deliberation — good for routine tasks
- **High** — the default, best all-around balance of quality and speed
- **xHigh** — built for long-running coding/agentic tasks, more depth than High without full Max cost
- **Max** — the most thorough option, for tasks that genuinely need the deepest possible reasoning

One important nuance the prompt's output should reflect: **effort is a behavioral dial, not a token guarantee or a correctness guarantee.** Higher effort means Claude tries harder and reasons longer — it doesn't mean a wrong answer becomes automatically right. Cranking a vague or ambiguous prompt up to Max mostly gets you a longer, more expensive answer to the same underlying question.

---

## Why the Interview Step Matters

The four intake questions map directly onto real tradeoffs:

| Question | What it actually determines |
|---|---|
| Situation (Student/Professional/Freelancer/Founder) | How much cost-sensitivity vs. output-stakes matters |
| Primary activities | Which tasks need Opus-level depth vs. Haiku-level speed |
| Usage frequency | Whether cost/token efficiency should shape your defaults |
| Output type needed | Whether you're optimizing for speed, depth, or creative range |

Skipping the interview and asking for "the best model and effort setting" in general produces generic advice ("use Sonnet, use High effort") that's true for almost nobody's *actual* week.

---

## What Good Output Looks Like

A well-run version of this prompt should give you:
- A **primary model recommendation** tied to your stated activities, not a blanket "always use the biggest model"
- Clear **when-to-switch** logic (e.g., "use Haiku for quick lookups, switch to Opus only when the task is genuinely hard, use High effort by default and reserve Max for high-stakes or highly ambiguous work")
- A **workflow table** mapping specific recurring tasks to specific model+effort combos, not generic categories
- One clear **"if you could only pick one" answer** — this is the most useful line in the whole output, because it gives you a default you don't have to think about on a normal day

---

## A Quick Sanity-Check Table

If the AI's final recommendation looks wildly different from this, it's worth asking it to justify the deviation:

| Task type | Typical model | Typical effort |
|---|---|---|
| Quick fact lookup, simple rewrite, formatting | Haiku | Low–Medium |
| Everyday writing, coding, research, learning support | Sonnet | High (default) |
| Complex/ambiguous coding, deep research, high-stakes strategy | Opus | High–xHigh |
| Rare, genuinely hard, high-stakes one-off problem | Opus | Max |

---

## Note on Accuracy

Model names, tier lineups, and effort-level details change as Anthropic ships new releases. If the AI's output references a specific model name or setting you don't recognize, it's worth double-checking against **support.claude.com** before treating it as current — this space moves fast enough that even a few months makes a difference.
