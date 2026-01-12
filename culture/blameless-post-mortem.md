# Blameless Post-Mortem

> **"We don't fire people for making mistakes. We fire people for hiding them."**

This document defines how we handle incidents and failures. Our approach prioritizes **psychological safety** and **systemic improvement** over individual blame.

---

## The Golden Rule

**Blaming individuals is explicitly forbidden.**

| Forbidden | Required |
|:---|:---|
| "Who caused this?" | "What allowed this to happen?" |
| "Why didn't you catch this?" | "What process gap let this through?" |
| "This was human error" | "Our system didn't prevent this error" |
| "Be more careful next time" | "Let's make this impossible to get wrong" |

---

## Why Blameless?

### The Psychology

When people fear punishment, they:
- Hide mistakes until they become disasters
- Avoid taking risks that could lead to innovation
- Spend energy on self-protection instead of problem-solving
- Leave the organization, taking knowledge with them

When people feel safe, they:
- Report issues early, when they're still small
- Experiment and innovate freely
- Focus on fixing problems, not defending themselves
- Stay and grow with the organization

### The Math

```
Fear of Blame = Hidden Problems = Bigger Incidents = Higher Cost

Psychological Safety = Early Detection = Small Fixes = Lower Cost
```

---

## The Post-Mortem Process

### Step 1: Gather Facts (Not Fault)

Focus on **what happened**, not **who did it**.

**Timeline Questions:**
- What was the sequence of events?
- What alerts fired (or didn't)?
- What actions were taken and when?
- What was the customer impact?

### Step 2: Five Whys (Systems Focus)

Dig into the **process**, not the **person**.

| Level | Question | Focus |
|:---|:---|:---|
| Why 1 | Why did the incident happen? | Immediate cause |
| Why 2 | Why did that cause exist? | Contributing factors |
| Why 3 | Why wasn't it caught earlier? | Detection gaps |
| Why 4 | Why did our process allow this? | Process gaps |
| Why 5 | Why hasn't this been fixed before? | Systemic issues |

### Step 3: Identify Process Gaps

Every incident reveals one or more gaps:

| Gap Type | Example | Fix Category |
|:---|:---|:---|
| **Detection** | No alert for this failure mode | Monitoring |
| **Prevention** | No validation for this input | Code/Config |
| **Recovery** | Rollback took too long | Runbooks |
| **Communication** | Stakeholders weren't notified | Process |
| **Knowledge** | Team didn't know this could happen | Documentation |

### Step 4: Action Items (Systemic Fixes)

Every action item must:
- Fix the **system**, not blame the **individual**
- Have a clear **owner** and **due date**
- Be **verifiable** (how will we know it's done?)

**Good Action Items:**
- Add automated config validation to CI pipeline
- Create runbook for this failure scenario
- Add monitoring for [specific metric]

**Bad Action Items:**
- "Be more careful"
- "Review changes more thoroughly"
- "Remember to check this next time"

---

## The Post-Mortem Meeting

### Ground Rules

1. **No blame.** Period. If someone starts blaming, redirect to systems.
2. **Assume good intent.** Everyone was trying to do their best with the information they had.
3. **Focus forward.** We can't change the past; we can improve the future.
4. **Celebrate learning.** The incident taught us something valuable.

### Agenda

| Time | Activity |
|:---|:---|
| 5 min | Review timeline and impact |
| 15 min | Walk through Five Whys |
| 10 min | Identify process gaps |
| 15 min | Define and assign action items |
| 5 min | Capture key learnings |

### Facilitation Tips

- If discussion turns to individuals, ask: *"What process allowed this to happen?"*
- If someone says "human error," ask: *"What can we build to prevent this error?"*
- If the room goes quiet, ask: *"What would have made this impossible?"*

---

## What We Believe

### About People

- People come to work wanting to do a good job
- Mistakes are inevitable; hiding them is optional
- The same person, in a better system, would have succeeded

### About Systems

- If a human can make a mistake, the system should catch it
- Processes exist to make success easy and failure hard
- Every incident is a gift—it shows us where our system is weak

### About Learning

- Failure is tuition for future success
- Shared learnings multiply value across the organization
- The goal is to fail safely, learn quickly, and improve continuously

---

## The Psychological Safety Contract

**We promise:**

1. **No retaliation** for reporting incidents or mistakes
2. **No public shaming** of individuals involved in incidents
3. **No career consequences** for good-faith errors
4. **Full support** for anyone who raises concerns early

**We expect:**

1. **Honest reporting** of what happened
2. **Active participation** in finding systemic fixes
3. **Follow-through** on assigned action items
4. **Sharing learnings** with the broader team

---

## Template

```markdown
# Post-Mortem: [Incident Title]

**Date:** YYYY-MM-DD
**Duration:** X hours
**Severity:** SEV-1/2/3
**Author:** [Name]

## Summary
[One paragraph: what happened, impact, key fix]

## Timeline
| Time (UTC) | Event |
|:---|:---|
| HH:MM | [Event] |

## Five Whys
1. Why: [Answer]
2. Why: [Answer]
3. Why: [Answer]
4. Why: [Answer]
5. Why: [Answer]

## Process Gaps Identified
- [ ] Gap 1
- [ ] Gap 2

## Action Items
| Action | Owner | Due | Status |
|:---|:---|:---|:---|
| [Systemic fix] | @name | YYYY-MM-DD | Pending |

## Key Learnings
- Learning 1
- Learning 2
```

---

## Final Thought

> **"The measure of a team is not whether they have incidents, but how they respond to them."**

A blameless culture doesn't mean a lack of accountability. It means holding the **system** accountable for enabling success, and holding **individuals** accountable for participating honestly in improvement.

---

<sub>**Management & Culture** | Vadym Shukurov</sub>
