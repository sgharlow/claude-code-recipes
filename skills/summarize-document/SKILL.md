---
name: summarize-document
description: Summarize a long document into an executive summary, key points, and role-specific implications. Use when the user says "summarize this document", "give me the key points", "do I need to read this?", or drops a long PDF, report, or contract and asks what matters in it.
---

# Document Summarization and Key Point Extraction

Read a long document and return a decision-ready digest tuned to the reader's role. The
summary must be faithful: every claim in it traces to the document, with section or page
references where the format allows.

## Steps

1. Confirm the target file and the reader's context — role, why they are reading it, and
   what they will do with it (present, decide, share). If context is missing, ask these
   three questions first; a summary without them is generic and half as useful.
2. Read the full document. For very long documents, read in passes: structure first
   (headings, tables, executive sections), then the sections that bear on the reader's
   stated purpose.
3. Produce, in order:
   - **Executive summary** — 3–5 sentences: what the document is, its central claim, why
     it matters to this reader.
   - **Key points** — 5–10 bullets, each with a section/page reference.
   - **Implications for your role** — 2–4 bullets connecting findings to the reader's
     stated purpose.
   - **Numbers that matter** — any figures, dates, or thresholds a decision would turn on.
   - **What the document does NOT cover** — gaps the reader might wrongly assume are addressed.
4. Verify: re-scan the document for any section not represented in the key points; either
   add it or state why it was omitted. Never present an inference as the document's claim —
   label reader-specific interpretation as "Implication", not "Finding".

## Constraints

- Do not summarize a document you could not fully read (unsupported format, truncated
  file) — say exactly what was unreadable instead of summarizing the fragment silently.
- Quote sparingly; a digest that is 40% quotation is not a digest.

Full walkthrough, examples, and variations: `recipes/Recipe-004-Document-Summarization.md`.
