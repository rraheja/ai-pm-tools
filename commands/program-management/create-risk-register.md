# Command: /create-risk-register

## Execution Context
**Primary Agent:** Program Management Agent  
**Required Skills:** program-management  
**Command Category:** Program Management  
**Version:** 2.0

## Purpose
Create comprehensive risk registers to proactively identify, assess, and mitigate program risks.

## When to Use
- Program kickoff
- Quarterly risk reviews
- Before major milestones
- When issues arise

## Required Skill
**Skill:** `program-management`

## Risk Register Structure
For each risk:
1. **Risk Description**
   - What could go wrong
   - Root cause

2. **Impact Assessment**
   - Severity: High/Medium/Low
   - Impact areas (timeline, quality, cost, scope)
   - Quantified impact if possible

3. **Probability**
   - Likelihood: High/Medium/Low (or %)
   - Timing: When could this occur

4. **Risk Score**
   - Impact × Probability
   - Priority ranking

5. **Mitigation Strategy**
   - Preventive actions
   - Contingency plans
   - Owner and timeline

6. **Status**
   - Open, Mitigated, Accepted, Closed

## Risk Categories
- **Technical**: Architecture, performance, integration
- **Resource**: Skills, availability, budget
- **Schedule**: Dependencies, timeline compression
- **External**: Vendors, market, regulatory
- **Organizational**: Change management, politics

## Example Usage
```
/create-risk-register

Program: AI platform launch
Major risks identified:
- Model accuracy below targets
- Regulatory approval delays
- Integration complexity with legacy systems
```


## Output Deliverables
- Risk register (spreadsheet or document)
- Risk heat map
- Mitigation action plan
- Escalation triggers

---
*Command Category: Program Management*  
*Version: 2.0 - Anthropic Best Practices*
*Last Updated: October 2025*
