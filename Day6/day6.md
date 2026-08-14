# ATS Resume Optimizer — Prompt README

A documentation guide for the "ATS optimization expert" prompt: what it does, how it behaves, and how to get the best results from it.

---

## What This Prompt Does

This is a **role + task + output-format prompt** that turns an AI into a resume-rewriting tool with a fixed, predictable output shape. Instead of a free-form "improve my resume" conversation, it constrains the AI to:

1. Take your existing resume (text or image) as the *only* source of truth
2. Optionally align it to a specific job description if you provide one
3. Return exactly two things, in a fixed order, with nothing extra around them

That last part — the strict output contract — is the most important design choice in the prompt. It's built for someone who wants a clean, copy-pasteable result, not a conversation.

---

## The Two-Part Output Contract

### Part 1 — ATS Score
A short before/after score plus 5–8 bullets explaining *specifically* what changed and why it helped (e.g., "Replaced passive phrasing with action verbs — improves keyword-to-role matching"). No long-form report, no fluff.

### Part 2 — Final Resume
A single-column, one-page, A4-ready resume with:
- Large bold name, plain-text contact line underneath
- Standard ATS-safe section headings (Summary, Education, Experience, Projects, Skills, Certifications)
- No tables, icons, columns, or text boxes — these are exactly the elements that break ATS parsers

This format matters because Applicant Tracking Systems parse resumes as raw text. Multi-column layouts, icons, and text boxes often get scrambled or dropped entirely by parsing software, even though they look fine to a human eye.

---

## The Guardrails (Why They're There)

| Rule | Why it matters |
|---|---|
| Use only information from the resume | Prevents the AI from fabricating achievements or metrics — a serious risk with resume-writing prompts otherwise |
| Never invent skills/certs/experience | Keeps the output legally and ethically safe to submit as your own |
| Suggest improvements instead of fabricating | If something's missing, you get a note to go add it yourself, not an invented substitute |
| Must fit one A4 page | Matches real recruiter behavior — most resumes get 6–10 seconds of initial attention |
| Ask for details if no resume is provided | Prevents the AI from generating a resume out of thin air with placeholder data |

This is the prompt's strongest design feature: it treats truthfulness as a hard constraint, not a suggestion, which is what makes the output actually safe to submit to a real employer.

---

## How to Use It Well

**With a job description (recommended):** Paste the job posting along with your resume. The AI aligns keywords and phrasing to that specific role, which meaningfully raises real ATS match scores — this is the single biggest lever in the whole prompt.

**Without a job description:** It optimizes generically for your field based on what's already in your resume — still useful, but less targeted.

**With no resume at all:** It should stop and ask you for: Name, Contact Info, Education, Experience, Projects, Skills, Certifications, and Target Field — then build from your answers rather than guessing.

---

## What to Expect vs. What Not to Expect

**Expect:**
- A tightened, reformatted, ATS-safe version of what you already have
- Honest feedback in the score section about what's weak or missing
- A one-pager, not a multi-page CV

**Don't expect:**
- New accomplishments or metrics you didn't provide
- Design flourishes (this is intentionally plain — that's what makes it ATS-safe)
- A resume longer than one page, even if your real experience is extensive (you'd need to explicitly relax that rule for senior/multi-page cases)

---

## Quick Tip

If your real resume genuinely needs more than one page (10+ years experience, extensive publications, etc.), tell the AI that up front — the one-page rule is a default optimized for early-to-mid career ATS submissions, not a hard truth about all good resumes.
