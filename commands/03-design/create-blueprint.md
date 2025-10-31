# Command: /create-blueprint

## Execution Context
**Primary Agent:** Product Manager Agent + Engineering Architect Agent
**Required Skills:** ai-usecase-blueprint
**Command Category:** Design & Development
**Version:** 2.0

## Purpose
Create comprehensive product blueprint including capabilities, architecture, technical specifications, pricing strategy, and responsible AI framework.

## When to Use
- After use case prioritization
- Starting product design phase
- Technical architecture planning
- Business model design

## Execution
Use **ai-usecase-blueprint** skill - see [skills/ai-usecase-blueprint/SKILL.md](../../skills/ai-usecase-blueprint/SKILL.md) for complete methodology including:
- Product blueprint template structure
- Lean Canvas for business model
- Technical architecture patterns
- Pricing archetypes analysis
- Responsible AI framework

## Example Usage
```
/create-blueprint

Use case: AI-powered code review assistant (prioritization score: 85/100)

Target users: 200 software engineers at B2B SaaS company

Technical context:
- GitHub Enterprise for version control
- Existing CI/CD with GitHub Actions
- Security: SOC 2 compliant infrastructure required

Business model: Per-seat subscription, freemium entry

Success criteria: 20% bug reduction, 70% adoption in 6 months, <500ms latency
```

---

*Command Category: Design & Development*
*Version: 2.0 - Wrapper for ai-usecase-blueprint skill*
*Last Updated: October 2025*
