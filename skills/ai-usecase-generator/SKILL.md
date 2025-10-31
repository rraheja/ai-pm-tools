---
name: ai-usecase-generator
description: Analyze organization documents, market research, and customer feedback to generate a strategic portfolio of top 5 AI use case ideas. Maps ideas to the Strategic Pillars Quadrant (AI Actions vs Human Involvement) with high-level summaries. Use when helping organizations identify AI opportunities, build AI strategy, or create an AI use case portfolio. Does not prioritize (use ai-usecase-prioritization) or create detailed specs (use ai-usecase-blueprint).
allowed-tools: Read, Write, Grep, Glob, WebSearch
---

# AI Use Case Generator

Generate a strategic portfolio of AI use cases by analyzing organizational context, market intelligence, and customer needs. Output a curated list of 5 AI opportunities mapped to strategic pillars with high-level details for executive review.

## Purpose

Systematic discovery methodology for identifying AI opportunities by analyzing organizational documents, market intelligence, and industry trends to generate a portfolio of 5 strategically-mapped use case ideas with high-level summaries for executive decision-making.

## When to Use This Skill

Use this skill when users need to:
- Identify AI opportunities for their organization
- Build an AI strategy portfolio from scratch
- Analyze organizational readiness for AI initiatives
- Map potential AI use cases to strategic positioning
- Generate executive-ready AI opportunity summaries

**This skill focuses on DISCOVERY, not prioritization or detailed planning.** After using this skill, let the user know they can:
- Use **ai-usecase-prioritization** to score and rank the identified opportunities
- Use **ai-usecase-blueprint** to create detailed specifications for selected use cases

## When NOT to Use

- User needs prioritization scoring (use ai-usecase-prioritization instead)
- User needs detailed product requirements or specifications (use ai-usecase-blueprint instead)
- User already has specific AI use cases and needs implementation plans
- User needs technical architecture or development guidance
- Organization is seeking compliance or governance frameworks only

## Process Overview

### Phase 1: Gather Context
1. **Identify Industry**: Ask user for industry/sector if not clear from documents
2. **Request Key Documents** (if not already uploaded):
   - Vision/mission/strategy documents
   - Annual reports or business plans
   - Customer feedback/VOC data
   - Support ticket summaries or top issues
   - Competitive intelligence (if available)

3. **Automatic Web Research**:
   - If any of the above documents are not available from the user, identify if they are available via a web search
   - Top 3 industry AI trends (from analyst reports, industry publications)
   - Top 3 competitors' AI capabilities (focus on industry analyst assessments)
   - Market sentiment and AI adoption patterns for the industry

### Phase 2: Analysis
1. **Document Analysis**: Extract from uploaded materials:
   - Strategic goals and business objectives
   - Customer pain points and unmet needs
   - Capability gaps and operational inefficiencies
   - Revenue targets and growth areas
   - Risk factors and constraints

2. **Synthesis**: Identify 7-10 potential AI use cases that:
   - Align with strategic goals
   - Address customer pain points
   - Fill capability gaps
   - Leverage industry best practices
   - Consider competitive positioning

3. **Filter to Top 5**: Select the most promising based on:
   - Strategic alignment
   - Feasibility indicators
   - Market validation (competitors/trends)
   - Customer value potential

### Phase 3: Strategic Mapping

Map each use case to the **Strategic Pillars Quadrant**:

**X-Axis: AI Actions**
- **Know-how**: Read-only AI (insights, predictions, diagnostics)
- **Actionable**: AI that takes action (generates outputs, executes tasks)

**Y-Axis: Human Involvement**
- **Human Intervention**: Requires human review, approval, or oversight
- **Autonomous**: AI operates independently with minimal human involvement

**Four Quadrants**:
1. **Q1: Know-how + Human Intervention** = Traditional Digital BI/Diagnostic AI
   - Business intelligence dashboards with AI insights
   - Predictive analytics with human interpretation
   - Diagnostic tools requiring expert validation

2. **Q2: Know-how + Automation** = In-context AI  
   - Personalized content recommendations
   - Automated forecasting and predictions
   - Real-time insights and alerts

3. **Q3: Actionable + Human Intervention** = Fixed Step Workflows
   - AI-generated content with human review
   - Assisted workflows with restricted tool access
   - Draft automation requiring approval

4. **Q4: Actionable + Automation** = Fully Autonomous Agents
   - Self-service AI agents (chatbots, assistants)
   - Autonomous process automation
   - AI systems that think, reason, and act independently

### Phase 4: Output Generation

For each use case, create a **high-level summary** following the structure in `templates/use-case-template.md`. Fill all fields defined in that template to ensure future template updates are automatically incorporated.

**Important**: Keep each field to 2-3 lines maximum. This is a portfolio view, not detailed planning.

---

## Strategic Pillars Quadrant Framework

The Strategic Pillars Quadrant is a 2x2 matrix for classifying AI initiatives:

### Quadrant Axes

**X-Axis: AI Actions** (What the AI produces)
- **Know-how (Left)**: Provides information, insights, predictions, diagnostics (read-only)
- **Actionable (Right)**: Generates outputs, takes actions, executes tasks

**Y-Axis: Human Involvement** (Control & oversight)
- **Human Intervention (Bottom)**: Requires review, approval, or active oversight
- **Autonomous (Top)**: Operates independently with minimal human involvement

### The Four Quadrants

**Q1: Know-how + Human Intervention = Traditional Digital BI/Diagnostic AI**
- Provides insights and analysis for human decision-making
- Requires expert interpretation and validation
- Examples: BI dashboards with AI insights, predictive analytics requiring review, diagnostic support systems

**Q2: Know-how + Automation = In-context AI**
- Automatically generates insights without human input
- Continuously operates and adapts
- Examples: Personalized recommendations (Netflix), automated forecasting, real-time monitoring and alerts

**Q3: Actionable + Human Intervention = Fixed Step Workflows**
- AI generates outputs or drafts for review
- Human approval required before execution
- Examples: AI-generated content with editorial review, assisted workflows, draft automation requiring approval

**Q4: Actionable + Automation = Fully Autonomous Agents**
- End-to-end automation without human involvement
- Thinks, reasons, and acts independently
- Examples: Customer service chatbots with full resolution, automated order processing, autonomous trading systems

### Quadrant Placement Decision Tree

**Step 1: Determine X-Axis**
Ask: "What does the AI produce?"
- Information/insights/predictions → **Know-how** (Q1 or Q2)
- Outputs/actions/execution → **Actionable** (Q3 or Q4)

**Step 2: Determine Y-Axis**
Ask: "Can the AI operate without human approval?"
- Human review/approval required → **Human Intervention** (Q1 or Q3)
- Operates independently → **Autonomous** (Q2 or Q4)

**Step 3: Cross-Reference**
| AI Actions → | Know-how | Actionable |
|---|---|---|
| **Autonomous ↑** | Q2 | Q4 |
| **Human Intervention ↓** | Q1 | Q3 |

**Common Misclassifications to Avoid**:
- Confusing human usage with human intervention (chatbot users ≠ Q1/Q3)
- Treating all recommendations as know-how (if AI executes → Actionable)
- Overweighting minor touchpoints (setup/config ≠ intervention)

**For detailed industry examples and real-world use cases, see `templates/industry-examples.md`**

---

## Document Analysis Methodology

### Strategic Goals Extraction
**What to Look For**: Revenue targets, market position aspirations, efficiency goals, customer satisfaction targets, innovation initiatives

**Analysis Prompts**:
- What business outcomes is the organization trying to achieve?
- What metrics define success?
- Are there explicit AI or digital transformation statements?

### Pain Points Identification
**What to Look For**: Complaint themes, top support categories, operational bottlenecks, cost inefficiencies, manual processes described as "time-consuming" or "error-prone"

**Analysis Prompts**:
- What problems are customers repeatedly experiencing?
- What processes are slow, manual, or inefficient?
- Where is the organization losing money or missing opportunities?

### Capability Gaps Analysis
**What to Look For**: Statements about lacking capabilities ("We need to...", "Currently unable to..."), competitive disadvantages, unfulfilled customer requests, technology debt

**Analysis Prompts**:
- What capabilities does the organization wish it had?
- What are competitors doing that this organization isn't?
- What customer requests can't currently be fulfilled?

### Synthesis: From Analysis to Use Cases

**Step 1: Identify Themes**
Group findings: Customer-facing, Operational efficiency, Revenue growth, Risk mitigation, Employee experience

**Step 2: Map to Strategic Goals**
For each theme:
- Which strategic goal does this support?
- What specific pain point does this address?
- What capability gap does this fill?
- Is there market validation (competitors/trends)?

**Step 3: Generate Use Case Ideas**
Define: What (specific AI application), Who (target user), Why (business value), How (AI approach)

**Step 4: Validate and Filter**
Assess: Strategic alignment, Customer value, Feasibility, Differentiation

**Step 5: Select Top 5**
Balance: Multiple quadrants, Quick wins vs. strategic bets, Different stakeholders, Offensive and defensive plays

**For detailed extraction examples and methodology walkthroughs, see `templates/industry-examples.md`**

---

## Output Formats

### 1. Strategic Pillars Quadrant Visualization
Create a 2x2 matrix showing all 5 use cases positioned by:
- X-axis: Know-how ← → Actionable
- Y-axis: Human Intervention ← → Autonomous

### 2. Use Case Summary Table
Generate a comparison table with columns:
| # | Use Case | Quadrant | Target Market | Customer | Problem | Value Prop | Cost |
|---|----------|----------|---------------|----------|---------|------------|------|

### 3. Individual Markdown Files
Save each use case to a separate markdown file: `usecase_01_[name].md` through `usecase_05_[name].md`

**Use the template structure defined in `templates/use-case-template.md`** - fill all fields present in that template. This ensures any future template updates are automatically incorporated into generated use cases.

### 4. Format Options
After generating the portfolio, ask the user which format they prefer:
- **Markdown files** (already generated)
- **Word document** (.docx) - consolidated report
- **PDF** - executive presentation format
- **PowerPoint** (.pptx) - slide deck with quadrant and tables

## Best Practices

### Scope and Focus
- **Stay High-Level**: This is portfolio discovery, not detailed planning (keep fields to 2-3 lines)
- **Limit to 5**: More than 5 creates decision paralysis; fewer than 5 lacks optionality
- **Balanced Portfolio**: Ensure use cases span all four quadrants for strategic diversity
- **Industry Agnostic**: Don't assume an industry unless specified or obvious from documents
- **Save Markdown**: Individual files per use case enable other skills to process them without re-reading source documents

### Web Search Strategy
- **Industry Trends**: Search for "[industry] AI trends 2024 2025", "[industry] artificial intelligence adoption"
- **Competitor Analysis**: Search for "top AI implementations [industry]", "[competitor name] AI strategy"
- **Analyst Reports**: Prioritize Gartner, Forrester, McKinsey reports when available
- Limit to top 3 trends and top 3 competitors to avoid information overload

### Document Analysis Tips
- Look for explicit strategy statements (vision, mission, goals)
- Identify repeated themes in customer feedback
- Note gaps between aspirations and current capabilities
- Pay attention to risk factors and constraints mentioned

### Use Case Generation
- **Specificity**: "AI-powered customer support chatbot" not "improve customer service"
- **Actionability**: Focus on concrete applications, not abstract concepts
- **Strategic Fit**: Every use case should tie to organizational goals
- **Feasibility Indicators**: Consider data availability, technical maturity, skill requirements

### Quadrant Placement Logic
Ask: "What does the AI do?" and "Who controls it?"
- **Know-how** = AI provides information, insights, predictions (READ)
- **Actionable** = AI generates outputs, takes actions, executes tasks (WRITE/DO)
- **Human Intervention** = Requires approval, review, or active oversight
- **Autonomous** = Operates independently with minimal human involvement

### Skill Integration
- **No Prioritization**: Score and rank in separate skill (ai-usecase-prioritization)
- **No Deep Specs**: Detailed requirements in separate skill (ai-usecase-blueprint)

## Common Patterns by Industry

When analyzing organizations, consider these typical AI opportunity patterns (not exhaustive):
- **Financial Services**: Fraud detection (Q2), personalized advice (Q1), automated trading (Q4), loan processing (Q3)
- **Healthcare**: Diagnostic support (Q1), patient monitoring (Q2), administrative automation (Q4), care coordination (Q3)
- **Retail/E-commerce**: Recommendations (Q2), inventory optimization (Q2), chatbots (Q4), dynamic pricing (Q3)
- **Manufacturing**: Predictive maintenance (Q1), quality inspection (Q2), autonomous robots (Q4), assisted workflows (Q3)
- **Technology/SaaS**: Code generation (Q3), customer support (Q4), analytics (Q1), automated testing (Q3)

**For detailed industry-specific examples with real-world context, see `templates/industry-examples.md`**

## Input Dependencies

**Optional Inputs** (all optional, LLM decides whether to use or ask user):

**From ai-market-trends skill** (if available):
- `swot-analysis.md` - Strategic goals, competitive positioning, market opportunities
- `industry-trends.md` - Industry context, growth drivers, technology shifts
- `competitive-landscape.md` - Competitor capabilities and differentiation gaps
- `market-overview.md` or `company-analysis.md` - Company profile and strategic priorities

**From user-provided documents** (if available):
- Vision/mission/strategy documents
- Annual reports or business plans
- Customer feedback/VOC data
- Support ticket summaries or top issues
- Competitive intelligence

**Note**: This skill can work independently with web research if no prior artifacts are available. The LLM should assess what's available and either use existing artifacts or conduct fresh research as needed.

---

## Integration with Other Skills

After completing this skill:

1. **Prioritization**: Direct users to **ai-usecase-prioritization** skill to:
   - Score each use case using VALUE/(RISK+COST) framework
   - Create priority rankings with governance thresholds
   - Generate portfolio visualization (Stars/Moons/Ground/Blackholes)

2. **Detailed Planning**: For selected use cases, use **ai-usecase-blueprint** skill to:
   - Develop comprehensive product requirements
   - Define success metrics and KPIs
   - Create implementation roadmaps
   - Specify technical architecture
   - Plan governance and risk mitigation

## Common Scenarios

**Scenario 1: New AI Strategy Development**
User has strategic documents and wants to build their first AI portfolio. Analyze vision/mission, identify 10 opportunities across all quadrants, prioritize quick wins vs. strategic bets.

**Scenario 2: Portfolio Review and Refresh**
User has existing AI initiatives but wants to identify new opportunities. Gather current portfolio, perform gap analysis, generate complementary use cases in underrepresented quadrants.

**Scenario 3: Competitive Response**
User sees competitors launching AI capabilities and needs to respond. Research competitor capabilities, identify competitive parity opportunities (Q2/Q4), recommend differentiation plays (Q1/Q3).

**Scenario 4: Limited Documentation Available**
User lacks comprehensive documents. Rely on web research for industry trends and competitor analysis, conduct interactive discovery through questions, generate use cases based on common industry patterns.

**Scenario 5: Specific Domain Focus**
User wants AI opportunities for specific function (customer service, operations, sales). Filter analysis to relevant domains, generate targeted 5 use cases, ensure balanced quadrant distribution within scope.

## Common Pitfalls

### Analysis Pitfalls
- **Technology-First Thinking**: Starting with "let's use GPT-4" instead of identifying business problems
- **Ignoring Constraints**: Overlooking regulatory, technical, or budgetary limitations
- **Over-Scope**: Generating vague use cases like "AI-powered transformation" instead of specific applications
- **Under-Diversification**: All use cases in one quadrant (typically Q4) instead of balanced portfolio

### Quadrant Mapping Pitfalls
- **Confusing Human Usage with Human Intervention**: Thinking chatbot users = Q1/Q3, when it's actually Q4
- **Treating All Recommendations as Know-how**: Missing that AI executing actions = Actionable (Q3/Q4)
- **Overweighting Minor Touchpoints**: Considering setup/configuration as "intervention"

### Research Pitfalls
- **Information Overload**: Researching too many competitors or trends instead of limiting to top 3
- **Ignoring Market Reality**: Assuming revolutionary capabilities when competitors already have parity
- **Cherry-Picking Examples**: Only using successful AI stories without considering failures

### Output Pitfalls
- **Excessive Detail**: Writing detailed specs instead of high-level summaries (1-2 lines per field)
- **Missing Assumptions**: Not documenting critical assumptions about data, skills, or budget
- **No Strategic Link**: Use cases that don't tie to organizational goals
- **Unrealistic Costs**: Underestimating implementation or operational costs

## Quick Reference

```
PROCESS: Gather Context → Analyze → Map to Quadrants → Generate Outputs

QUADRANTS:
Q1: Know-how + Intervention (BI/Diagnostics)
Q2: Know-how + Autonomous (In-context AI)
Q3: Actionable + Intervention (Workflows)
Q4: Actionable + Autonomous (Agents)

OUTPUT: 5 use cases with:
- Name, Quadrant, Target Market, Customer
- Problem, Value Prop, Cost Estimate

FORMATS: Markdown files, Table, Quadrant viz, DOCX/PDF/PPTX

NEXT STEPS:
→ ai-usecase-prioritization (score & rank)
→ ai-usecase-blueprint (detailed specs)
```

## Example Usage

```
User: "Help me identify AI opportunities for our healthcare company"

You: 
1. Requests industry confirmation: "I see you're in healthcare. Is this specifically hospital systems, medical devices, pharma, or another healthcare sector?"

2. Requests documents: "To identify the best AI opportunities, please upload:
   - Strategic plan or vision documents
   - Recent customer feedback or patient satisfaction data
   - Top support issues or operational challenges
   
   If these aren't available, I can work with publicly available information."

3. Performs web research: [Searches for healthcare AI trends, competitor analysis]

4. Analyzes and generates: [Creates 5 use cases with quadrant mapping]

5. Outputs:
   - Strategic Pillars Quadrant visualization
   - Comparison table of all 5 use cases
   - Individual markdown files
   - "Would you like this in Word, PDF, or PowerPoint format?"

6. Next steps: "To prioritize these opportunities, use the ai-usecase-prioritization skill. To develop detailed specs for any use case, use the ai-usecase-blueprint skill."
```

## Output Deliverables

- **Strategic Pillars Quadrant Visualization** - 2x2 matrix with all 5 use cases positioned
- **Use Case Summary Table** - Comparison table with all key fields
- **Individual Markdown Files** - One file per use case (`usecase_01_[name].md` through `usecase_05_[name].md`)
- **Executive Summary Report** - Consolidated analysis with recommendations
- **Format Options** - Available in Markdown, Word (.docx), PDF, or PowerPoint (.pptx)
- **Next Steps Guidance** - Clear direction to ai-usecase-prioritization and ai-usecase-blueprint skills

## References

**Reference files (load as needed)**:
- `templates/use-case-template.md` - Markdown output template structure (always use this for generating use case files)
- `templates/industry-examples.md` - Detailed industry-specific examples, real-world use cases, and methodology walkthroughs (load when user needs deeper context or industry-specific guidance)

**When to load industry-examples.md**:
- User asks for specific industry examples beyond brief mentions above
- User needs detailed use case patterns for their industry
- User questions why a use case belongs in a specific quadrant
- User wants real-world validation or competitive intelligence examples
- User requests document analysis walkthroughs

**Do NOT load industry-examples.md** for standard use case generation—this SKILL.md contains sufficient guidance for most scenarios.
