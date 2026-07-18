# Data Quality Assessment

**Recipe #59: Find and Fix the Data Problems Before They Find You**

---

| Setup Time | Time Saved | Difficulty | Best For |
|------------|------------|------------|----------|
| 5 minutes (first time) / 2 minutes (repeat) | 2-4 hours per assessment | Intermediate | Analysts, Data Teams, Operations, Finance |

---

## The Problem

Bad data leads to bad decisions. Missing values corrupt reports. Duplicate records inflate metrics. Inconsistent formats break automations. Data quality problems are discovered at the worst times—during board presentations, customer calls, or audit reviews. By then, credibility is damaged and fixing the data is urgent and expensive. What's needed is proactive assessment to find problems before they cause harm.

**Pain Points:**
- Data quality issues discovered during critical moments
- No systematic way to assess data health
- Duplicate records inflating counts and revenue
- Missing data causing incorrect calculations
- Inconsistent formats breaking reports
- No documentation of known data issues
- Finger-pointing when problems surface

---

## The Outcome

A structured data quality assessment that identifies issues before they cause problems. Documentation of data health across dimensions: completeness, accuracy, consistency, timeliness, and uniqueness. Prioritized remediation plan based on business impact. Confidence in data reliability.

**What You'll Have When Done:**
- Data quality scorecard
- Issue inventory with severity ratings
- Root cause analysis
- Remediation roadmap
- Monitoring recommendations
- Business impact assessment
- Stakeholder communication

---

## When to Use This Recipe

**Good Fit:**
- Before major reporting cycles
- During system migrations
- After data integration projects
- Quarterly data health reviews
- Pre-audit preparation
- When trust in data is low
- Before automation implementation

**Not a Good Fit:**
- Real-time data monitoring (need different tools)
- Deep statistical analysis (need specialized expertise)
- Data governance policy creation (different scope)
- Small, simple datasets

---

## Before You Start: Quick Checklist

- [ ] Claude Code is installed and working
- [ ] You have access to the data you want to assess
- [ ] You can run queries or export data samples
- [ ] You understand the business context and use cases
- [ ] You have 45-90 minutes for comprehensive assessment

---

## How Claude Code Helps

**What Claude Code Does Well:**
- Structures assessment frameworks
- Identifies quality dimensions to check
- Creates validation rule templates
- Documents findings clearly
- Prioritizes issues by impact
- Generates remediation plans

**Where Human Judgment Is Essential:**
- Running actual data queries
- Validating findings against source systems
- Understanding business context
- Prioritizing remediation efforts
- Approving action plans
- Implementing fixes

---

## Input Examples

**Ideal Source Materials:**

| Input Type | Example | What Claude Uses It For |
|------------|---------|------------------------|
| Data profile | Row counts, field distributions | Completeness assessment |
| Sample records | Representative data rows | Pattern analysis |
| Business rules | How data should look | Validation criteria |
| Known issues | Current problems | Issue inventory |
| Use cases | How data is used | Impact assessment |

**Sample Input:**
```
Data Quality Assessment Request

DATASET: Customer Master Table
SYSTEM: Salesforce + Data Warehouse (Snowflake)
RECORDS: 45,287 customer records
LAST UPDATED: November 15, 2024
CRITICALITY: High (used for revenue reporting, customer communications, billing)

DATA PROFILE SUMMARY:

Field-Level Statistics:
| Field | Completeness | Unique Values | Sample Values |
|-------|--------------|---------------|---------------|
| customer_id | 100% | 45,287 | CUST-001, CUST-002 |
| company_name | 99.2% | 44,892 | Acme Corp, TechStart Inc |
| email | 94.5% | 38,421 | john@acme.com, NULL |
| phone | 78.3% | 32,456 | +1-555-1234, 555.123.4567 |
| address_line1 | 85.2% | 38,234 | 123 Main St, PO Box 45 |
| city | 84.8% | 12,345 | New York, new york, NYC |
| state | 83.1% | 847 | CA, California, calif |
| zip_code | 82.4% | 15,678 | 94105, 94105-1234, 9410 |
| country | 91.2% | 89 | USA, US, United States |
| created_date | 100% | 2,456 | 2020-01-15, 2024-11-10 |
| account_owner | 97.8% | 145 | Sarah Chen, UNKNOWN |
| industry | 72.4% | 234 | Technology, Tech, Software |
| annual_revenue | 65.3% | 8,456 | 1000000, $1M, NULL |
| employee_count | 58.7% | 423 | 150, 150-200, ~150 |
| customer_status | 100% | 5 | Active, Inactive, Churned |
| contract_value | 88.4% | 12,345 | 50000, $50,000, 50k |

DUPLICATE ANALYSIS:
- Potential duplicate company names: 1,234 (2.7%)
- Potential duplicate emails: 456 (1.0%)
- Records with same company name + city: 892

KNOWN ISSUES:
- Phone numbers have inconsistent formatting
- State field has abbreviations and full names mixed
- Some annual_revenue values are estimates in different formats
- Industry field has many variations of the same values
- ~500 "test" or "demo" accounts in production data

DATA USAGE:
- Revenue reporting: customer_status, contract_value
- Marketing campaigns: email, industry, annual_revenue
- Sales territory assignment: state, city
- Customer success: account_owner, contract_value
- Billing: All contact fields

RECENT PROBLEMS:
- Marketing email bounced to 2,400 addresses (invalid emails)
- Revenue report was $340K off due to duplicate customers
- Sales territories had gaps due to inconsistent state values
- Customer success couldn't identify account owners for 1,200 accounts

TOLERANCE LEVELS:
- Revenue-impacting fields: Must be >98% accurate
- Communication fields: Must be >95% accurate
- Operational fields: >90% acceptable
```

---

## Step-by-Step Implementation

### Step 1: Profile Your Data
**Time: 15-20 minutes**

Run basic profiling:
- Row counts
- Null percentages by field
- Unique value counts
- Sample values
- Distribution patterns

---

### Step 2: Launch Claude Code
**Time: 30 seconds**

```bash
claude
```

---

### Step 3: Run the Data Quality Assessment Prompt
**Time: 5-10 minutes for Claude to process**

---

**PRIMARY PROMPT: Data Quality Assessment**

```
Please conduct a data quality assessment for this dataset.

DATASET: [Name]
SYSTEM: [Source system(s)]
RECORDS: [Count]
CRITICALITY: [High/Medium/Low] - [Why it matters]

DATA PROFILE:
[Paste field-level statistics]

DUPLICATE ANALYSIS:
[Paste duplicate findings]

KNOWN ISSUES:
[Current problems]

DATA USAGE:
[How this data is used]

RECENT PROBLEMS:
[Issues that have occurred]

TOLERANCE LEVELS:
[Acceptable quality thresholds]

ASSESSMENT REQUIREMENTS:

1. EXECUTIVE SUMMARY
   - Overall data quality score (1-100)
   - Most critical issue
   - Business risk level
   - Recommended priority actions
   - Timeline urgency

2. QUALITY DIMENSION ANALYSIS

   For each dimension, assess:

   **COMPLETENESS**
   Missing data analysis:
   | Field | Completeness | Target | Gap | Impact | Priority |
   |-------|--------------|--------|-----|--------|----------|

   Key findings:
   - [Finding 1]

   **ACCURACY**
   Data correctness assessment:
   | Field | Likely Accuracy | Evidence | Impact | Priority |
   |-------|-----------------|----------|--------|----------|

   Key findings:
   - [Finding 1]

   **CONSISTENCY**
   Format and standard conformance:
   | Field | Issue | Examples | Records Affected | Priority |
   |-------|-------|----------|------------------|----------|

   Key findings:
   - [Finding 1]

   **UNIQUENESS**
   Duplicate analysis:
   | Duplicate Type | Count | % of Total | Impact | Priority |
   |----------------|-------|------------|--------|----------|

   Key findings:
   - [Finding 1]

   **TIMELINESS**
   Data freshness assessment:
   - Last update: [Date]
   - Update frequency: [Actual vs expected]
   - Stale data risk: [Assessment]

   **VALIDITY**
   Business rule conformance:
   | Rule | Field(s) | Violations | % | Impact |
   |------|----------|------------|---|--------|

3. ISSUE INVENTORY

   **Critical Issues (must fix immediately):**
   | Issue | Field(s) | Records | Business Impact | Root Cause |
   |-------|----------|---------|-----------------|------------|

   **High Priority (fix within 30 days):**
   | Issue | Field(s) | Records | Business Impact | Root Cause |
   |-------|----------|---------|-----------------|------------|

   **Medium Priority (fix within 90 days):**
   | Issue | Field(s) | Records | Business Impact | Root Cause |
   |-------|----------|---------|-----------------|------------|

   **Low Priority (monitor):**
   | Issue | Field(s) | Records | Business Impact | Root Cause |
   |-------|----------|---------|-----------------|------------|

4. ROOT CAUSE ANALYSIS

   For each critical issue:

   **Issue: [Name]**
   - Symptom: [What we see]
   - Root cause: [Why it's happening]
   - Contributing factors: [What makes it worse]
   - Prevention: [How to stop it from recurring]

5. BUSINESS IMPACT ASSESSMENT

   | Issue | Affected Process | Impact Type | Quantified Impact |
   |-------|------------------|-------------|-------------------|

   Total estimated impact:
   - Revenue at risk: $[X]
   - Operational cost: $[X]
   - Reputation risk: [Assessment]

6. DATA QUALITY SCORECARD

   | Dimension | Score | Target | Gap | Trend |
   |-----------|-------|--------|-----|-------|
   | Completeness | X/100 | 95 | | |
   | Accuracy | X/100 | 98 | | |
   | Consistency | X/100 | 95 | | |
   | Uniqueness | X/100 | 99 | | |
   | Timeliness | X/100 | 95 | | |
   | Validity | X/100 | 98 | | |
   | **Overall** | X/100 | 95 | | |

7. REMEDIATION ROADMAP

   **Phase 1: Critical Fixes (Week 1-2)**
   | Action | Issue Addressed | Owner | Effort |
   |--------|-----------------|-------|--------|

   **Phase 2: High Priority (Month 1)**
   | Action | Issue Addressed | Owner | Effort |
   |--------|-----------------|-------|--------|

   **Phase 3: Ongoing Improvement (Quarter 1)**
   | Action | Issue Addressed | Owner | Effort |
   |--------|-----------------|-------|--------|

8. VALIDATION RULES

   Recommended data quality rules to implement:

   | Rule Name | Logic | Field(s) | Alert Threshold |
   |-----------|-------|----------|-----------------|

9. MONITORING RECOMMENDATIONS

   **Metrics to Track:**
   | Metric | Current | Target | Frequency |
   |--------|---------|--------|-----------|

   **Alerts to Configure:**
   | Alert | Trigger | Action |
   |-------|---------|--------|

10. QUICK WINS

    Low-effort, high-impact fixes:
    1. [Quick win 1] — [Impact] — [Effort]
    2. [Quick win 2] — [Impact] — [Effort]

11. STAKEHOLDER COMMUNICATION

    **For Leadership:**
    [Summary of risk and required investment]

    **For Data Team:**
    [Technical findings and remediation steps]

    **For Business Users:**
    [Impact on their processes and workarounds]

Be specific about issues found. Quantify impact where possible.
```

---

### Step 4: Validate Findings
**Time: 15-20 minutes**

Verify identified issues:
- Run queries to confirm problem counts
- Check sample records for accuracy
- Validate root cause hypotheses
- Confirm business impact estimates

---

### Step 5: Refine Assessment
**Time: 5-10 minutes**

```
Update the assessment with these validated findings:

CONFIRMED ISSUES:
- [Issue X] confirmed: Actual count is [X]
- [Issue Y] not as severe: Only [X] records affected

ADDITIONAL CONTEXT:
- [Issue X] is caused by: [Root cause found]
- Business impact is higher because: [Reason]

CONSTRAINTS:
- Cannot fix [X] because: [Reason]
- Must prioritize [Y] because: [Business driver]
```

---

### Step 6: Generate Action Plan
**Time: 5 minutes**

```
Create final deliverable package:

1. DATA QUALITY ASSESSMENT REPORT
   Complete assessment with all findings

2. EXECUTIVE SUMMARY (1 page)
   - Overall health score
   - Critical issues (3-5)
   - Business impact
   - Recommended investment
   - Timeline

3. REMEDIATION TRACKER
   | Issue | Priority | Owner | Action | Due | Status |
   [Actionable task list]

4. VALIDATION RULES SPECIFICATION
   Technical specification for data quality rules to implement

5. COMMUNICATION TEMPLATES
   Email templates for different stakeholders
```

---

## Example Output

Below is an abbreviated data quality assessment example:

---

> **DATA QUALITY ASSESSMENT**
>
> **Customer Master Table | November 2024**
>
> ---
>
> ## Executive Summary
>
> **Overall Data Quality Score: 68/100** (Poor - Requires Urgent Attention)
>
> The Customer Master has significant quality issues across multiple dimensions. Revenue reporting is at risk due to duplicates, marketing campaigns are ineffective due to invalid emails, and operational processes are impaired by inconsistent formatting.
>
> **Most Critical Issue:** 1,234 duplicate customer records are inflating revenue by an estimated $340K and causing double-counting across all downstream reports.
>
> **Business Risk Level:** HIGH
>
> **Recommended Priority Actions:**
> 1. Deduplicate customer records (Week 1)
> 2. Validate and cleanse email addresses (Week 2)
> 3. Standardize state/country values (Week 3)
> 4. Implement data quality rules to prevent recurrence (Month 1)
>
> **Timeline Urgency:** Critical fixes needed before month-end close.
>
> ---
>
> ## Quality Dimension Analysis
>
> ### COMPLETENESS
>
> | Field | Completeness | Target | Gap | Impact | Priority |
> |-------|--------------|--------|-----|--------|----------|
> | email | 94.5% | 98% | -3.5% | Marketing reach | High |
> | phone | 78.3% | 90% | -11.7% | Sales outreach | Medium |
> | annual_revenue | 65.3% | 85% | -19.7% | Segmentation | Medium |
> | employee_count | 58.7% | 80% | -21.3% | Segmentation | Low |
> | industry | 72.4% | 90% | -17.6% | Targeting | High |
>
> **Key Findings:**
> - 2,478 customers (5.5%) have no email, blocking marketing communication
> - Annual revenue missing for 34.7% prevents proper segmentation
> - Phone completeness (78%) is acceptable for B2B but limits outreach
>
> ---
>
> ### ACCURACY
>
> | Field | Likely Accuracy | Evidence | Impact | Priority |
> |-------|-----------------|----------|--------|----------|
> | email | ~92% | 2,400 bounces (5.3%) | Campaign waste | Critical |
> | contract_value | ~95% | Reconciliation gaps | Revenue accuracy | High |
> | annual_revenue | ~70% | Mixed formats, estimates | Segmentation errors | Medium |
> | account_owner | ~98% | UNKNOWN values (2.2%) | Routing failures | High |
>
> **Key Findings:**
> - Email bounce rate of 5.3% indicates ~2,400 invalid email addresses
> - Contract values have format inconsistencies (50000 vs $50,000 vs 50k) suggesting some values may be misinterpreted
> - Annual revenue has "~" and ranges suggesting low confidence estimates
>
> ---
>
> ### CONSISTENCY
>
> | Field | Issue | Examples | Records Affected | Priority |
> |-------|-------|----------|------------------|----------|
> | state | Mixed formats | CA, California, calif | 7,621 (16.8%) | High |
> | country | Mixed formats | USA, US, United States | 3,982 (8.8%) | High |
> | phone | No standard format | +1-555-1234, 555.123.4567 | 35,456 (78%) | Medium |
> | city | Case inconsistency | New York, new york, NYC | 5,234 (11.6%) | Medium |
> | industry | Duplicate values | Technology, Tech, Software | 12,456 (27.5%) | High |
>
> **Key Findings:**
> - State field has 847 unique values when only 50 US states + territories exist
> - Industry field has 234 unique values but likely represents <50 true industries
> - Phone inconsistency doesn't break usage but complicates analysis
>
> ---
>
> ### UNIQUENESS
>
> | Duplicate Type | Count | % of Total | Impact | Priority |
> |----------------|-------|------------|--------|----------|
> | Same company name | 1,234 | 2.7% | Revenue inflation | Critical |
> | Same email address | 456 | 1.0% | Communication issues | High |
> | Same company + city | 892 | 2.0% | Likely true duplicates | Critical |
>
> **Key Findings:**
> - 1,234 potential duplicate company names suggests 600+ truly duplicate accounts
> - Same company + city (892) is the strongest duplicate indicator
> - Estimated $340K revenue over-reported due to duplicates (based on recent finding)
>
> ---
>
> ### VALIDITY
>
> | Rule | Field(s) | Violations | % | Impact |
> |------|----------|------------|---|--------|
> | Valid email format | email | 1,245 | 2.8% | Undeliverable |
> | Valid US state code | state | 847 non-standard | 2.2% | Territory gaps |
> | Numeric only | contract_value | 2,345 | 5.2% | Calculation errors |
> | No test data | company_name | 500 | 1.1% | Polluted metrics |
>
> **Key Findings:**
> - 1,245 records have malformed email addresses (not just missing—actually invalid)
> - 500 test/demo accounts in production data affecting all metrics
> - Contract values with non-numeric characters will fail in calculations
>
> ---
>
> ## Issue Inventory
>
> ### Critical Issues (Fix Immediately)
>
> | Issue | Field(s) | Records | Business Impact | Root Cause |
> |-------|----------|---------|-----------------|------------|
> | Duplicate customers | company_name, email | 1,234 | $340K revenue inflation | No duplicate prevention at entry |
> | Invalid emails | email | 2,400 | 5.3% campaign waste | No validation on import |
> | Test data in production | all | 500 | All metrics polluted | No data isolation |
>
> ### High Priority (30 Days)
>
> | Issue | Field(s) | Records | Business Impact | Root Cause |
> |-------|----------|---------|-----------------|------------|
> | State inconsistency | state | 7,621 | Territory gaps, reporting errors | No standardization |
> | Industry variations | industry | 12,456 | Poor segmentation | Free-text entry |
> | Unknown account owners | account_owner | 1,200 | Unassigned accounts | Departed employees |
>
> ---
>
> ## Root Cause Analysis
>
> ### Issue: Duplicate Customers
>
> - **Symptom:** 1,234 customer records with duplicate company names
> - **Root Cause:** No duplicate detection at point of entry in Salesforce. Multiple sales reps creating records for same company.
> - **Contributing Factors:** Lack of global view, incentive structure rewards new accounts, no merge process
> - **Prevention:** Implement duplicate detection rules in Salesforce, require verification before new account creation
>
> ### Issue: Invalid Emails
>
> - **Symptom:** 2,400 bounced emails, 1,245 malformed addresses
> - **Root Cause:** Bulk import from acquired company without validation. Manual entry without format checking.
> - **Contributing Factors:** No email verification service, pressure to import quickly
> - **Prevention:** Email validation at entry, periodic verification sweep, bounce handling automation
>
> ---
>
> ## Business Impact Assessment
>
> | Issue | Affected Process | Impact Type | Quantified Impact |
> |-------|------------------|-------------|-------------------|
> | Duplicates | Revenue reporting | Over-statement | $340K |
> | Duplicates | Commission calculation | Overpayment | ~$17K |
> | Invalid emails | Marketing campaigns | Wasted spend | $8K/campaign |
> | State inconsistency | Territory assignment | Unassigned accounts | 892 accounts |
> | Missing account owner | Customer success | No coverage | 1,200 accounts |
>
> **Total Estimated Annual Impact:** ~$450K
>
> ---
>
> ## Data Quality Scorecard
>
> | Dimension | Score | Target | Gap | Status |
> |-----------|-------|--------|-----|--------|
> | Completeness | 78/100 | 95 | -17 | ⚠️ |
> | Accuracy | 72/100 | 98 | -26 | 🔴 |
> | Consistency | 58/100 | 95 | -37 | 🔴 |
> | Uniqueness | 85/100 | 99 | -14 | ⚠️ |
> | Timeliness | 92/100 | 95 | -3 | ✅ |
> | Validity | 82/100 | 98 | -16 | ⚠️ |
> | **Overall** | **68/100** | **95** | **-27** | 🔴 |
>
> ---
>
> ## Remediation Roadmap
>
> ### Phase 1: Critical Fixes (Week 1-2)
>
> | Action | Issue Addressed | Owner | Effort |
> |--------|-----------------|-------|--------|
> | Run deduplication process | Duplicate customers | Data team | 16 hrs |
> | Remove test accounts | Test data pollution | Data team | 4 hrs |
> | Email validation sweep | Invalid emails | Marketing ops | 8 hrs |
> | Fix revenue reports | Duplicate impact | Finance | 4 hrs |
>
> ### Phase 2: Standardization (Month 1)
>
> | Action | Issue Addressed | Owner | Effort |
> |--------|-----------------|-------|--------|
> | Standardize state values | State inconsistency | Data team | 8 hrs |
> | Create industry picklist | Industry variations | Sales ops | 12 hrs |
> | Assign orphaned accounts | Missing owners | Sales ops | 8 hrs |
> | Implement duplicate detection | Prevent new duplicates | Salesforce admin | 16 hrs |
>
> ---
>
> ## Quick Wins
>
> 1. **Remove 500 test accounts** — Immediate metric improvement — 2 hours
> 2. **Standardize country to 'US'** — 3,982 records fixed with one update — 1 hour
> 3. **Assign 'UNKNOWN' owners to manager** — Route accounts for reassignment — 1 hour
> 4. **Run email verification on imports** — Prevent new bad data — 4 hours setup
>
> ---
>
> ## Validation Rules to Implement
>
> | Rule Name | Logic | Field(s) | Alert Threshold |
> |-----------|-------|----------|-----------------|
> | Email format check | Regex validation | email | Any violation |
> | Duplicate detection | Match on company name + domain | company_name, email | 85% confidence |
> | State standardization | Convert to 2-letter code | state | Any non-standard |
> | Contract value numeric | Strip non-numeric characters | contract_value | Any violation |
> | Test data flag | Regex for 'test', 'demo', 'sample' | company_name | Any match |
>
> ---
>
> ## Monitoring Recommendations
>
> **Metrics to Track:**
>
> | Metric | Current | Target | Frequency |
> |--------|---------|--------|-----------|
> | Overall quality score | 68 | 95 | Monthly |
> | Duplicate rate | 2.7% | <0.5% | Weekly |
> | Email bounce rate | 5.3% | <1% | Per campaign |
> | Completeness (email) | 94.5% | 98% | Monthly |
> | Format compliance (state) | 83.2% | 99% | Monthly |
>
> **Alerts to Configure:**
>
> | Alert | Trigger | Action |
> |-------|---------|--------|
> | New duplicate detected | Duplicate score >85% | Block creation, review |
> | Bulk import quality | <95% valid emails | Reject import |
> | Completeness drop | Any field drops >2% | Investigate source |

---

## Troubleshooting Common Issues

| Problem | Likely Cause | Solution |
|---------|--------------|----------|
| Can't quantify impact | Missing business context | Ask: "How is this data used? What decisions depend on it?" |
| Too many issues | No prioritization | Ask: "Rank by business impact. What would cause the most harm if wrong?" |
| Root causes unclear | Surface-level analysis | Ask: "For each issue, keep asking 'why' until you reach the system or process cause" |
| Recommendations too generic | Not actionable | Ask: "Specify exact actions, owners, and effort for each remediation step" |
| Stakeholders don't care | Impact not communicated | Ask: "Translate data quality scores into business language: revenue, risk, cost" |

---

## Tips from Experience

1. **Lead with business impact.** "68/100 quality score" means nothing; "$340K over-reported revenue" gets attention.

2. **Fix the source, not just the symptom.** Cleaning data without fixing the entry process means cleaning forever.

3. **Quick wins build momentum.** Start with easy fixes that show visible improvement.

4. **Make quality measurable.** If you can't measure it, you can't improve it.

5. **Prevention beats remediation.** One validation rule saves hours of cleanup.

6. **Document the baseline.** You need to show improvement, which requires knowing where you started.

---

## Measuring Success

**You've succeeded with this recipe when:**
- [ ] Quality score improves to target level
- [ ] Critical issues are remediated
- [ ] Data-related incidents decrease
- [ ] User confidence in data increases
- [ ] Quality monitoring is operational
- [ ] Prevention rules are in place

**Track over time:**
- Overall data quality score
- Issue count by severity
- Remediation completion rate
- Time between issue and fix
- User-reported data problems
- Business metrics affected by data quality

---

## Variations

### Pre-Migration Assessment
Before system migrations:
```
Assess source data quality before migration:
- What will break in the new system?
- What needs transformation?
- What should be excluded?
- What cleanup is required pre-migration?
- What validation rules should be applied?

Focus on: Blocking issues, transformation requirements
```

### Financial Data Quality
For finance-critical data:
```
Assess with financial controls focus:
- Reconciliation accuracy
- Audit trail completeness
- Control point validation
- Segregation of duties compliance
- Historical accuracy

Include: SOX compliance considerations, materiality thresholds
```

### Customer Data Quality
For CRM and customer data:
```
Assess customer data with emphasis on:
- Contact reachability (email, phone validity)
- Duplicate customers and contacts
- Segmentation accuracy
- Consent and preference data
- GDPR/privacy compliance

Focus on: Communication effectiveness, privacy compliance
```

### Product/Inventory Data
For operational data:
```
Assess product/inventory data:
- SKU accuracy
- Pricing consistency
- Stock level accuracy
- Attribute completeness
- Category consistency

Focus on: Operational impact, customer-facing accuracy
```

---

## Building Your Repeatable System

After initial assessment, establish:

1. **Regular assessment cadence** (monthly or quarterly)
2. **Consistent scoring methodology**
3. **Automated monitoring** for critical metrics
4. **Issue tracking** from discovery to resolution
5. **Trend reporting** to show improvement

**Sample Setup:**
```
data-quality/
├── assessments/
│   ├── 2024-11-customer-master.md
│   ├── 2024-10-customer-master.md
│   └── [monthly assessments]
├── issues/
│   ├── active-issues.md
│   ├── resolved-issues.md
│   └── issue-template.md
├── rules/
│   ├── validation-rules.md
│   └── monitoring-rules.md
├── remediation/
│   ├── deduplication-playbook.md
│   ├── standardization-scripts/
│   └── cleanup-procedures.md
├── reporting/
│   ├── quality-scorecard.xlsx
│   └── trend-dashboard/
└── reference/
    ├── business-rules.md
    └── field-definitions.md
```

---

## How This Pattern Applies Elsewhere

This recipe's core pattern—**profile data → assess dimensions → quantify impact → prioritize remediation**—applies broadly:

| Role | Application |
|------|-------------|
| **Finance** | GL data, transaction records |
| **Sales** | CRM data, pipeline |
| **Marketing** | Contact data, campaign data |
| **Operations** | Inventory, orders |
| **HR** | Employee records, payroll |
| **IT** | Asset data, configuration |

---

## Next Steps

1. **Choose a dataset:** High-criticality, high-usage data
2. **Profile the data:** Run completeness, uniqueness, pattern analysis
3. **Document issues:** Inventory what you find
4. **Assess impact:** Quantify business consequences
5. **Prioritize remediation:** Critical → High → Medium → Low
6. **Implement monitoring:** Prevent recurrence

---

*Recipe #59 of 100 in the Claude Code Knowledge Worker Recipe Collection*

---

**Related tooling:** the verification philosophy this recipe applies by hand is implemented for AI-assisted code in [ai-control-framework](https://github.com/sgharlow/ai-control-framework) — deployment-readiness scoring and evidence-backed gates.
