# Command: /create-incident-report

## Execution Context
**Primary Agent:** SRE Operations Agent  
**Required Skills:** sre-practices  
**Command Category:** SRE Operations  
**Version:** 2.0

## Purpose
Create post-mortem incident reports focusing on learning and prevention.

## When to Use
- After production incidents
- Service outages
- Security breaches
- Data loss events

## Required Skill
**Skill:** `sre-practices`

## Incident Report Structure
1. **Incident Summary**
   - What happened
   - Impact (users, revenue, duration)
   - Severity classification

2. **Timeline**
   - Detection
   - Response actions
   - Resolution

3. **Root Cause Analysis**
   - Contributing factors
   - Why it wasn't caught earlier

4. **Impact Assessment**
   - User impact
   - Business impact
   - SLO/SLA violations

5. **Action Items**
   - Immediate fixes
   - Long-term improvements
   - Process changes
   - Owners and deadlines

6. **Lessons Learned**
   - What went well
   - What to improve

## Example Usage
```
/create-incident-report

Incident: Database outage
Duration: 45 minutes
Impact: 30% of users unable to access app
Root cause: Resource exhaustion from inefficient query
```


## Output Deliverables
- Blameless post-mortem document
- Action item tracker
- Communication summary

---
*Command Category: SRE Operations*  
*Version: 2.0 - Anthropic Best Practices*
*Last Updated: October 2025*
