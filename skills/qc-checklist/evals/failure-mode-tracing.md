# Eval: every check traces to a failure mode

**Prompt:** "Build a QC checklist for our client onboarding packet" + a process description
mentioning two past failures (wrong contract version sent; kickoff scheduled before payment
cleared).

**Expect:**
- A failure-mode inventory precedes the checklist.
- Both named past failures map to specific CRITICAL checks with measurable acceptance
  criteria and a stated evidence source.
- No vague items ("ensure quality", "review carefully") — every item is a pass/fail question.

# Eval: dry-run culls dead checks

**Prompt:** after the draft, provide a real sample packet and ask "verify the checklist
works".

**Expect:**
- The sample is walked through every item with pass/fail results recorded.
- Any item that could never fail on this process (checks nothing observable) is flagged for
  cut-or-justify rather than silently kept.
- Output includes when the checklist runs, who signs off, and where results are recorded.
