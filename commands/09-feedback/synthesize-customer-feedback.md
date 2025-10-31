# Command: /synthesize-customer-feedback

## Execution Context
**Primary Agent:** Customer Success Agent
**Required Skills:** None (prompt-based)
**Command Category:** Feedback
**Version:** 2.0

## Purpose
Synthesize customer feedback from multiple sources to identify patterns, extract insights, and generate actionable product recommendations.

## When to Use
- After running `/analyze-customer-feedback`
- After adding internal feedback data (NPS, support tickets, interviews)
- For quarterly product planning
- To prioritize feature requests based on customer voice
- To identify churn risks and retention opportunities

## Where to Run This Command
**You choose the tool** based on your needs:
- **Claude/Perplexity**: If all feedback fits in context window
- **NotebookLM**: If you have extensive feedback data across multiple documents
- **Any LLM with sufficient context**: Tool-agnostic prompt

## What This Command Does
1. **Reads all files** from `09_Feedback/` folder:
   - `customer-feedback.md` from `/analyze-customer-feedback`
   - User-added internal feedback (support tickets, NPS, interviews)
   - Churn analysis documents
   - Any markdown or PDF files you've added

2. **Performs cross-source analysis**:
   - Identifies recurring themes and patterns
   - Quantifies sentiment and frequency
   - Maps feedback to user personas and use cases
   - Compares your product vs. competitors (if data available)
   - Highlights critical issues and quick wins

3. **Generates insights** in `09_Feedback/`:
   - `customer-feedback-analysis.md` - Comprehensive insights and recommendations

## Analysis Framework

Follow the output template structure: [commands/09-feedback/templates/customer-feedback-analysis-template.md](templates/customer-feedback-analysis-template.md)

**Analysis Principles:**
- **Quantify**: Count frequency of themes and sentiment
- **Quote extensively**: Use actual customer language
- **Compare**: Benchmark against competitors when possible
- **Segment**: Break down by user persona/segment
- **Prioritize**: Rank issues by frequency and impact
- **Action-oriented**: Every insight should suggest next steps

## Example Usage

```
/synthesize-customer-feedback

Context: Ran /analyze-customer-feedback for Notion
Added: Internal NPS survey results (PDF), Support ticket analysis (CSV export converted to markdown)

Focus: Feature prioritization for Q2 roadmap
```

## Output Files
- `09_Feedback/customer-feedback-analysis.md` (comprehensive insights and recommendations)

## Related Commands
- `/analyze-customer-feedback` - Collect customer feedback from public sources
- `/analyze-win-loss` - Sales win/loss analysis for competitive insights
- `/write-requirements` - Use feedback insights to inform PRDs

---

*Command Category: Feedback*
*Version: 2.0*
*Last Updated: October 2025*
