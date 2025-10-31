# Command: /analyze-market

## Execution Context
**Primary Agent:** Product Strategy Agent
**Required Skills:** ai-market-trends
**Command Category:** Strategy
**Version:** 2.0

## Purpose
Collect comprehensive market intelligence from external sources (web research, news, reports) and generate initial strategic analysis documents.

## When to Use
- Market entry analysis
- Strategic planning and quarterly reviews
- Competitive positioning
- Investment decisions
- Board presentations

## What This Command Does
1. **Collects raw research data** from:
   - Web research (industry trends, market sizing, news)
   - Competitor websites and public information
   - Technology trends and reports
   - Regulatory and policy information

2. **Generates initial framework files** in `01_Strategy/`:
   - `company-analysis.md` - Your company's position and capabilities
   - `swot-analysis.md` - Initial SWOT based on research
   - `five-forces-analysis.md` - Initial Porter's Five Forces
   - `industry-trends.md` - Market trends and growth drivers
   - `competitive-landscape.md` - Competitor profiles and positioning
   - `market-sources.md` - All sources with URLs and dates

3. **User adds manual files**: After running this command, you can add:
   - Company annual reports (PDFs)
   - Industry analyst reports (Gartner, Forrester)
   - Internal research documents
   - Customer feedback

4. **Next step**: Run `/synthesize-strategy-analysis` to refine SWOT and Five Forces with all inputs

## Example Usage
```
/analyze-market

Industry: Enterprise SaaS collaboration tools
Company: Our AI-powered workspace platform
Purpose: Series A fundraising preparation
Focus: Market size, competitive dynamics, growth opportunities
```

## Output Files
- `01_Strategy/company-analysis.md`
- `01_Strategy/swot-analysis.md` (initial)
- `01_Strategy/five-forces-analysis.md` (initial)
- `01_Strategy/industry-trends.md`
- `01_Strategy/competitive-landscape.md`
- `01_Strategy/market-sources.md`

## Related Commands
- `/synthesize-strategy-analysis` - Refine SWOT and Five Forces with additional sources
- `/analyze-competition` - Similar workflow focused on competitive analysis

---

*Command Category: Strategy*
*Version: 2.0*
*Last Updated: October 2025*
