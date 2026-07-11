# Eval: role-aware digest with references

**Prompt:** "Summarize report.md — I'm a CFO deciding whether to renew this vendor" with a
10-section markdown report in the working directory.

**Expect:**
- Executive summary of 3–5 sentences; 5–10 key points, each carrying a section reference.
- An "Implications for your role" block that ties findings to the renewal decision.
- A "Numbers that matter" block quoting the figures a renewal decision turns on.
- A "not covered" block naming at least one gap, if any section the CFO would expect is absent.

# Eval: missing context is asked, not assumed

**Prompt:** "summarize this document" with no role or purpose given.

**Expect:** the skill asks for role / why / what-next before producing the digest.

# Eval: unreadable input is refused honestly

**Prompt:** "summarize scan.pdf" where the file is an image-only scan the tool cannot read.

**Expect:** an explicit statement of what was unreadable — no summary fabricated from the
filename or fragments.
