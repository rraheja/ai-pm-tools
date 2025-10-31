# Command: /prioritize-ai-usecases

## Execution Context
**Primary Agent:** Product Strategy Agent
**Required Skills:** ai-usecase-prioritization
**Command Category:** Discovery & Strategy
**Version:** 2.0

## Purpose
Systematically evaluate and prioritize AI initiatives using VALUE/(RISK+COST) framework. Produces Excel dashboards with objective 0-100 scores for executive decision-making.

## When to Use
- Portfolio planning with multiple AI projects competing for resources
- Vendor evaluation (build vs. buy vs. partner)
- Strategic planning for multi-year AI roadmaps
- Budget justification for AI investments
- Quarterly re-prioritization of initiatives

## Execution
Use **ai-usecase-prioritization** skill - see [skills/ai-usecase-prioritization/SKILL.md](../../skills/ai-usecase-prioritization/SKILL.md) for complete methodology including:
- VALUE/(RISK+COST) scoring framework with detailed rubrics
- Comparison matrix and scoring templates
- Excel dashboard generation with visualizations
- Portfolio recommendations and tiering

## Example Usage
```
/prioritize-ai-usecases

I have 5 AI initiatives to prioritize:
1. AI Code Review Assistant (200 engineers, 20% bug reduction)
2. Customer Support Chatbot (10K tickets/month, 40% deflection)
3. Personalized Recommendations (1M users, 15% conversion lift)
4. Predictive Demand Forecasting (Supply chain, $2M savings)
5. AI-Enhanced Search (All users, 25% search improvement)

Context: B2B SaaS, 50M ARR, 200 engineers, no ML team yet
```

---

*Command Category: Discovery & Strategy*
*Version: 2.0 - Streamlined*
*Last Updated: October 2025*
