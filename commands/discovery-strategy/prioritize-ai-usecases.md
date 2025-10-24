# Command: /prioritize-ai-usecases

## Execution Context
**Primary Agent:** Product Strategy Agent  
**Required Skills:** ai-usecase-prioritization  
**Command Category:** Discovery & Strategy  
**Version:** 2.0

## Purpose
Systematically evaluate and prioritize AI initiatives using a rigorous VALUE/(RISK+COST) framework to guide investment decisions and resource allocation. This command produces a comprehensive analysis with visual dashboards suitable for executive decision-making.

## When to Use
- **Portfolio planning**: Multiple AI projects competing for limited resources
- **Vendor evaluation**: Comparing build vs. buy vs. partner options for AI capabilities
- **Strategic planning**: Creating multi-year AI investment roadmaps
- **Stakeholder alignment**: Need objective framework for prioritization discussions
- **Budget justification**: Building business cases for AI investments
- **Quarterly planning**: Re-evaluating and re-prioritizing existing AI initiatives

## Required Context from User

Before executing, gather:
1. **AI Initiatives**: List of AI use cases or projects under consideration (3-10 items)
2. **Business Context**: Strategic priorities, constraints, competitive pressures
3. **Current State**: Existing AI capabilities, infrastructure, team expertise
4. **Timeline**: When decisions need to be made
5. **Stakeholders**: Who will review and approve the prioritization
6. **Success Criteria**: What a successful prioritization looks like

## Task Execution Framework

### Step 1: Context Discovery & Initiative Definition
- Understand each AI initiative at a high level
- Clarify business objectives and expected outcomes
- Identify stakeholders and decision-makers
- Note any must-haves or constraints

### Step 2: Comparative Analysis
Create a side-by-side comparison matrix covering:
- **Problem Statement**: What problem does each initiative solve?
- **Target Users**: Who benefits from this AI capability?
- **Current Alternative**: How is this problem solved today?
- **Expected Impact**: Business metrics that will improve
- **Dependencies**: Technical, data, or organizational prerequisites
- **Timeline**: Estimated time to production
- **Strategic Alignment**: How it supports company strategy

### Step 3: Systematic Scoring
Evaluate each initiative across 7 criteria using the VALUE/(RISK+COST) framework:

**VALUE Dimensions (0-10 scale):**
1. **Business Impact**: Revenue, cost savings, competitive advantage
2. **Strategic Alignment**: Fit with company vision and priorities
3. **User Value**: Magnitude of benefit to end users
4. **Feasibility**: Technical complexity and data availability

**RISK Dimensions (0-10 scale):**
5. **Technical Risk**: Novelty, complexity, unproven technology
6. **Business Risk**: Market uncertainty, competitive response, regulatory

**COST Dimensions:**
7. **Implementation Cost**: Development, infrastructure, third-party costs

Calculate final score: **VALUE / (RISK + COST)**

### Step 4: Documentation & Justification
For each initiative, document:
- Scoring rationale for each dimension with specific evidence
- Key assumptions and data sources
- Risks and mitigating factors
- Dependencies and prerequisites
- Recommended next steps

### Step 5: Prioritization Dashboard Creation
Generate Excel workbook with:

**Sheet 1: Comparison Matrix**
- Side-by-side initiative comparison
- Key attributes in table format
- Color-coded priority indicators

**Sheet 2: Scoring Details**
- Detailed scoring for each criterion
- Justification notes
- Calculation formulas
- Final prioritization ranking

**Sheet 3: Visualizations**
- Bubble chart: Value vs. Risk (size = Cost)
- Priority tiers (High/Medium/Low)
- Bar chart: Score comparison
- Radar chart: Dimension breakdown

**Sheet 4: Recommendations**
- Tiered recommendations (Invest Now, Evaluate Further, Defer)
- Portfolio balance analysis
- Implementation sequencing suggestions
- Resource allocation guidance

### Step 6: Strategic Recommendations
Provide executive summary with:
- **Top 3 priorities** with clear rationale
- **Portfolio strategy**: Balance of quick wins vs. transformational bets
- **Sequencing logic**: Dependencies and optimal order
- **Resource requirements**: Team, budget, infrastructure needs
- **Risk mitigation**: How to de-risk top priorities
- **Decision framework**: How to use this for ongoing prioritization

## Quality Criteria

The prioritization should be:
- ✅ **Objective**: Based on defined criteria, not politics or opinions
- ✅ **Data-driven**: Grounded in market research, user feedback, technical assessment
- ✅ **Transparent**: Clear methodology that stakeholders can validate
- ✅ **Actionable**: Produces clear go/no-go decisions
- ✅ **Balanced**: Considers multiple dimensions (not just ROI)
- ✅ **Stakeholder-aligned**: Addresses concerns of different audiences
- ✅ **Defensible**: Can withstand scrutiny and questions

## Example Usage

```
/prioritize-ai-usecases

I have 5 AI initiatives to prioritize for 2025:

1. AI-Powered Code Review Assistant
   - Automated code quality and security scanning
   - Target: 200 engineering team
   - Expected: 20% reduction in bugs

2. Customer Support Chatbot
   - Handles tier-1 support questions
   - Target: 10K monthly support tickets
   - Expected: 40% deflection rate

3. Personalized Product Recommendations
   - ML-based recommendation engine
   - Target: 1M monthly active users
   - Expected: 15% increase in conversion

4. Predictive Demand Forecasting
   - Inventory and capacity planning
   - Target: Supply chain operations
   - Expected: $2M annual savings

5. AI-Enhanced Search
   - Natural language search with semantic understanding
   - Target: All product users
   - Expected: 25% improvement in search success rate

Context:
- We're a B2B SaaS company with 50M ARR
- Engineering team of 200, no dedicated ML team yet
- Limited AI/ML infrastructure currently
- CEO wants to see AI strategy next month
```

## Adaptation Logic

**For 3-5 initiatives:**
- Full detailed analysis appropriate
- Can go deep on each dimension
- Include detailed recommendation section

**For 6-10 initiatives:**
- May need to group similar initiatives
- Focus scoring discussion on top contenders
- Provide tiered recommendations (High/Med/Low)

**For 10+ initiatives:**
- Recommend initial filtering to reduce list
- Use rapid scoring first, then detailed analysis on top candidates
- Consider portfolio view with categories (e.g., revenue, efficiency, innovation)

**For build vs. buy decisions:**
- Add comparison of in-house vs. vendor vs. partner
- Include make/buy decision framework
- Consider strategic control and differentiation

## Follow-up Recommendations

After creating prioritization:
1. **Stakeholder review session** (2-hour workshop to validate scores)
2. **Deep-dive analysis** on top 2-3 initiatives (business cases, technical specs)
3. **Quarterly re-prioritization** as new data emerges
4. **Resource allocation plan** mapping initiatives to teams
5. **Success metrics definition** for selected initiatives

## Notes for Execution

- Load the Product Strategy Agent persona before beginning
- Reference ai-usecase-prioritization skill for framework details and templates
- Be rigorous about scoring - avoid grade inflation
- Call out uncertainties and assumptions explicitly
- Consider portfolio balance, not just individual scores
- Think about organizational change management, not just technical feasibility
- Create Excel file using Python with proper formatting and charts
- Provide both summary and detailed views for different audiences

---

*Command Category: Discovery & Strategy*  
*Version: 2.0 - Anthropic Best Practices*  
*Last Updated: October 2025*
