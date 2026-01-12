# Management & Culture

<p align="center">
  <img src="https://img.shields.io/badge/Focus-Engineering%20Leadership-blue?style=for-the-badge" alt="Focus: Engineering Leadership">
  <img src="https://img.shields.io/badge/Philosophy-Autonomy%20%2B%20Accountability-green?style=for-the-badge" alt="Philosophy: Autonomy + Accountability">
  <img src="https://img.shields.io/badge/Author-Vadym%20Shukurov-red?style=for-the-badge" alt="Author: Vadym Shukurov">
</p>

> **Building high-performing engineering teams through intentional culture, clear ownership, and scalable processes.**

This repository contains frameworks, philosophies, and practical guides for engineering leadership—distilled from years of experience scaling teams and delivering results.

---

## The Developer Lifecycle

```mermaid
flowchart LR
    subgraph ONBOARDING["🚀 Onboarding"]
        A[Week 1: Observe] --> B[Week 2: Practice]
        B --> C[Week 3: Expand]
        C --> D[Week 4: Lead]
    end
    
    subgraph GROWTH["📈 Growth"]
        E[Pair Programming] --> F[Code Ownership]
        F --> G[Technical Leadership]
        G --> H[Mentorship]
    end
    
    subgraph EXCELLENCE["⭐ Excellence"]
        I[Ship Features] --> J[Own Systems]
        J --> K[Define Standards]
        K --> L[Build Teams]
    end
    
    D --> E
    H --> I
    L --> |Cycle Continues| A
    
    style ONBOARDING fill:#e1f5fe
    style GROWTH fill:#f3e5f5
    style EXCELLENCE fill:#e8f5e9
```

---

## Repository Structure

```
management-and-culture/
├── MY_USER_MANUAL.md           # How to work with Vadym
├── management/                 # People & process frameworks
├── culture/                    # Engineering culture & standards
├── technical-strategy/         # Code ownership & governance
└── incident-management/        # Post-mortem & failure handling
```

---

## Working With Me

> **Start here if you're joining my team.**

| Document | Description |
|:---|:---|
| [My User Manual](./MY_USER_MANUAL.md) | How I communicate, what I value, and how to give me feedback |

---

## Management

Frameworks for developing people and running effective teams.

| Document | Description |
|:---|:---|
| [1-on-1 Framework](./management/1-on-1-framework.md) | Structured meeting format for meaningful manager-report conversations |
| [Onboarding Philosophy](./management/onboarding-philosophy.md) | 4-week high-touch immersion program with pair programming |

### Key Principles

- **Ownership over checklist** — Teams define their social fabric
- **High-touch onboarding** — 4 weeks of structured pair programming
- **Gradual autonomy** — From observation to leadership

---

## Culture

Standards and philosophies that define how we work together.

| Document | Description |
|:---|:---|
| [Engineering Standards](./culture/engineering-standards.md) | Code style, Scout Rule, blameless post-mortems, ADRs |
| [Ownership Model](./culture/ownership-model.md) | Stewardship over gatekeeping, anti-bottleneck strategies |

### Key Principles

- **Stewardship > Gatekeeping** — Owners mentor, not block
- **Automated consistency** — Let linters handle style debates
- **Blameless culture** — Systems fail, not people
- **Default to public** — Context should be searchable

---

## Technical Strategy

Governance structures for code quality and team scalability.

| Document | Description |
|:---|:---|
| [Code Guardianship](./technical-strategy/code-guardianship.md) | CODEOWNERS structure with tiered ownership |

### Key Principles

- **Clear accountability** — Every file has a defined owner
- **Appropriate expertise** — Critical paths get senior review
- **Reduced cognitive load** — Automated PR assignment
- **Safety nets** — Ship fast within guardrails

---

## Incident Management

How we handle failures and turn them into improvements.

| Document | Description |
|:---|:---|
| [Post-Mortem Template](./incident-management/post-mortem-template.md) | Blameless incident analysis with Five Whys and action items |

### Key Principles

- **Blameless by default** — We examine systems, not individuals
- **Every incident is a gift** — Opportunities for systemic improvement
- **Action-oriented** — Every post-mortem produces concrete fixes
- **Transparent sharing** — Learnings benefit the entire organization

---

## Philosophy Summary

```mermaid
flowchart TB
    subgraph INPUTS["Inputs"]
        A[Autonomy]
        B[Accountability]
    end
    
    subgraph PRACTICES["Practices"]
        C[Clear Ownership]
        D[Blameless Culture]
        E[Continuous Learning]
    end
    
    subgraph OUTCOMES["Outcomes"]
        F[High-Performing Teams]
        G[Sustainable Velocity]
        H[Engineering Excellence]
    end
    
    A --> C
    A --> D
    B --> C
    B --> E
    C --> F
    D --> G
    E --> H
    
    style INPUTS fill:#fff3e0
    style PRACTICES fill:#e3f2fd
    style OUTCOMES fill:#e8f5e9
```

### The Goal

> **Build systems so robust and teams so informed that leadership presence is a luxury, not a requirement.**

---

## Quick Start

| If you are... | Start with... |
|:---|:---|
| **Joining my team** | [My User Manual](./MY_USER_MANUAL.md) |
| **A new manager** | [1-on-1 Framework](./management/1-on-1-framework.md) |
| **A team lead** | [Ownership Model](./culture/ownership-model.md) |
| **An architect** | [Code Guardianship](./technical-strategy/code-guardianship.md) |
| **Handling an incident** | [Post-Mortem Template](./incident-management/post-mortem-template.md) |
| **Everyone** | [Engineering Standards](./culture/engineering-standards.md) |

---

## About

These documents represent battle-tested approaches to engineering leadership, developed through scaling teams, shipping products, and learning from both successes and failures.

**Core beliefs:**
- Great teams are built, not hired
- Culture is what you do, not what you say
- Processes should enable, not constrain
- Documentation beats tribal knowledge
- Failures are investments in future resilience

---

<sub>**Vadym Shukurov** | Engineering Leadership</sub>
