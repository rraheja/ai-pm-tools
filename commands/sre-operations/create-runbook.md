# Command: /create-runbook

## Execution Context
**Primary Agent:** SRE Operations Agent  
**Required Skills:** sre-practices  
**Command Category:** SRE Operations  
**Version:** 2.0

## Purpose
Create operational runbooks documenting procedures for common operational tasks and incident response.

## When to Use
- Onboarding new team members
- Documenting operational procedures
- Preparing for on-call rotation
- Reducing MTTR (Mean Time To Recovery)

## Required Skill
**Skill:** `sre-practices`

## Runbook Structure
1. **Overview**
   - Service description
   - Architecture diagram
   - Key dependencies

2. **Common Operations**
   - Deployment procedures
   - Scaling operations
   - Backup and restore
   - Configuration changes

3. **Monitoring & Alerts**
   - Key metrics
   - Alert definitions
   - Dashboards and tools

4. **Troubleshooting**
   - Common issues and solutions
   - Diagnostic procedures
   - Log locations

5. **Incident Response**
   - Severity classification
   - Escalation procedures
   - Communication templates

6. **Contacts**
   - On-call rotation
   - Escalation paths
   - Vendor support

## Example Usage
```
/create-runbook

Service: Payment processing system
Team: Payments SRE
Common incidents: High latency, failed transactions, integration failures
```


## Output Deliverables
- Runbook document (Markdown)
- Quick reference cards
- Alert response playbooks

---
*Command Category: SRE Operations*  
*Version: 2.0 - Anthropic Best Practices*
*Last Updated: October 2025*
