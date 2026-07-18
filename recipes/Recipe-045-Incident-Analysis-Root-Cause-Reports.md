# Incident Analysis and Root Cause Reports

**Recipe #45: From "What Happened?" to "Never Again"**

---

| Setup Time | Time Saved | Difficulty | Best For |
|------------|------------|------------|----------|
| 10 minutes (first time) / 5 minutes (repeat) | 3-5 hours per incident | Intermediate | IT, Operations, Engineering, Quality |

---

## The Problem

When something goes wrong—a system outage, a production defect, a process failure—the aftermath is often chaotic. Teams scramble to fix the problem, then move on without truly understanding why it happened. Post-mortems are skipped or rushed. The same types of incidents keep recurring. When post-mortems do happen, they become blame sessions or generate reports that go unread. The opportunity to learn and improve is lost.

**Pain Points:**
- Incident happens, gets fixed, nobody learns why
- Post-mortems delayed or skipped
- Analysis is shallow ("human error")
- Same root causes keep appearing
- Reports are dense and unread
- No follow-through on action items
- Blame culture discourages honest analysis

---

## The Outcome

Structured, blameless incident analysis that identifies true root causes and generates actionable preventive measures. Reports that are clear enough to drive organizational learning and track follow-through.

**What You'll Have When Done:**
- Clear incident timeline
- Impact assessment
- Root cause analysis (5 Whys, fishbone)
- Contributing factors identified
- Action items with owners and deadlines
- Lessons learned summary
- Tracking mechanism for implementation

---

## When to Use This Recipe

**Good Fit:**
- System outages and service disruptions
- Production defects and quality issues
- Process failures and near-misses
- Security incidents
- Customer-impacting events
- Safety incidents
- Significant financial errors

**Not a Good Fit:**
- Minor issues not worth deep analysis
- Incidents still being resolved (stabilize first)
- Performance issues (different analysis type)
- Ongoing investigations with legal implications

---

## Before You Start: Quick Checklist

- [ ] Claude Code is installed and working
- [ ] Incident is resolved (or stabilized)
- [ ] You have timeline and log information
- [ ] Key participants are available for input
- [ ] You have 2-4 hours for thorough analysis

---

## How Claude Code Helps

**What Claude Code Does Well:**
- Structures incident timeline
- Facilitates root cause analysis techniques
- Identifies patterns in contributing factors
- Generates action items from findings
- Creates clear, readable reports
- Tracks relationships between causes

**Where Human Judgment Is Essential:**
- Technical accuracy of timeline
- Root cause identification
- Feasibility of action items
- Organizational context
- Sensitive handling of human factors
- Final validation and approval

---

## Input Examples

**Ideal Source Materials:**

| Input Type | Example | What Claude Uses It For |
|------------|---------|------------------------|
| Timeline | What happened when | Chronological reconstruction |
| Logs | System/application logs | Technical evidence |
| Communications | Slack, email during incident | Response analysis |
| Impact data | Duration, customers affected | Severity assessment |
| Participant input | What people observed | Context and details |

**Sample Input:**
```
Incident Report Request

INCIDENT SUMMARY:
Production database outage on Tuesday, November 12, 2024
Duration: 2 hours 17 minutes (14:23 - 16:40 UTC)
Impact: All customer-facing services unavailable

INCIDENT TIMELINE (raw):
- 14:23: Monitoring alert - database connections exhausted
- 14:25: On-call engineer paged (Sarah)
- 14:28: Sarah acknowledges, begins investigation
- 14:35: Sarah identifies connection pool exhaustion
- 14:40: Incident commander (Marcus) joins
- 14:45: Decision to restart database cluster
- 14:50: Restart initiated
- 15:05: Restart complete, connections still exhausted
- 15:15: Investigation continues - found runaway batch job
- 15:25: Batch job identified as new deployment from that morning
- 15:30: Batch job killed, connections start recovering
- 15:45: Services coming back online
- 16:10: All services restored
- 16:40: Incident declared resolved after monitoring period

LOG SNIPPETS:
[Paste relevant log excerpts]

IMPACT:
- Duration: 2h 17m
- Customers affected: ~12,000 active users
- Revenue impact: Estimated $45,000 in lost transactions
- SLA breach: 99.9% monthly SLA now at risk
- Support tickets: 347 tickets opened

COMMUNICATIONS DURING INCIDENT:
[Paste relevant Slack/email snippets]

IMMEDIATE CAUSE:
New batch job deployed that morning opened thousands of database connections without proper pooling, exhausting the connection pool.

KNOWN CONTRIBUTING FACTORS:
- Batch job wasn't load tested
- No connection limits configured for batch system
- Deployment happened during peak hours
- Monitoring didn't alert until connections fully exhausted

PEOPLE INVOLVED:
- Sarah Chen (On-call engineer)
- Marcus Johnson (Incident commander)
- Alex Rivera (Batch job developer)
- Deployment was approved by: [Unknown - checking]

ENVIRONMENT:
- Production database: PostgreSQL cluster (3 nodes)
- Connection pool: PgBouncer (max 500 connections)
- Batch system: Custom Python job runner
```

---

## Step-by-Step Implementation

### Step 1: Gather Incident Data
**Time: 20-30 minutes**

Collect while fresh:
- Detailed timeline with timestamps
- Log excerpts
- Communications during incident
- Participant observations
- Impact metrics

---

### Step 2: Launch Claude Code
**Time: 30 seconds**

```bash
claude
```

---

### Step 3: Run the Incident Analysis Prompt
**Time: 7-10 minutes for Claude to process**

---

**PRIMARY PROMPT: Incident Analysis and Root Cause Report**

```
Please help me create a comprehensive incident post-mortem.

INCIDENT BASICS:
- Date/Time: [When it occurred]
- Duration: [How long]
- Severity: [Critical/High/Medium/Low]
- Services affected: [What was impacted]

INCIDENT TIMELINE:
[Paste your detailed timeline]

LOGS AND EVIDENCE:
[Paste relevant logs, screenshots descriptions, communications]

IMPACT ASSESSMENT:
- Users/Customers affected: [Number]
- Revenue impact: [If known]
- SLA impact: [If applicable]
- Other business impact: [Reputation, operations, etc.]

IMMEDIATE CAUSE:
[What directly caused the incident]

KNOWN CONTRIBUTING FACTORS:
[What else contributed]

PEOPLE INVOLVED:
[Key responders and their roles]

PLEASE CREATE A COMPLETE POST-MORTEM:

1. EXECUTIVE SUMMARY
   One paragraph covering:
   - What happened
   - Duration and impact
   - Root cause (one sentence)
   - Key action being taken

2. DETAILED TIMELINE
   Table format:
   | Time (UTC) | Event | Actor | Source |

   Include:
   - Detection/alert
   - Response actions
   - Key decisions
   - Resolution steps
   - Recovery confirmation

3. IMPACT ANALYSIS
   Quantify the damage:
   - User impact (numbers)
   - Business impact (revenue, SLA)
   - Operational impact
   - Reputation impact

4. ROOT CAUSE ANALYSIS

   A. The Five Whys
   Walk through systematically:
   - Why did [immediate cause] happen?
   - Why did that happen?
   - Continue until reaching systemic cause

   B. Contributing Factors
   Categorize using fishbone/Ishikawa:
   - People: [Human factors]
   - Process: [Process failures]
   - Technology: [Technical factors]
   - Environment: [External factors]

   C. Root Cause Statement
   Clear, blameless statement of the fundamental cause

5. WHAT WENT WELL
   - Detection mechanisms that worked
   - Response actions that helped
   - Communication that was effective
   - Recovery steps that succeeded

6. WHAT COULD IMPROVE
   - Where detection failed or was slow
   - Response gaps
   - Communication issues
   - Recovery challenges

7. ACTION ITEMS
   For each action item:
   | # | Action | Owner | Priority | Due Date | Type |

   Types:
   - Detect: Improve detection of this issue
   - Mitigate: Reduce impact if it happens again
   - Prevent: Stop it from happening

   Prioritize:
   - P1: Must do immediately
   - P2: Should do within 30 days
   - P3: Plan within 90 days

8. LESSONS LEARNED
   - What this incident taught us
   - How it changes our thinking
   - What others should know

9. SIMILAR INCIDENTS
   - Have we seen this before?
   - Are there related incidents?
   - Is this part of a pattern?

10. REVIEW AND APPROVAL
    - Author
    - Reviewers
    - Approval date
    - Next review date

Use blameless language throughout. Focus on systems and processes, not individuals.
```

---

### Step 4: Deepen Root Cause Analysis
**Time: 15-20 minutes**

If the initial analysis is shallow:

**To push deeper on root causes:**
```
The root cause analysis stopped at "the batch job wasn't tested." Let's go deeper:
- Why wasn't it tested?
- What about our process allowed untested code to reach production?
- What systemic factors enabled this?
```

**To explore contributing factors:**
```
Let's explore more contributing factors:
- What decisions made this more likely?
- What safeguards should have caught this but didn't?
- What environmental factors contributed?
```

**To avoid blame:**
```
Rewrite to be more blameless. Instead of "Alex didn't test the batch job," focus on "The system allowed deployment without load testing." What process changes would make the right action the easy action?
```

---

### Step 5: Generate Actionable Items
**Time: 10-15 minutes**

**To improve action items:**
```
Make action items more specific and actionable:
- "Improve testing" → "Implement automated load testing for batch jobs in CI/CD pipeline"
- Add clear success criteria for each action
- Ensure each action has a single owner
```

**To prioritize actions:**
```
Help prioritize these action items:
- What would have prevented this incident entirely?
- What would have reduced detection time?
- What would have reduced impact?
- What's the effort vs. value for each?
```

---

### Step 6: Create Final Deliverables
**Time: 10 minutes**

```
Create the final post-mortem package:

1. FULL POST-MORTEM DOCUMENT
   Complete analysis with all sections

2. EXECUTIVE SUMMARY (1 page)
   For leadership:
   - What happened
   - Impact
   - Root cause
   - Key actions
   - Status

3. ACTION ITEM TRACKER
   Format for tracking completion:
   | # | Action | Owner | Due | Status | Completion Date |

4. LESSONS LEARNED SUMMARY
   Sharable format for org-wide learning

5. PREVENTION CHECKLIST
   For similar deployments/changes:
   - Questions to ask
   - Checks to perform
   - Signs of risk

6. COMMUNICATION DRAFT
   For stakeholder update:
   - What happened
   - What we're doing about it
   - Commitment to improvement
```

---

## Example Output

Below is an abbreviated post-mortem example:

---

> **INCIDENT POST-MORTEM**
>
> **Production Database Outage - November 12, 2024**
>
> ---
>
> ## Executive Summary
>
> On November 12, 2024, all customer-facing services were unavailable for 2 hours and 17 minutes due to database connection exhaustion. The root cause was a new batch processing job deployed that morning which opened thousands of database connections without proper connection pooling, overwhelming our connection limit of 500. Approximately 12,000 users were affected, with an estimated $45,000 in lost transactions and our monthly SLA now at risk of breach.
>
> **Root Cause:** A batch job with a database connection leak was deployed to production without load testing, exhausting the shared connection pool.
>
> **Key Action:** Implementing mandatory load testing for all batch jobs before production deployment, with connection usage monitoring as a gate.
>
> ---
>
> ## Detailed Timeline
>
> | Time (UTC) | Event | Actor | Source |
> |------------|-------|-------|--------|
> | 09:15 | Batch job v2.3.1 deployed to production | CI/CD | Deploy log |
> | 09:15-14:23 | Batch job running, slowly consuming connections | System | DB logs |
> | 14:23 | Alert: "Database connections exhausted" | PagerDuty | Monitoring |
> | 14:25 | On-call engineer Sarah Chen paged | PagerDuty | Page log |
> | 14:28 | Sarah acknowledges page, begins investigation | Sarah | Slack |
> | 14:35 | Sarah identifies connection pool at 100% | Sarah | PgBouncer |
> | 14:40 | Incident commander Marcus Johnson joins | Marcus | Slack |
> | 14:45 | Decision: Restart database cluster | Marcus/Sarah | Incident call |
> | 14:50 | Database cluster restart initiated | Sarah | Runbook |
> | 15:05 | Restart complete, connections still exhausted | System | Monitoring |
> | 15:15 | Investigation reveals connections from batch system | Sarah | DB query |
> | 15:25 | Batch job v2.3.1 identified as source | Sarah | Process list |
> | 15:30 | Batch job process killed | Sarah | Manual |
> | 15:35 | Connections begin recovering | System | Monitoring |
> | 15:45 | First services coming back online | System | Status page |
> | 16:10 | All services restored | System | Monitoring |
> | 16:40 | Incident resolved after stability monitoring | Marcus | Slack |
>
> ---
>
> ## Impact Analysis
>
> | Impact Area | Measurement |
> |-------------|-------------|
> | Duration | 2 hours, 17 minutes (14:23-16:40 UTC) |
> | Users affected | ~12,000 active users during window |
> | Transactions lost | ~$45,000 estimated revenue |
> | Support tickets | 347 tickets opened |
> | SLA impact | Monthly uptime now 99.84% (target: 99.9%) |
> | Engineering time | ~20 person-hours in response |
>
> **Severity:** Critical (all services unavailable)
>
> ---
>
> ## Root Cause Analysis
>
> ### The Five Whys
>
> 1. **Why were services unavailable?**
>    → The database connection pool was exhausted, preventing new connections.
>
> 2. **Why was the connection pool exhausted?**
>    → A batch job opened thousands of connections and didn't close them.
>
> 3. **Why did the batch job open so many connections?**
>    → The new version (v2.3.1) had a connection leak bug—connections weren't returned to the pool after use.
>
> 4. **Why wasn't this connection leak caught before production?**
>    → The batch job was not load tested. Unit tests passed but didn't test concurrent execution or connection behavior at scale.
>
> 5. **Why wasn't load testing required?**
>    → There's no automated gate for batch jobs requiring load testing. The deployment checklist mentions it but it's optional and easily skipped under deadline pressure.
>
> ### Contributing Factors (Fishbone Analysis)
>
> **People:**
> - Developer was unaware of connection pooling requirements for batch jobs
> - Reviewer focused on business logic, not resource management
> - No ownership of "batch job best practices" documentation
>
> **Process:**
> - No mandatory load testing gate for batch deployments
> - Deployment checklist treats load testing as optional
> - No review of resource usage patterns in code review
> - Deployment during peak hours (9 AM) is allowed
>
> **Technology:**
> - Batch system doesn't have connection limits configured
> - Monitoring alerts at exhaustion (500/500), not warning level (400/500)
> - No automated rollback when connection usage spikes
> - No isolation between batch and web application connection pools
>
> **Environment:**
> - Shared database connection pool between batch and web
> - Peak usage time increased impact
>
> ### Root Cause Statement
>
> The incident occurred because our deployment process allows batch jobs to reach production without verifying their database connection behavior under load. While the immediate cause was a connection leak bug, the systemic issue is that we lack automated safeguards to catch resource management issues before they affect production.
>
> ---
>
> ## What Went Well
>
> ✅ **Alerting detected the issue** - Connection exhaustion alert fired promptly
> ✅ **On-call response was fast** - Sarah acknowledged in 3 minutes
> ✅ **Incident commander joined quickly** - Marcus provided coordination
> ✅ **Team found the root cause** - Identified batch job within 45 minutes
> ✅ **Recovery was clean** - Once batch job was killed, services recovered
> ✅ **Communication was good** - Status page updated, stakeholders informed
>
> ---
>
> ## What Could Improve
>
> ❌ **Earlier warning** - Alert at 100% exhaustion is too late; need warning threshold
> ❌ **Quicker identification** - Initial restart attempt delayed root cause identification
> ❌ **Blast radius** - Batch and web sharing connection pool meant total outage
> ❌ **Prevention** - This should never have reached production
> ❌ **Testing gap** - Load testing isn't enforced for batch jobs
> ❌ **Deployment timing** - Production deployment during peak hours increased impact
>
> ---
>
> ## Action Items
>
> | # | Action | Owner | Priority | Due | Type |
> |---|--------|-------|----------|-----|------|
> | 1 | Implement mandatory load testing gate for batch jobs in CI/CD | Platform Team | P1 | Nov 22 | Prevent |
> | 2 | Add connection usage warning alert at 80% threshold | SRE | P1 | Nov 18 | Detect |
> | 3 | Configure connection limits per-service in PgBouncer | Database Team | P1 | Nov 25 | Mitigate |
> | 4 | Separate batch and web application connection pools | Architecture | P2 | Dec 15 | Mitigate |
> | 5 | Implement automated rollback on connection spike | Platform Team | P2 | Dec 30 | Mitigate |
> | 6 | Update deployment policy: no production deploys 9AM-5PM without approval | Engineering Mgr | P2 | Nov 18 | Prevent |
> | 7 | Create batch job development guide with connection pooling requirements | Tech Writing | P3 | Jan 15 | Prevent |
> | 8 | Add connection behavior to code review checklist | Engineering | P3 | Dec 1 | Prevent |
>
> ---
>
> ## Lessons Learned
>
> 1. **Load testing must be mandatory for resource-intensive jobs.** Our testing caught functional bugs but missed resource management issues that only appear at scale.
>
> 2. **Alert thresholds should warn, not just fail.** By the time we knew about the issue, we were already in full outage.
>
> 3. **Shared resources need isolation.** When batch and web share the same connection pool, batch can take down web. Isolation reduces blast radius.
>
> 4. **"Easy to skip" safeguards get skipped.** Optional checklist items aren't safeguards. Automated gates are.
>
> 5. **First response isn't always best response.** Restarting the database felt right but delayed root cause identification.
>
> ---
>
> ## Similar Incidents
>
> | Incident | Date | Similarity |
> |----------|------|------------|
> | API rate limiter memory leak | Aug 2024 | Resource exhaustion, missed in testing |
> | Cache connection storm | Mar 2024 | Connection management issue |
>
> **Pattern identified:** Resource management issues are repeatedly reaching production. This reinforces the need for automated resource testing in CI/CD.
>
> ---
>
> ## Review and Approval
>
> | Role | Name | Date |
> |------|------|------|
> | Author | [Name] | Nov 14, 2024 |
> | Technical Review | Sarah Chen | |
> | Management Review | [Engineering Manager] | |
> | Action Item Approval | [VP Engineering] | |
>
> **Next Review:** 30 days to verify action item completion

---

## Troubleshooting Common Issues

| Problem | Likely Cause | Solution |
|---------|--------------|----------|
| Root cause is "human error" | Stopped too shallow | Ask: "Why did the system allow this error? What would make the right action easier?" |
| Analysis becomes blame session | Cultural or language issues | Ask: "Reframe to focus on systems and processes. Remove names from cause analysis" |
| Too many action items | Everything seems important | Ask: "Which actions would have prevented this incident? Prioritize prevention over detection" |
| Actions never get done | No ownership or tracking | Ask: "Assign single owner and specific date. Create tracking mechanism" |
| Same incidents recur | Lessons not learned | Ask: "Why didn't previous actions prevent this? What's blocking real change?" |
| Report too long | Over-detailed | Ask: "Create executive summary. Move details to appendices" |

---

## Tips from Experience

1. **Do the post-mortem while it's fresh.** Memory fades quickly. Capture details within 48-72 hours.

2. **Blameless doesn't mean accountability-free.** Focus on systems, but still track action items to completion.

3. **The Five Whys isn't magic.** It's a starting point. Complex incidents have multiple contributing factors.

4. **Ask "What made this possible?"** Every incident requires multiple failures. Find them all.

5. **Actions need owners, not teams.** "Engineering will fix this" means nobody owns it.

6. **Share widely, learn collectively.** Incidents are expensive lessons. Make sure the whole organization benefits.

---

## Measuring Success

**You've succeeded with this recipe when:**
- [ ] Post-mortem completed within 5 days of incident
- [ ] Root cause is systemic, not individual blame
- [ ] Action items are specific and assigned
- [ ] Stakeholders understand what happened and why
- [ ] Similar incidents decrease over time
- [ ] Action items are actually completed

**Track over time:**
- Mean time to post-mortem
- Action item completion rate
- Repeat incident rate
- Time to detect similar issues
- Post-mortem quality scores

---

## Variations

### Security Incident Post-Mortem
For security events:
```
Conduct security incident post-mortem.

Incident: [Security event description]
Classification: [Data breach, unauthorized access, etc.]

Additional analysis:
- Attack vector identification
- Indicators of compromise
- Data exposure assessment
- Containment effectiveness
- Regulatory notification requirements

Output: Security incident report with compliance sections
```

### Near-Miss Analysis
For events that almost caused incidents:
```
Analyze this near-miss.

What happened: [Event]
What prevented the incident: [Safeguard that worked]
What could have made it worse: [If safeguard failed]

Analyze:
- Why did the near-miss happen?
- Are our safeguards reliable?
- What can we learn without the cost of an actual incident?

Output: Near-miss report with preventive recommendations
```

### Recurring Incident Pattern Analysis
For incidents that keep happening:
```
Analyze pattern in recurring incidents.

Incidents: [List of related incidents]
Common factors: [What they share]

Analyze:
- Why do our fixes not work?
- What systemic issue enables recurrence?
- What fundamental change is needed?

Output: Pattern analysis with systemic recommendations
```

### Customer-Facing Incident Report
For external communication:
```
Create customer-facing incident report.

Internal post-mortem: [Reference]
Audience: [Customers, partners]

Create:
- Appropriate level of detail
- Focus on impact and resolution
- Commitment to prevention
- Professional tone

Output: External incident report
```

---

## Building Your Repeatable System

After several post-mortems, build your system:

1. **Create incident templates** for different severity levels
2. **Establish timeline for completion** (e.g., 5 days post-incident)
3. **Track action items centrally** with completion visibility
4. **Review patterns quarterly** to identify systemic issues
5. **Share learnings** across teams and organization

**Sample Setup:**
```
incident-management/
├── templates/
│   ├── post-mortem-template.md
│   ├── executive-summary-template.md
│   ├── security-incident-template.md
│   └── customer-report-template.md
├── post-mortems/
│   ├── 2024/
│   │   ├── 2024-11-12-database-outage/
│   │   │   ├── post-mortem.md
│   │   │   ├── timeline.md
│   │   │   ├── evidence/
│   │   │   └── action-items.md
│   │   └── [other incidents]/
├── action-items/
│   └── tracker.xlsx
├── patterns/
│   └── recurring-issues.md
└── reference/
    ├── severity-definitions.md
    └── process-guide.md
```

---

## How This Pattern Applies Elsewhere

This recipe's core pattern—**document timeline → analyze root causes → identify improvements → track to completion**—applies broadly:

| Role | Application |
|------|-------------|
| **IT/Engineering** | System outages, bugs |
| **Operations** | Process failures, quality issues |
| **Security** | Security incidents, breaches |
| **Quality** | Manufacturing defects, complaints |
| **Finance** | Financial errors, audit findings |
| **Customer Success** | Major customer issues |

---

## Next Steps

1. **Gather incident data:** Collect timeline, logs, communications
2. **Run analysis:** Use this recipe to structure the post-mortem
3. **Review with team:** Validate findings with those involved
4. **Generate action items:** Specific, owned, dated
5. **Share and learn:** Distribute findings for organizational learning
6. **Track completion:** Follow up on action items

---

*Recipe #45 of 100 in the Claude Code Knowledge Worker Recipe Collection*

---

**Related tooling:** the verification philosophy this recipe applies by hand is implemented for AI-assisted code in [ai-control-framework](https://github.com/sgharlow/ai-control-framework) — deployment-readiness scoring and evidence-backed gates.
