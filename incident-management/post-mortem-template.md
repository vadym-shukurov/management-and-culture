# Blameless Post-Mortem Template

> **"Every incident is a gift-an opportunity to make our systems more resilient."**

This template guides teams through a structured, blameless analysis of incidents. The goal is systemic improvement, not individual blame.

---

## Core Principles

| Principle | What It Means |
|:---|:---|
| **Blameless** | We examine systems, not individuals |
| **Transparent** | Findings are shared openly |
| **Action-Oriented** | Every post-mortem produces concrete improvements |
| **Learning-Focused** | Incidents are investments in future reliability |

---

## Post-Mortem Document

### Incident Metadata

| Field | Value |
|:---|:---|
| **Incident ID** | INC-YYYY-MM-DD-XXX |
| **Date** | YYYY-MM-DD |
| **Duration** | XX hours XX minutes |
| **Severity** | SEV-1 / SEV-2 / SEV-3 |
| **Author** | [Name] |
| **Reviewers** | [Names] |
| **Status** | Draft / In Review / Final |

---

### Executive Summary

> *One paragraph describing what happened, the impact, and the key takeaway.*

**Example:**
> On [DATE], a configuration change to the payment service caused a 45-minute outage affecting approximately 12,000 customers. The root cause was a missing validation check in our deployment pipeline. We have since implemented automated config validation, reducing the likelihood of similar incidents by an estimated 95%.

---

### Impact Assessment

| Metric | Value |
|:---|:---|
| **Users Affected** | [Number] |
| **Revenue Impact** | $[Amount] or N/A |
| **SLA Breach** | Yes / No |
| **Data Loss** | Yes / No |
| **Reputational Impact** | Low / Medium / High |

---

### Timeline

> *Detailed chronological account of events. Use 24-hour UTC timestamps.*

| Time (UTC) | Event |
|:---|:---|
| 14:00 | Deployment initiated for payment-service v2.3.1 |
| 14:05 | First alert triggered: "Payment API latency > 5s" |
| 14:08 | On-call engineer acknowledges alert |
| 14:15 | Incident declared, war room opened |
| 14:32 | Root cause identified: malformed config |
| 14:45 | Rollback completed, service restored |
| 15:00 | All-clear communicated to stakeholders |

---

### Root Cause Analysis

#### The Five Whys

| Level | Question | Answer |
|:---|:---|:---|
| **Why 1** | Why did the service go down? | Config file contained invalid values |
| **Why 2** | Why was an invalid config deployed? | No validation in the deployment pipeline |
| **Why 3** | Why was there no validation? | It was a manual process, assumed correct |
| **Why 4** | Why was it manual? | Validation tooling was deprioritized |
| **Why 5** | Why was it deprioritized? | No previous incidents-risk was underestimated |

#### Root Cause Statement

> *One clear sentence describing the systemic root cause.*

**Example:**
> The deployment pipeline lacked automated configuration validation, allowing invalid values to reach production.

---

### What Went Well

> *Acknowledge what worked. This reinforces good practices.*

- [ ] Alert fired within expected threshold
- [ ] On-call response was swift
- [ ] Communication to stakeholders was clear
- [ ] Rollback procedure worked as designed
- [ ] Team collaboration was effective

---

### What Went Wrong

> *Identify systemic failures-not individual mistakes.*

- [ ] No automated config validation
- [ ] Runbook was outdated
- [ ] Monitoring gap in [specific area]
- [ ] Unclear escalation path
- [ ] [Other systemic issue]

---

### Action Items

> *Every post-mortem must produce actionable improvements with clear ownership.*

| Priority | Action | Owner | Due Date | Status |
|:---|:---|:---|:---|:---|
| P0 | Implement automated config validation | @platform-team | YYYY-MM-DD | In Progress |
| P1 | Update deployment runbook | @devops-lead | YYYY-MM-DD | Not Started |
| P1 | Add monitoring for [gap] | @sre-team | YYYY-MM-DD | Not Started |
| P2 | Conduct training on new validation tool | @tech-lead | YYYY-MM-DD | Not Started |

---

### Lessons Learned

> *Broader insights that apply beyond this specific incident.*

1. **Automation over process:** Manual gates will eventually fail. Invest in automated validation.
2. **Test in staging what you fear in production:** Config changes should be tested with production-like data.
3. **Runbooks decay:** Schedule quarterly runbook reviews.

---

### Supporting Materials

- [ ] Link to incident Slack channel
- [ ] Link to relevant dashboards
- [ ] Link to deployment logs
- [ ] Link to related tickets/PRs

---

## Post-Mortem Meeting Agenda

| Time | Activity |
|:---|:---|
| 5 min | Review timeline and impact |
| 15 min | Walk through root cause analysis |
| 10 min | Discuss what went well/wrong |
| 15 min | Prioritize and assign action items |
| 5 min | Capture lessons learned |
| 5 min | Schedule follow-up review |

---

## The Blameless Mindset

### What We Say

| Instead of... | We say... |
|:---|:---|
| "Who caused this?" | "What allowed this to happen?" |
| "Why didn't you catch this?" | "What can we build to catch this automatically?" |
| "This was a human error" | "Our system didn't prevent this error" |
| "Be more careful next time" | "Let's make this impossible to get wrong" |

### Why Blameless Works

- **Psychological safety** → People report issues faster
- **Full disclosure** → Better root cause analysis
- **Systemic fixes** → Problems don't recur
- **Learning culture** → Team gets stronger after every incident

> **"If a human can make a mistake, our system should make it impossible-or at least recoverable."**

---

<sub>**Management & Culture** | Vadym Shukurov</sub>
