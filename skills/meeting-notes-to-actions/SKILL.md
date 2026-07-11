---
name: meeting-notes-to-actions
description: Turn raw meeting notes into a shareable summary, an action-item table with owners and deadlines, and follow-up email drafts. Use when the user says "process my meeting notes", "extract action items", "who owns what from this meeting", or "draft the follow-ups" — or pastes messy notes right after a meeting.
---

# Meeting Notes to Action Items

Convert disorganized meeting notes into structured accountability: a clean summary, an
action-item table, and a personalized follow-up draft per owner. Work only from what the
notes actually say — never invent owners, deadlines, or decisions that are not in the notes.

## Steps

1. Get the notes. Accept pasted text, a file path, or a transcript. If the notes name
   attendees ambiguously (initials, first names shared by two people), ask the user to
   resolve them before assigning ownership.
2. Extract, citing the notes:
   - **Decisions made** — each with the sentence in the notes that records it.
   - **Action items** — task, owner, deadline, and one line of context. If the notes give
     no owner or deadline, mark it `UNASSIGNED` / `NO DATE` rather than guessing, and list
     those gaps for the user to fill.
   - **Open questions** — anything discussed but unresolved.
3. Render three outputs in this order:
   - A 3–5 sentence meeting summary suitable for forwarding.
   - An action-item table: `Owner | Task | Deadline | Context`.
   - One short follow-up email draft per owner covering only that owner's items.
4. Verify before presenting: every action item in the table must trace to a line in the
   notes, and every owner must appear in the attendee list. Ask the user to confirm the
   `UNASSIGNED` / `NO DATE` gaps — do not send or save drafts until they have reviewed them.

## Constraints

- Drafts are drafts: Claude only writes text; the user reviews and delivers everything
  from their own mail client.
- Keep each follow-up email under ~120 words — one ask, one deadline, no filler.
- If the notes contain fewer than three concrete items, say the skill is overkill and
  offer a two-line summary instead.

Full walkthrough, examples, and variations: `recipes/Recipe-001-Meeting-Notes-to-Action-Items.md`.
