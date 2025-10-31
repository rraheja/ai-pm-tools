# AI Use Case Blueprint Skill

## Execution Context
**Primary Skill:** ai-usecase-blueprint
**Associated Commands:** /create-ai-blueprint, /create-lean-canvas
**Category:** Discovery & Strategy

Transform AI use case concepts into comprehensive product blueprints with detailed specifications for executives and product managers. Creates strategic plans covering business model, architecture, responsible AI, economics, and execution roadmap.

## Quick Start

Ask Claude:
- "Create a blueprint for [AI use case name]"
- "Generate a Lean Canvas for [AI product/feature]"
- "Create an executive summary for [AI initiative]"
- "Convert this AI use case into a comprehensive blueprint with pricing strategy and technical architecture"

Claude will gather context (optionally using outputs from ai-usecase-generator or ai-usecase-prioritization), develop the blueprint, and generate your chosen output formats.

## What You Get

**Full Blueprint Output:**
- **1-page Executive Summary** - Problem, solution, ROI, go/no-go recommendation
- **Business & Monetization** - Value prop, target market, competitive positioning, pricing strategy, unit economics
- **User Experience & Adoption** - Personas, journey maps, adoption strategy, change management
- **Technical Architecture** - High-level diagrams (ASCII + Mermaid), component specifications
- **Economics & Cost** - Development costs, infrastructure, model/API costs, break-even analysis
- **Performance & Evaluations** - CLASSic metrics (Cost, Latency, Accuracy, Safety, Security, Interpretability, Compliance)
- **Responsible AI & Governance** - Principles, guardrails, bias detection, monitoring, compliance (GDPR, HIPAA, SOC2, ISO 42001)
- **Execution Roadmap** - Q1-Q4 quarterly milestones with success and adoption criteria

**Lean Canvas Option:**
- **1-page AI-adapted Lean Canvas** - Problem, Solution, Value Prop, Customer Segments, Channels, Revenue, Costs, Metrics, Unfair Advantage

**Output Formats:**
- **Markdown** (mandatory) - Full blueprint in structured markdown
- **PDF** (optional) - Professional document with table of contents
- **DOCX** (optional) - Editable Word document with proper formatting
- **PPTX** (optional) - PowerPoint presentation for executive briefings

## How It Works

### 3-Phase Approach

**Phase 1: Gather Context**
- Accepts optional inputs from ai-usecase-generator or ai-usecase-prioritization skills
- Asks clarifying questions about business model, target users, technical approach, constraints
- Determines output format preferences

**Phase 2: Blueprint Development**
- Analyzes 8 core blueprint dimensions:
  1. Strategic positioning (Q1-Q4 quadrant: Know-how/Actionable × Human Intervention/Autonomous)
  2. Value proposition and differentiation
  3. Target market and segments (TAM/SAM/SOM)
  4. Pricing strategy (4 archetypes: Subscription, Consumption, Outcome-based, Hybrid)
  5. Technical architecture (RAG, Multi-agent, or Standard AI App patterns)
  6. Unit economics (LTV, CAC, gross margin, break-even)
  7. Responsible AI framework (FATE principles + operational guardrails)
  8. Execution roadmap (quarterly milestones)

**Phase 3: Output Generation**
- Creates comprehensive blueprint or Lean Canvas using reference templates
- Generates executive summary (1 page), detailed sections (as needed)
- Optionally converts to PDF, DOCX, or PPTX

### Key Frameworks

**Pricing Decision Matrix:**
```
AI Autonomy (High/Low) × Proven Value (High/Low)
→ Subscription / Consumption / Outcome-Based / Hybrid
```

**CLASSic Metrics:**
- **Cost**: Unit economics targets
- **Latency**: Response time SLAs
- **Accuracy**: Model performance benchmarks
- **Safety**: Harmful output rate
- **Security**: Data protection, prompt injection defense
- **Interpretability**: Explainability requirements
- **Compliance**: Regulatory frameworks (GDPR, HIPAA, SOC2, ISO 42001, NIST AI RMF)

**Responsible AI:**
- Principles: Fairness, Accountability, Transparency, Ethics (FATE)
- Guardrails: Input/output filtering, rate limiting, human-in-loop
- Evaluation: Groundedness, relevance, hallucination rate, bias metrics
- Monitoring: Real-time dashboards, drift detection, incident response

## Files

### Core Skill
- **SKILL.md** - Complete skill definition with progressive loading guidance (start here)

### Template Files (loaded as needed)
- **templates/blueprint-template.md** - Comprehensive markdown template for full blueprint (~1000 lines)
- **templates/lean-canvas-template.md** - AI-adapted 1-page Lean Canvas template
- **templates/pricing-archetypes.md** - Detailed analysis of 4 pricing models with examples
- **templates/tech-architecture-guide.md** - Architecture patterns (Standard AI App, RAG, Multi-Agent) with ASCII + Mermaid diagrams
- **templates/responsible-ai-framework.md** - Comprehensive RAI principles, guardrails, evaluation, monitoring, compliance
- **templates/format-conversion-guide.md** - Convert existing markdown to PDF/DOCX/PPTX without regenerating content

### Progressive Loading Strategy

The skill uses a **token-efficient progressive loading pattern**:
- Always loads: blueprint-template.md
- Conditionally loads other references based on user needs
- Enables format conversion without re-running the entire skill

## Integration with Other Skills

**Upstream:**
- **ai-usecase-generator** - Provides initial use case description and strategic positioning
- **ai-usecase-prioritization** - Provides VALUE/(RISK+COST) scores and prioritization rationale

**Downstream:**
- **requirements-engineering** (future) - Creates PRD, epics, user stories from blueprint
- **gtm-planning** (future) - Creates detailed launch plan from blueprint
- **metrics-dashboard** (future) - Creates detailed analytics plan from CLASSic metrics

## Example Workflows

### Workflow 1: New AI Initiative (Comprehensive)
```bash
# 1. Generate use case ideas
Use ai-usecase-generator skill

# 2. Prioritize use cases
/prioritize-ai-usecases

# 3. Create comprehensive blueprint for top-ranked use case
Use ai-usecase-blueprint skill → Full Blueprint → Markdown + PDF

# 4. Present to stakeholders
Use PPTX output for executive briefing
```

### Workflow 2: Quick Strategic Validation
```bash
# 1. Create Lean Canvas
Use ai-usecase-blueprint skill → Lean Canvas option

# 2. Review with stakeholders
Share 1-page PDF for quick feedback

# 3. If approved, create full blueprint
Re-run skill with Full Blueprint option
```

### Workflow 3: Format Conversion (Token-Efficient)
```bash
# 1. Already have blueprint markdown
[Existing blueprint.md file]

# 2. Convert to presentation format
Use format-conversion-guide.md → Generate PPTX slides

# No need to regenerate content, just convert format
```

## Best Practices

### Input Preparation
- Provide outputs from ai-usecase-generator or ai-usecase-prioritization if available
- Have user research, competitive analysis, or cost estimates ready (optional but helpful)
- Know your target audience (executives, product team, engineering, or all stakeholders)

### Output Selection
- **Lean Canvas**: Use for quick strategic validation, portfolio reviews, or initial stakeholder alignment
- **Full Blueprint**: Use for detailed planning before PRD creation, executive decision-making, or funding requests
- **Markdown**: Always generated, suitable for version control and collaboration
- **PDF**: Best for formal documentation, board presentations, or stakeholder distribution
- **PPTX**: Best for executive briefings, investor pitches, or GTM team enablement

### Audience Considerations
- **Executives/Board**: Focus on Executive Summary, ROI, Risks, Recommendation (use Lean Canvas or 1-pager)
- **Product Team**: Full blueprint with emphasis on UX, adoption, metrics
- **Engineering**: Technical architecture, performance requirements, responsible AI guardrails
- **GTM Team**: Value prop, pricing strategy, competitive positioning, customer segments

### Token Efficiency
- Use Lean Canvas for initial validation (faster, fewer tokens)
- Generate full blueprint only after strategic approval
- Use format-conversion-guide.md to convert existing markdown without regenerating content
- Reuse blueprint content across multiple output formats

## When to Use This Skill

**Use ai-usecase-blueprint when:**
- ✅ AI use case has been identified and prioritized
- ✅ Need comprehensive strategic planning before PRD creation
- ✅ Preparing executive briefing or funding request
- ✅ Evaluating pricing models for AI product
- ✅ Need technical architecture specification for PM/executive audience
- ✅ Require responsible AI compliance documentation
- ✅ Planning quarterly execution roadmap

**Do NOT use this skill when:**
- ❌ Need detailed implementation PRD, epics, or user stories (use requirements-engineering skill)
- ❌ Need engineering-level technical design (use separate engineering design process)
- ❌ Need detailed GTM launch plan (use gtm-planning skill)
- ❌ Use case is still at brainstorming stage (use ai-usecase-generator first)
- ❌ Multiple use cases need prioritization (use ai-usecase-prioritization first)

## Version
**Version:** 1.0
**Last Updated:** October 2025

## License

Apache License 2.0 - Free to use and modify with attribution
