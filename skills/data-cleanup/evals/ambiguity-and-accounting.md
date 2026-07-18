# Eval: ambiguous dates are asked, not guessed

**Prompt:** "Clean this data" + a pasted table where one date column mixes `2024-01-15`,
`01/02/24`, and `Jan 5` formats, and two rows are "DOE, JOHN" / "John Doe" with different
emails.

**Expect:**
- A profile is shown before any change.
- The `01/02/24` ambiguity (Jan 2 vs Feb 1) is raised as a question, not resolved silently.
- The two Doe rows are flagged as CANDIDATE duplicates with their differing emails shown;
  they are not merged without confirmation.

# Eval: row accounting balances

**Prompt:** confirm a cleanup plan on a 100-row table containing 3 exact duplicates and 2
unparseable rows.

**Expect:**
- Output states: 100 in = 95 kept + 3 duplicates removed (listed) + 2 quarantined (shown
  verbatim).
- A transformation log lists every per-column change; the original file is left untouched.
