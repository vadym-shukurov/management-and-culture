# Prompt Engineering for Engineering Leads

> **"The quality of AI output is directly proportional to the quality of your input."**

This guide teaches engineering leads how to craft effective prompts that maximize AI utility while maintaining quality and security standards.

---

## Why Prompt Engineering Matters for Leads

| Traditional Skill | AI-Era Equivalent |
|:---|:---|
| Writing good specs | Writing good prompts |
| Code review | Output validation |
| Delegation | Task decomposition for AI |
| Mentoring | Prompt template sharing |

**Your team's AI productivity depends on your prompt quality.**

---

## The Anatomy of an Effective Prompt

### The CRAFT Framework

| Component | Description | Example |
|:---|:---|:---|
| **C**ontext | Background information | "In a Node.js Express API..." |
| **R**ole | Who the AI should be | "Act as a senior security engineer..." |
| **A**ction | What to do | "Review this code for vulnerabilities..." |
| **F**ormat | How to structure output | "Provide a table of findings..." |
| **T**one | Style of response | "Be concise and actionable..." |

### Basic Structure

```markdown
## Context
[Provide relevant background]

## Role
[Define the expertise needed]

## Task
[Clearly state what you need]

## Constraints
[Define boundaries and requirements]

## Output Format
[Specify how you want the response]
```

---

## Prompt Patterns for Engineering Leads

### Pattern 1: Code Review Assistant

```markdown
You are a senior engineer conducting a code review.

Review this code for:
1. Security vulnerabilities (OWASP Top 10)
2. Performance issues
3. Error handling gaps
4. Code style violations
5. Test coverage gaps

For each issue found, provide:
- Severity (Critical/High/Medium/Low)
- Location (file and line if applicable)
- Description of the issue
- Suggested fix with code example

Code to review:
[paste sanitized code]
```

### Pattern 2: Architecture Review

```markdown
You are a solutions architect reviewing a system design.

Context: [describe the system and its purpose]

Review this architecture for:
1. Scalability bottlenecks
2. Single points of failure
3. Security concerns
4. Cost optimization opportunities
5. Operational complexity

Provide your analysis in this format:
- **Finding**: [description]
- **Risk Level**: High/Medium/Low
- **Recommendation**: [actionable suggestion]
- **Trade-offs**: [what you'd sacrifice]

Architecture:
[paste design or diagram description]
```

### Pattern 3: Incident Analysis

```markdown
You are an SRE helping with incident analysis.

Incident Summary:
[describe what happened]

Timeline:
[paste timeline of events]

Help me identify:
1. Potential root causes (use 5 Whys)
2. Contributing factors
3. Similar patterns from common incidents
4. Preventive measures

Focus on systemic issues, not individual blame.
Format as a structured post-mortem section.
```

### Pattern 4: Technical Decision Support

```markdown
I need to decide between [Option A] and [Option B] for [use case].

Context:
- Team size: [X engineers]
- Timeline: [X months]
- Scale: [expected load/data volume]
- Constraints: [budget, existing tech, skills]

For each option, analyze:
1. Pros and cons
2. Implementation effort
3. Long-term maintenance burden
4. Risk factors
5. Team skill requirements

Conclude with a recommendation and reasoning.
```

### Pattern 5: Documentation Generator

```markdown
Generate documentation for this [code/API/system].

Target audience: [junior developers/external users/ops team]

Include:
1. Overview and purpose
2. Quick start guide
3. Key concepts
4. API reference (if applicable)
5. Common use cases with examples
6. Troubleshooting section

Style: Clear, concise, with code examples.
Format: Markdown suitable for GitHub.

Source:
[paste code or specs]
```

### Pattern 6: Test Strategy

```markdown
You are a QA architect designing a test strategy.

Feature: [describe the feature]
Requirements: [paste requirements]

Create a test strategy including:
1. Unit test scenarios (with edge cases)
2. Integration test scenarios
3. E2E critical paths
4. Performance test considerations
5. Security test scenarios

For each scenario, specify:
- Test description
- Input/preconditions
- Expected outcome
- Priority (P0-P3)

Focus on coverage, not just happy paths.
```

---

## Advanced Techniques

### Chain of Thought Prompting

Force the AI to show reasoning:

```markdown
Think through this step by step:

1. First, identify all the components involved
2. Then, trace the data flow
3. Next, identify potential failure points
4. Finally, suggest mitigations

Problem: [describe problem]

Show your reasoning for each step.
```

### Few-Shot Learning

Provide examples of desired output:

```markdown
Generate error messages following this pattern:

Example 1:
Input: User not found
Output: "We couldn't find an account with that email. Please check the spelling or create a new account."

Example 2:
Input: Invalid password
Output: "The password you entered is incorrect. Please try again or reset your password."

Now generate for:
Input: Rate limit exceeded
```

### Iterative Refinement

Start broad, then narrow:

```markdown
Round 1: "Give me an overview of caching strategies for this API"

Round 2: "Let's focus on Redis. What are the key considerations?"

Round 3: "Show me implementation code for cache invalidation"

Round 4: "Now add error handling and fallback logic"
```

### Constraint Injection

Add explicit boundaries:

```markdown
Generate a solution with these constraints:
- Must work with Node.js 18+
- Cannot use external dependencies beyond [list]
- Must handle 10K requests/second
- Must complete in under 100ms p99
- Must be backward compatible with v2 API

[describe problem]
```

---

## Security-First Prompting

### Data Sanitization Checklist

Before prompting, remove:

```
❌ Real customer IDs → Use: "USER_123"
❌ API keys/tokens → Use: "API_KEY_PLACEHOLDER"
❌ Internal URLs → Use: "https://api.example.com"
❌ Employee names → Use: "Engineer A, Engineer B"
❌ Financial data → Use: synthetic numbers
❌ PII → Use: "john.doe@example.com"
```

### Safe Prompt Template

```markdown
[SANITIZED CODE - All credentials and PII removed]

Context: [generic description without company specifics]

Task: [what you need]

Note: This code has been sanitized. Please provide 
generic guidance that I can adapt to my specific 
implementation.
```

---

## Prompt Library for Common Tasks

### Sprint Planning

```markdown
Help me break down this epic into sprint-sized stories:

Epic: [description]
Team velocity: [X points/sprint]
Sprint length: [X weeks]

For each story, provide:
- Title
- Description
- Acceptance criteria
- Estimated complexity (S/M/L)
- Dependencies
```

### Onboarding Documentation

```markdown
Create an onboarding guide for a new engineer joining 
a team that works on [system description].

Include:
1. System overview (ELI5)
2. Key repositories and their purposes
3. Local development setup steps
4. First week suggested tasks
5. Key people to connect with (roles, not names)
6. Common gotchas and tips
```

### Performance Review Prep

```markdown
Help me structure feedback for a mid-level engineer.

Areas to cover:
1. Technical skills growth
2. Collaboration and communication
3. Ownership and initiative
4. Areas for development

For each area, prompt me with questions to consider.
Do not write the actual feedback-help me think through it.
```

### Meeting Facilitation

```markdown
I'm facilitating a [type] meeting with [X] participants.

Goal: [meeting objective]
Time: [X minutes]
Participants: [roles, not names]

Create:
1. Agenda with time allocations
2. Key questions to drive discussion
3. Decision framework if needed
4. Action item template
```

---

## Common Mistakes to Avoid

| Mistake | Problem | Fix |
|:---|:---|:---|
| **Vague prompts** | Generic, unhelpful output | Be specific about context and needs |
| **No examples** | AI guesses your preferred format | Provide example of desired output |
| **One giant prompt** | Overwhelms the model | Break into smaller, focused prompts |
| **No constraints** | Output may not fit your context | Specify technical and business constraints |
| **Trusting blindly** | AI makes confident-sounding mistakes | Always validate output |
| **Exposing secrets** | Security risk | Sanitize all inputs |

---

## Teaching Your Team

### Prompt Sharing Protocol

1. **Document effective prompts** in team wiki
2. **Share during retros** what worked well
3. **Create templates** for common tasks
4. **Review prompt quality** in 1:1s
5. **Celebrate innovations** in prompt engineering

### Prompt Review Checklist

When reviewing team prompts:

- [ ] Context is clear and complete
- [ ] No sensitive data included
- [ ] Output format is specified
- [ ] Constraints are defined
- [ ] Examples provided where helpful

---

## Measuring Prompt Effectiveness

| Metric | Good | Needs Improvement |
|:---|:---|:---|
| **First-try success rate** | >70% | <50% |
| **Iterations needed** | 1-2 | >3 |
| **Output usability** | Minor edits | Major rework |
| **Time saved** | >50% vs manual | <25% |

---

## Quick Reference

```
┌─────────────────────────────────────────────────────────────┐
│                 PROMPT ENGINEERING CHECKLIST                │
├─────────────────────────────────────────────────────────────┤
│                                                             │
│  BEFORE PROMPTING                                           │
│  ────────────────                                           │
│  □ Sanitize sensitive data                                  │
│  □ Define clear objective                                   │
│  □ Identify constraints                                     │
│                                                             │
│  IN YOUR PROMPT                                             │
│  ───────────────                                            │
│  □ Provide context                                          │
│  □ Specify role/expertise needed                            │
│  □ Define output format                                     │
│  □ Include examples if complex                              │
│  □ Add constraints                                          │
│                                                             │
│  AFTER RECEIVING OUTPUT                                     │
│  ─────────────────────                                      │
│  □ Validate accuracy                                        │
│  □ Check for security issues                                │
│  □ Test before using                                        │
│  □ Document what worked                                     │
│                                                             │
└─────────────────────────────────────────────────────────────┘
```

---

<sub>**Management & Culture** | Vadym Shukurov</sub>
