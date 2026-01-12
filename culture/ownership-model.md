# Code Ownership Model

> **"Code ownership is not about 'gatekeeping'; it's about stewardship."**

It ensures that every line of code has a mentor, and every contributor has a clear path to getting their work reviewed by the right expert.

---

## Philosophy

### Gatekeeping vs. Stewardship

| Gatekeeping | Stewardship |
|:---|:---|
| "This is MY code" | "I mentor this area" |
| Blocks contributions | Enables contributors |
| Single point of failure | Knowledge multiplier |
| Hoards context | Shares context |
| Reviews to protect | Reviews to elevate |

### Why This Matters

- **Scalability:** Stewards build systems that outlast their own involvement
- **Velocity:** Removing "single points of failure" prevents PR bottlenecks
- **Growth:** "Reviews to elevate" turns every code review into a learning opportunity

---

## The "Anti-Bottle-Neck" Strategy

### Collective Ownership vs. Silos

> **While we use `CODEOWNERS`, we rotate names every quarter.**

This prevents "Knowledge Silos" and ensures that the "owner" is actually a **facilitator of quality**, not a single point of failure.

### Quarterly Rotation Example

| Module | Q1 | Q2 | Q3 | Q4 |
|:---|:---|:---|:---|:---|
| `/payments/` | Alice | Bob | Carol | Alice |
| `/auth/` | Bob | Carol | Alice | Bob |
| `/api/` | Carol | Alice | Bob | Carol |

### Traditional vs. Rotating CODEOWNERS

| Traditional CODEOWNERS | Rotating CODEOWNERS |
|:---|:---|
| Knowledge concentrated | Knowledge distributed |
| Vacation = bottleneck | Team remains unblocked |
| Expertise becomes tribal | Expertise becomes shared |
| Single reviewer burnout | Balanced review load |

---

### Empowered Approval: The Emergency Break Rule

> **If a CODEOWNER is OOO (Out of Office), the "Emergency Break" rule applies.**

A Peer Lead can override, but **must document the delta** in a follow-up ticket.

### Emergency Break Flow

| Step | Action |
|:---:|:---|
| 1 | PR Ready for Review |
| 2 | Check: Is CODEOWNER available? |
| 3a | **Yes** → Standard Review |
| 3b | **No** → Emergency Break triggered |
| 4 | Peer Lead reviews the PR |
| 5 | Approval + Merge |
| 6 | Create follow-up ticket: "Delta Review: PR #123" |
| 7 | CODEOWNER reviews on return |

### Emergency Break Checklist

- [ ] CODEOWNER confirmed OOO or unresponsive (>24h for urgent PRs)
- [ ] Peer Lead has sufficient context to review
- [ ] PR passes all automated checks
- [ ] Follow-up ticket created with:
  - Link to original PR
  - Reason for emergency override
  - Areas requiring CODEOWNER attention on return

---

## CODEOWNERS Best Practices

```bash
# Example CODEOWNERS file with rotation notes

# Core Platform (Rotate: Q1-Alice, Q2-Bob, Q3-Carol, Q4-Alice)
/src/core/           @current-quarter-owner

# Payments (Critical Path - Always 2 reviewers)
/src/payments/       @payments-primary @payments-secondary

# Documentation (Lower barrier - any senior can approve)
/docs/               @engineering-leads

# Infrastructure (Requires platform team)
/infra/              @platform-team
```

---

## Key Principles

| Principle | Implementation |
|:---|:---|
| **No Single Points of Failure** | Quarterly rotation of owners |
| **Velocity Over Gatekeeping** | Emergency break rule for OOO |
| **Documentation Over Memory** | Follow-up tickets capture context |
| **Mentorship Over Control** | Owners guide, not block |

---

## From Theory to Practice

### How to Spot Gatekeeping in the Wild

* **The "I'll just do it" trap:** A lead taking over a complex task because "it's faster than explaining it."
* **Review Gatekeeping:** PR comments that focus on personal preference rather than functionality or growth.
* **The Whisper Network:** Important architectural decisions happening in private DMs instead of public RFCs/Channels.

### How to Act as a Steward

1. **Record as you go:** If you explain a concept twice, document it once.
2. **The "Review to Elevate" Rule:** Every PR review should include at least one "Why" or a link to documentation, not just a "Fix this."
3. **Default to Public:** Move technical discussions to public channels so the "context" is searchable for the next person.

> **The Steward's Goal:** To build a system so robust and a team so informed that your presence is a luxury, not a requirement.

---

## Summary

> **Every line of code has a MENTOR**
> 
> **Every contributor has a clear PATH**
> 
> **Every review is about ELEVATION**
> 
> **= SUSTAINABLE CODE OWNERSHIP**

---

<sub>**Management & Culture** | Vadym Shukurov</sub>
