# Quality Control Checklists and Standards

**Recipe #48: From Inconsistent Quality to Reliable Excellence**

---

| Setup Time | Time Saved | Difficulty | Best For |
|------------|------------|------------|----------|
| 10 minutes (first time) / 5 minutes (repeat) | 3-5 hours per checklist | Beginner | Operations, QA, Production, Any Process Owner |

---

## The Problem

Quality depends on whoever is doing the work. Without standardized checklists and criteria, "good enough" means different things to different people. Experienced staff catch issues intuitively, but new hires miss them. Critical checks get skipped under time pressure. When quality problems surface, it's unclear whether the process failed or just wasn't followed. The result is inconsistent output, rework, customer complaints, and an inability to scale without scaling problems too.

**Pain Points:**
- Quality varies by who's doing the work
- Critical checks skipped under pressure
- New hires don't know what to look for
- No clear acceptance criteria
- Quality issues discovered too late
- Difficult to train and onboard
- Can't scale without quality degradation

---

## The Outcome

Comprehensive checklists and standards that ensure consistent quality regardless of who's performing the work. Clear criteria that enable objective quality assessment and early problem detection.

**What You'll Have When Done:**
- Standardized quality checklists
- Clear acceptance criteria
- Inspection points and frequency
- Defect classification system
- Escalation procedures
- Training materials
- Continuous improvement framework

---

## When to Use This Recipe

**Good Fit:**
- Manufacturing and production quality
- Service delivery standards
- Document and deliverable review
- Software release quality gates
- Customer-facing output verification
- Any repeatable process with quality requirements

**Not a Good Fit:**
- Highly creative work without standards
- One-time unique projects
- Research and exploration
- Early-stage process development

---

## Before You Start: Quick Checklist

- [ ] Claude Code is installed and working
- [ ] You understand the process or output needing quality control
- [ ] You know the quality requirements (regulatory, customer, internal)
- [ ] You have examples of good and poor quality
- [ ] You have 1-2 hours for checklist development

---

## How Claude Code Helps

**What Claude Code Does Well:**
- Creates comprehensive checklist structures
- Identifies inspection categories
- Develops clear acceptance criteria
- Structures defect classification systems
- Generates training materials
- Creates consistent formatting

**Where Human Judgment Is Essential:**
- Defining actual quality requirements
- Setting acceptance thresholds
- Validating checklist completeness
- Training on judgment calls
- Exception handling decisions
- Continuous improvement feedback

---

## Input Examples

**Ideal Source Materials:**

| Input Type | Example | What Claude Uses It For |
|------------|---------|------------------------|
| Process description | What's being produced/delivered | Context for checklist |
| Quality requirements | Standards, specs, customer needs | Criteria definition |
| Common defects | What goes wrong | Checkpoint focus |
| Current checks | Existing quality process | Gap identification |
| Good examples | What quality looks like | Standard setting |

**Sample Input:**
```
Quality Checklist Request

PROCESS: Customer Proposal Development

OUTPUT: Customer-facing sales proposals

QUALITY REQUIREMENTS:
- Professional appearance (brand standards)
- Accurate pricing (matches CRM quotes)
- Correct customer information (name, address, contacts)
- Complete scope (all requested items addressed)
- Proper approvals (pricing exceptions, terms exceptions)
- Compliance (legal disclaimers, terms and conditions)
- Technical accuracy (product capabilities correctly stated)

COMMON QUALITY ISSUES:
- Typos in customer name
- Wrong pricing tier applied
- Missing sections (scope items not addressed)
- Outdated product information
- Expired pricing
- Missing or wrong terms
- Formatting inconsistencies
- Wrong contact information

WHO CREATES PROPOSALS:
- Sales representatives (varying experience levels)
- Sales support (more consistent quality)
- Some new hires creating proposals within weeks

CURRENT QUALITY PROCESS:
- Manager review for deals over $50K
- No formal checklist
- Quality depends on experience
- Problems caught by customers (bad)

VOLUME:
- ~200 proposals per month
- Quality review bottleneck at manager level

GOAL:
- Enable self-review before manager review
- Catch obvious issues before escalation
- Consistent quality across all experience levels
- Reduce customer-caught errors to near zero
```

---

## Step-by-Step Implementation

### Step 1: Define Quality Requirements
**Time: 10-15 minutes**

Document:
- What does "quality" mean for this output?
- What are the must-have requirements?
- What are nice-to-have quality characteristics?
- What are the common failure modes?

---

### Step 2: Launch Claude Code
**Time: 30 seconds**

```bash
claude
```

---

### Step 3: Run the Quality Checklist Prompt
**Time: 5-7 minutes for Claude to process**

---

**PRIMARY PROMPT: Quality Control Checklist Development**

```
Please help me create a quality control checklist.

PROCESS/OUTPUT:
[What's being produced or delivered]

QUALITY REQUIREMENTS:
[List quality standards, specifications, or requirements]

COMMON QUALITY ISSUES:
[What typically goes wrong]

WHO PERFORMS THIS WORK:
[Roles, experience levels, volume]

CURRENT QUALITY PROCESS:
[How quality is checked today]

PLEASE CREATE:

1. COMPREHENSIVE QUALITY CHECKLIST

   Structure by category:

   ## Category 1: [e.g., Accuracy]
   - [ ] [Check item] - [What to verify] - [Pass criteria]
   - [ ] [Check item] - [What to verify] - [Pass criteria]

   ## Category 2: [e.g., Completeness]
   - [ ] [Check item] - [What to verify] - [Pass criteria]

   [Continue for all relevant categories]

   Include for each item:
   - The check itself (what to verify)
   - How to verify it (method)
   - Pass/fail criteria (what constitutes pass)
   - Severity if failed (Critical/Major/Minor)

2. ACCEPTANCE CRITERIA TABLE

   | Criterion | Standard | Measurement Method | Accept/Reject Threshold |

3. DEFECT CLASSIFICATION

   Define defect severity:

   **Critical:** [Definition - requires immediate action]
   Examples: [Specific examples]

   **Major:** [Definition - significant impact]
   Examples: [Specific examples]

   **Minor:** [Definition - limited impact]
   Examples: [Specific examples]

4. INSPECTION PROCESS

   SELF-INSPECTION:
   - When: [At what stage]
   - Duration: [Expected time]
   - Checklist: [Which sections]
   - Action if issues found: [What to do]

   PEER REVIEW (if applicable):
   - When: [Triggers for peer review]
   - Reviewer qualifications: [Who can review]
   - Focus areas: [What peer reviews]

   MANAGEMENT REVIEW (if applicable):
   - When: [Triggers for management review]
   - Focus areas: [What management reviews]
   - Approval process: [How approval works]

5. QUICK REFERENCE CARD

   One-page version for daily use:
   - Critical checks only
   - Easy to scan
   - Fits on desk/wall

6. COMMON MISTAKES GUIDE

   | Mistake | How to Catch | How to Prevent |

7. ESCALATION PROCEDURES

   When to escalate:
   - [Situation 1] → [Escalation path]
   - [Situation 2] → [Escalation path]

   How to escalate:
   - [Process]

8. QUALITY METRICS

   Metrics to track:
   - [Metric 1]: [What it measures] [Target]
   - [Metric 2]: [What it measures] [Target]

9. TRAINING GUIDE

   For new team members:
   - Checklist orientation
   - Practice exercises
   - Common scenarios
   - When to ask for help

10. CONTINUOUS IMPROVEMENT

    How to update the checklist:
    - New defect types: [Process]
    - Feedback mechanism: [How to submit]
    - Review cadence: [How often updated]

Make the checklist practical and usable. Every item should be verifiable and actionable.
```

---

### Step 4: Validate Completeness
**Time: 15-20 minutes**

Review the checklist:
- Does it cover all known quality issues?
- Are the criteria clear and measurable?
- Is it practical to use in the workflow?
- Is anything missing?

---

### Step 5: Refine for Usability
**Time: 10-15 minutes**

**To improve clarity:**
```
The criterion "[item]" is vague. Make it more specific:
- What exactly should the checker look for?
- How do they know if it passes or fails?
- What's an example of pass vs. fail?
```

**To prioritize:**
```
This checklist is too long for regular use. Prioritize:
- Which items catch the most common/serious issues?
- What's the minimum viable checklist?
- What can be checked less frequently?
```

**To add examples:**
```
Add examples for each criterion showing:
- What good looks like
- What bad looks like
- Borderline cases and how to decide
```

---

### Step 6: Create Final Deliverables
**Time: 10 minutes**

```
Create the final quality control package:

1. FULL CHECKLIST
   Complete checklist with all items

2. QUICK REFERENCE CARD
   One-page essential checks

3. TRAINING PRESENTATION
   For onboarding new team members

4. POSTER/WALL VERSION
   Visual reminder for work area

5. DIGITAL FORM
   If applicable, format for tool input (Google Form, checklist app, etc.)

6. TRACKING TEMPLATE
   For recording quality metrics
```

---

## Example Output

Below is an abbreviated quality checklist example:

---

> **PROPOSAL QUALITY CHECKLIST**
>
> **Version 1.0 | Effective: [Date]**
>
> ---
>
> ## Instructions
>
> Complete this checklist before submitting any proposal for manager review.
> - ✅ Check each item that passes
> - ❌ Mark any items that fail and correct before submission
> - ⚠️ For borderline cases, note the issue and request peer review
>
> **Time to complete:** 10-15 minutes
>
> ---
>
> ## 1. Customer Information Accuracy
>
> | # | Check | How to Verify | Pass Criteria | Severity |
> |---|-------|---------------|---------------|----------|
> | 1.1 | Customer legal name correct | Compare to CRM account name | Exact match, proper capitalization | 🔴 Critical |
> | 1.2 | Customer address correct | Verify against CRM or customer-provided | Matches current address | 🟡 Major |
> | 1.3 | Contact names correct | Cross-check with email/CRM | Names spelled correctly | 🔴 Critical |
> | 1.4 | Contact titles current | Verify with contact or CRM | Title matches current role | 🟢 Minor |
> | 1.5 | Contact information included | Check proposal header/footer | Email and phone present | 🟡 Major |
>
> **Common mistakes:**
> - Copying from old proposal with outdated contacts
> - Misspelling names (especially non-English names)
> - Using "Inc." vs "LLC" incorrectly
>
> ---
>
> ## 2. Pricing Accuracy
>
> | # | Check | How to Verify | Pass Criteria | Severity |
> |---|-------|---------------|---------------|----------|
> | 2.1 | Pricing matches approved quote | Compare line-by-line to CRM quote | All prices match exactly | 🔴 Critical |
> | 2.2 | Pricing tier correct | Verify customer qualifies for tier | Tier matches qualification | 🔴 Critical |
> | 2.3 | Discounts approved | Check approval in CRM/email | Discount has documented approval | 🔴 Critical |
> | 2.4 | Math correct | Recalculate totals | Subtotals and totals accurate | 🔴 Critical |
> | 2.5 | Pricing not expired | Check quote expiration | Quote date within validity period | 🟡 Major |
> | 2.6 | Currency correct | Verify customer's currency | Matches customer location/preference | 🟡 Major |
>
> **Common mistakes:**
> - Using last year's pricing
> - Applying wrong discount tier
> - Calculation errors in multi-year deals
> - Missing tax/shipping where applicable
>
> ---
>
> ## 3. Scope Completeness
>
> | # | Check | How to Verify | Pass Criteria | Severity |
> |---|-------|---------------|---------------|----------|
> | 3.1 | All RFP items addressed | Cross-reference RFP requirements | Every requirement has response | 🔴 Critical |
> | 3.2 | Scope matches discussion | Compare to meeting notes/emails | All verbal commitments included | 🟡 Major |
> | 3.3 | Out-of-scope clearly stated | Review exclusions section | Boundaries clearly defined | 🟡 Major |
> | 3.4 | Timeline included | Check project timeline section | Deliverable dates specified | 🟡 Major |
> | 3.5 | Assumptions documented | Review assumptions section | Key assumptions stated | 🟢 Minor |
>
> **Common mistakes:**
> - Missing items from complex RFPs
> - Forgetting verbal agreements from calls
> - Vague scope leading to disputes
>
> ---
>
> ## 4. Technical Accuracy
>
> | # | Check | How to Verify | Pass Criteria | Severity |
> |---|-------|---------------|---------------|----------|
> | 4.1 | Product names current | Check current product list | No deprecated product names | 🟡 Major |
> | 4.2 | Features accurately described | Reference product documentation | Capabilities correctly stated | 🔴 Critical |
> | 4.3 | Integration claims valid | Verify with product team if unsure | Only documented integrations | 🔴 Critical |
> | 4.4 | Performance claims supported | Reference official specs | No unsupported performance claims | 🔴 Critical |
>
> **Common mistakes:**
> - Copying old proposals with outdated product info
> - Overstating capabilities
> - Claiming integrations that require customization
>
> ---
>
> ## 5. Compliance and Legal
>
> | # | Check | How to Verify | Pass Criteria | Severity |
> |---|-------|---------------|---------------|----------|
> | 5.1 | Terms and conditions included | Check for T&C attachment | Current T&C version attached | 🔴 Critical |
> | 5.2 | Required disclaimers present | Review compliance checklist | All required disclaimers included | 🔴 Critical |
> | 5.3 | Non-standard terms flagged | Compare to standard terms | Deviations marked for legal review | 🔴 Critical |
> | 5.4 | Confidentiality appropriate | Review confidential markings | Properly marked if confidential | 🟢 Minor |
>
> ---
>
> ## 6. Professional Presentation
>
> | # | Check | How to Verify | Pass Criteria | Severity |
> |---|-------|---------------|---------------|----------|
> | 6.1 | Uses current template | Compare to template library | Latest template version used | 🟡 Major |
> | 6.2 | Logo and branding correct | Visual inspection | Current logo, brand colors | 🟡 Major |
> | 6.3 | Spelling and grammar | Run spell-check + read through | No errors | 🟡 Major |
> | 6.4 | Formatting consistent | Visual inspection | Headers, fonts, spacing consistent | 🟢 Minor |
> | 6.5 | Page numbers correct | Check footer | Pages numbered correctly | 🟢 Minor |
> | 6.6 | Table of contents accurate | Click each link | Links work, page numbers match | 🟢 Minor |
>
> **Common mistakes:**
> - Old logo/branding
> - Mixed fonts from copying
> - Spell-check misses context errors (their/there)
>
> ---
>
> ## Quick Reference Card
>
> **THE CRITICAL 10 (Must Check Every Time)**
>
> Before submitting ANY proposal:
>
> 1. ☐ Customer name spelled correctly
> 2. ☐ Contact names spelled correctly
> 3. ☐ Pricing matches CRM quote exactly
> 4. ☐ All discounts have documented approval
> 5. ☐ Math is correct (recalculate totals)
> 6. ☐ All RFP requirements addressed
> 7. ☐ Product capabilities accurately stated
> 8. ☐ No unsupported performance claims
> 9. ☐ Current T&C attached
> 10. ☐ Required disclaimers included
>
> **If ANY of these fail, do not submit until corrected.**
>
> ---
>
> ## Defect Classification
>
> **🔴 Critical Defects**
> - Would embarrass us with the customer
> - Could create legal/contractual exposure
> - Pricing errors affecting deal value
> - Examples: Wrong customer name, incorrect pricing, missing compliance items
>
> **🟡 Major Defects**
> - Noticeable quality issue
> - Could affect customer confidence
> - Requires rework before sending
> - Examples: Wrong contacts, formatting issues, missing sections
>
> **🟢 Minor Defects**
> - Small quality issue
> - Unlikely to affect decision
> - Should fix if time permits
> - Examples: Minor typos, formatting inconsistencies
>
> ---
>
> ## Escalation Procedures
>
> | Situation | Action |
> |-----------|--------|
> | Unsure if product claim is accurate | Ask Solutions Engineering before including |
> | Discount exceeds normal authority | Get VP Sales approval before quoting |
> | Customer requesting non-standard terms | Flag for Legal review |
> | Can't meet requested timeline | Discuss with manager before committing |
> | RFP requirement unclear | Clarify with customer before responding |
>
> ---
>
> ## Quality Metrics to Track
>
> | Metric | Definition | Target |
> |--------|------------|--------|
> | First-pass rate | % of proposals passing self-review on first check | >85% |
> | Customer-caught errors | Errors identified by customer | 0 |
> | Manager revision rate | % requiring manager-requested changes | <15% |
> | Critical defect rate | Critical defects per 100 proposals | <2% |
>
> ---
>
> ## Training Checklist (New Team Members)
>
> Before creating proposals independently:
>
> - [ ] Read this quality checklist thoroughly
> - [ ] Review 3 exemplary proposals (ask manager)
> - [ ] Create 2 practice proposals with supervision
> - [ ] Pass quiz on critical checks (80% minimum)
> - [ ] Have first 5 proposals peer-reviewed
> - [ ] Graduate to self-review with spot checks

---

## Troubleshooting Common Issues

| Problem | Likely Cause | Solution |
|---------|--------------|----------|
| Checklist too long | Trying to catch everything | Ask: "Prioritize by impact. What are the top 10 must-checks?" |
| Criteria too vague | Not specific enough | Ask: "For each item, add specific pass/fail examples" |
| People skip checklist | Too burdensome | Ask: "Create a 2-minute quick version for routine use" |
| Still having quality issues | Checklist incomplete | Ask: "What defects are still occurring? Add to checklist" |
| Different people interpret differently | Criteria not objective | Ask: "Make criteria more measurable. Remove judgment calls" |
| Checklist doesn't fit workflow | Not integrated into process | Ask: "When exactly should this be used? Add to the process" |

---

## Tips from Experience

1. **Start with the top 10.** A short checklist that's used beats a comprehensive checklist that's ignored.

2. **Make pass/fail objective.** "Looks professional" is subjective. "Uses current template" is objective.

3. **Include the "why."** People follow checklists better when they understand why each item matters.

4. **Test with users.** Have people actually use the checklist and give feedback before finalizing.

5. **Build into workflow.** The checklist should be a required step, not an optional extra.

6. **Update regularly.** When new defect types appear, add them. When old ones disappear, consider removing.

---

## Measuring Success

**You've succeeded with this recipe when:**
- [ ] Quality is consistent regardless of who does the work
- [ ] Defect rate decreases after implementation
- [ ] New hires achieve quality faster
- [ ] Customer-caught errors approach zero
- [ ] Less time spent on rework
- [ ] Checklist is actually used

**Track over time:**
- Defect rate by type
- First-pass rate (no rework needed)
- Time to quality for new hires
- Customer complaints related to quality
- Checklist completion rate

---

## Variations

### Manufacturing Quality Checklist
For production environments:
```
Create a manufacturing quality checklist.

Product: [What's being manufactured]
Specifications: [Quality standards and tolerances]
Inspection points: [Where to check in process]

Include:
- Incoming material inspection
- In-process checkpoints
- Final inspection criteria
- Measurement methods
- Accept/reject criteria
- Documentation requirements
```

### Service Delivery Checklist
For service quality:
```
Create a service delivery quality checklist.

Service: [What service is delivered]
Customer expectations: [SLA, quality standards]
Common issues: [Service failures]

Include:
- Pre-service preparation checks
- During-service quality points
- Post-service verification
- Customer confirmation
- Documentation requirements
```

### Software Release Checklist
For software quality gates:
```
Create a software release quality checklist.

Release type: [Feature, hotfix, maintenance]
Quality gates: [Existing gates]
Common issues: [Defects that escape]

Include:
- Code quality checks
- Testing requirements
- Security verification
- Performance validation
- Documentation completion
- Rollback readiness
```

### Document Quality Checklist
For document review:
```
Create a document quality checklist.

Document type: [Report, contract, policy, etc.]
Quality standards: [Accuracy, formatting, etc.]
Common issues: [Typical document errors]

Include:
- Content accuracy checks
- Formatting standards
- Required sections
- Approval requirements
- Version control
```

---

## Building Your Repeatable System

After creating several checklists, build your system:

1. **Create checklist library** organized by process
2. **Establish review cadence** for updates
3. **Track effectiveness** of each checklist
4. **Collect feedback** for continuous improvement
5. **Share best practices** across teams

**Sample Setup:**
```
quality-management/
├── checklists/
│   ├── sales/
│   │   ├── proposal-quality.md
│   │   ├── contract-review.md
│   │   └── demo-preparation.md
│   ├── operations/
│   │   ├── order-processing.md
│   │   └── fulfillment.md
│   └── service/
│       ├── support-ticket.md
│       └── onboarding.md
├── standards/
│   ├── acceptance-criteria/
│   └── defect-definitions/
├── training/
│   ├── checklist-training.pptx
│   └── examples/
├── metrics/
│   └── quality-tracking.xlsx
└── feedback/
    └── improvement-log.md
```

---

## How This Pattern Applies Elsewhere

This recipe's core pattern—**define quality criteria → create verification steps → classify defects → enable consistent checking**—applies broadly:

| Role | Application |
|------|-------------|
| **Sales** | Proposal, quote, contract quality |
| **Operations** | Process and output quality |
| **Manufacturing** | Product quality control |
| **Service** | Service delivery quality |
| **IT** | Release and deployment quality |
| **Any** | Deliverable quality assurance |

---

## Next Steps

1. **Identify quality gaps:** Where is quality inconsistent?
2. **Document requirements:** What does "quality" mean?
3. **Generate checklist:** Use this recipe
4. **Test with users:** Validate practicality
5. **Implement and train:** Roll out with support
6. **Monitor and improve:** Track effectiveness and update

---

*Recipe #48 of 100 in the Claude Code Knowledge Worker Recipe Collection*

---

**Related tooling:** the verification philosophy this recipe applies by hand is implemented for AI-assisted code in [ai-control-framework](https://github.com/sgharlow/ai-control-framework) — deployment-readiness scoring and evidence-backed gates.
