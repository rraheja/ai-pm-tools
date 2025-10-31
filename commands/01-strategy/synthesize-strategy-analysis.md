# Command: /synthesize-strategy-analysis

## Execution Context
**Primary Agent:** Product Strategy Agent
**Required Skills:** None (prompt-based)
**Command Category:** Strategy
**Version:** 2.0

## Purpose
Synthesize all strategic research and data sources to produce refined SWOT and Porter's Five Forces analysis with deep cross-source validation.

## When to Use
- After running `/analyze-market` or `/analyze-competition`
- After adding manual research files (PDFs, reports, internal documents)
- When you need comprehensive strategic frameworks based on multiple sources
- For board presentations or strategic planning sessions

## Where to Run This Command
**You choose the tool** based on your needs:
- **Claude/Perplexity**: If all sources fit in context window
- **NotebookLM**: If you have many PDFs or need cross-document synthesis
- **Any LLM with sufficient context**: Tool-agnostic prompt

## What This Command Does
1. **Reads all files** from `01_Strategy/` folder:
   - Initial framework files from `/analyze-market` or `/analyze-competition`
   - User-added PDFs (annual reports, analyst reports)
   - Internal research documents
   - Any markdown files you've added

2. **Performs cross-source analysis**:
   - Validates findings across multiple sources
   - Identifies patterns and contradictions
   - Synthesizes quantitative and qualitative data
   - Applies rigorous strategic frameworks

3. **Generates refined outputs** in `01_Strategy/`:
   - `swot-analysis.md` - Comprehensive SWOT with evidence from all sources
   - `five-forces-analysis.md` - Detailed Porter's Five Forces with competitive dynamics

## Instructions for Execution

### Context to Provide
When running this command, provide:
1. All markdown files from `01_Strategy/`
2. Any PDFs or additional research documents
3. Specific focus areas (if any)

### What You'll Generate
Execute comprehensive cross-source analysis following these frameworks:

**Output Templates:**
- **SWOT Analysis**: See [skills/ai-market-trends/templates/swot-output-template.md](../../skills/ai-market-trends/templates/swot-output-template.md)
- **Porter's Five Forces**: See [skills/ai-market-trends/templates/five-forces-output-template.md](../../skills/ai-market-trends/templates/five-forces-output-template.md)

**Analysis Principles:**
- **Cite rigorously**: Reference specific sources for every claim
- **Quantify**: Use numbers, percentages, growth rates wherever possible
- **Validate across sources**: Check if multiple sources agree
- **Note contradictions**: Highlight when sources disagree
- **Be balanced**: Present both positive and negative findings
- **Stay objective**: Avoid promotional language

## Example Usage

```
/synthesize-strategy-analysis

Context: I've run /analyze-market and added:
- Salesforce 2024 Annual Report (PDF)
- Gartner Magic Quadrant for CRM (PDF)
- Internal win/loss analysis (markdown)

Focus: Refine SWOT and Five Forces for board presentation
```

## Output Files
- `01_Strategy/swot-analysis.md` (refined with all sources)
- `01_Strategy/five-forces-analysis.md` (refined with all sources)

## Best Practices
- **Cite rigorously**: Reference specific sources for every claim
- **Quantify**: Use numbers, percentages, growth rates wherever possible
- **Validate across sources**: Check if multiple sources agree
- **Note contradictions**: Highlight when sources disagree
- **Be balanced**: Present both positive and negative findings
- **Stay objective**: Avoid promotional language

## Related Commands
- `/analyze-market` - Collect initial market intelligence
- `/analyze-competition` - Collect competitive intelligence
- `/generate-usecases` - Use strategic insights to generate AI use cases

---

*Command Category: Strategy*
*Version: 2.0*
*Last Updated: October 2025*
