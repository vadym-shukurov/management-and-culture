# Code Guardianship

> **Structured ownership that scales with your organization.**

A practical example of how to implement tiered code ownership using GitHub's `CODEOWNERS` file.

---

## Team Structure Overview

| Path | Owner | Rationale |
|:---|:---|:---|
| `/terraform/` | Platform Team | Infrastructure requires specialized expertise |
| `/src/domain/` | Technical Leads | Core business logic needs senior oversight |
| `/docs/` | Engineering Team | Documentation is a shared responsibility |

---

## CODEOWNERS Configuration

```bash
# =============================================================================
# CODEOWNERS - Vadym's Team Structure
# =============================================================================
# This file defines code ownership for automated PR review assignment.
# Documentation: https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-code-owners
# =============================================================================

# -----------------------------------------------------------------------------
# INFRASTRUCTURE
# -----------------------------------------------------------------------------
# Owned by the Platform Champions
# Requires expertise in IaC, cloud architecture, and security
/terraform/  @vadym-shukurov/platform-team

# -----------------------------------------------------------------------------
# CORE BUSINESS LOGIC
# -----------------------------------------------------------------------------
# Requires a Senior/Lead review
# Critical path - changes here impact the entire system
/src/domain/  @vadym-shukurov/technical-leads

# -----------------------------------------------------------------------------
# DOCUMENTATION & ONBOARDING
# -----------------------------------------------------------------------------
# Owned by the WHOLE team
# Everyone contributes, everyone reviews - knowledge is shared
/docs/  @vadym-shukurov/engineering-team
```

---

## Ownership Tiers Explained

### Tier 1: Platform Team (`/terraform/`)

**Why specialized ownership?**
- Infrastructure changes have blast radius across all services
- Requires deep knowledge of cloud providers and security
- Mistakes can be costly and hard to reverse

**Review expectations:**
- Security implications assessed
- Cost impact evaluated
- Rollback plan documented

---

### Tier 2: Technical Leads (`/src/domain/`)

**Why senior oversight?**
- Core business logic defines the product
- Architectural decisions have long-term impact
- Consistency across the domain is critical

**Review expectations:**
- Alignment with domain model
- Performance considerations
- Test coverage verified

---

### Tier 3: Engineering Team (`/docs/`)

**Why shared ownership?**
- Documentation is everyone's responsibility
- Lowers barrier to contribution
- Diverse perspectives improve clarity

**Review expectations:**
- Accuracy of content
- Readability and structure
- Up-to-date with codebase

---

## Benefits of This Structure

| Benefit | Description |
|:---|:---|
| **Clear Accountability** | Every file has a defined owner |
| **Appropriate Expertise** | Critical paths get senior review |
| **Team Empowerment** | Shared areas encourage participation |
| **Scalable Process** | Automated assignment reduces bottlenecks |

---

## Why This Works

### Reduced Cognitive Load

> **New hires don't have to guess who should review their PR. GitHub does it for them.**

- No more Slack messages asking "Who should review this?"
- Automatic assignment based on file paths
- Onboarding friction eliminated from day one

### Safety Nets

> **You can enforce that "Code Owner Approval" is required before merging. This is how you sleep at night while empowering the team to ship fast.**

- Branch protection rules ensure the right eyes see critical changes
- Teams ship autonomously within guardrails
- Leadership trusts the process, not individual heroics

| Without CODEOWNERS | With CODEOWNERS |
|:---|:---|
| "Who reviews infrastructure PRs?" | Automatically assigned to Platform Team |
| Hope the right person notices | Guaranteed expert review |
| Manual coordination overhead | Zero-friction assignment |
| Inconsistent review quality | Consistent expertise applied |

---

## Implementation Checklist

- [ ] Create `.github/CODEOWNERS` file in repository root
- [ ] Define GitHub teams for each ownership tier
- [ ] Communicate ownership expectations to the team
- [ ] Set up branch protection rules requiring CODEOWNERS approval
- [ ] Schedule quarterly rotation reviews (see [Ownership Model](../culture/ownership-model.md))

---

<sub>**Management & Culture** | Vadym Shukurov</sub>
