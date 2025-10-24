# Command: /create-lean-canvas

## Execution Context
**Primary Agent:** Product Strategy Agent  
**Required Skills:** lean-canvas  
**Command Category:** Discovery & Strategy  
**Version:** 2.0

## Purpose
Create a Lean Canvas to articulate product strategy, business model, and key assumptions in a concise, one-page format that drives validation and iteration.

## When to Use
- **Starting a new product**: Need to define business model and strategy
- **Pivoting product strategy**: Reassess assumptions and direction
- **Seeking stakeholder alignment**: Get everyone on same page about strategy
- **Validating product-market fit**: Test assumptions systematically
- **Fundraising or pitching**: Concise business model overview
- **Strategy refresh**: Revisit and update product strategy

## Required Context from User

Before executing, gather:
1. **Product/Feature Overview**: What are you building?
2. **Target Market**: Who are the customers?
3. **Problem Understanding**: What problems exist?
4. **Business Context**: Company stage, competitive landscape
5. **Constraints**: Time, budget, resources
6. **Existing Research**: Any customer insights or market data

## Task Execution Framework

### Step 1: Problem Discovery
- Identify top 3 customer problems worth solving
- Rank problems by severity and frequency
- Validate problems with customer evidence
- Consider existing alternatives customers use today

### Step 2: Customer Segmentation
- Define target customer segments
- Identify early adopters who feel pain most acutely
- Characterize customer demographics and behaviors
- Assess market size and accessibility

### Step 3: Value Proposition
- Craft single, clear, compelling value statement
- Focus on outcomes, not features
- Differentiate from alternatives
- Make it memorable and repeatable

### Step 4: Solution Design
- Identify top 3 features that address problems
- Prioritize minimum viable features
- Consider technical feasibility
- Define what makes solution unique

### Step 5: Business Model
- **Channels**: How will customers discover and buy?
- **Revenue Streams**: How will you monetize?
- **Cost Structure**: What are the major costs?
- **Key Metrics**: What numbers indicate health and progress?

### Step 6: Unfair Advantage
- Identify what can't be easily copied or bought
- Consider: insider information, existing customers, team, technology, brand
- Be honest - it's okay if this is "TBD"

### Step 7: Assumptions Documentation
- List all key assumptions in the canvas
- Prioritize riskiest assumptions to test first
- Define how to validate each assumption

## Quality Criteria

The Lean Canvas should be:
- ✅ **One page**: Fits on single page/screen for easy sharing
- ✅ **Specific**: Concrete statements, not vague generalities
- ✅ **Validated**: Based on customer research, not pure speculation
- ✅ **Actionable**: Identifies clear next steps and tests
- ✅ **Assumption-explicit**: Key unknowns are documented
- ✅ **Focused**: Limited to essential elements, not comprehensive business plan

## Example Usage

```
/create-lean-canvas

Product: AI-powered meeting assistant for remote teams
Target: Product teams at B2B SaaS companies (50-500 employees)
Context: Post-COVID, meetings have doubled but productivity hasn't
Problem: Teams spend 40% of time in meetings, struggle to track decisions and action items
Current alternatives: Manual note-taking, Otter.ai, Google Docs
Goal: Validate product-market fit before building MVP
```

## Lean Canvas Components Template

**1. Problem**
- Problem #1: [Most severe customer problem]
- Problem #2: [Second critical problem]
- Problem #3: [Third problem]
- Existing Alternatives: How people solve this today

**2. Customer Segments**
- Target Customers: [Who needs this most]
- Early Adopters: [Who will try first]

**3. Unique Value Proposition**
- Single, clear message: [Your differentiated value]
- High-level concept: [The "X for Y" pitch]

**4. Solution**
- Feature #1: [Top feature]
- Feature #2: [Second feature]
- Feature #3: [Third feature]

**5. Channels**
- Path to Customers: [How you'll reach them]

**6. Revenue Streams**
- Revenue Model: [How you'll make money]
- Lifetime Value: [Expected LTV]

**7. Cost Structure**
- Key Costs: [Major expenses]
- Customer Acquisition Cost: [Expected CAC]

**8. Key Metrics**
- Metric #1: [Most important number]
- Metric #2: [Second key metric]
- Metric #3: [Third metric]

**9. Unfair Advantage**
- [What can't be easily copied or bought]
- (It's OK to leave this blank initially)

## Adaptation Logic

**For New Products:**
- More speculation, that's okay - flag assumptions clearly
- Focus on problem validation before solution
- Keep solution section very lean (MVP mindset)

**For Existing Products (Pivot):**
- Review what you've learned from current product
- Update assumptions based on actual data
- Be brutally honest about what's not working

**For Mature Products (Strategy Refresh):**
- Use as forcing function to reassess strategy
- Challenge assumptions that may no longer be true
- Consider whether you're solving right problems

## Follow-up Recommendations

After creating the Lean Canvas:
1. **Prioritize riskiest assumptions** to test first (usually problem/market fit)
2. **Design validation experiments** for top 3 assumptions
3. **Share with stakeholders** to get alignment and feedback
4. **Revisit regularly** (monthly) as you learn and iterate
5. **Create assumption board** to track validation progress
6. **Connect to roadmap** - ensure work validates key assumptions

## Notes for Execution

- Load the Product Strategy Agent persona before beginning
- Reference lean-canvas skill for framework details and examples
- Push user to be specific and concrete, not vague
- Challenge assumptions - ask "how do you know?"
- Encourage evidence-based answers over speculation
- Create visual canvas output (table or diagram format)
- Include validation plan as separate deliverable
- Remind that canvas is living document to iterate

---

*Command Category: Discovery & Strategy*  
*Version: 2.0 - Anthropic Best Practices*  
*Last Updated: October 2025*
