# Command: /analyze-system-health

## Execution Context
**Primary Agent:** SRE Operations Agent  
**Required Skills:** sre-practices  
**Command Category:** SRE Operations  
**Version:** 2.0

## Purpose
Create system health dashboards and analysis reports for operational visibility.

## When to Use
- Regular system reviews
- SLO/SLA reporting
- Identifying performance trends
- Executive operational updates

## Required Skill
**Skill:** `sre-practices`

## Health Analysis Components
1. **Availability Metrics**
   - Uptime percentage
   - SLO compliance
   - Incident frequency

2. **Performance Metrics**
   - Response times (p50, p95, p99)
   - Throughput
   - Error rates

3. **Resource Utilization**
   - CPU, memory, storage
   - Cost efficiency
   - Capacity headroom

4. **Trends & Patterns**
   - Week-over-week comparison
   - Seasonal patterns
   - Degradation indicators

5. **Action Items**
   - Optimization opportunities
   - Scalability concerns
   - Technical debt

## Example Usage
```
/analyze-system-health

System: E-commerce platform
Time period: Last 30 days
Focus: API performance, database health, cost optimization
SLO: 99.9% uptime, p95 latency < 200ms
```


## Output Deliverables
- System health report
- Dashboard specifications
- Improvement recommendations

---
*Command Category: SRE Operations*  
*Version: 2.0 - Anthropic Best Practices*
*Last Updated: October 2025*
