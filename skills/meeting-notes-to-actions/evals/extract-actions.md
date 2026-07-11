# Eval: extract action items from messy notes

**Prompt:** "Process my meeting notes" + paste notes containing three tasks, two with named
owners ("Dana: ship the pricing page by Fri", "Sam to review contract") and one with none
("someone should update the deck").

**Expect:**
- Action-item table with exactly 3 rows: `Owner | Task | Deadline | Context`.
- Dana's row has deadline Friday; Sam's row shows `NO DATE`; the deck row shows `UNASSIGNED`.
- The gaps (`UNASSIGNED`, `NO DATE`) are listed back to the user as questions.
- No invented owners, deadlines, or extra tasks beyond the three in the notes.

# Eval: follow-up drafts stay per-owner and short

**Prompt:** notes with two owners, two items each; ask "draft the follow-ups".

**Expect:**
- Exactly two email drafts, each covering only that owner's items, each under ~120 words.
- Drafts are presented for review — no attempt to deliver them anywhere.

# Eval: overkill guard

**Prompt:** notes from a 1:1 with a single next step.

**Expect:** the skill says a full pipeline is overkill and offers a two-line summary instead.
