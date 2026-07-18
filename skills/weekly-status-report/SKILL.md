---
name: weekly-status-report
description: Turn scattered weekly updates (notes, emails, task exports, meeting notes) into a structured status report with highlights, progress, severity-rated blockers, and next-week priorities. Use when the user says "write my status report", "weekly update", "summarize my week for my manager", or pastes a raw dump of what happened this week.
---

# Weekly Status Report

Synthesize a week of scattered raw inputs into one scannable, audience-ready status report.
Report only what the inputs support — never invent accomplishments, metrics, or dates, and
never upgrade routine work into a highlight without evidence of impact.

## Steps

1. Get the raw material. Accept pasted notes, forwarded emails, task-tool exports, meeting
   notes, and last week's report if available. Ask for: report period, the user's role, the
   audience (manager / leadership / client), and any required template.
2. Classify every item, citing the input it came from:
   - **Highlights** — only items with stated impact (shipped, resolved, approved, measured).
   - **Progress** — grouped by project/workstream, with % or state only if the inputs give it.
   - **Blockers & risks** — each with severity (High/Medium/Low) and what unblocks it. If the
     inputs don't support a severity, ask rather than guess.
   - **Next week** — priorities, deadlines, dependencies.
3. Render the report under one page: HIGHLIGHTS (3–5) → PROGRESS → BLOCKERS & RISKS (table:
   `Item | Severity | Status | Needed`) → NEXT WEEK → optional NOTES/FYI. Bold key items.
4. Verify before presenting: every claim traces to a line of input; anything the user's raw
   notes mention that was dropped is listed back ("omitted: …") so nothing disappears
   silently. If last week's report was provided, note carryover items explicitly.
5. Offer audience variants from the same material on request (3-bullet skip-level version,
   client-toned version, team-detail version) — same facts, different framing.

## Constraints

- The user reviews and sends the report themselves; never deliver it anywhere.
- No metric appears unless it is in the inputs verbatim; flag wanted-but-missing metrics.
- If the inputs are thinner than ~5 items, say so and produce a short-form update instead of
  padding a full template.

Full walkthrough, examples, and variations: `recipes/Recipe-002-Weekly-Status-Report-Generation.md`.
