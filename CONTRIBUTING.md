# Contributing to Claude Code Recipes

Thank you for your interest in improving the Top 100 Claude Code Recipes collection!

---

## Ways to Contribute

### Report Issues

Found a problem with a recipe? Please open an issue with:

- **Recipe number and name** (e.g., "Recipe 042 - Process Documentation")
- **What's wrong** — Be specific about the issue
- **Expected behavior** — What should happen instead
- **Your environment** — Claude Code version, operating system

### Suggest Improvements

Have an idea to make a recipe better? Open an issue with:

- **Recipe number and name**
- **Your suggestion** — Be specific and actionable
- **Why it helps** — Explain the benefit to users

### Request New Recipes

Want a recipe for a task not covered? Open an issue with:

- **Task description** — What are you trying to accomplish?
- **Who benefits** — What role or function uses this?
- **Current pain point** — Why is this hard without a recipe?

---

## Guidelines

### Before Opening an Issue

1. **Search existing issues** to avoid duplicates
2. **Check the FAQ** — Your question may already be answered
3. **Try the recipe first** — Make sure you've followed all steps

### Quality Standards

All recipes in this collection follow these standards:

- **Practical** — Based on real professional tasks
- **Complete** — Include all steps from start to finish
- **Accurate** — Prompts work with current Claude Code
- **Accessible** — Written for non-technical users

### Code of Conduct

- Be respectful and constructive
- Focus on the content, not the person
- Help others learn

---

## Submitting a New Recipe

New recipes are welcome. The path:

1. **Open a "recipe proposal" issue first** — one paragraph: the recurring task, who has it,
   and the outcome. This avoids duplicate work before you write anything.
2. On a 👍 from a maintainer, **submit a PR** with one file:
   `recipes/Recipe-XXX-Your-Title.md`, following the structure of any existing recipe
   (Problem → Outcome → When to Use → Steps with a copy-ready prompt → Troubleshooting →
   Measuring Success). Real examples beat hypothetical ones.
3. Recipes that ship a **Skill** (`skills/<name>/SKILL.md` + at least one eval) are graded
   with [Skill Crossroads](https://skillcrossroads.com) before merge — include your grade in
   the PR (`npx skillcrossroads ./skills/<name>`). B or better merges; below that we'll help
   you fix the findings.

## Not Accepting

To maintain quality and consistency, we are **not** accepting:

- Recipes requiring specialized technical knowledge beyond a general knowledge worker's reach
- Content that duplicates existing recipes
- Promotional or commercial content

---

## Questions?

- Check [FAQ.md](FAQ.md) for common questions
- Check [GLOSSARY.md](GLOSSARY.md) for term definitions
- Open an issue for anything else

---

*Thank you for helping make Claude Code more accessible to knowledge workers everywhere.*
