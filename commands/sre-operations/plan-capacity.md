# Command: /plan-capacity

## Execution Context
**Primary Agent:** SRE Operations Agent  
**Required Skills:** sre-practices  
**Command Category:** SRE Operations  
**Version:** 2.0

## Purpose
Forecast infrastructure capacity needs and plan for growth.

## When to Use
- Quarterly capacity planning
- Before major launches
- Cost optimization initiatives
- Scaling preparations

## Required Skill
**Skill:** `sre-practices`

## Capacity Plan Components
1. **Current State**
   - Resource utilization (CPU, memory, storage, network)
   - Cost breakdown
   - Performance metrics

2. **Growth Projections**
   - User growth forecasts
   - Transaction volume trends
   - Data storage projections

3. **Capacity Requirements**
   - Compute needs
   - Storage expansion
   - Network bandwidth
   - Database scaling

4. **Scaling Strategy**
   - Horizontal vs vertical scaling
   - Auto-scaling policies
   - Geographic expansion

5. **Cost Analysis**
   - Current spend
   - Projected costs
   - Optimization opportunities

6. **Risk Mitigation**
   - Single points of failure
   - Redundancy plans
   - Disaster recovery

## Example Usage
```
/plan-capacity

Current: 100K DAU, 5TB storage
Projected: 500K DAU by Q4
Infrastructure: AWS, multi-region
Budget: $200K/month capacity target
```


## Output Deliverables
- Capacity plan document
- Cost forecast
- Scaling recommendations

---
*Command Category: SRE Operations*  
*Version: 2.0 - Anthropic Best Practices*
*Last Updated: October 2025*
