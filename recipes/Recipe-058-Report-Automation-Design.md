# Report Automation Design

**Recipe #58: Design Reports That Generate Themselves**

---

| Setup Time | Time Saved | Difficulty | Best For |
|------------|------------|------------|----------|
| 30-60 minutes (design) / 2-4 hours (implementation) | 4-8 hours per reporting cycle | Advanced | Analysts, Operations, Finance, RevOps |

---

## The Problem

Every week, month, or quarter, someone spends hours pulling data, formatting spreadsheets, creating charts, writing summaries, and emailing reports. The same work, repeated endlessly. Manual reporting is error-prone, time-consuming, and prevents talented people from doing higher-value work. But "automation" feels overwhelming—where do you even start?

**Pain Points:**
- Hours spent on repetitive report creation
- Manual data pulls prone to errors
- Inconsistent formatting across time periods
- Delayed reports due to dependencies
- Analysts stuck doing data assembly instead of analysis
- No time for ad-hoc analysis because of report burden
- Reports that nobody reads but everyone requires

---

## The Outcome

A comprehensive design document for automating your most time-consuming reports. Clear specification of data sources, transformations, outputs, and distribution. An implementation roadmap that any technical resource can execute. Freedom from manual reporting so analysts can do actual analysis.

**What You'll Have When Done:**
- Report requirements specification
- Data flow architecture
- Automation design document
- Implementation roadmap
- Template specifications
- Distribution and alerting design
- Maintenance plan

---

## When to Use This Recipe

**Good Fit:**
- Recurring reports (weekly, monthly, quarterly)
- Reports with stable structure
- Data from accessible systems (databases, APIs)
- Reports consuming >4 hours per cycle
- Multiple stakeholders receiving similar reports
- Standard metrics with defined calculations

**Not a Good Fit:**
- One-time analysis
- Highly variable ad-hoc reports
- Reports requiring subjective interpretation
- Data not yet in structured systems
- Reports that change structure frequently

---

## Before You Start: Quick Checklist

- [ ] Claude Code is installed and working
- [ ] You have a report that consumes significant time
- [ ] You understand the current manual process
- [ ] You have access to data source documentation
- [ ] You know who uses the report and how
- [ ] You have 60-90 minutes for comprehensive design

---

## How Claude Code Helps

**What Claude Code Does Well:**
- Structures automation requirements
- Identifies data dependencies
- Designs data flow architecture
- Creates implementation specifications
- Documents technical requirements
- Plans migration and rollout

**Where Human Judgment Is Essential:**
- Validating data source access
- Confirming calculation logic
- Setting priorities
- Assessing technical feasibility
- Approving final design
- Implementing the automation

---

## Input Examples

**Ideal Source Materials:**

| Input Type | Example | What Claude Uses It For |
|------------|---------|------------------------|
| Current report | Sample report output | Understanding requirements |
| Manual process | Steps to create report | Automation design |
| Data sources | Systems used | Architecture design |
| Audience | Who receives, how used | Distribution design |
| Pain points | What's hardest | Priority focus |

**Sample Input:**
```
Report Automation Design Request

REPORT NAME: Weekly Sales Performance Report
CURRENT TIME TO PRODUCE: 6 hours every Monday
FREQUENCY: Weekly (every Monday by 9 AM)
AUDIENCE: Sales leadership (5 people), Finance (2 people), CEO

CURRENT MANUAL PROCESS:

Step 1: Data Extraction (2 hours)
- Log into Salesforce, run Opportunity report for prior week
- Export to Excel
- Log into HubSpot, pull activity metrics
- Export to Excel
- Log into Stripe, download revenue data
- Export to Excel
- Log into Gong, pull call metrics
- Screenshot summary stats

Step 2: Data Processing (1.5 hours)
- Combine Salesforce and HubSpot data by Account
- Calculate win rates (Closed Won / Closed Won + Closed Lost)
- Calculate pipeline coverage (Pipeline / Target)
- Reconcile Stripe revenue to Salesforce closed amounts
- Calculate rep-level metrics
- Handle timezone conversions for different regions

Step 3: Report Assembly (1.5 hours)
- Update PowerPoint template with new numbers
- Update 8 charts with new data
- Write 1-page narrative summary
- Calculate week-over-week changes
- Highlight top/bottom performers
- Add commentary on major deals

Step 4: Distribution (1 hour)
- Export PowerPoint to PDF
- Create email with key highlights
- Send to distribution list
- Answer immediate follow-up questions
- Update Slack channel with summary

CURRENT REPORT SECTIONS:
1. Executive Summary (narrative + 5 KPIs)
2. Revenue Performance (charts + table)
3. Pipeline Health (funnel chart + metrics)
4. Activity Metrics (table by rep)
5. Deal Highlights (top 5 won/lost)
6. Rep Performance (scorecard)
7. Week-over-Week Comparison
8. Appendix: Detailed data tables

DATA SOURCES:
- Salesforce: CRM (Opportunities, Accounts, Activities)
- HubSpot: Marketing automation (Meetings, Emails, Calls)
- Stripe: Payments (Revenue, Subscriptions)
- Gong: Conversation intelligence (Calls, Talk time)

CURRENT PAIN POINTS:
- Monday mornings are wasted on manual work
- Data often has discrepancies I have to reconcile
- PowerPoint charts are tedious to update
- Same questions asked every week could be pre-answered
- Sometimes late because of upstream data issues
- No historical trend tracking—each week starts fresh

DESIRED IMPROVEMENTS:
- Reduce manual time to <1 hour
- Automated data refresh
- Interactive dashboard option
- Anomaly highlighting
- Historical comparisons built-in
- Email sent automatically

TECHNICAL CONTEXT:
- We have Fivetran for some data pipelines
- Snowflake data warehouse (some data loaded)
- Tableau license available but underused
- Limited engineering resources
- I know basic SQL but not Python

CONSTRAINTS:
- Budget for new tools is limited
- Need to maintain current report format initially
- CEO likes the PowerPoint format for board meetings
- Must have PDF version for email
```

---

## Step-by-Step Implementation

### Step 1: Document Current Process
**Time: 15-20 minutes**

Capture:
- Every step in current report creation
- Time spent on each step
- Data sources and access methods
- Pain points and failure modes
- Output format and distribution

---

### Step 2: Launch Claude Code
**Time: 30 seconds**

```bash
claude
```

---

### Step 3: Run the Automation Design Prompt
**Time: 10-15 minutes for Claude to process**

---

**PRIMARY PROMPT: Report Automation Design**

```
Please design an automation solution for this recurring report.

REPORT NAME: [Name]
FREQUENCY: [How often]
CURRENT TIME: [Hours spent]
AUDIENCE: [Who receives it]

CURRENT MANUAL PROCESS:
[Describe each step and time]

REPORT SECTIONS:
[What the report contains]

DATA SOURCES:
[Systems and data used]

CURRENT PAIN POINTS:
[What's hardest/most error-prone]

DESIRED IMPROVEMENTS:
[What better looks like]

TECHNICAL CONTEXT:
[Available tools, skills, constraints]

DESIGN REQUIREMENTS:

1. EXECUTIVE SUMMARY
   - Current state assessment
   - Recommended automation approach
   - Expected time savings
   - Implementation complexity
   - Key dependencies

2. REQUIREMENTS SPECIFICATION

   **Functional Requirements:**
   | Requirement | Priority | Current | Automated |
   |-------------|----------|---------|-----------|
   [List each capability]

   **Non-Functional Requirements:**
   - Performance: [Speed expectations]
   - Reliability: [Uptime needs]
   - Flexibility: [Change tolerance]
   - Maintainability: [Update ease]

3. DATA ARCHITECTURE

   **Source Systems:**
   | System | Data | Current Access | Automated Access |
   |--------|------|----------------|------------------|
   [Each data source]

   **Data Flow Diagram:**
   [Source] → [Staging] → [Transformation] → [Output]

   **Data Transformations:**
   | Transform | Input | Logic | Output |
   |-----------|-------|-------|--------|
   [Each calculation]

   **Data Quality Rules:**
   - [Validation 1]
   - [Validation 2]

4. AUTOMATION ARCHITECTURE

   **Recommended Stack:**
   | Component | Tool | Why |
   |-----------|------|-----|
   | Data extraction | [Tool] | [Rationale] |
   | Transformation | [Tool] | [Rationale] |
   | Visualization | [Tool] | [Rationale] |
   | Distribution | [Tool] | [Rationale] |

   **Architecture Diagram:**
   [Visual representation of components]

   **Alternative Options:**
   | Option | Pros | Cons | When to Choose |
   |--------|------|------|---------------|

5. OUTPUT SPECIFICATIONS

   **Report Format:**
   | Section | Content | Data Source | Update Frequency |
   |---------|---------|-------------|------------------|
   [Each section]

   **Template Design:**
   [Specification for automated template]

   **Distribution Channels:**
   | Channel | Audience | Format | Timing |
   |---------|----------|--------|--------|
   [Each distribution method]

6. IMPLEMENTATION ROADMAP

   **Phase 1: Foundation**
   Duration: [X weeks]
   - [Task 1]
   - [Task 2]
   Milestone: [What's delivered]

   **Phase 2: Automation**
   Duration: [X weeks]
   - [Task 1]
   - [Task 2]
   Milestone: [What's delivered]

   **Phase 3: Enhancement**
   Duration: [X weeks]
   - [Task 1]
   - [Task 2]
   Milestone: [What's delivered]

   **Resource Requirements:**
   | Role | Time | Skills Needed |
   |------|------|---------------|

7. METRICS DEFINITIONS

   **Calculations:**
   | Metric | Formula | Source Fields | Notes |
   |--------|---------|---------------|-------|
   [Each KPI with precise calculation]

8. ALERTING AND MONITORING

   **Automated Alerts:**
   | Condition | Threshold | Action | Recipient |
   |-----------|-----------|--------|-----------|
   [Each alert rule]

   **Data Quality Monitoring:**
   - [Check 1]
   - [Check 2]

   **Process Monitoring:**
   - [Job success/failure alerts]
   - [Latency monitoring]

9. EXCEPTION HANDLING

   **Common Issues:**
   | Issue | Detection | Resolution | Escalation |
   |-------|-----------|------------|------------|
   [Known failure modes]

   **Manual Override Process:**
   [How to intervene when automation fails]

10. MAINTENANCE PLAN

    **Ongoing Tasks:**
    | Task | Frequency | Time | Owner |
    |------|-----------|------|-------|
    [Maintenance activities]

    **Change Management:**
    - Adding new metrics: [Process]
    - Modifying calculations: [Process]
    - Adding recipients: [Process]

11. MIGRATION PLAN

    **Parallel Run Period:**
    - Duration: [X weeks]
    - Comparison process: [How to validate]
    - Go/no-go criteria: [What determines success]

    **Cutover Plan:**
    - [Step-by-step transition]

    **Rollback Plan:**
    - [How to revert if needed]

12. COST-BENEFIT ANALYSIS

    **Costs:**
    | Item | One-Time | Recurring |
    |------|----------|-----------|
    [Implementation and ongoing costs]

    **Benefits:**
    | Benefit | Quantified Value |
    |---------|------------------|
    [Time savings, accuracy improvements]

    **Payback Period:** [X months]

Provide specific, actionable design that can be implemented.
```

---

### Step 4: Refine Technical Design
**Time: 10-15 minutes**

```
Refine the automation design with these specifics:

DATA SOURCE DETAILS:
- Salesforce API: [Specific objects and fields needed]
- HubSpot API: [Available integrations]
- Snowflake: [Existing tables]

TECHNICAL CONSTRAINTS:
- [Constraint 1]: Must use [specific tool]
- [Constraint 2]: Cannot use [tool] because [reason]

ADDITIONAL REQUIREMENTS:
- Must preserve: [Specific format element]
- Must add: [New capability]
```

---

### Step 5: Create Implementation Artifacts
**Time: 10 minutes**

```
Create implementation-ready artifacts:

1. SQL QUERIES
   For each data pull, provide:
   - Query template
   - Parameters needed
   - Expected output schema

2. METRIC FORMULAS
   Precise calculation for each metric:
   - Numerator definition
   - Denominator definition
   - Edge case handling
   - Rounding rules

3. TEMPLATE SPECIFICATION
   For each report section:
   - Data fields needed
   - Formatting rules
   - Conditional logic

4. DISTRIBUTION SCRIPT
   Email/notification template:
   - Subject line format
   - Body content
   - Attachment handling
```

---

### Step 6: Generate Final Documentation
**Time: 5 minutes**

```
Create final deliverable package:

1. DESIGN DOCUMENT
   Complete automation design specification

2. TECHNICAL SPECIFICATION
   Detailed implementation requirements

3. IMPLEMENTATION CHECKLIST
   Step-by-step tasks with dependencies

4. USER DOCUMENTATION
   How to interact with automated system

5. HANDOFF BRIEF
   Summary for engineering/implementation team
```

---

## Example Output

Below is an abbreviated report automation design example:

---

> **REPORT AUTOMATION DESIGN**
>
> **Weekly Sales Performance Report**
>
> ---
>
> ## Executive Summary
>
> **Current State:** The Weekly Sales Performance Report requires 6 hours of manual work every Monday, involving 4 data sources, complex reconciliation, and manual chart updates. This is unsustainable and prevents the analyst from higher-value work.
>
> **Recommended Approach:** Implement a three-phase automation using existing tools (Fivetran, Snowflake, Tableau) with automated email distribution.
>
> **Expected Time Savings:** Reduce from 6 hours to 30 minutes (review and commentary only). 92% time reduction.
>
> **Implementation Complexity:** Medium. Data pipelines need setup; visualization is straightforward; distribution is simple.
>
> **Key Dependencies:** Salesforce API access, HubSpot integration, Stripe data in Snowflake, engineering support for Fivetran setup.
>
> ---
>
> ## Data Architecture
>
> ### Source Systems
>
> | System | Data Needed | Current Access | Automated Access |
> |--------|-------------|----------------|------------------|
> | Salesforce | Opportunities, Activities | Manual export | Fivetran connector |
> | HubSpot | Meetings, Emails, Calls | Manual export | Fivetran connector |
> | Stripe | Revenue, Subscriptions | Manual export | Fivetran connector |
> | Gong | Call metrics | Screenshot | API (phase 2) |
>
> ### Data Flow
>
> ```
> Source Systems → Fivetran → Snowflake (Raw) → dbt (Transform) →
> Snowflake (Analytics) → Tableau → Email Distribution
> ```
>
> ### Data Transformations
>
> | Transform | Input | Logic | Output |
> |-----------|-------|-------|--------|
> | Win Rate | Closed Won, Closed Lost | Won / (Won + Lost) | Percentage |
> | Pipeline Coverage | Open Pipeline, Target | Pipeline / Target | Ratio |
> | Revenue Reconciliation | Stripe, Salesforce | Match by Account, flag deltas | Reconciled revenue |
> | Rep Scorecard | Activities, Opportunities | Weighted metrics | Score (0-100) |
>
> ---
>
> ## Automation Architecture
>
> ### Recommended Stack
>
> | Component | Tool | Why |
> |-----------|------|-----|
> | Data Extraction | Fivetran | Already licensed, connectors exist |
> | Data Warehouse | Snowflake | Already in use, scalable |
> | Transformation | dbt | SQL-based, version controlled |
> | Visualization | Tableau | Licensed, existing skills |
> | Distribution | Tableau + SendGrid | Automated PDF and email |
>
> ### Architecture Diagram
>
> ```
> ┌─────────────┐    ┌─────────────┐    ┌─────────────┐
> │ Salesforce  │    │  HubSpot    │    │   Stripe    │
> └──────┬──────┘    └──────┬──────┘    └──────┬──────┘
>        │                  │                  │
>        └──────────────────┼──────────────────┘
>                           │
>                    ┌──────▼──────┐
>                    │   Fivetran   │  (Extract)
>                    └──────┬──────┘
>                           │
>                    ┌──────▼──────┐
>                    │  Snowflake   │  (Raw)
>                    └──────┬──────┘
>                           │
>                    ┌──────▼──────┐
>                    │     dbt      │  (Transform)
>                    └──────┬──────┘
>                           │
>                    ┌──────▼──────┐
>                    │  Snowflake   │  (Analytics)
>                    └──────┬──────┘
>                           │
>                    ┌──────▼──────┐
>                    │   Tableau    │  (Visualize)
>                    └──────┬──────┘
>                           │
>        ┌──────────────────┼──────────────────┐
>        │                  │                  │
> ┌──────▼──────┐    ┌──────▼──────┐    ┌──────▼──────┐
> │  Dashboard  │    │ PDF Export  │    │   Email     │
> │(Interactive)│    │(PowerPoint) │    │ (SendGrid)  │
> └─────────────┘    └─────────────┘    └─────────────┘
> ```
>
> ---
>
> ## Output Specifications
>
> ### Report Sections
>
> | Section | Content | Data Source | Refresh |
> |---------|---------|-------------|---------|
> | Executive Summary | 5 KPIs + narrative placeholder | analytics.weekly_summary | Daily |
> | Revenue Performance | Chart + table | analytics.revenue_weekly | Daily |
> | Pipeline Health | Funnel + metrics | analytics.pipeline_health | Daily |
> | Activity Metrics | Rep activity table | analytics.rep_activities | Daily |
> | Deal Highlights | Top 5 won/lost | analytics.deal_highlights | Daily |
> | Rep Performance | Scorecard | analytics.rep_scorecard | Daily |
> | WoW Comparison | Delta calculations | analytics.wow_comparison | Daily |
> | Appendix | Raw data tables | analytics.detailed_data | Daily |
>
> ### Distribution Channels
>
> | Channel | Audience | Format | Timing |
> |---------|----------|--------|--------|
> | Tableau Dashboard | All users | Interactive | Always available |
> | Email (PDF) | Leadership | PDF attachment | Monday 8 AM |
> | Slack | Sales team | Key metrics summary | Monday 8 AM |
> | PowerPoint | CEO | .pptx via email | Monday 8 AM |
>
> ---
>
> ## Implementation Roadmap
>
> ### Phase 1: Data Foundation (Weeks 1-2)
>
> **Week 1:**
> - [ ] Set up Fivetran Salesforce connector
> - [ ] Set up Fivetran HubSpot connector
> - [ ] Verify Stripe data already in Snowflake
> - [ ] Create Snowflake raw schema for new sources
>
> **Week 2:**
> - [ ] Initial data sync and validation
> - [ ] Compare to manual exports for accuracy
> - [ ] Document field mappings
>
> **Milestone:** All source data flowing to Snowflake daily.
>
> ### Phase 2: Transformation Layer (Weeks 3-4)
>
> **Week 3:**
> - [ ] Create dbt project structure
> - [ ] Build staging models (raw → cleaned)
> - [ ] Build metric calculation models
> - [ ] Implement data quality tests
>
> **Week 4:**
> - [ ] Build final analytics tables
> - [ ] Validate calculations against manual report
> - [ ] Set up dbt scheduling (daily 5 AM)
>
> **Milestone:** Automated daily data refresh with validated metrics.
>
> ### Phase 3: Visualization & Distribution (Weeks 5-6)
>
> **Week 5:**
> - [ ] Build Tableau dashboard
> - [ ] Match existing report sections
> - [ ] Add interactive filters
> - [ ] Create PDF export template
>
> **Week 6:**
> - [ ] Set up Tableau subscriptions
> - [ ] Configure email distribution
> - [ ] Build PowerPoint export (via Slides → PPTX)
> - [ ] Test end-to-end automation
>
> **Milestone:** Full automation running in parallel with manual process.
>
> ### Phase 4: Validation & Cutover (Weeks 7-8)
>
> **Week 7:**
> - [ ] Parallel run: automated vs manual comparison
> - [ ] Document discrepancies
> - [ ] Fix issues found
> - [ ] Gather user feedback
>
> **Week 8:**
> - [ ] Final validation
> - [ ] Cutover to automated report
> - [ ] Retire manual process
> - [ ] Document runbooks
>
> **Milestone:** Fully automated report in production.
>
> ---
>
> ## Metrics Definitions
>
> | Metric | Formula | Source Fields | Edge Cases |
> |--------|---------|---------------|------------|
> | Win Rate | COUNT(Stage='Closed Won') / COUNT(Stage IN ('Closed Won','Closed Lost')) | opportunity.stage_name | Exclude if no closed deals |
> | Pipeline Coverage | SUM(Amount WHERE Stage NOT IN ('Closed Won','Closed Lost','Qualified Out')) / quarterly_target | opportunity.amount, targets.quarterly_target | Handle $0 target (null coverage) |
> | Rep Activity Score | (0.3 × calls) + (0.3 × emails) + (0.4 × meetings) normalized to 100 | hubspot.activities | Min 0, Max 100 |
> | Revenue (Recognized) | SUM(Stripe.amount WHERE status='paid' AND period=current_week) | stripe.charges | Exclude refunds |
> | WoW Change | (current_week_value - prior_week_value) / prior_week_value | Calculated | Handle divide by zero (null if prior=0) |
>
> ---
>
> ## Alerting and Monitoring
>
> ### Automated Alerts
>
> | Condition | Threshold | Action | Recipient |
> |-----------|-----------|--------|-----------|
> | Data refresh failure | Job fails | PagerDuty alert | Data team |
> | Data freshness | >6 hours stale | Email alert | Analyst |
> | Win rate anomaly | >30% change WoW | Flag in report | Sales leadership |
> | Pipeline coverage | <2.0x | Highlight red | Sales leadership |
>
> ### Data Quality Monitoring
>
> - **Row count checks:** Compare to expected range
> - **Null checks:** Key fields must not be null
> - **Referential integrity:** All opportunities have accounts
> - **Freshness:** Data must be <24 hours old
>
> ---
>
> ## Cost-Benefit Analysis
>
> ### Costs
>
> | Item | One-Time | Annual Recurring |
> |------|----------|------------------|
> | Fivetran setup (2 connectors) | $0 (included) | $2,400 |
> | dbt Cloud (Team plan) | $0 | $1,200 |
> | Engineering time (40 hours) | $6,000 | $0 |
> | Analyst time (20 hours) | $1,500 | $0 |
> | **Total** | **$7,500** | **$3,600** |
>
> ### Benefits
>
> | Benefit | Quantified Value |
> |---------|------------------|
> | Analyst time saved (5.5 hrs × 52 weeks × $75/hr) | $21,450/year |
> | Error reduction (estimated 10 hrs rework/year) | $750/year |
> | Faster decisions (qualitative) | Significant |
> | **Total Annual Benefit** | **$22,200** |
>
> ### Payback Period
>
> ($7,500 + $3,600) / $22,200 = **5 months**
>
> ---
>
> ## Migration Plan
>
> ### Parallel Run Period
>
> **Duration:** 4 weeks (Weeks 7-10)
>
> **Process:**
> 1. Generate automated report on Friday
> 2. Generate manual report on Monday
> 3. Compare all metrics (must match within 1%)
> 4. Document any discrepancies
> 5. Fix and re-test
>
> **Go/No-Go Criteria:**
> - All metrics match within 1% for 3 consecutive weeks
> - No data refresh failures in 2 weeks
> - Positive user feedback from 2+ stakeholders
>
> ### Cutover Steps
>
> 1. Final parallel validation
> 2. Send announcement to stakeholders
> 3. Enable automated distribution
> 4. Disable manual calendar reminders
> 5. Monitor first automated delivery
> 6. Confirm receipt with stakeholders
>
> ### Rollback Plan
>
> If automated report fails:
> 1. Immediately generate manual report
> 2. Investigate root cause
> 3. Fix and validate
> 4. Resume automation

---

## Troubleshooting Common Issues

| Problem | Likely Cause | Solution |
|---------|--------------|----------|
| Design too high-level | Missing technical details | Ask: "Provide specific field names, SQL logic, and tool configurations" |
| Missing edge cases | Happy path only | Ask: "What happens when data is missing, late, or incorrect? Design exception handling." |
| Unrealistic timeline | Underestimated complexity | Ask: "Add buffer time. What typically goes wrong in implementations like this?" |
| Tools don't match context | Generic recommendations | Provide: Specific tools available, constraints, technical skills |
| No migration plan | Focus on end state | Ask: "How do we get from current to future state without disruption?" |

---

## Tips from Experience

1. **Start with the hardest data source.** If Salesforce is the pain point, solve that first.

2. **Automate 80%, perfect later.** A mostly-automated report that works beats a perfect design that never ships.

3. **Keep the manual escape hatch.** Always have a way to intervene when automation fails.

4. **Validate obsessively.** Automated wrong is worse than manual correct.

5. **Design for maintenance.** The person maintaining this may not be the person building it.

6. **Don't automate bad processes.** If the current report is flawed, fix the logic before automating it.

---

## Measuring Success

**You've succeeded with this recipe when:**
- [ ] Automation design is complete and implementable
- [ ] Stakeholders approve the approach
- [ ] Implementation begins without major rework
- [ ] Parallel run validates accuracy
- [ ] Cutover happens on schedule
- [ ] Time savings are realized

**Track over time:**
- Time spent on report (target: <30 min for review)
- Data accuracy (match to source systems)
- On-time delivery rate (target: 100%)
- User satisfaction with report quality
- Maintenance burden (hours per month)

---

## Variations

### Dashboard Automation
For interactive dashboards:
```
Design dashboard automation with:
- Real-time data refresh requirements
- Interactive filter design
- Drill-down capabilities
- Mobile responsiveness
- Embedding requirements
- Performance optimization

Focus on: User interaction patterns, self-service capabilities
```

### Financial Report Automation
For accounting and finance:
```
Design financial report automation with:
- Audit trail requirements
- Approval workflows
- Period-close dependencies
- Multi-currency handling
- GAAP compliance checks
- Reconciliation automation

Focus on: Controls, accuracy, auditability
```

### Executive Briefing Automation
For leadership reports:
```
Design executive briefing automation:
- Exception-based reporting (only show anomalies)
- Commentary automation using AI
- Comparison to targets and forecasts
- Action item tracking
- Board-ready formatting

Focus on: Narrative generation, insight highlighting
```

### Operational Metrics Automation
For ops and support teams:
```
Design operational dashboard automation:
- Near-real-time refresh (hourly or less)
- Alerting and escalation
- SLA monitoring
- Trend visualization
- Capacity forecasting

Focus on: Speed, alerting, operational response
```

---

## Building Your Repeatable System

After successful automation, create:

1. **Automation catalog** of all automated reports
2. **Standard architecture patterns** for future reports
3. **Runbook templates** for operations
4. **Onboarding documentation** for new team members
5. **Maintenance schedule** and owners

**Sample Setup:**
```
report-automation/
├── designs/
│   ├── weekly-sales-automation.md
│   ├── monthly-finance-automation.md
│   └── [report designs]
├── implementations/
│   ├── dbt-models/
│   ├── tableau-workbooks/
│   └── distribution-scripts/
├── runbooks/
│   ├── weekly-sales-runbook.md
│   └── troubleshooting-guide.md
├── monitoring/
│   ├── alerting-rules.yaml
│   └── sla-definitions.md
└── documentation/
    ├── user-guide.md
    └── architecture-overview.md
```

---

## How This Pattern Applies Elsewhere

This recipe's core pattern—**document current state → design automation → plan implementation → migrate safely**—applies broadly:

| Role | Application |
|------|-------------|
| **Finance** | Month-end close, financial statements |
| **Operations** | Operational dashboards, SLA reports |
| **Sales** | Pipeline reports, forecasting |
| **Marketing** | Campaign performance, attribution |
| **HR** | Headcount, hiring, engagement |
| **Customer Success** | Health scores, renewal tracking |

---

## Next Steps

1. **Identify report:** Which recurring report consumes most time?
2. **Document process:** How is it created today?
3. **Assess tools:** What automation capabilities exist?
4. **Design solution:** Use this recipe
5. **Get buy-in:** Present design to stakeholders
6. **Implement:** Execute the roadmap

---

*Recipe #58 of 100 in the Claude Code Knowledge Worker Recipe Collection*

---

**Related tooling:** when a report pipeline grows past one person, [orchestra-lite](https://github.com/sgharlow/orchestra-lite) runs the parallel-agent version of this workflow, and [ai-pr-bot](https://github.com/sgharlow/ai-pr-bot) enforces the checks at PR time.
