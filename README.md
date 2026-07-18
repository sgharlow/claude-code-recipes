# Top 100 Claude Code Recipes for Knowledge Workers

[![Skill Crossroads](https://skillcrossroads.com/api/badge/sgharlow/claude-code-recipes.svg)](https://skillcrossroads.com/s/sgharlow/claude-code-recipes)

Claude Code artifacts graded by [Skill Crossroads](https://skillcrossroads.com) — click the badge for the evidence-cited scorecard.

**Your Complete Guide to AI-Powered Productivity**

*Version 1.0 — December 2025*

---

## Welcome

This collection contains 100 practical recipes for using Claude Code to automate, accelerate, and enhance your professional work. Each recipe provides step-by-step instructions, ready-to-use prompts, and real-world examples that you can apply immediately.

Whether you're drafting emails, analyzing data, preparing presentations, or managing complex projects, there's a recipe here that will save you hours of work.

---

> **Want all 200 recipes as ready-to-use slash commands?**
>
> The **[Premium Collection](https://learningai365.lemonsqueezy.com/buy/703305ce-b87f-4ccc-bf8c-b629c3116f7b?utm_source=github&utm_medium=readme&utm_campaign=launch)** includes 200 slash commands you can install in seconds. Just type `/recipe-001` and Claude does the rest. No copying prompts. No setup. **$79.99 one-time purchase.**
>
> **[Get the Premium Collection →](https://learningai365.lemonsqueezy.com/buy/703305ce-b87f-4ccc-bf8c-b629c3116f7b?utm_source=github&utm_medium=readme&utm_campaign=launch)**


## Installable skills (new)

Three of the most-used recipes now ship as real Claude Code **Skills** you can drop into
`~/.claude/skills/` (or a project's `.claude/skills/`) — no prompt copying:

| Skill | From recipe | What it does |
|-------|-------------|--------------|
| [`meeting-notes-to-actions`](skills/meeting-notes-to-actions/SKILL.md) | #1 | Raw notes → summary, owner/deadline table, follow-up drafts |
| [`weekly-status-report`](skills/weekly-status-report/SKILL.md) | #2 | Scattered weekly updates → one-page report with severity-rated blockers |
| [`summarize-document`](skills/summarize-document/SKILL.md) | #4 | Long document → role-aware, reference-cited digest |
| [`research-synthesis`](skills/research-synthesis/SKILL.md) | #7 | Many sources → themes, contradictions, gaps, bottom line |
| [`data-cleanup`](skills/data-cleanup/SKILL.md) | #9 | Messy tabular data → analysis-ready, with a full transformation log |
| [`qc-checklist`](skills/qc-checklist/SKILL.md) | #48 | Process description → pass/fail QC checklist traced to real failure modes |

Each skill includes evals and is quality-graded — click the badge above for the scorecard.

## The system behind these recipes

The recipes are the **what**. The rest of the toolchain is how the same work ships with
verification instead of vibes:

| | Repo | Role |
|---|---|---|
| **How** | [ai-control-framework](https://github.com/sgharlow/ai-control-framework) | The verification methodology: deployment-readiness scoring, evidence-backed gates |
| **Scale** | [orchestra-lite](https://github.com/sgharlow/orchestra-lite) | Running parallel AI agents on real repos without losing control |
| **Enforcement** | [ai-pr-bot](https://github.com/sgharlow/ai-pr-bot) | The gates, run where the code lands: at PR time |
| **Grade** | [skillcrossroads](https://github.com/sgharlow/skillcrossroads) | Evidence-cited scoring for the skills themselves — live at [skillcrossroads.com](https://skillcrossroads.com) |

One rule ties them together: **no claim without a check you can run.**

---

## Getting Started

**New to Claude Code?** Start here:

1. **[GETTING-STARTED.md](GETTING-STARTED.md)** - Installation guide for Windows, macOS, and Linux
2. **[FAQ.md](FAQ.md)** - Common questions answered
3. **[GLOSSARY.md](GLOSSARY.md)** - Terms and definitions
4. Pick a recipe from Tier 1 below (the universal high-frequency wins)

---

## How to Use This Book

### Reading Strategies

**Don't read sequentially.** This is a reference book, not a novel. Instead:

1. **Start with a task you're facing today** — Scan the table of contents for something relevant
2. **Try one recipe completely** — Follow all the steps, including the refinement prompts
3. **Customize as you go** — The prompts are templates; adapt them to your situation
4. **Build from there** — Once you've mastered one recipe, explore related ones

### Understanding the Difficulty Levels

| Level | What It Means | Typical User |
|-------|---------------|--------------|
| **Beginner** | Simple inputs, straightforward prompts, quick results | Anyone, even first-time Claude Code users |
| **Intermediate** | Multiple inputs, some iteration needed, judgment required | Comfortable with Claude Code basics |
| **Advanced** | Complex inputs, multiple steps, significant customization | Regular Claude Code users, domain expertise helpful |

### Understanding Time Estimates

Each recipe shows:
- **Setup Time** — How long the first use takes (includes learning the workflow)
- **Time Saved** — Hours saved compared to doing the task manually

These are realistic estimates for typical professional work. Your actual times may vary based on the complexity of your specific task.

### Getting the Best Results

1. **Be specific in your prompts** — "Analyze Q3 sales focusing on regional trends" beats "Analyze sales"
2. **Provide context** — Tell Claude your role, your audience, and what "good" looks like
3. **Iterate** — Treat first outputs as drafts; ask for revisions and refinements
4. **Review everything** — AI output needs human judgment before use in professional contexts

### What Each Recipe Contains

Every recipe follows a consistent structure:

| Section | What It Tells You |
|---------|-------------------|
| **The Problem** | What pain point this recipe solves |
| **The Outcome** | What you'll have when done |
| **When to Use** | Good fit vs. not a good fit scenarios |
| **Prerequisites** | What you need before starting |
| **How Claude Helps** | What Claude does well vs. where you add judgment |
| **Step-by-Step** | Detailed walkthrough with prompts |
| **Example Output** | What good results look like |
| **Troubleshooting** | Common issues and solutions |
| **Variations** | Alternative approaches for different needs |

---

## How the Recipes Are Organized

The 100 recipes are organized into 10 tiers, progressing from universal daily tasks to specialized professional functions:

| Tier | Category | Recipes | Best For |
|------|----------|---------|----------|
| 1 | Universal High-Frequency Wins | 001-010 | Everyone - start here |
| 2 | Leadership & Management | 011-020 | Managers, Directors, Executives |
| 3 | Strategy & Analysis | 021-030 | Analysts, Strategists, Finance |
| 4 | Professional Communication | 031-040 | Marketing, Communications, Sales |
| 5 | Operations & Compliance | 041-050 | Operations, Legal, Quality |
| 6 | Data & Reporting | 051-060 | Analysts, Business Intelligence |
| 7 | HR & People Operations | 061-070 | HR, L&D, People Managers |
| 8 | Sales & Customer Operations | 071-080 | Sales, Customer Success, Marketing |
| 9 | Project & Product Management | 081-090 | PMs, Product Managers, Scrum Masters |
| 10 | Technical & Specialized | 091-100 | Technical Writers, IT, Legal |

---

## Complete Recipe Index

### Tier 1: Universal High-Frequency Wins (001-010)

*Tasks everyone does daily or weekly. Start here for immediate productivity gains.*

| # | Recipe | Time Saved |
|---|--------|------------|
| 001 | [Meeting Notes to Action Items](recipes/Recipe-001-Meeting-Notes-to-Action-Items.md) | 30-60 min/meeting |
| 002 | [Weekly Status Report Generation](recipes/Recipe-002-Weekly-Status-Report-Generation.md) | 2-3 hours/week |
| 003 | [Email Drafting and Response](recipes/Recipe-003-Email-Drafting-and-Response.md) | 1-2 hours/day |
| 004 | [Document Summarization](recipes/Recipe-004-Document-Summarization.md) | 1-2 hours/document |
| 005 | [Rapid Presentation Development](recipes/Recipe-005-Rapid-Presentation-Development.md) | 3-6 hours/deck |
| 006 | [Calendar and Schedule Optimization](recipes/Recipe-006-Calendar-Schedule-Optimization.md) | 1-2 hours/week |
| 007 | [Research Synthesis](recipes/Recipe-007-Research-Synthesis.md) | 2-4 hours/project |
| 008 | [Task and Project List Organization](recipes/Recipe-008-Task-Project-List-Organization.md) | 1-2 hours/week |
| 009 | [Data Cleanup and Formatting](recipes/Recipe-009-Data-Cleanup-Formatting.md) | 2-4 hours/dataset |
| 010 | [Quick Reference Guide Creation](recipes/Recipe-010-Quick-Reference-Guide-Creation.md) | 2-3 hours/guide |

---

### Tier 2: Leadership & Management (011-020)

*For managers, directors, and executives managing teams and making decisions.*

| # | Recipe | Time Saved |
|---|--------|------------|
| 011 | [Board and Leadership Meeting Prep](recipes/Recipe-011-Board-Leadership-Meeting-Prep.md) | 4-8 hours/meeting |
| 012 | [High-Stakes Communication Drafting](recipes/Recipe-012-High-Stakes-Communication-Drafting.md) | 1-2 hours/message |
| 013 | [Performance Review Writing](recipes/Recipe-013-Performance-Review-Writing.md) | 2-3 hours/review |
| 014 | [One-on-One Meeting Prep](recipes/Recipe-014-One-on-One-Meeting-Prep.md) | 30-60 min/meeting |
| 015 | [Team Capacity and Resource Planning](recipes/Recipe-015-Team-Capacity-Resource-Planning.md) | 3-5 hours/cycle |
| 016 | [Budget Scenario Modeling](recipes/Recipe-016-Budget-Scenario-Modeling.md) | 4-8 hours/cycle |
| 017 | [OKR and Goal Setting](recipes/Recipe-017-OKR-Goal-Setting.md) | 3-5 hours/cycle |
| 018 | [Delegation Brief Creation](recipes/Recipe-018-Delegation-Brief-Creation.md) | 1-2 hours/task |
| 019 | [Meeting Facilitation Planning](recipes/Recipe-019-Meeting-Facilitation-Planning.md) | 1-2 hours/meeting |
| 020 | [Org Design and Structure Analysis](recipes/Recipe-020-Org-Design-Structure-Analysis.md) | 5-10 hours/analysis |

---

### Tier 3: Strategy & Analysis (021-030)

*For strategic planning, financial analysis, and business intelligence.*

| # | Recipe | Time Saved |
|---|--------|------------|
| 021 | [Competitive Intelligence Synthesis](recipes/Recipe-021-Competitive-Intelligence-Synthesis.md) | 6-10 hours/report |
| 022 | [Strategic Planning Document Synthesis](recipes/Recipe-022-Strategic-Planning-Document-Synthesis.md) | 15-25 hours/cycle |
| 023 | [Market Research Analysis Summary](recipes/Recipe-023-Market-Research-Analysis-Summary.md) | 4-8 hours/report |
| 024 | [Customer Account Analysis Deep Dives](recipes/Recipe-024-Customer-Account-Analysis-Deep-Dives.md) | 3-5 hours/analysis |
| 025 | [Financial Analysis and Trend Interpretation](recipes/Recipe-025-Financial-Analysis-Trend-Interpretation.md) | 3-6 hours/analysis |
| 026 | [Risk Assessment and Mitigation Planning](recipes/Recipe-026-Risk-Assessment-Mitigation-Planning.md) | 4-8 hours/assessment |
| 027 | [Business Case Development](recipes/Recipe-027-Business-Case-Development.md) | 6-12 hours/case |
| 028 | [Benchmarking Analysis](recipes/Recipe-028-Benchmarking-Analysis.md) | 4-8 hours/analysis |
| 029 | [SWOT and Strategic Framework Analysis](recipes/Recipe-029-SWOT-Strategic-Framework-Analysis.md) | 3-6 hours/analysis |
| 030 | [Investor and Board Materials Preparation](recipes/Recipe-030-Investor-Board-Materials-Preparation.md) | 8-15 hours/package |

---

### Tier 4: Professional Communication (031-040)

*For creating compelling content and professional communications.*

| # | Recipe | Time Saved |
|---|--------|------------|
| 031 | [Proposal and Pitch Document Creation](recipes/Recipe-031-Proposal-Pitch-Document-Creation.md) | 4-8 hours/proposal |
| 032 | [RFP and Government Contract Response](recipes/Recipe-032-RFP-Government-Contract-Response.md) | 10-20 hours/response |
| 033 | [Newsletter and Update Content Creation](recipes/Recipe-033-Newsletter-Update-Content-Creation.md) | 2-4 hours/issue |
| 034 | [Blog Post and Thought Leadership](recipes/Recipe-034-Blog-Post-Thought-Leadership.md) | 3-5 hours/post |
| 035 | [Case Study Development](recipes/Recipe-035-Case-Study-Development.md) | 4-8 hours/study |
| 036 | [Executive Communication Ghostwriting](recipes/Recipe-036-Executive-Communication-Ghostwriting.md) | 2-4 hours/piece |
| 037 | [Press Release and Media Statement Drafting](recipes/Recipe-037-Press-Release-Media-Statement-Drafting.md) | 2-4 hours/release |
| 038 | [Customer Communication Templates](recipes/Recipe-038-Customer-Communication-Templates.md) | 3-6 hours/template set |
| 039 | [Technical Writing for Non-Technical Audiences](recipes/Recipe-039-Technical-Writing-Non-Technical-Audiences.md) | 3-5 hours/document |
| 040 | [Speech and Presentation Script Writing](recipes/Recipe-040-Speech-Presentation-Script-Writing.md) | 4-8 hours/speech |

---

### Tier 5: Operations & Compliance (041-050)

*For operational excellence, compliance, and process documentation.*

| # | Recipe | Time Saved |
|---|--------|------------|
| 041 | [Policy and Procedure Documentation](recipes/Recipe-041-Policy-Procedure-Documentation.md) | 8-15 hours/policy |
| 042 | [Process Documentation and SOPs](recipes/Recipe-042-Process-Documentation-SOPs.md) | 4-8 hours/process |
| 043 | [Contract Review and Risk Summarization](recipes/Recipe-043-Contract-Review-Risk-Summarization.md) | 2-4 hours/contract |
| 044 | [Vendor and Technology Evaluation Matrices](recipes/Recipe-044-Vendor-Technology-Evaluation-Matrices.md) | 4-6 hours/evaluation |
| 045 | [Incident Analysis and Root Cause Reports](recipes/Recipe-045-Incident-Analysis-Root-Cause-Reports.md) | 3-5 hours/incident |
| 046 | [Regulatory Change Impact Assessment](recipes/Recipe-046-Regulatory-Change-Impact-Assessment.md) | 6-12 hours/assessment |
| 047 | [Audit Preparation Documentation](recipes/Recipe-047-Audit-Preparation-Documentation.md) | 8-15 hours/audit |
| 048 | [Quality Control Checklists and Standards](recipes/Recipe-048-Quality-Control-Checklists-Standards.md) | 4-8 hours/checklist |
| 049 | [Change Management Documentation](recipes/Recipe-049-Change-Management-Documentation.md) | 5-10 hours/change |
| 050 | [Service Level Agreement Development](recipes/Recipe-050-Service-Level-Agreement-Development.md) | 6-12 hours/SLA |

---

### Tier 6: Data & Reporting (051-060)

*For data analysis, visualization narratives, and business reporting.*

| # | Recipe | Time Saved |
|---|--------|------------|
| 051 | [Dashboard Narrative Generation](recipes/Recipe-051-Dashboard-Narrative-Generation.md) | 1-2 hours/report |
| 052 | [Survey Results Analysis and Reporting](recipes/Recipe-052-Survey-Results-Analysis-Reporting.md) | 3-6 hours/survey |
| 053 | [KPI Variance Analysis and Commentary](recipes/Recipe-053-KPI-Variance-Analysis-Commentary.md) | 2-4 hours/review |
| 054 | [Customer Feedback Synthesis](recipes/Recipe-054-Customer-Feedback-Synthesis.md) | 3-5 hours/synthesis |
| 055 | [Sales Pipeline Analysis and Commentary](recipes/Recipe-055-Sales-Pipeline-Analysis-Commentary.md) | 2-3 hours/review |
| 056 | [Cohort and Segment Analysis](recipes/Recipe-056-Cohort-Segment-Analysis.md) | 3-5 hours/analysis |
| 057 | [Trend Identification and Forecasting Narratives](recipes/Recipe-057-Trend-Identification-Forecasting-Narratives.md) | 3-6 hours/forecast |
| 058 | [Report Automation Design](recipes/Recipe-058-Report-Automation-Design.md) | 4-8 hours/setup |
| 059 | [Data Quality Assessment](recipes/Recipe-059-Data-Quality-Assessment.md) | 3-6 hours/assessment |
| 060 | [Executive Summary Generation from Detailed Reports](recipes/Recipe-060-Executive-Summary-Generation-Detailed-Reports.md) | 30-60 min/summary |

---

### Tier 7: HR & People Operations (061-070)

*For human resources, learning & development, and people management.*

| # | Recipe | Time Saved |
|---|--------|------------|
| 061 | [Job Descriptions and Role Documentation](recipes/Recipe-061-Job-Descriptions-Role-Documentation.md) | 2-3 hours/role |
| 062 | [Interview Question Banks and Scorecards](recipes/Recipe-062-Interview-Question-Banks-Scorecards.md) | 3-5 hours/role |
| 063 | [Employee Handbook and Policy Updates](recipes/Recipe-063-Employee-Handbook-Policy-Updates.md) | 6-12 hours/update |
| 064 | [Training Material Development](recipes/Recipe-064-Training-Material-Development.md) | 10-20 hours/course |
| 065 | [Onboarding Documentation and Checklists](recipes/Recipe-065-Onboarding-Documentation-Checklists.md) | 4-6 hours/program |
| 066 | [Employee Communication Campaigns](recipes/Recipe-066-Employee-Communication-Campaigns.md) | 3-6 hours/campaign |
| 067 | [Exit Interview Analysis and Themes](recipes/Recipe-067-Exit-Interview-Analysis-Themes.md) | 3-5 hours/analysis |
| 068 | [Compensation Analysis and Recommendations](recipes/Recipe-068-Compensation-Analysis-Recommendations.md) | 4-8 hours/analysis |
| 069 | [Diversity and Inclusion Reporting](recipes/Recipe-069-Diversity-Inclusion-Reporting.md) | 4-8 hours/report |
| 070 | [Skills Gap Analysis](recipes/Recipe-070-Skills-Gap-Analysis.md) | 4-8 hours/analysis |

---

### Tier 8: Sales & Customer Operations (071-080)

*For sales teams, customer success, and revenue operations.*

| # | Recipe | Time Saved |
|---|--------|------------|
| 071 | [Sales Call Preparation Briefs](recipes/Recipe-071-Sales-Call-Preparation-Briefs.md) | 30-60 min/call |
| 072 | [Win/Loss Analysis and Themes](recipes/Recipe-072-Win-Loss-Analysis-Themes.md) | 4-6 hours/analysis |
| 073 | [Customer Success Playbook Development](recipes/Recipe-073-Customer-Success-Playbook-Development.md) | 8-15 hours/playbook |
| 074 | [QBR Preparation](recipes/Recipe-074-QBR-Preparation.md) | 2-4 hours/QBR |
| 075 | [Sales Enablement Content Creation](recipes/Recipe-075-Sales-Enablement-Content-Creation.md) | 3-5 hours/asset |
| 076 | [Lead Scoring and Prioritization Analysis](recipes/Recipe-076-Lead-Scoring-Prioritization-Analysis.md) | 2-4 hours/analysis |
| 077 | [Customer Journey Mapping](recipes/Recipe-077-Customer-Journey-Mapping.md) | 4-8 hours/map |
| 078 | [Pricing Analysis and Recommendation](recipes/Recipe-078-Pricing-Analysis-Recommendation.md) | 4-6 hours/analysis |
| 079 | [Territory and Account Assignment Analysis](recipes/Recipe-079-Territory-Account-Assignment-Analysis.md) | 4-8 hours/analysis |
| 080 | [Campaign Performance Analysis](recipes/Recipe-080-Campaign-Performance-Analysis.md) | 2-4 hours/campaign |

---

### Tier 9: Project & Product Management (081-090)

*For project managers, product managers, and agile teams.*

| # | Recipe | Time Saved |
|---|--------|------------|
| 081 | [Project Charter and Kickoff Documentation](recipes/Recipe-081-Project-Charter-Kickoff-Documentation.md) | 3-5 hours/project |
| 082 | [Requirements Documentation](recipes/Recipe-082-Requirements-Documentation.md) | 4-8 hours/document |
| 083 | [Sprint Planning and Backlog Refinement](recipes/Recipe-083-Sprint-Planning-Backlog-Refinement.md) | 2-3 hours/sprint |
| 084 | [Product Roadmap Communication](recipes/Recipe-084-Product-Roadmap-Communication.md) | 3-5 hours/update |
| 085 | [Release Notes and Changelog Generation](recipes/Recipe-085-Release-Notes-Changelog-Generation.md) | 1-2 hours/release |
| 086 | [Project Status and Health Reporting](recipes/Recipe-086-Project-Status-Health-Reporting.md) | 2-3 hours/report |
| 087 | [Stakeholder Analysis and Communication Planning](recipes/Recipe-087-Stakeholder-Analysis-Communication-Planning.md) | 3-5 hours/analysis |
| 088 | [Lessons Learned Facilitation and Documentation](recipes/Recipe-088-Lessons-Learned-Facilitation-Documentation.md) | 3-5 hours/session |
| 089 | [Product Feature Prioritization Analysis](recipes/Recipe-089-Product-Feature-Prioritization-Analysis.md) | 3-5 hours/cycle |
| 090 | [User Research Synthesis](recipes/Recipe-090-User-Research-Synthesis.md) | 4-8 hours/study |

---

### Tier 10: Technical & Specialized Functions (091-100)

*For technical documentation, IT operations, and specialized professional functions.*

| # | Recipe | Time Saved |
|---|--------|------------|
| 091 | [Technical Documentation from Engineering Inputs](recipes/Recipe-091-Technical-Documentation-From-Engineering-Inputs.md) | 3-5 hours/document |
| 092 | [API and Integration Documentation](recipes/Recipe-092-API-Integration-Documentation.md) | 4-6 hours/API |
| 093 | [Security Assessment Documentation](recipes/Recipe-093-Security-Assessment-Documentation.md) | 4-8 hours/assessment |
| 094 | [Knowledge Base and FAQ Generation](recipes/Recipe-094-Knowledge-Base-FAQ-Generation.md) | 3-6 hours/section |
| 095 | [IT Service Catalog Development](recipes/Recipe-095-IT-Service-Catalog-Development.md) | 8-12 hours/section |
| 096 | [Technical Specification Writing](recipes/Recipe-096-Technical-Specification-Writing.md) | 4-8 hours/spec |
| 097 | [Code Review Summary and Documentation](recipes/Recipe-097-Code-Review-Summary-Documentation.md) | 1-2 hours/review |
| 098 | [M&A and Partnership Due Diligence](recipes/Recipe-098-MA-Partnership-Due-Diligence.md) | 10-20 hours/deal |
| 099 | [Legal Research Summarization](recipes/Recipe-099-Legal-Research-Summarization.md) | 4-8 hours/research |
| 100 | [Intellectual Property Documentation](recipes/Recipe-100-Intellectual-Property-Documentation.md) | 6-12 hours/portfolio |

---

## Quick Start by Role

### If you're a **Manager or Director**
Start with: [001](recipes/Recipe-001-Meeting-Notes-to-Action-Items.md), [002](recipes/Recipe-002-Weekly-Status-Report-Generation.md), [013](recipes/Recipe-013-Performance-Review-Writing.md), [014](recipes/Recipe-014-One-on-One-Meeting-Prep.md)

### If you're an **Executive**
Start with: [011](recipes/Recipe-011-Board-Leadership-Meeting-Prep.md), [012](recipes/Recipe-012-High-Stakes-Communication-Drafting.md), [022](recipes/Recipe-022-Strategic-Planning-Document-Synthesis.md), [030](recipes/Recipe-030-Investor-Board-Materials-Preparation.md)

### If you're in **Sales**
Start with: [003](recipes/Recipe-003-Email-Drafting-and-Response.md), [071](recipes/Recipe-071-Sales-Call-Preparation-Briefs.md), [055](recipes/Recipe-055-Sales-Pipeline-Analysis-Commentary.md), [075](recipes/Recipe-075-Sales-Enablement-Content-Creation.md)

### If you're in **Marketing**
Start with: [033](recipes/Recipe-033-Newsletter-Update-Content-Creation.md), [034](recipes/Recipe-034-Blog-Post-Thought-Leadership.md), [035](recipes/Recipe-035-Case-Study-Development.md), [080](recipes/Recipe-080-Campaign-Performance-Analysis.md)

### If you're in **HR**
Start with: [061](recipes/Recipe-061-Job-Descriptions-Role-Documentation.md), [062](recipes/Recipe-062-Interview-Question-Banks-Scorecards.md), [065](recipes/Recipe-065-Onboarding-Documentation-Checklists.md), [064](recipes/Recipe-064-Training-Material-Development.md)

### If you're a **Product Manager**
Start with: [082](recipes/Recipe-082-Requirements-Documentation.md), [084](recipes/Recipe-084-Product-Roadmap-Communication.md), [089](recipes/Recipe-089-Product-Feature-Prioritization-Analysis.md), [090](recipes/Recipe-090-User-Research-Synthesis.md)

### If you're a **Project Manager**
Start with: [001](recipes/Recipe-001-Meeting-Notes-to-Action-Items.md), [081](recipes/Recipe-081-Project-Charter-Kickoff-Documentation.md), [086](recipes/Recipe-086-Project-Status-Health-Reporting.md), [087](recipes/Recipe-087-Stakeholder-Analysis-Communication-Planning.md)

### If you're an **Analyst**
Start with: [004](recipes/Recipe-004-Document-Summarization.md), [007](recipes/Recipe-007-Research-Synthesis.md), [051](recipes/Recipe-051-Dashboard-Narrative-Generation.md), [060](recipes/Recipe-060-Executive-Summary-Generation-Detailed-Reports.md)

---

## How to Use Each Recipe

Every recipe follows the same structure:

1. **The Problem** - What pain point this recipe solves
2. **The Outcome** - What you'll have when done
3. **When to Use** - Good fit vs. not a good fit scenarios
4. **Prerequisites** - What you need before starting
5. **How Claude Code Helps** - What Claude does well and where you add judgment
6. **Input Examples** - What to feed Claude
7. **Step-by-Step Implementation** - Detailed walkthrough with prompts
8. **Example Output** - What good results look like
9. **Troubleshooting** - Common issues and solutions
10. **Tips from Experience** - Practical wisdom from real use
11. **Variations** - Alternative approaches for different situations
12. **Building Your System** - How to make it repeatable

---

## Premium Collection: 200 Recipes as Slash Commands

Want to skip copying prompts? The **Premium Collection** includes all 200 recipes as ready-to-use Claude Code slash commands.

```
/recipe-001 Here are my meeting notes from today...
```

One command. Instant results.

### What's in the `premium/` Folder

| File | Description |
|------|-------------|
| `PREMIUM.md` | Full details on the Premium Collection |
| `README.md` | Installation guide for sample commands |
| `recipe-001.md` to `recipe-010.md` | 10 free sample slash commands to try |

### Try the Samples

Install the 10 free sample commands:

```bash
# Mac/Linux
cp premium/recipe-*.md ~/.claude/commands/

# Windows PowerShell
Copy-Item -Path "premium\recipe-*.md" -Destination "$env:USERPROFILE\.claude\commands\"
```

Then use them in Claude Code:
```
/recipe-001 Team standup: John finished API. Sarah blocked on design. Demo Friday.
```

### Premium Collection Includes

- **200 slash commands** covering all 100 core recipes plus 100 advanced recipes
- **20 categories** from daily tasks to enterprise strategy
- Role-based quick-start guides
- Cheat sheets and ROI tracking templates

See [`premium/PREMIUM.md`](premium/PREMIUM.md) for full details and purchase options.

---

## Contributing

Found a bug? Have an improvement? Want to add a recipe?

Open an issue or submit a pull request.

---

## License

This recipe collection is provided for educational and professional use. See [LICENSE.md](LICENSE.md) for full terms.

---

## Version History

See [CHANGELOG.md](CHANGELOG.md) for version history and updates.

---

*100 Recipes. Unlimited Productivity.*

*Version 1.0 — Built for Claude Code — December 2025*
