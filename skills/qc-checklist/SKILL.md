---
name: qc-checklist
description: Turn a process description into an operational quality-control checklist — binary pass/fail checks, acceptance criteria, critical-vs-routine tiers, and failure modes with catch-points. Use when the user says "build a QC checklist", "standardize how we review X", "acceptance criteria for this process", or describes quality varying by who does the work.
---

# Quality Control Checklist

Convert "experienced people just know" into checks anyone can run. A good check is binary
(pass/fail), observable (no judgment calls hidden inside), and placed at the point where the
failure it catches actually happens.

## Steps

1. Get the process: what's produced, the steps, who performs it, and — most important —
   what has actually gone wrong before. Real past failures anchor the checklist; ask for
   2–3 if none are offered.
2. Draft the failure-mode inventory first: for each step, what can go wrong, how it would be
   detected, and the cost of missing it. Every checklist item must trace to a failure mode —
   a check that catches nothing is process theater.
3. Build the checklist in two tiers:
   - **Critical (stop-the-line):** failures that are costly or invisible downstream. These
     are never skippable and each states its acceptance criterion measurably.
   - **Routine:** consistency checks that tolerate an occasional miss.
   Phrase every item as a verifiable pass/fail question with the evidence to look at —
   "Invoice total matches PO total (compare field X to field Y)", not "check invoice".
4. Add the operating shell: when the checklist runs (per unit / per batch / per release),
   who signs off, where results are recorded, and the escalation when a critical check
   fails. A checklist without a recorded result is a suggestion.
5. Verify by dry-run: walk one recent real work product through the draft. Every past
   failure the user named must be caught by some item; items that catch nothing on the
   dry-run get justified or cut. Then hand over with a 90-day review note — checklists
   drift as processes change.

## Constraints

- No item without a named failure mode it exists to catch.
- Acceptance criteria are measurable ("≤ 2 business days", "all 4 fields populated") — no
  "appropriate", "sufficient", or "high quality".
- Keep it runnable: if the full list exceeds ~15 items per tier, split by role or stage
  rather than shipping a wall nobody completes under time pressure.

Full walkthrough, examples, and variations: `recipes/Recipe-048-Quality-Control-Checklists-Standards.md`.
For enforcing checks on AI-assisted code specifically, the same philosophy is implemented in
[ai-control-framework](https://github.com/sgharlow/ai-control-framework).
