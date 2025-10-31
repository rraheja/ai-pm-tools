---
name: ai-market-trends
description: Enterprise market and competitive intelligence framework using multi-source research and strategic analysis frameworks (SWOT, Porter's Five Forces, Industry Trends, Competitive Landscape, Company Analysis). Helps product managers analyze industries, competitors, and strategic positioning. Use when asked to analyze markets, assess competition, evaluate industry trends, or create strategic intelligence reports.
allowed-tools: Read, Write, Edit, Grep, Glob, WebFetch, WebSearch
license: Apache-2.0
---

# AI Market Trends & Strategic Intelligence Framework

## Purpose

Systematic methodology for gathering competitive and market intelligence, synthesizing multi-source research, and generating strategic analysis using industry-standard frameworks.

**Core Philosophy:**
```
Intelligence = Discovery (Research) + Synthesis (Analysis) + Frameworks (Structure)

Research Sources: AI-Generated + Public Filings + Expert Reports
Analysis Output: Markdown files per framework
Strategic Value: Actionable insights for planning, product strategy, and positioning
```

**Output Structure:**
- Separate markdown files per framework (industry-agnostic, configurable output location)
- Cross-source synthesis for comprehensive analysis
- Iterative refinement workflow (research → collect → synthesize → analyze)

## When to Use

- **Market entry**: Analyzing new markets, industries, or competitive landscapes
- **Strategic planning**: Building context for product strategy and roadmapping
- **Competitive positioning**: Understanding competitor strengths, weaknesses, and strategies
- **Investment decisions**: Evaluating market attractiveness and strategic opportunities
- **Product discovery**: Gathering context for AI use case prioritization or product planning
- **Quarterly reviews**: Updating market intelligence and competitive positioning
- **Board presentations**: Creating comprehensive market and competitive analysis

### When NOT to Use

- Real-time competitive monitoring (use dedicated competitive intelligence tools)
- Financial modeling or detailed valuation (use financial analysis tools)
- Customer research or user interviews (use voice-of-customer research methods)
- Operational benchmarking (use operational excellence frameworks)

---

## Analysis Frameworks

Generate 5 strategic analysis files using templates in `templates/` folder:

1. **`company-analysis.md`** - Company profile, strengths, market position, resources, strategic priorities
2. **`swot-analysis.md`** - Internal strengths/weaknesses, external opportunities/threats, strategic implications matrix (template: `swot-output-template.md`)
3. **`five-forces-analysis.md`** - Industry competitive dynamics: rivalry, new entrants, suppliers, buyers, substitutes (template: `five-forces-output-template.md`)
4. **`industry-trends.md`** - Historical context, growth drivers, technology shifts, regulatory environment, economic dynamics, future scenarios
5. **`competitive-landscape.md`** - Competitor profiles, market share, positioning, strategic moves, differentiation, gaps

**Execution Requirements**:
- Cite sources rigorously for every claim
- Include strategic implications for each framework
- Cross-reference findings across frameworks
- Quantify with numbers, percentages, growth rates where available

---

## Research Strategy: Three-Tier Sourcing

### Tier 1: AI-Generated Intelligence

**Use For**:
- Initial industry overview and market sizing
- Competitor identification and profiling
- Technology trend research
- News and recent developments
- Regulatory and policy research

**Process**:
1. Start with broad research queries (e.g., "SaaS CRM market size and trends 2024")
2. Generate focused reports (8,000-10,000 words per topic)
3. Save outputs as markdown in research folder
4. Refine and iterate based on gaps

**Advantages**: Fast, comprehensive, current information

---

### Tier 2: Public Company Filings & Reports

**Sources**: Annual reports (10-K), investor presentations, earnings calls, SEC filings

**Use For**:
- Financial performance and metrics
- Strategic priorities and initiatives
- Management commentary and outlook
- Risk factors and challenges
- Business model details

**Process**:
1. Identify 5-7 key companies representing value chain
2. Download annual reports and investor materials
3. Extract relevant sections (strategy, financials, risks)
4. Save extracts as markdown or PDFs in research folder

**Advantages**: Authoritative, detailed, strategic context

---

### Tier 3: External Expert Reports

**Sources**: Industry analyst reports (Gartner, Forrester), consulting reports, academic research, trade associations

**Use For**:
- Independent market analysis
- Industry benchmarks and best practices
- Technology evaluation and maturity
- Strategic frameworks and methodologies

**Process**:
1. Search for free industry reports and whitepapers
2. Download PDFs or save markdown extracts
3. Identify key insights and frameworks
4. Reference in source tracking

**Advantages**: Expert perspective, benchmarking, frameworks

---

## Structure/Components

### Execution Workflow

**Iterative Process**: Research and collect iteratively → Synthesize in one step → Analyze interactively

```
┌─────────────────────────────────────────────────────────────────┐
│ PHASE 1: RESEARCH & COLLECT (Iterative - Multiple Rounds)      │
├─────────────────────────────────────────────────────────────────┤
│ 1. User provides starting point (company or industry)           │
│ 2. Infer industry context if company name provided              │
│ 3. Generate research checklist (templates/research-checklist.md)│
│ 4. Conduct comprehensive research using available sources       │
│ 5. Prompt for public filings and expert reports                 │
│ 6. Track sources (templates/source-tracking.md)                 │
│ 7. Refine and iterate until sufficient coverage                 │
└─────────────────────────────────────────────────────────────────┘
              ↓
┌─────────────────────────────────────────────────────────────────┐
│ PHASE 2: SYNTHESIZE (Cross-Source Analysis)                    │
├─────────────────────────────────────────────────────────────────┤
│ 1. Concatenate all research files                               │
│ 2. Perform cross-source analysis and validation                 │
│ 3. Identify key insights and patterns                           │
│ 4. Generate synthesis summary markdown                          │
└─────────────────────────────────────────────────────────────────┘
              ↓
┌─────────────────────────────────────────────────────────────────┐
│ PHASE 3: ANALYZE (Interactive - Framework Application)         │
├─────────────────────────────────────────────────────────────────┤
│ 1. Generate company-analysis.md                                 │
│ 2. Generate swot-analysis.md                                    │
│ 3. Generate five-forces-analysis.md                             │
│ 4. Generate industry-trends.md                                  │
│ 5. Generate competitive-landscape.md                            │
│ 6. Create summary with cross-references                         │
│ 7. Refine based on user feedback                                │
│ 8. Export to PDF/PPTX as needed                                 │
└─────────────────────────────────────────────────────────────────┘
```

---

### Configuration: Output Folder Mapping

**Default Behavior**: Outputs to current working directory under `./ai-market-trends-output/`

**Configurable Behavior**: If `.aipmconfig` file exists in project root, read configuration for output folder mapping.

**Example `.aipmconfig`**:
```yaml
---
project-name: "Project Alpha"
framework: PMSpecKit

output-folders:
  ai-market-trends: "01_Strategy"
  ai-usecase-prioritization: "02_Planning"

default-output: "./output"
---
```

**Folder Resolution Logic**:
1. Check if `.aipmconfig` exists in current directory or parent directories
2. If exists, read `output-folders.ai-market-trends` configuration
3. If configured folder exists, write outputs there
4. If configured folder does not exist, create it
5. If no configuration, use default: `./ai-market-trends-output/`

---

### Re-run Behavior: Using Existing Markdown

**If markdown files already exist in output folder:**

1. **Prompt user**: "I found existing analysis files ([list files]). Would you like me to:"
   - **Option A**: Use existing files as input for additional/updated analysis
   - **Option B**: Start fresh analysis (archive existing files)
   - **Option C**: Review existing files only (no new analysis)

2. **If Option A selected**:
   - Read existing markdown files
   - Prompt: "What additional analysis or updates do you need?"
   - Incorporate new research if provided
   - Update existing markdown files with new insights
   - Maintain version history in file frontmatter

3. **If Option B selected**:
   - Move existing files to `_archive/[timestamp]/`
   - Start fresh analysis

4. **If Option C selected**:
   - Provide summary of existing analysis
   - Offer to export to different formats

---

## Template Usage

### Files

**User-Fillable Templates** (`/templates/`):
- `templates/research-checklist.md` - Systematic checklist for what to research
- `templates/source-tracking.md` - Track sources, URLs, dates, reliability
- `templates/analysis-questions.md` - Question templates for each framework
- `templates/synthesis-prompt.md` - Comprehensive synthesis prompt guidance

**Generated Output Files** (written to configured folder):
- `company-analysis.md` - Company profile, strengths, market position
- `swot-analysis.md` - SWOT matrix with strategic implications
- `five-forces-analysis.md` - Industry competitive dynamics
- `industry-trends.md` - Historical context, growth drivers, future scenarios
- `competitive-landscape.md` - Competitor profiles and positioning
- `_summary.md` - High-level overview with cross-references
- `_sources.md` - All sources with metadata

---

### Workflow Process

```
Step 1: Initialize Skill
  - User: "Analyze the SaaS CRM market" OR "Analyze Salesforce"
  - Skill: Infer industry if company provided
  - Generate research checklist (templates/research-checklist.md)
  - Check for .aipmconfig for output folder
  - Check for existing markdown files (re-run behavior)

Step 2: Research & Collect (Iterative)
  Round 1:
    - Conduct comprehensive research
    - Generate initial reports (8,000-10,000 words per topic)
    - Save as markdown in research folder
    - Update source tracking

  Round 2 (if gaps exist):
    - Prompt user: "I need public company filings for [companies]. Can you provide?"
    - If yes: Process provided files
    - If no: Continue with available research to fill gaps
    - Update source tracking

  Round 3 (if needed):
    - Prompt user: "Do you have expert reports (Gartner, Forrester)?"
    - Process if provided
    - Mark research as complete

Step 3: Synthesize (Cross-Source Analysis)
  - Concatenate all research files
  - Perform cross-source analysis
  - Validate findings across sources
  - Generate synthesis summary

Step 4: Analyze (Interactive)
  - Generate company-analysis.md (if focal company)
  - Generate swot-analysis.md
  - Generate five-forces-analysis.md
  - Generate industry-trends.md
  - Generate competitive-landscape.md
  - Create _summary.md with cross-references
  - Compile _sources.md
  - Ask user: "Would you like refinements or exports?"

Step 5: Export & Finalize
  - Export selected files to PDF/PPTX
  - Provide next steps for using outputs in planning
```

---

## Output Deliverables

**Strategic Analysis Files (Markdown)**:
- `company-analysis.md` - Company profile, strengths, market position (if focal company provided)
- `swot-analysis.md` - SWOT matrix with strategic implications
- `five-forces-analysis.md` - Industry competitive dynamics and attractiveness
- `industry-trends.md` - Historical context, growth drivers, technology shifts, future scenarios
- `competitive-landscape.md` - Competitor profiles, positioning, differentiation, gaps
- `_summary.md` - Executive summary with key insights and strategic recommendations
- `_sources.md` - Comprehensive source documentation with URLs, dates, reliability ratings

**Supporting Documentation**:
- `templates/research-checklist.md` - Completed checklist with coverage tracking
- `templates/source-tracking.md` - Full source inventory with metadata

**Export Formats** (optional):
- PDF exports for stakeholder distribution
- PPTX exports for presentations
- DOCX exports for collaborative editing

---

## Integration with Other Skills

**This Skill's Outputs Feed Into**:
- `ai-usecase-generator`: Market context and competitive insights inform use case generation
- `ai-usecase-prioritization`: Strategic context informs differentiation and impact scores
- `/commands/create-lean-canvas`: Industry trends and competitive landscape inform business model canvas
- `/commands/analyze-competition`: Detailed competitive analysis builds on competitive landscape
- `/commands/write-requirements`: Strategic context shapes product requirements and priorities

**Input Dependencies**:

**Optional Inputs** (all optional, LLM decides whether to use or ask user):
- User-provided market research reports, PDFs, or analyst documents
- Company annual reports or investor presentations
- Existing market analysis files (if re-running the skill for updates)
- Industry-specific documents or whitepapers

**Note**: This skill is designed to work independently using web research (AI-generated intelligence, public filings, expert reports). The LLM should assess what research is available and either leverage user-provided materials or conduct fresh research as needed.

**Works With PMSpecKit**:
- Outputs populate `01_Strategy/` phase when `.aipmconfig` is configured
- Provides strategic foundation for subsequent planning phases

---

## Common Scenarios

**Scenario 1: New Market Entry**
- User: "Analyze the AI-powered customer service market"
- Process: Research (AI + public reports) → Synthesize → All 5 frameworks → Export for board presentation

**Scenario 2: Competitive Positioning**
- User: "Analyze our position vs. competitors in SaaS CRM"
- Process: Research (focus on competitors) → Synthesize → Competitive landscape + SWOT → Strategy recommendations

**Scenario 3: Strategic Planning Input**
- User: "Provide market context for our 2025 roadmap"
- Process: Research (trends + industry) → Synthesize → Industry trends + Five Forces → Feed into planning phase

**Scenario 4: Company-Specific Analysis**
- User: "Analyze Salesforce's market position"
- Process: Infer industry (SaaS CRM) → Research (Salesforce + competitors) → All frameworks → Company-specific insights

**Scenario 5: Quarterly Update**
- User: "Update our competitive landscape for Q4"
- Process: Re-run with existing files → Research (recent news + developments) → Update competitive landscape → Highlight changes

---

## Best Practices for AI Execution

- **Ask clarifying questions**: Company vs. industry? Existing research available?
- **Infer industry context**: If user provides company name, research and infer industry
- **Prompt for missing sources**: If initial research insufficient, ask for filings or reports
- **Don't guess**: If data not available, clearly state limitations
- **Generate comprehensive frameworks**: Use full structure for each framework
- **Reference real-world examples**: Cite specific companies, trends, data points
- **Use template structure**: Follow templates for consistency
- **Check for .aipmconfig**: Respect output folder configuration
- **Handle re-runs gracefully**: Prompt for existing file usage
- **Enable iteration**: Support refinement based on user feedback

---

## Common Pitfalls

### Research Errors
1. **Insufficient depth**: Relying only on AI-generated content without filings or expert reports
2. **Outdated information**: Not checking publication dates of sources
3. **Narrow focus**: Missing adjacent competitors or substitute threats
4. **Confirmation bias**: Only seeking information that supports preconceptions
5. **Source reliability**: Not tracking or validating source credibility

### Analysis Errors
1. **Framework misapplication**: Using SWOT for competitive dynamics (use Five Forces)
2. **Static analysis**: Not considering industry evolution or future scenarios
3. **Over-generalization**: Treating all competitors as equal threats
4. **Missing context**: Not connecting frameworks to strategic implications
5. **Ignoring synthesis**: Skipping cross-source analysis and validation

### Technical Errors
1. **Output folder confusion**: Not checking for .aipmconfig before writing files
2. **Poor source tracking**: Losing track of where information came from
3. **Incomplete research checklist**: Not systematically covering all areas
4. **Skipping synthesis**: Missing cross-document analysis benefits
5. **No iteration**: Accepting first-pass research without refinement
6. **Ignoring existing files**: Not prompting for re-run behavior

---

*Skill Category: Discovery & Strategy*
*Version: 2.0 - Tool-Agnostic*
*Last Updated: 2025-10-29*
