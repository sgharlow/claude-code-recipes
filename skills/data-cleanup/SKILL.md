---
name: data-cleanup
description: Clean and standardize messy tabular data (CSV, spreadsheet paste, system exports) into an analysis-ready dataset — consistent dates and names, typed columns, duplicates identified, missing values handled explicitly. Use when the user says "clean this data", "standardize this CSV", "dedupe this list", or pastes a table with inconsistent formatting.
---

# Data Cleanup and Formatting

Standardize messy tabular data without ever silently changing what it says. Every
transformation is declared; every ambiguous value is surfaced, not guessed.

## Steps

1. Get the data (file path or paste) and profile it first: row count, columns, detected
   types, distinct-value oddities (mixed date formats, case-inconsistent names, stray
   whitespace, mixed types in one column), missing-value counts, and candidate duplicates.
   Present this profile BEFORE changing anything.
2. Propose the cleanup plan as a checklist the user confirms: target date format, name
   casing, type per column, duplicate rule (exact vs. fuzzy key), and missing-value policy
   per column (leave blank / fill with sentinel / drop row — never a silent default).
3. Apply the confirmed plan. For anything ambiguous (is `02/03/24` Feb 3 or Mar 2? are
   "J. Smith" and "John Smith" the same person?), stop and ask — wrong-but-tidy is worse
   than messy.
4. Deliver: the cleaned dataset, plus a transformation log — rows in/out, per-column changes
   applied, duplicates found (listed, not just deleted), missing values and how each was
   handled, and any rows quarantined as unparseable rather than mangled.
5. Verify: spot-check that no value changed meaning (dates shifted, names merged wrongly);
   re-state the row count arithmetic (in = out + dropped + quarantined) so nothing vanishes.

## Constraints

- Never delete or merge rows without listing exactly which ones and why.
- Never guess an ambiguous date, unit, or identity — ask.
- The original input is never overwritten; cleaned output is a new file/table.
- If the data is too large to show fully, show the profile + a sample and operate via a
  script the user can inspect, not invisible edits.

Full walkthrough, examples, and variations: `recipes/Recipe-009-Data-Cleanup-Formatting.md`.
