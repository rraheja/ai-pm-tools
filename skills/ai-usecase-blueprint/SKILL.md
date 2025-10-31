---
name: ai-usecase-blueprint
description: Transform AI use case concepts into comprehensive product blueprints with detailed specifications for executives and product managers. Creates strategic plans covering business model, architecture, responsible AI, economics, and execution roadmap. Use when an AI use case has been identified and prioritized, and needs detailed planning before PRD creation. Does not create PRDs, epics, or user stories (use separate skills for implementation details).
allowed-tools: Read, Write, Grep, Glob, WebSearch
---

# AI Use Case Blueprint

Transform prioritized AI use cases into comprehensive, executive-ready product blueprints that bridge strategy and execution with detailed specifications for business, architecture, responsible AI, and go-to-market planning.

## Purpose

Systematic methodology for developing detailed AI product specifications that translate strategic use case concepts into actionable blueprints covering all critical dimensions: business model, technical architecture, responsible AI governance, unit economics, pricing strategy, and phased execution with measurable success criteria.

## When to Use This Skill

Use this skill when you need to:
- Develop comprehensive specifications for a prioritized AI use case
- Create executive-ready documentation for AI product approval
- Define detailed architecture, economics, and governance for AI initiatives
- Plan phased rollout with quarterly milestones and success criteria
- Establish responsible AI framework and compliance approach
- Design pricing strategy and monetization model for AI features
- Bridge the gap between strategic use case and implementation planning

**This skill focuses on DETAILED PLANNING, not implementation.** After using this skill:
- Use **PRD creation skills** for detailed product requirements documents
- Use **epic/user story skills** for agile development planning
- Leverage blueprint outputs to inform technical design and architecture reviews

## When NOT to Use

- User needs just a high-level use case description (use ai-usecase-generator instead)
- User needs prioritization and scoring (use ai-usecase-prioritization instead)
- User needs implementation-level PRD or user stories (use separate implementation skills)
- User needs detailed sprint planning or resource allocation
- AI use case has not yet been validated or prioritized

## Process Overview

### Phase 1: Gather Context & Inputs

1. **Use Case Inputs** (all optional, use if available):
   - Markdown from `ai-usecase-generator` skill
   - Prioritization scores from `ai-usecase-prioritization` skill
   - User-provided use case descriptions
   - Strategic documents or constraints

2. **Clarify Scope and Preferences**:
   - Confirm use case strategic positioning (quadrant)
   - Identify target audience for blueprint (executives, PM team, board)
   - Determine output preferences (full blueprint, lean canvas, format conversion)
   - Gather additional context via questions

3. **Research & Validation**:
   - Review similar AI products for benchmarks
   - Research pricing models in the industry
   - Identify relevant compliance requirements
   - Gather technical architecture patterns

### Phase 2: Blueprint Development

Create comprehensive specifications across 8 core dimensions:

**1. Executive Summary** (1 page)
- Use case overview and strategic positioning
- Value proposition and expected ROI
- Key risks and mitigation strategies
- Recommended approach and go/no-go assessment

**2. Business & Monetization**
- Detailed value proposition and target market
- Competitive landscape and differentiation
- Pricing strategy analysis (4 archetypes with recommendation)
- Unit economics and financial model
- ROI calculations and payback period

**3. User Experience & Adoption**
- User personas and journey maps
- Adoption strategy and change management
- Training and enablement requirements
- Success criteria and engagement metrics

**4. Technical Architecture**
- High-level system diagram (ASCII + Mermaid)
- Component specifications and data flows
- AI/ML stack and model serving architecture
- Integration points and dependencies
- Scalability and performance considerations

**5. Economics & Cost**
- Comprehensive cost breakdown (data, infrastructure, model licensing, operations)
- Scaling cost projections
- Cost containment strategies (caching, model routing, optimization)
- Unit economics (cost per user, per transaction, per inference)
- Break-even analysis

**6. Performance & Evaluations**
- CLASSic metrics framework (Cost, Latency, Accuracy, Safety, Security)
- Evaluation strategy (groundedness, relevance, hallucination detection)
- Benchmarks and performance targets
- Testing approach and quality gates

**7. Responsible AI & Governance**
- RAI principles and ethical framework
- Guardrails and safety measures
- Bias detection and mitigation strategies
- Monitoring and observability requirements
- Compliance framework (GDPR, HIPAA, ISO 42001, NIST AI RMF)
- Governance structure and approval processes
- Audit trail and transparency requirements

**8. Execution Roadmap** (Quarterly)
- Q1-Q4 milestone definitions
- Success criteria per quarter
- Adoption metrics and targets
- Key dependencies and risks
- Resource requirements (high-level)

### Phase 3: Output Generation

Generate deliverables based on user preferences:

**1. Comprehensive Blueprint** (Markdown - Always)
- Full specification following `templates/blueprint-template.md`
- 14-16 pages of detailed documentation
- Executive-ready with clear sections

**2. One-Page Lean Canvas** (Optional)
- AI-adapted Lean Canvas following `templates/lean-canvas-template.md`
- Single-page strategic overview
- Suitable for executive briefings

**3. Format Conversion** (Optional)
- PDF, DOCX, PPTX conversion guidance
- Use existing markdown via `templates/format-conversion-guide.md`
- Skip full skill re-run if markdown already exists

---

## Blueprint Sections Framework

### Executive Summary Components

**Use Case Overview**:
- Name, one-line description, strategic quadrant positioning
- Problem being solved and target users
- Expected business impact (quantified)

**Value Proposition & ROI**:
- Key benefits to customers and business
- Estimated ROI with assumptions
- Time to value and payback period

**Key Risks & Mitigations**:
- Top 3 risks with mitigation strategies
- Governance requirements
- Prerequisites for success

**Recommendation**:
- Go/No-Go assessment with rationale
- Recommended next steps
- Decision criteria for leadership

### Pricing Strategy Framework

Analyze all 4 pricing archetypes from the presentation with pros/cons:

**1. Subscription / Seat-Based**
- **Model**: Fixed monthly/annual fee per user
- **Best For**: Workflow products with human-in-loop, predictable usage
- **Examples**: ChatGPT Plus ($20/user), Cursor, Canva
- **Pros**: Predictable revenue, proven SaaS model, easy to understand
- **Cons**: Cost overruns if single user drives high usage, may leave revenue on table

**2. Consumption / Usage-Based**
- **Model**: Pay per API call, token, GPU hour, or transaction
- **Best For**: Developer tools, infrastructure, variable workloads
- **Examples**: Hyperscalers (AWS, Azure, GCP), OpenAI API, Anthropic API
- **Pros**: Scales with value, aligns cost to usage
- **Cons**: Meter anxiety, unpredictable bills, hard to forecast

**3. Outcome / Value-Based**
- **Model**: Charge based on business outcome delivered
- **Best For**: Proven KPI improvement, autonomous agents with measurable ROI
- **Examples**: Salesforce Agentforce ($2/conversation), charge per lead converted, per fraud detected
- **Pros**: Win-win alignment, premium pricing for proven value
- **Cons**: Requires clear attribution, customer hesitation if ROI unclear

**4. Hybrid / Seat + Usage**
- **Model**: Base subscription + usage overage charges
- **Best For**: Balancing predictability with usage flexibility
- **Examples**: Many AI SaaS products with tiered models and usage limits
- **Pros**: Best of both worlds, accommodates different usage patterns
- **Cons**: Complex implementation, potential user confusion

**For the recommended archetype**: Provide detailed pricing including example tiers, pricing levels, usage limits, and rationale tied to AI autonomy level and proven value.

### Technical Architecture Specification

**High-Level System Diagram**:
- Provide both ASCII and Mermaid-compliant diagram
- Show: Data sources → AI Stack → Application Layer → User Interface
- Include: Feedback loops, human-in-loop integration points, monitoring

**Component Specifications**:
- Data ingestion and pipeline architecture
- Feature store and data versioning
- Model serving infrastructure (real-time, batch)
- Agent orchestration and reasoning engine
- API layer and integration points
- Monitoring and observability stack
- Feedback collection and model retraining

**Reference**: Use `templates/tech-architecture-guide.md` for diagram patterns and detailed component specifications.

### Responsible AI Framework

**High-Level Principles**:
- Fairness: Equitable treatment across user segments
- Transparency: Explainable AI outputs and decision-making
- Accountability: Clear ownership and governance
- Privacy: Data protection and user control
- Safety: Harm prevention and risk mitigation

**Operational Implementation**:
- **Guardrails**: Content filters, rate limits, harmful output prevention, human-in-loop triggers
- **Evaluations**: Groundedness metrics, relevance scoring, hallucination detection, bias testing
- **Bias Detection**: Fairness metrics across demographics, synthetic data testing, bias mitigation strategies
- **Monitoring**: Real-time dashboards, drift detection, performance degradation alerts, incident response
- **Compliance**: GDPR (data privacy), HIPAA (healthcare), SOC2 (security), ISO 42001 (AI management), NIST AI RMF (risk framework)
- **Governance**: Approval workflows, model review boards, quarterly audits, version control, rollback procedures
- **Audit Trail**: Logging all decisions, predictions, human overrides, and policy changes

**Reference**: Full framework in `templates/responsible-ai-framework.md`.

### CLASSic Metrics Framework

**Cost**: Per-unit costs (per user, per inference, per conversation)
**Latency**: Response time targets (p50, p95, p99) for user experience
**Accuracy**: Precision, recall, F1, relevance scores for model performance
**Safety**: Harmful output rate, guardrail trigger frequency, incident counts
**Security**: Vulnerability scan results, prompt injection resistance, data protection
**Interpretability**: Explainability scores, citation accuracy, user trust metrics
**Compliance**: Audit pass rate, regulatory alignment, policy adherence

Track these metrics quarterly and report to governance board.

### Execution Roadmap Structure

**Q1 - Foundation & Pilot**:
- Milestones: Data pipeline setup, initial model training, pilot with 10-50 users
- Success Criteria: Model accuracy >X%, latency <Yms, pilot NPS >Z
- Adoption Metrics: X% of pilot users activate, Y% daily usage

**Q2 - Beta & Scale**:
- Milestones: Beta with 100-500 users, monitoring infrastructure, feedback loops
- Success Criteria: Accuracy >X%, cost per user <$Y, churn <Z%
- Adoption Metrics: X% of beta users, Y feature usage rate

**Q3 - Production Launch**:
- Milestones: General availability, full monitoring, pricing go-live
- Success Criteria: SLA targets met, revenue >$X, customer satisfaction >Y
- Adoption Metrics: X% target market penetration, Y% feature engagement

**Q4 - Optimization & Growth**:
- Milestones: Cost optimization, model improvements, expansion features
- Success Criteria: Unit economics improved X%, NPS >Y, expansion revenue $Z
- Adoption Metrics: X% YoY growth, Y% of customers on paid tier

---

## Input Dependencies

**Optional Inputs** (all optional, LLM decides whether to use or ask user):

**From ai-usecase-generator skill** (if available):
- `usecase-NN-{slug}.md` - Individual use case markdown with problem statement, target users, quadrant positioning, value proposition
- `usecases-summary.md` - Portfolio overview for context on strategic fit

**From ai-usecase-prioritization skill** (if available):
- `prioritization-scores.xlsx` - VALUE/(RISK+COST) scores indicating strategic priority
- `prioritization-justification.md` - Detailed scoring rationale for Impact, Adoption, Differentiation, Risk factors
- Priority tier classification (Strategic Priority, Opportunity, Caution, Deprioritize)

**From ai-market-trends skill** (if available):
- `competitive-landscape.md` - Competitor capabilities and positioning for differentiation analysis
- `industry-trends.md` - Market context and technology trends for strategic fit
- `swot-analysis.md` - Strategic context and organizational capabilities

**From user-provided information** (if available):
- Use case description (name, problem, solution, users)
- Strategic constraints or requirements
- Budget guidance or cost targets
- Timeline and launch expectations
- Compliance or regulatory requirements

**Note**: This skill can work with minimal input (even just a use case name) by asking clarifying questions. The LLM should assess available context and either leverage existing artifacts or gather information interactively.

---

## Integration with Other Skills

**Upstream Dependencies**:
- `ai-usecase-generator`: Provides use case concept and quadrant positioning
- `ai-usecase-prioritization`: Provides strategic priority and justification
- `ai-market-trends`: Provides competitive and market context

**This Skill's Outputs Feed Into**:
- PRD creation: Blueprint provides foundation for detailed product requirements
- Technical design: Architecture sections inform engineering design docs
- GTM planning: Business model and pricing inform go-to-market strategy
- Executive decision-making: Comprehensive blueprint supports approval processes
- Resource planning: Cost estimates and roadmap inform team staffing

**Note**: This skill is designed to work independently - it can generate comprehensive blueprints from scratch using interactive Q&A if no prior artifacts are available.

---

## Output Deliverables

**Primary Outputs**:
- **Comprehensive Blueprint (Markdown)**: 14-16 page detailed specification - ALWAYS generated
- **One-Page Lean Canvas (Optional)**: AI-adapted strategic overview for executive briefings
- **Format Conversions (Optional)**: PDF, DOCX, PPTX - use existing markdown via conversion guide

**Supporting Artifacts**:
- Technical architecture diagrams (ASCII + Mermaid)
- Pricing analysis and financial models
- Responsible AI governance framework
- Quarterly execution roadmap
- Success metrics dashboard specification

---

## Best Practices

### Scope and Focus
- **Executive Audience**: Write for C-level and product leaders, not engineers
- **Strategic Depth**: Go deep on business, economics, and governance - not implementation
- **Quantify Everything**: Use numbers, metrics, and ROI calculations extensively
- **Quarterly Granularity**: Execution roadmap at Q1-Q4 level only, not sprints
- **Template-Driven**: Always reference template files to enable dynamic updates

### Input Handling
- **Optional Inputs**: Work with whatever user provides - markdown, docs, or verbal description
- **Leverage Previous Skills**: Use ai-usecase-generator and ai-usecase-prioritization outputs if available
- **Ask Questions**: Proactively gather missing context rather than assuming

### Architecture Guidance
- **Both Formats**: Always provide ASCII and Mermaid diagrams for accessibility
- **Component Focus**: Specify what, not how - leave implementation to engineering
- **Standards-Based**: Reference MCP, A2A, and established AI patterns
- **Cost Awareness**: Highlight caching, model routing, and cost containment strategies

### Pricing Strategy
- **Analyze All 4**: Show pros/cons of subscription, consumption, outcome, hybrid
- **Recommend One**: Provide detailed analysis for best-fit archetype
- **Tie to Autonomy**: Match pricing to AI autonomy level (assistive vs. autonomous)
- **Include Examples**: Real pricing from comparable products

### Responsible AI
- **Principles + Operations**: High-level framework AND tactical implementation
- **Compliance-Specific**: Tailor to industry (healthcare = HIPAA, finance = SOC2, etc.)
- **Measurable**: Define metrics for bias, safety, transparency
- **Governance Structure**: Specify who approves, reviews, and audits

---

## Common Scenarios

**Scenario 1: From Use Case to Blueprint**
User has markdown from ai-usecase-generator and prioritization score. Create full blueprint with all sections, recommend pricing based on quadrant (Q4 = outcome-based, Q1 = subscription), and provide quarterly roadmap.

**Scenario 2: Executive Presentation Needed**
User needs quick Lean Canvas for board presentation. Generate 1-page AI-adapted Lean Canvas with key strategic elements, skip full blueprint unless requested.

**Scenario 3: Existing Markdown to Format Conversion**
User has blueprint markdown and wants PDF/PPTX. Use format-conversion-guide.md to convert without re-running entire skill. Save tokens and time.

**Scenario 4: Industry-Specific Blueprint**
Healthcare use case requires HIPAA compliance, patient safety focus. Tailor Responsible AI section to medical regulations, add clinical trial considerations, emphasize audit trails.

**Scenario 5: High-Risk Use Case**
Prioritization shows Consequence=3 (safety-critical). Emphasize governance, human-in-loop design, extensive testing requirements, quarterly safety reviews, C-suite approval workflows.

---

## Common Pitfalls

### Business & Strategy
- **Vague ROI**: Quantify benefits with specific metrics, not "improve customer satisfaction"
- **Unrealistic Pricing**: Match pricing to AI maturity and proven value, not aspirations
- **Ignoring Competition**: Research what competitors charge and how they position
- **No Moat**: Fail to articulate sustainable differentiation beyond "we use AI"

### Technical Architecture
- **Over-Specification**: This is not a detailed design doc - stay high-level
- **Vendor Lock-In**: Specify capabilities needed, not specific vendor products
- **Cost Blindness**: Forget to include caching, model routing, and cost controls
- **No Feedback Loops**: Miss the critical learning and improvement mechanisms

### Responsible AI
- **Principles Without Operations**: High-level ethics without concrete guardrails and metrics
- **Compliance Afterthought**: Retrofit governance instead of designing it in from start
- **One-Size-Fits-All**: Use generic RAI framework without industry-specific tailoring
- **No Measurement**: Fail to define how bias, safety, and transparency will be tracked

### Execution
- **Too Much Detail**: Quarterly roadmap includes sprint-level tasks (wrong granularity)
- **No Success Criteria**: Milestones without measurable outcomes
- **Ignoring Adoption**: Focus only on feature delivery, not user engagement metrics
- **Missing Dependencies**: Don't identify critical path items and prerequisites

---

## Quick Reference

```
PURPOSE: Transform prioritized AI use cases into comprehensive blueprints

INPUT: Optional markdown from ai-usecase-generator, ai-usecase-prioritization, or user description

SECTIONS:
1. Executive Summary (1 page)
2. Business & Monetization (pricing archetypes analysis)
3. User Experience & Adoption
4. Technical Architecture (ASCII + Mermaid diagrams)
5. Economics & Cost (unit economics, scaling)
6. Performance & Evaluations (CLASSic metrics)
7. Responsible AI & Governance (principles + operations)
8. Execution Roadmap (Q1-Q4 with success criteria)

OUTPUTS:
- Comprehensive Blueprint (Markdown) - ALWAYS
- Lean Canvas (1-pager) - OPTIONAL
- Format Conversion (PDF/DOCX/PPTX) - OPTIONAL

AUDIENCE: Executives and Product Managers

NEXT STEPS:
→ PRD creation for detailed requirements
→ Epic/User story breakdown for development
```

---

## Parameter Validation & Guidance

When working with you, if critical information is missing, I will proactively ask for:

**For Use Case Context:**
- "Do you have markdown output from ai-usecase-generator or ai-usecase-prioritization?"
- "What is the AI use case name and strategic positioning (Q1/Q2/Q3/Q4)?"
- "Who is the target customer and what problem are we solving?"
- "What business outcomes are we targeting (revenue, cost savings, efficiency)?"

**For Blueprint Scope:**
- "Which sections do you want detailed vs. high-level?"
- "Do you need the full blueprint, just Lean Canvas, or both?"
- "What is the target audience (board, C-suite, product team)?"
- "Are there industry-specific compliance requirements (HIPAA, GDPR, SOC2)?"

**For Technical Context:**
- "What existing systems need integration?"
- "What data sources are available for this AI use case?"
- "What infrastructure constraints exist (cloud provider, budget)?"
- "What AI/ML capabilities already exist in the organization?"

**For Pricing & Economics:**
- "What is the expected usage pattern (per user, per transaction, variable)?"
- "What are acceptable unit economics targets (LTV:CAC, gross margin)?"
- "How mature is the AI value - proven ROI or anecdotal?"
- "What do competitors charge for similar AI capabilities?"

**For Execution Planning:**
- "What is the target timeline (6 months, 12 months, 18 months)?"
- "What are the key milestones and decision gates?"
- "What success criteria matter most (adoption, revenue, cost reduction)?"
- "What dependencies or prerequisites exist?"

---

## How You Add Value

1. **Bridge strategy to execution** with comprehensive, actionable blueprints
2. **Quantify business impact** through detailed ROI and unit economics analysis
3. **Mitigate risk** with responsible AI governance and compliance frameworks
4. **Enable decision-making** with clear recommendations and trade-off analysis
5. **Accelerate planning** with structured templates and proven methodologies
6. **Ensure readiness** by identifying prerequisites, dependencies, and gaps
7. **Build confidence** with measurable success criteria and quarterly milestones
8. **Create alignment** across executives, product, and technical stakeholders

---

## References

**Reference Files (loaded as needed)**:

**Always Load**:
- `templates/blueprint-template.md` - Complete markdown template for comprehensive blueprint

**Load Based on User Selection**:
- `templates/lean-canvas-template.md` - AI-adapted 1-page Lean Canvas (if user requests)
- `templates/pricing-archetypes.md` - Detailed analysis of 4 pricing models (always needed for pricing section)
- `templates/tech-architecture-guide.md` - Diagram patterns and component specs (for architecture section)
- `templates/responsible-ai-framework.md` - Comprehensive RAI principles and operations (for governance section)
- `templates/format-conversion-guide.md` - Convert existing markdown to PDF/DOCX/PPTX (only if converting)

**When to Load Each Reference**:
- **blueprint-template.md**: Always load to ensure output structure matches latest template
- **lean-canvas-template.md**: Load if user requests 1-page Lean Canvas output
- **pricing-archetypes.md**: Always load when developing pricing strategy section
- **tech-architecture-guide.md**: Load when creating technical architecture section
- **responsible-ai-framework.md**: Load when developing responsible AI governance section
- **format-conversion-guide.md**: Load ONLY when user has existing markdown and wants format conversion

**Progressive Loading Pattern**: Load only what's needed for the specific blueprint scope to optimize context usage.

---

*Skill Category: Strategy & Detailed Planning*
*Version: 1.0 - Anthropic Best Practices*
*Last Updated: October 2025*
