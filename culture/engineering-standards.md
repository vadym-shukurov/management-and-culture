# Engineering Standards

> **Principles That Enable Autonomy and Excellence**

A shared set of standards that eliminate friction, encourage ownership, and create a culture of continuous improvement.

---

## Common Code Style Standards

### Automated Consistency

> **"We don't argue about linting in PRs. If the linter passes, the style is fine. If we hate a rule, we PR the `.eslintrc` or `gofmt` config."**

```
┌─────────────────────────────────────────────────────────────┐
│                    STYLE DECISION FLOW                      │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│   Code Change                                               │
│       │                                                     │
│       ▼                                                     │
│   ┌───────────────┐                                         │
│   │ Linter Passes │───Yes──▶ Style is Acceptable            │
│   └───────────────┘                                         │
│       │                                                     │
│       No                                                    │
│       │                                                     │
│       ▼                                                     │
│   Fix the Code (Not the Config)                             │
│                                                             │
│   ─────────────────────────────────────────────────────     │
│                                                             │
│   Hate a Rule?                                              │
│       │                                                     │
│       ▼                                                     │
│   PR the Config ───▶ Team Discussion ───▶ Consensus         │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

**Key Principle:** Automate style enforcement to free mental energy for solving real problems.

---

### Meaningful Naming

> **Variables and functions must describe intent, not implementation.**

| Avoid | Prefer |
|:---|:---|
| `checkFlag123` | `isUserEligible` |
| `processData` | `calculateMonthlyRevenue` |
| `temp` | `pendingTransactions` |
| `handleClick` | `submitPaymentForm` |
| `doStuff` | `syncInventoryWithWarehouse` |

**The Test:** Can someone understand what this does without reading the implementation?

```
// Intent is clear from the name alone
const isUserEligibleForDiscount = (user) => { ... }

// vs.

// Requires reading implementation to understand
const checkFlag123 = (u) => { ... }
```

---

### The Scout Rule

> **"Always leave the code slightly better than you found it."**

```
┌─────────────────────────────────────────────────────────────┐
│                                                             │
│   Before Your Change              After Your Change         │
│   ──────────────────              ─────────────────         │
│                                                             │
│   Working Code                    Working Code              │
│       +                               +                     │
│   Technical Debt                  Slightly Less Debt        │
│       +                               +                     │
│   Confusing Comment               Clear Comment             │
│       +                               +                     │
│   Missing Test                    One More Test             │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

**Examples of Scout Rule in Action:**
- Rename a confusing variable while fixing a bug
- Add a missing docstring to a function you're modifying
- Extract a magic number into a named constant
- Delete dead code you encounter

---

## Empowerment Through Reflection

### Post-Mortems as Learning

> **Incidents are "System Failures," not "Human Failures."**

We hold **blameless post-mortems** to reflect on how our standards failed us.

```
┌─────────────────────────────────────────────────────────────┐
│                   BLAMELESS POST-MORTEM                     │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│   ❌  "Who made this mistake?"                              │
│                                                             │
│   ✅  "What in our system allowed this to happen?"          │
│                                                             │
│   ─────────────────────────────────────────────────────     │
│                                                             │
│   FOCUS AREAS:                                              │
│                                                             │
│   • What monitoring gaps existed?                           │
│   • What guardrails were missing?                           │
│   • What process allowed this to reach production?          │
│   • How can we make this class of error impossible?         │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

**The Goal:** Transform every incident into a systemic improvement.

---

### ADRs (Architecture Decision Records)

> **Every major change requires a reflection on "Why."**

This empowers the builder to **own the history** of the decision.

#### ADR Template

```markdown
# ADR-001: [Title of Decision]

## Status
Accepted | Proposed | Deprecated | Superseded

## Context
What is the issue that we're seeing that is motivating this decision?

## Decision
What is the change that we're proposing and/or doing?

## Consequences
What becomes easier or more difficult because of this change?

## Alternatives Considered
What other options were evaluated? Why were they rejected?
```

#### Why ADRs Matter

| Without ADRs | With ADRs |
|:---|:---|
| "Why was this built this way?" | Clear historical context |
| Repeated debates on solved problems | Reference past decisions |
| Tribal knowledge lost when people leave | Knowledge persists |
| Fear of changing "legacy" code | Confidence to evolve |

---

## Summary

| Standard | Core Principle |
|:---|:---|
| **Automated Consistency** | Let machines handle style, humans handle logic |
| **Meaningful Naming** | Intent over implementation |
| **Scout Rule** | Continuous incremental improvement |
| **Blameless Post-Mortems** | Systems fail, not people |
| **ADRs** | Decisions deserve documentation |

---

<sub>**Management & Culture** | Vadym Shukurov</sub>
