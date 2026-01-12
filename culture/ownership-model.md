# Code Ownership Model

> **"Code ownership is not about 'gatekeeping'; it's about stewardship."**

It ensures that every line of code has a mentor, and every contributor has a clear path to getting their work reviewed by the right expert.

---

## Philosophy

```
# Engineering Culture: Gatekeeping vs. Stewardship


| **Gatekeeping** ❌ | **Stewardship** ✅ |
| :--- | :--- |
| **"This is MY code"** | **"I mentor this area"** |
| Blocks contributions | Enables contributors |
| Single point of failure | Knowledge multiplier |
| Hoards context | Shares context |
| Reviews to protect | Reviews to elevate |

---

### Why this matters
* **Scalability:** Stewards build systems that outlast their own involvement.
* **Velocity:** Removing "Single points of failure" prevents PR bottlenecks.
* **Growth:** "Reviews to elevate" turns every code review into a learning opportunity.
```

---

## The "Anti-Bottle-Neck" Strategy

### Collective Ownership vs. Silos

> **While we use `CODEOWNERS`, we rotate names every quarter.**

This prevents "Knowledge Silos" and ensures that the "owner" is actually a **facilitator of quality**, not a single point of failure.

```
┌──────────────────────────────────────────────────────────────────────┐
│                   QUARTERLY ROTATION                                 │
├──────────────────────────────────────────────────────────────────────┤
│                                                                      │
│   Q1                Q2                Q3                    Q4       │
│   ──                ──                ──                    ──       │
│                                                                      │
│   /payments/        /payments/        /payments/        /payments/   │
│   Owner: Alice  →   Owner: Bob    →   Owner: Carol  →   Owner: Alice │
│                                                                      │
│   /auth/            /auth/            /auth/            /auth/       │
│   Owner: Bob    →   Owner: Carol  →   Owner: Alice  →   Owner: Bob   │
│                                                                      │
│   /api/             /api/             /api/             /api/        │
│   Owner: Carol  →   Owner: Alice →   Owner: Bob    →   Owner: Carol  │
│                                                                      │
└──────────────────────────────────────────────────────────────────────┘
```

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

```
┌─────────────────────────────────────────────────────────────┐
│                    EMERGENCY BREAK FLOW                     │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│   PR Ready for Review                                       │
│       │                                                     │
│       ▼                                                     │
│   ┌─────────────────────┐                                   │
│   │ CODEOWNER Available │                                   │
│   └─────────────────────┘                                   │
│       │           │                                         │
│      Yes          No                                        │
│       │           │                                         │
│       ▼           ▼                                         │
│   Standard    ┌─────────────────┐                           │
│   Review      │ Emergency Break │                           │
│               └─────────────────┘                           │
│                       │                                     │
│                       ▼                                     │
│               Peer Lead Reviews                             │
│                       │                                     │
│                       ▼                                     │
│               Approval + Merge                              │
│                       │                                     │
│                       ▼                                     │
│             ┌─────────────────────────┐                     │
│             │ Create Follow-up Ticket │                     │
│             │ "Delta Review: PR #123" │                     │
│             └─────────────────────────┘                     │
│                       │                                     │
│                       ▼                                     │
│               CODEOWNER Reviews on Return                   │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

#### Emergency Break Checklist

- [ ] CODEOWNER confirmed OOO or unresponsive (>24h for urgent PRs)
- [ ] Peer Lead has sufficient context to review
- [ ] PR passes all automated checks
- [ ] Follow-up ticket created with:
  - Link to original PR
  - Reason for emergency override
  - Areas requiring CODEOWNER attention on return

---

## CODEOWNERS Best Practices

```
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

## Summary

```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│   Every line of code has a MENTOR                           │
│                    +                                        │
│   Every contributor has a clear PATH                        │
│                    +                                        │
│   Every review is about ELEVATION                           │
│                    =                                        │
│   SUSTAINABLE CODE OWNERSHIP                                │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

<sub>**Management & Culture** | Vadym Shukurov</sub>
