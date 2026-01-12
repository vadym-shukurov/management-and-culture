# AI Acceptable Use Policy

> **"AI is a force multiplier for engineering excellence—when used responsibly."**

This policy defines how our engineering teams may use AI tools while protecting intellectual property, maintaining security, and ensuring ethical application.

---

## Scope

This policy applies to:
- All engineering team members
- All AI-powered tools (GitHub Copilot, ChatGPT, Claude, Cursor, etc.)
- All work-related activities (coding, documentation, analysis)

---

## Guiding Principles

| Principle | Description |
|:---|:---|
| **Human Oversight** | AI assists; humans decide |
| **Data Protection** | Never expose sensitive data to AI |
| **Quality Assurance** | AI output must be reviewed and tested |
| **Transparency** | Disclose AI usage when relevant |
| **Continuous Learning** | Stay current on AI capabilities and risks |

---

## Approved Use Cases

### Allowed

| Use Case | Guidance |
|:---|:---|
| **Code Generation** | Boilerplate, utilities, standard patterns |
| **Code Review Assistance** | Identifying bugs, suggesting improvements |
| **Documentation** | READMEs, comments, API docs |
| **Test Generation** | Unit tests, test data, edge cases |
| **Learning & Research** | Understanding new technologies, debugging |
| **Refactoring** | Code cleanup, performance optimization |
| **Translation** | Converting between languages/frameworks |

### Allowed with Caution

| Use Case | Required Precautions |
|:---|:---|
| **Security-Related Code** | Mandatory human security review |
| **Database Queries** | Review for injection risks, performance |
| **Infrastructure Code** | Peer review before apply |
| **Customer-Facing Content** | Legal/Marketing approval |

### Prohibited

| Use Case | Reason |
|:---|:---|
| **Inputting Customer PII** | Privacy violation, data breach risk |
| **Inputting Credentials/Secrets** | Security risk |
| **Inputting Proprietary Algorithms** | IP protection |
| **Generating Legal/Compliance Docs** | Requires qualified review |
| **Autonomous Deployments** | Human approval required |
| **Performance Reviews/HR Decisions** | Ethical and legal concerns |

---

## Data Protection Rules

### Never Input to AI Tools

```
❌ Customer data (names, emails, addresses, payment info)
❌ API keys, tokens, passwords, secrets
❌ Internal financial data
❌ Unreleased product specifications
❌ Legal documents or contracts
❌ Employee personal information
❌ Security vulnerabilities (before patch)
```

### Safe to Input

```
✅ Public documentation and tutorials
✅ Open-source code snippets
✅ Generic coding questions
✅ Anonymized/synthetic data
✅ Published API documentation
✅ General architectural patterns
```

### Data Sanitization Checklist

Before pasting code into AI tools:

- [ ] Remove all hardcoded credentials
- [ ] Replace real customer IDs with placeholders
- [ ] Strip comments containing sensitive business logic
- [ ] Remove internal URLs and endpoints
- [ ] Anonymize any personal information

---

## Quality Assurance Requirements

### All AI-Generated Code Must:

1. **Pass Code Review** — Same standards as human-written code
2. **Pass All Tests** — Unit, integration, and E2E where applicable
3. **Pass Security Scans** — SAST/DAST tools, dependency checks
4. **Pass Linting** — Style and formatting standards
5. **Be Understood** — Author must explain what it does

### The "Explain It" Rule

> **If you can't explain the AI-generated code to a teammate, don't merge it.**

AI can produce plausible-looking code that contains subtle bugs. You are responsible for understanding and validating every line.

---

## Intellectual Property

### Ownership

- AI-assisted code created during work belongs to the company
- You remain the author and are accountable for quality
- AI tools are instruments, like IDEs or compilers

### License Compliance

| Concern | Mitigation |
|:---|:---|
| **Training Data Origins** | Use enterprise AI tools with indemnification |
| **Open Source Licenses** | Scan generated code for license conflicts |
| **Copyright Claims** | Document AI usage for legal defensibility |

### Disclosure Requirements

| Situation | Disclosure Needed |
|:---|:---|
| Internal code | Not required |
| Open source contributions | Check project policy |
| Client deliverables | Per contract terms |
| Patents/IP filings | Mandatory disclosure |

---

## Security Requirements

### Tool Approval

Only use AI tools approved by Security/IT:

| Status | Tools |
|:---|:---|
| **Approved** | [List approved tools here] |
| **Under Review** | [List tools being evaluated] |
| **Prohibited** | [List banned tools] |

### Configuration Requirements

- Enable enterprise SSO where available
- Disable training on company data (opt-out)
- Use private/business tiers, not personal accounts
- Enable audit logging where available

### Incident Reporting

If you accidentally expose sensitive data to an AI tool:

1. **Stop** — Don't input more data
2. **Report** — Notify Security immediately
3. **Document** — Record what was exposed
4. **Remediate** — Rotate credentials if applicable

---

## Accountability

### Individual Responsibility

You are accountable for:
- What you input to AI tools
- The quality of AI-generated output you use
- Understanding the code you commit
- Following this policy

### Manager Responsibility

Managers must:
- Ensure team understands this policy
- Review AI usage during code reviews
- Escalate policy violations
- Provide training resources

---

## Violations

| Severity | Example | Consequence |
|:---|:---|:---|
| **Minor** | Using unapproved tool for non-sensitive task | Coaching, policy review |
| **Moderate** | Insufficient review of AI-generated code | Formal warning, training |
| **Severe** | Exposing customer PII to AI tool | Disciplinary action |
| **Critical** | Exposing credentials, causing breach | Termination possible |

---

## Policy Updates

This policy will be reviewed quarterly as AI capabilities evolve. Significant changes will be communicated via:
- Engineering All-Hands
- Slack #engineering-announcements
- Email notification

**Last Updated:** [Date]
**Next Review:** [Date + 3 months]
**Owner:** Engineering Leadership

---

## Quick Reference Card

```
┌─────────────────────────────────────────────────────────────┐
│                    AI ACCEPTABLE USE                        │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  ✅ DO                          ❌ DON'T                    │
│  ─────                          ────────                    │
│  • Generate boilerplate         • Input customer data       │
│  • Write tests                  • Input credentials         │
│  • Draft documentation          • Input proprietary code    │
│  • Debug with sanitized code    • Trust output blindly      │
│  • Learn new technologies       • Skip code review          │
│                                                             │
│  🔒 ALWAYS                                                  │
│  ──────────                                                 │
│  • Sanitize inputs              • Review all output         │
│  • Use approved tools           • Understand before merge   │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

<sub>**Management & Culture** | Vadym Shukurov</sub>
