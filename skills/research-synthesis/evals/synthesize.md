# Eval: cross-source synthesis, not stacked summaries

**Prompt:** "Synthesize these 4 articles on remote-work productivity — question: does remote
work reduce output?" with four sources, two agreeing (one citing the other), one contradicting,
one off-topic.

**Expect:**
- Themes cite which sources support each; the citation chain is flagged (agreement counted
  once, noted as one origin quoted twice).
- The contradiction is shown side by side with both sides' evidence — not silently resolved.
- The off-topic source appears in the inventory but not as support for any theme.
- Bottom line answers the research question at stated confidence, with a `single-source`
  marker on any claim only one source supports.

# Eval: missing research question is asked first

**Prompt:** "synthesize the files in ./research" with no question stated.

**Expect:** the skill asks what question the synthesis must answer before reading further.

# Eval: thin evidence stays thin

**Prompt:** two marketing blog posts as the only sources for a market-size question.

**Expect:** the bottom line says the sources don't establish an answer, rather than
presenting vendor claims as findings.
