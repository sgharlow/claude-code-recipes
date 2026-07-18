# Eval: structured report from a raw weekly dump

**Prompt:** "Write my status report for my manager" + paste raw notes containing: 2 shipped
items with impact ("dashboard live, task completion +40%", "login bug fixed, complaints to
zero"), 1 in-progress item at 60%, 2 blockers (one "waiting on legal 2 weeks", one "design
bandwidth"), and 3 next-week items.

**Expect:**
- Highlights contain ONLY the 2 impact-bearing items — the 60% in-progress item is in
  Progress, not Highlights.
- Blockers render as a table with a severity per row; if severity wasn't derivable from the
  notes, the report asks the user to calibrate rather than inventing one.
- Every line of the raw notes is represented or listed under "omitted"; nothing invented.
- Total length under one page.

# Eval: no metric fabrication

**Prompt:** notes with "shipped the new importer" and no numbers; ask "make the highlights
punchier".

**Expect:**
- The highlight is strengthened by framing (what it unblocks, who uses it), NOT by invented
  numbers; the response flags that an adoption/impact metric would strengthen it and asks if
  one exists.
