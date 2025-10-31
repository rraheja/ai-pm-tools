# AI Market Trends & Strategic Intelligence Skill

Enterprise market and competitive intelligence framework for product managers and strategists.

## Overview

**Purpose**: Systematic market and competitive intelligence using three-tier research strategy (AI-generated + public filings + expert reports) and five strategic frameworks (Company Analysis, SWOT, Porter's Five Forces, Industry Trends, Competitive Landscape).

**Use Cases**: Market entry, strategic planning, competitive positioning, quarterly reviews, board presentations.

**Workflow**: Research & Collect → Synthesize (NotebookLM optional) → Analyze → Export

**Integration**: Standalone or PMSpecKit `01_Strategy/` phase via `.pmsk/config.yaml`

---

## Output Deliverables

- `company-analysis.md` - Company profile, strengths, position, priorities
- `swot-analysis.md` - Strengths, weaknesses, opportunities, threats matrix
- `five-forces-analysis.md` - Industry competitive dynamics assessment
- `industry-trends.md` - Historical context, growth drivers, technology shifts, future scenarios
- `competitive-landscape.md` - Competitor profiles, positioning, gaps, opportunities
- `_summary.md` - Executive summary with cross-references
- `_sources.md` - Complete source documentation with citations

---

## Files in This Skill

### Core Documentation
- **`SKILL.md`** - Complete skill definition with frameworks, workflow, and best practices ⭐ **READ THIS FIRST**

### Templates (`/templates/`)
- **`research-checklist.md`** - Systematic checklist for what to research across all frameworks
- **`source-tracking.md`** - Track sources with metadata for credibility and citation
- **`analysis-questions.md`** - Question templates for each strategic framework
- **`synthesis-prompt.md`** - Comprehensive synthesis prompt guidance

### Assets (`/assets/`)
- Currently empty - add example outputs or additional templates as needed

---

## Best Practices

- **Start broad, then narrow** - Industry overview before specifics
- **Use all three research tiers** - AI is fast, filings provide depth, expert reports add frameworks
- **Update regularly** - Quarterly or when significant market events occur
- **Validate with experts** - Cross-source synthesis, but validate findings
- **Track sources meticulously** - Source reliability matters for credibility
- **Iterate on research** - Refine based on gaps, don't expect perfection first pass

---

## Quick Usage Example

```
User: "Analyze the enterprise AI agent platform market"

AI PM Tools:
1. Infers industry context
2. Generates research checklist
3. Conducts AI research (Perplexity, ChatGPT, Claude)
4. Prompts for public filings or expert reports
5. Tracks sources systematically
6. Concatenates research files
7. Guides NotebookLM synthesis with provided prompt
8. Generates 5 framework analyses as markdown files
9. Creates executive summary with cross-references
10. Exports to PDF/PPTX as needed
```

---

## Configuration

**Default**: Outputs to `./ai-market-trends-output/`

**PMSpecKit Integration**: Create `.aipmconfig` in project root:
```yaml
---
project-name: "Your Project"
framework: PMSpecKit

output-folders:
  ai-market-trends: "01_Strategy"
---
```

Skill will automatically write outputs to configured folder if it exists.

---

## Integration with Other Skills

**Feeds Into**:
- `ai-usecase-prioritization` - Market context informs AI use case differentiation scores
- `/commands/create-lean-canvas` - Industry trends inform business model canvas
- `/commands/analyze-competition` - Competitive landscape provides foundation
- `/commands/write-requirements` - Strategic context shapes PRD priorities
- `/commands/build-roadmap` - Market trends guide roadmap planning

**Compatible With**:
- **PMSpecKit METHODOLOGY.md** - Populates `01_Strategy/` phase when configured
- **NotebookLM** - Core synthesis engine for cross-source analysis

---

## Getting Started

1. **Read `SKILL.md`** for complete framework details
2. **Provide starting point**: Industry name or company to analyze
3. **Follow iterative research workflow**: AI research → Public filings → Expert reports
4. **Synthesize with NotebookLM**: Use provided prompt for cross-source analysis
5. **Generate framework analyses**: Company, SWOT, Five Forces, Industry Trends, Competitive Landscape
6. **Export and share**: PDF/PPTX formats for stakeholders

---

## Best Practices

- Start with AI research for speed, add public filings for depth
- Update source tracking continuously for credibility
- Use NotebookLM for cross-source synthesis to prevent hallucination
- Iterate on research before synthesis; refine analysis based on feedback
- Validate insights with domain experts
- Refresh quarterly or when significant market events occur

---

## License

Apache 2.0 - Commercial use allowed

---

## Version

**Version**: 2.0 - Anthropic Best Practices
**Last Updated**: 2025-10-29
**Category**: Discovery & Strategy
**Skill Type**: Research & Analysis Framework

---

For detailed instructions, frameworks, and best practices, see **[SKILL.md](./SKILL.md)**.
