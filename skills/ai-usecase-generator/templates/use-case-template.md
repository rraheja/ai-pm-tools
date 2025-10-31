# AI Use Case Template

---

# Use Case: [Clear, Business-Focused Name]

> **One-line description**: [Single sentence short and impactful description capturing the essence of this use case]

> **Short description**: [2-3 sentences capturing the essence of this use case]

---

## Strategic Positioning

- **Quadrant**: Q[1/2/3/4] - [Quadrant Name]
  - Q1: Know-how + Human Intervention (Traditional Digital BI/Diagnostic AI)
  - Q2: Know-how + Automation (In-context AI)
  - Q3: Actionable + Human Intervention (Fixed Step Workflows)
  - Q4: Actionable + Automation (Fully Autonomous Agents)

- **AI Actions**: [Know-how / Actionable]
  - Know-how: Provides insights, predictions, diagnostics (read-only)
  - Actionable: Generates outputs, takes actions, executes tasks

- **Human Involvement**: [Intervention / Autonomous]
  - Intervention: Requires human review, approval, or oversight
  - Autonomous: Operates independently with minimal human involvement

---

## Business Context

### Target Market
[1-2 lines describing the market segment]
- Example: Enterprise SaaS companies with 100-1000 employees
- Example: Regional healthcare providers in urban markets

### Customer  
[1-2 lines describing the specific customer persona or role]
- Example: Customer support managers seeking to reduce response times
- Example: CFOs looking to improve forecasting accuracy

### Problem Space
[1-2 lines describing the core problem being solved]
- Example: Support teams overwhelmed by repetitive tier-1 questions, leading to delayed responses and customer frustration
- Example: Manual financial forecasting processes are time-consuming and prone to errors

### Value Proposition
[1-2 lines describing the expected business value]
- Example: Reduce support costs by 30% while improving response times from 4 hours to 15 minutes
- Example: Increase forecast accuracy by 20% and reduce planning cycle time from 2 weeks to 2 days

### Competitive Differentiator
[1-2 lines describing how this feature can help differentiate]
- Example: Provide better customer experience than rest of the compeition

### Sustainable Moat
[1-2 lines describing how this differentiation can be sustained over time]
- Example: Improving the customer experience using our proprietary data will compound benefits over time, which won't be easily replicable by our competition even if they use the same AI models and duplicate this capability

---

## High-Level Considerations

### Estimated Costs
[Low / Medium / High - with brief reasoning]

**Cost Level**: [Low/Medium/High]

**Rationale**: [1-2 sentences explaining the cost assessment]

**Cost Factors**:
- Development: [Low/Medium/High]
- Infrastructure: [Low/Medium/High]
- Data: [Low/Medium/High]
- Ongoing operations: [Low/Medium/High]

**Examples:**
- Low: Leverages existing data, uses pre-trained models, limited integration
- Medium: Requires custom model training, moderate data preparation, standard integrations
- High: Extensive data collection, custom infrastructure, complex integrations, significant ongoing maintenance

---

### Key Assumptions
[1-2 critical assumptions that must hold true for success]

1. **[Assumption Category]**: [Specific assumption statement]
2. **[Assumption Category]**: [Specific assumption statement]

**Assumption Categories**: Data availability, User adoption, Technical feasibility, Regulatory approval, Budget availability, Skill availability

**Examples:**
1. **Data Availability**: Historical support tickets (12+ months) are accessible and properly labeled
2. **User Adoption**: Support agents are willing to use AI-assisted tools and provide feedback

---

## Next Steps

### Immediate Actions
1. **Prioritization**: Use the **ai-usecase-prioritization** skill to:
   - Score this opportunity using the VALUE/(RISK+COST) framework
   - Compare against other portfolio opportunities
   - Determine governance approval level required

2. **Detailed Planning**: If prioritization score warrants proceeding, use the **ai-usecase-blueprint** skill to:
   - Develop comprehensive product requirements
   - Define success metrics and KPIs
   - Create implementation roadmap
   - Specify technical architecture
   - Plan governance and risk mitigation

### Questions to Investigate
[2-3 key questions that need answers before proceeding]

**Examples:**
- What is the current volume and cost of handling these requests manually?
- What percentage of inquiries could be handled by AI vs. requiring human escalation?
- What existing systems need to integrate with this solution?

---

## Research Sources

### Internal Documents Referenced
- [List key internal documents analyzed for this use case]

### External Research
- [List key industry trends, competitor capabilities, or market insights]

### Validation Points
- [Note any evidence from research that supports this use case]

---

## Template Usage Notes

**When filling out this template:**

1. **Be Concise**: Keep each section to 1-2 lines as specified. This is a portfolio view, not a detailed spec.

2. **Focus on Business Value**: Emphasize business outcomes over technical implementation.

3. **Quadrant Accuracy**: Ensure the quadrant placement aligns with the definitions. Use the strategic-pillars.md reference if unsure.

4. **Cost Realism**: Don't underestimate costs. Consider development, infrastructure, data, operations, and maintenance.

5. **Critical Assumptions**: Identify assumptions that, if wrong, would cause the initiative to fail.

6. **Next Steps**: Always reference the ai-usecase-prioritization and ai-usecase-blueprint skills as the logical next steps.

7. **Save for Reuse**: This markdown file will be used by other skills, so maintain consistent structure and formatting.
