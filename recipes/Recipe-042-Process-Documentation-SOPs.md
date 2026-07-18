# Process Documentation and SOPs

**Recipe #42: From Tribal Knowledge to Reliable Operations**

---

| Setup Time | Time Saved | Difficulty | Best For |
|------------|------------|------------|----------|
| 10 minutes (first time) / 5 minutes (repeat) | 4-8 hours per process | Beginner | Operations, All Departments, Trainers |

---

## The Problem

Critical processes live in people's heads, not in documentation. When that person is sick, on vacation, or leaves the company, the knowledge goes with them. Even when processes are documented, the documentation is often outdated, incomplete, or so confusing that people don't follow it. The result is inconsistent execution, errors, lengthy onboarding, and operational fragility.

**Pain Points:**
- Tribal knowledge dependencies
- Inconsistent process execution
- Long onboarding times for new staff
- Errors when regular person is unavailable
- Outdated or incomplete documentation
- "Just ask Sarah" as the operating procedure
- Quality varies by who's doing the work

---

## The Outcome

Clear, complete, and maintainable standard operating procedures that enable anyone with appropriate training to execute the process correctly. Documentation that actually gets used because it's practical and accurate.

**What You'll Have When Done:**
- Complete SOP with step-by-step instructions
- Decision points clearly mapped
- Exception handling documented
- Visual process flow
- Quality checkpoints
- Training-ready materials
- Maintenance plan for updates

---

## When to Use This Recipe

**Good Fit:**
- Recurring operational processes
- Cross-training documentation
- Quality-critical procedures
- Compliance-required processes
- New hire onboarding materials
- Knowledge capture from departing employees

**Not a Good Fit:**
- One-time projects (not recurring)
- Creative work without standard steps
- Executive decision-making (not proceduralizable)
- Processes still being designed

---

## Before You Start: Quick Checklist

- [ ] Claude Code is installed and working
- [ ] You have process knowledge (from experience or SME)
- [ ] You know the scope and boundaries of the process
- [ ] You understand who will use this documentation
- [ ] You have 1-3 hours for initial documentation

---

## How Claude Code Helps

**What Claude Code Does Well:**
- Structures process information logically
- Creates clear step-by-step instructions
- Identifies decision points and branches
- Generates exception handling sections
- Suggests quality checkpoints
- Creates visual flow descriptions

**Where Human Judgment Is Essential:**
- Actual process knowledge and accuracy
- What steps are truly required vs. habit
- Exception scenarios from experience
- Organizational context
- Tool and system specifics
- Testing and validation

---

## Input Examples

**Ideal Source Materials:**

| Input Type | Example | What Claude Uses It For |
|------------|---------|------------------------|
| Process overview | What gets done and why | Scope and purpose |
| Step notes | Rough steps or verbal description | Core procedure |
| Decision points | Where choices are made | Branching logic |
| Exceptions | What can go wrong | Exception handling |
| Tools used | Systems and applications | Technical instructions |

**Sample Input:**
```
SOP Documentation Request

PROCESS NAME: Monthly Revenue Recognition Close

PROCESS OVERVIEW:
Every month-end, we need to recognize revenue from contracts according to ASC 606.
This involves reviewing new contracts, calculating recognition schedules, posting
entries, and reconciling to the subledger.

PURPOSE:
- Accurate GAAP revenue recognition
- Clean financial close
- Audit-ready documentation

TRIGGER: First business day after month-end

FREQUENCY: Monthly

OWNER: Revenue Accounting Manager

ROUGH STEPS (as I know them):
1. Pull list of all new contracts signed during the month from Salesforce
2. Review each contract for revenue recognition treatment
3. Check if contract has performance obligations we need to separate
4. Calculate revenue schedules in Excel
5. Upload schedules to NetSuite
6. Run recognition for the month
7. Review output and post entries
8. Reconcile revenue subledger to GL
9. Document any issues or adjustments
10. Get manager sign-off

SYSTEMS USED:
- Salesforce (contract data)
- Excel (calculations)
- NetSuite (ERP/GL)
- SharePoint (documentation)

DECISION POINTS:
- Whether to recognize ratably or at point in time
- Whether there are multiple performance obligations
- How to handle contract modifications
- What to do with unusual terms

COMMON EXCEPTIONS:
- Contracts with non-standard terms
- Multi-year deals with variable consideration
- Contract modifications mid-stream
- Credits and refunds

WHO WILL USE THIS:
- Revenue accountants (daily executors)
- New hires during training
- Auditors during review
- Backup personnel when primary is out

CURRENT PROBLEMS WITH THE PROCESS:
- Too much variation in how different people do it
- New people take months to get up to speed
- Auditors always have questions about documentation
- When the main person is out, things get missed
```

---

## Step-by-Step Implementation

### Step 1: Capture Process Knowledge
**Time: 15-30 minutes**

Get the information:
- Interview the SME or document from your own experience
- Capture the rough flow first
- Note decision points and exceptions
- Identify tools and systems
- Understand quality requirements

---

### Step 2: Launch Claude Code
**Time: 30 seconds**

```bash
claude
```

---

### Step 3: Run the SOP Generation Prompt
**Time: 5-7 minutes for Claude to process**

---

**PRIMARY PROMPT: Process Documentation and SOPs**

```
Please help me create a Standard Operating Procedure (SOP) document.

PROCESS NAME: [Name]

PROCESS PURPOSE:
[Why this process exists, what it accomplishes]

SCOPE:
- Included: [What this process covers]
- Excluded: [What's outside this process]

TRIGGER: [What initiates this process]
FREQUENCY: [How often it runs]
OWNER: [Responsible role]

ROUGH PROCESS STEPS:
[Paste your notes or verbal description of the process]

SYSTEMS AND TOOLS:
- [System 1]: [What it's used for]
- [System 2]: [What it's used for]
(etc.)

DECISION POINTS:
[Where choices need to be made]

COMMON EXCEPTIONS:
[What can go wrong or require special handling]

AUDIENCE:
[Who will use this documentation]

PLEASE CREATE A COMPLETE SOP:

1. SOP HEADER
   - Document title
   - Document ID (placeholder)
   - Version and effective date
   - Process owner
   - Last reviewed date
   - Approval signatures (placeholders)

2. OVERVIEW SECTION
   - Purpose: Why this process exists
   - Scope: What's included and excluded
   - Inputs: What you need before starting
   - Outputs: What's produced when complete
   - Key metrics: How success is measured

3. ROLES AND RESPONSIBILITIES
   Table format:
   | Role | Responsibilities | Backup |

4. PREREQUISITES
   - Required access/permissions
   - Required training
   - Required materials/information
   - System availability requirements

5. DETAILED PROCEDURE
   For each step:
   - Step number and name
   - Detailed instructions (assume reader needs guidance)
   - System/tool used
   - Screenshots placeholders [SCREENSHOT: description]
   - Expected outcome
   - Quality checkpoint (if applicable)
   - Potential issues and resolution

   Use sub-steps (1.1, 1.2) for complex steps

6. DECISION FLOWCHART
   Text-based flowchart or decision tree showing:
   - Main process flow
   - Decision points with branches
   - Exception paths
   - End points

7. EXCEPTION HANDLING
   For each exception type:
   - How to identify
   - What to do
   - Who to escalate to
   - Documentation requirements

8. QUALITY CHECKPOINTS
   | Checkpoint | What to Verify | Action if Failed |

9. TROUBLESHOOTING
   | Issue | Likely Cause | Solution |

10. APPENDICES
    - Reference data
    - Template samples
    - Contact information
    - Related documents

Write in clear, action-oriented language. Each step should tell the reader exactly what to do. Assume the reader is new but trained.
```

---

### Step 4: Review for Accuracy and Completeness
**Time: 20-30 minutes**

Check the SOP:
- Is every step accurate?
- Are there missing steps?
- Can a trained newcomer follow this?
- Are decision points clear?
- Are exceptions covered?

---

### Step 5: Refine and Enhance
**Time: 15-20 minutes**

**To add detail to steps:**
```
Step [X] needs more detail. A new person wouldn't know how to [specific action]. Break this down into sub-steps and include what to look for.
```

**To improve decision points:**
```
The decision at step [X] isn't clear. Add specific criteria for each path. When exactly do you choose option A vs. option B?
```

**To add exception handling:**
```
What happens if [scenario]? This isn't covered. Add exception handling for this situation.
```

**To improve usability:**
```
This is very detailed but hard to reference quickly. Create a one-page quick reference version with just the essential steps for experienced users.
```

**To add verification:**
```
Add quality checkpoints after steps [X, Y, Z]. What should the user verify before proceeding?
```

---

### Step 6: Create Final Documentation Package
**Time: 10 minutes**

```
Create the complete SOP documentation package:

1. FULL SOP DOCUMENT
   - Complete procedure as documented
   - All sections finalized
   - Ready for review and approval

2. QUICK REFERENCE GUIDE
   - One-page summary
   - Key steps only
   - For experienced users

3. PROCESS FLOWCHART
   - Visual representation
   - Decision points clear
   - Suitable for wall posting or training

4. TRAINING CHECKLIST
   - Skills to develop
   - Steps to practice
   - Competency verification

5. MAINTENANCE NOTES
   - What triggers updates
   - Review schedule
   - Who maintains

6. CHANGE LOG TEMPLATE
   - Version tracking format
   - Change summary format
```

---

## Example Output

Below is an abbreviated SOP example:

---

> **STANDARD OPERATING PROCEDURE**
>
> ---
>
> | Document ID | FIN-SOP-2024-015 |
> |-------------|-----------------|
> | Title | Monthly Revenue Recognition Close |
> | Version | 1.0 |
> | Effective Date | [Date] |
> | Process Owner | Revenue Accounting Manager |
> | Last Reviewed | [Date] |
>
> ---
>
> ## 1. Overview
>
> ### 1.1 Purpose
> This procedure ensures accurate recognition of revenue in accordance with ASC 606 requirements, enabling timely financial close and audit-ready documentation.
>
> ### 1.2 Scope
> **Included:**
> - All customer contracts generating revenue
> - Revenue recognition calculations and posting
> - Subledger reconciliation
>
> **Excluded:**
> - Contract negotiation and execution (Sales process)
> - Collections and cash application (AR process)
> - Deferred revenue reporting (separate SOP)
>
> ### 1.3 Inputs
> - Signed contracts from Salesforce
> - Contract terms and amendments
> - Prior month recognition schedules
>
> ### 1.4 Outputs
> - Posted revenue entries in NetSuite
> - Updated recognition schedules
> - Reconciliation documentation
> - Manager sign-off
>
> ### 1.5 Key Metrics
> - Process completed by: Close Day +3
> - Reconciliation variance: ≤ $100
> - Documentation complete: 100%
>
> ---
>
> ## 2. Roles and Responsibilities
>
> | Role | Responsibilities | Backup |
> |------|-----------------|--------|
> | Revenue Accountant | Execute steps 1-9, prepare documentation | Senior Accountant |
> | Revenue Accounting Manager | Review and approve, handle exceptions | Controller |
> | Controller | Final sign-off on entries | CFO |
>
> ---
>
> ## 3. Prerequisites
>
> **Before starting this process, ensure:**
>
> - [ ] You have read/write access to Salesforce Contracts module
> - [ ] You have posting access to NetSuite Revenue accounts
> - [ ] You have completed ASC 606 training
> - [ ] Prior month close is complete
> - [ ] All contract data has been entered in Salesforce
>
> ---
>
> ## 4. Detailed Procedure
>
> ### Step 1: Generate New Contracts Report
> **System:** Salesforce
> **Time:** 15 minutes
>
> 1.1. Log into Salesforce
>
> 1.2. Navigate to **Reports > Revenue Accounting > New Contracts**
>
> 1.3. Set date range:
>    - Start Date: First day of month
>    - End Date: Last day of month
>
> 1.4. Click **Run Report**
>
> 1.5. Export to Excel:
>    - Click **Export**
>    - Select **Excel Format**
>    - Save as: `NewContracts_[YYYY-MM].xlsx`
>
> [SCREENSHOT: Salesforce report screen with date filters]
>
> **Quality Checkpoint:** Verify row count matches "New Contracts" dashboard tile
>
> **Expected Outcome:** Excel file with all new contracts for the month
>
> **Potential Issues:**
> | Issue | Solution |
> |-------|----------|
> | Report times out | Reduce date range, run in batches |
> | Missing contracts | Check with Sales Ops for late entries |
>
> ---
>
> ### Step 2: Review Contracts for Recognition Treatment
> **System:** Excel, Contract Documents
> **Time:** 30-60 minutes depending on volume
>
> For each contract in the export:
>
> 2.1. Open the contract document (linked in Salesforce)
>
> 2.2. Identify **performance obligations**:
>    - What distinct goods/services are promised?
>    - Can they be separated?
>
>    **Decision Point: Single vs. Multiple Performance Obligations**
>    - If ONE performance obligation → Continue to Step 2.3
>    - If MULTIPLE → Go to Step 2.2a (Allocation Sub-process)
>
> 2.3. Determine **recognition timing**:
>
>    | Contract Type | Recognition Method |
>    |--------------|-------------------|
>    | Subscription/SaaS | Ratably over term |
>    | Professional Services (time-based) | As delivered |
>    | Professional Services (milestone) | At milestone completion |
>    | Perpetual License | At delivery |
>    | Support/Maintenance | Ratably over term |
>
> 2.4. Document in tracking spreadsheet:
>    - Contract ID
>    - Recognition method
>    - Start/end dates
>    - Monthly recognition amount
>    - Notes on any unusual terms
>
> [SCREENSHOT: Recognition tracking spreadsheet template]
>
> **Quality Checkpoint:** All contracts have documented recognition method
>
> ---
>
> ### Step 2.2a: Multiple Performance Obligation Allocation
> **When to use:** Contract has more than one distinct deliverable
>
> 2.2a.1. List each performance obligation
>
> 2.2a.2. Determine **standalone selling price (SSP)** for each:
>    - Use actual price if sold separately
>    - Use similar transaction pricing
>    - Use cost-plus margin if needed
>
> 2.2a.3. Allocate total contract value based on relative SSP:
>    ```
>    Obligation Amount = Total Contract × (Obligation SSP / Total SSP)
>    ```
>
> 2.2a.4. Apply recognition method to each allocated amount
>
> 2.2a.5. Document allocation and rationale
>
> **Exception:** If unsure about allocation, escalate to Revenue Accounting Manager before proceeding
>
> ---
>
> ### Step 3: Calculate Recognition Schedules
> **System:** Excel (Revenue Schedule Template)
> **Time:** 30-45 minutes
>
> 3.1. Open `Revenue_Schedule_Template.xlsx`
>
> 3.2. For each contract, enter:
>    - Contract ID
>    - Customer name
>    - Total contract value
>    - Recognition method
>    - Start date
>    - End date
>
> 3.3. Verify formula calculations:
>    - Monthly amounts should equal total contract value when summed
>    - Recognition should not begin before contract start date
>
> 3.4. Save file as: `Revenue_Schedules_[YYYY-MM].xlsx`
>
> **Quality Checkpoint:**
> - Sum of all schedules = Total new contract value (±$1 for rounding)
> - No recognition before contract execution date
>
> ---
>
> ### Step 4: Upload to NetSuite
> **System:** NetSuite
> **Time:** 15-20 minutes
>
> 4.1. Log into NetSuite
>
> 4.2. Navigate to **Transactions > Revenue > Revenue Schedule Upload**
>
> 4.3. Click **Choose File** and select your schedule file
>
> 4.4. Click **Validate**:
>    - Review any errors
>    - Correct in source file if needed
>    - Re-upload until validation passes
>
> 4.5. Click **Upload**
>
> 4.6. Note the upload batch ID: ____________
>
> [SCREENSHOT: NetSuite upload screen with validation results]
>
> **Potential Issues:**
> | Issue | Solution |
> |-------|----------|
> | Customer not found | Add customer in NetSuite first |
> | Date format error | Ensure dates are MM/DD/YYYY |
> | Duplicate schedule | Check if contract already loaded |
>
> ---
>
> ### Step 5: Run Monthly Recognition
> **System:** NetSuite
> **Time:** 10 minutes
>
> 5.1. Navigate to **Transactions > Revenue > Process Revenue Recognition**
>
> 5.2. Set parameters:
>    - Period: [Current month]
>    - Subsidiary: All
>
> 5.3. Click **Preview** first to review
>
> 5.4. Review preview for:
>    - Expected amounts
>    - Correct accounts
>    - No unusual items
>
> 5.5. If preview looks correct, click **Process**
>
> 5.6. Note process batch ID: ____________
>
> **Quality Checkpoint:** Compare total recognized amount to prior month ± expected growth
>
> ---
>
> [Steps 6-10 continue in similar detail...]
>
> ---
>
> ## 5. Decision Flowchart
>
> ```
> START: New contracts report generated
>        |
>        v
> For each contract:
>        |
>        v
> +------------------+
> | Multiple         |
> | performance      |--YES--> Allocate based on SSP
> | obligations?     |                |
> +------------------+                |
>        |                            |
>        NO                           |
>        |<---------------------------+
>        v
> +------------------+
> | What type?       |
> +------------------+
>   |     |     |
>   v     v     v
> Sub  License  Service
>   |     |        |
>   v     v        v
> Ratable  Point  As delivered
>              in time
>        |
>        v
> Calculate schedule --> Upload --> Run recognition
>        |
>        v
> +------------------+
> | Reconciliation   |
> | variance > $100? |--YES--> Investigate before proceeding
> +------------------+
>        |
>        NO
>        v
> Document and get sign-off
>        |
>        v
> END
> ```
>
> ---
>
> ## 6. Exception Handling
>
> ### 6.1 Non-Standard Contract Terms
> **Trigger:** Contract has terms not fitting standard recognition patterns
>
> **Action:**
> 1. Document the unusual terms
> 2. Research ASC 606 guidance
> 3. Escalate to Revenue Accounting Manager with recommendation
> 4. Document conclusion in contract file
>
> ### 6.2 Contract Modifications
> **Trigger:** Existing contract is amended mid-term
>
> **Action:**
> 1. Determine if modification creates new contract or changes existing
> 2. If new: Process as new contract
> 3. If change: Adjust schedule prospectively or cumulatively per ASC 606
> 4. Document modification treatment
>
> ### 6.3 Credits and Refunds
> **Trigger:** Customer issued credit or refund
>
> **Action:**
> 1. Reverse recognized revenue if already recognized
> 2. Adjust future schedules if not yet recognized
> 3. Document reason for credit
>
> ---
>
> ## 7. Troubleshooting
>
> | Issue | Likely Cause | Solution |
> |-------|--------------|----------|
> | Schedule doesn't balance | Rounding or date calculation | Check formula, adjust manually if <$1 |
> | NetSuite upload fails | Format or data issues | Check error log, correct source data |
> | Reconciliation variance | Timing or missed item | Review posting dates, check for missed entries |
> | Prior period adjustment needed | Error discovered | Escalate to Manager for correction process |
>
> ---
>
> ## 8. Quick Reference (Experienced Users)
>
> 1. Pull new contracts report (Salesforce)
> 2. Review each contract, document treatment
> 3. Calculate schedules (template)
> 4. Upload to NetSuite, validate
> 5. Run recognition
> 6. Post entries
> 7. Reconcile (variance ≤ $100)
> 8. Document in SharePoint
> 9. Get manager sign-off
> 10. Close checklist
>
> **Key Deadlines:** Complete by Close Day +3

---

## Troubleshooting Common Issues

| Problem | Likely Cause | Solution |
|---------|--------------|----------|
| Steps too vague | Insufficient detail | Ask: "A new person wouldn't know how to do [X]. Add specific instructions" |
| Too much detail | Over-documentation | Ask: "Focus on what's essential. What can be assumed vs. must be stated?" |
| Decision points unclear | Missing criteria | Ask: "Add specific criteria for when to choose each option" |
| Exceptions not covered | Limited experience | Ask: "What happens if [edge case]? Add exception handling" |
| Hard to follow | Poor organization | Ask: "Reorganize with clearer numbering and visual structure" |
| Doesn't match reality | Documented ideal, not actual | Ask: "Adjust to reflect how this actually works, including workarounds" |

---

## Tips from Experience

1. **Document the actual process, not the ideal.** If there are workarounds, document them (and maybe fix them later).

2. **Be specific about systems.** "Enter the data" is useless. "Click the blue 'Submit' button in the lower right" is helpful.

3. **Include decision criteria.** "Use judgment" isn't a procedure. "If order value exceeds $50,000, escalate to manager" is.

4. **Test with someone new.** Have someone unfamiliar with the process try to follow your SOP. Where they get stuck is where you need more detail.

5. **Build in quality checkpoints.** Tell users how to verify they're on track before continuing.

6. **Plan for maintenance.** SOPs rot quickly if not updated. Assign ownership and review schedules.

---

## Measuring Success

**You've succeeded with this recipe when:**
- [ ] New users can execute the process correctly
- [ ] Error rates decrease
- [ ] Process is executed consistently regardless of who does it
- [ ] Onboarding time reduces
- [ ] Documentation is actually used and referenced

**Track over time:**
- Errors and exceptions by users
- Time to competency for new staff
- Questions about the process (should decrease)
- Process deviations and why
- SOP update frequency

---

## Variations

### Quick Reference Card
For experienced users:
```
Create a quick reference card for this SOP.

Full SOP:
[Paste or reference full SOP]

Create:
- One-page summary
- Essential steps only
- Key decision points
- Critical warnings
- Important contacts

Format for desk reference or lamination
```

### Training Module
For onboarding new staff:
```
Create a training module from this SOP.

SOP:
[Reference SOP]

Create:
- Learning objectives
- Pre-training requirements
- Step-by-step practice exercises
- Knowledge check questions
- Competency verification checklist
- Estimated training time
```

### Process Audit Checklist
For verification:
```
Create an audit checklist for this process.

SOP:
[Reference SOP]

Create:
- Items to verify
- Evidence to collect
- Common findings
- Scoring/rating criteria
- Audit report template
```

### Process Improvement Analysis
For optimizing existing processes:
```
Analyze this process for improvement opportunities.

Current SOP:
[Paste current SOP]

Pain points:
[Known issues]

Analyze:
- Steps that could be eliminated
- Steps that could be automated
- Decision points that could be simplified
- Quality issues and root causes
- Time/resource optimization opportunities
```

---

## Building Your Repeatable System

After documenting several processes, build your system:

1. **Create SOP template** for consistency
2. **Establish naming convention** for documents
3. **Set up central repository** accessible to users
4. **Define review cycle** (quarterly, annually)
5. **Track usage and feedback** for improvements

**Sample Setup:**
```
sops/
├── by-department/
│   ├── finance/
│   │   ├── FIN-SOP-001-monthly-close.md
│   │   ├── FIN-SOP-002-ap-processing.md
│   │   └── FIN-SOP-003-revenue-recognition.md
│   ├── operations/
│   ├── sales/
│   └── hr/
├── templates/
│   ├── sop-template.md
│   ├── quick-ref-template.md
│   └── training-checklist.md
├── register/
│   └── sop-register.xlsx
├── training/
│   └── by-process/
└── archive/
    └── superseded/
```

---

## How This Pattern Applies Elsewhere

This recipe's core pattern—**capture process knowledge → structure in actionable steps → include decisions and exceptions → make executable by others**—applies broadly:

| Role | Application |
|------|-------------|
| **Operations** | All operational processes |
| **Finance** | Financial close, reporting, controls |
| **HR** | Hiring, onboarding, offboarding |
| **IT** | System administration, incident response |
| **Sales** | Lead handling, quoting, contracting |
| **Customer Success** | Onboarding, support, renewals |

---

## Next Steps

1. **Identify critical processes:** What's most important or most problematic?
2. **Capture knowledge:** Interview SMEs or document your own expertise
3. **Generate SOP:** Use this recipe for structured documentation
4. **Test with users:** Have someone follow the SOP
5. **Refine based on feedback:** Fix gaps and unclear areas
6. **Implement and maintain:** Deploy and keep updated

---

*Recipe #42 of 100 in the Claude Code Knowledge Worker Recipe Collection*

---

**Related tooling:** the verification philosophy this recipe applies by hand is implemented for AI-assisted code in [ai-control-framework](https://github.com/sgharlow/ai-control-framework) — deployment-readiness scoring and evidence-backed gates.
