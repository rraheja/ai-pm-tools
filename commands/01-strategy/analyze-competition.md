# Command: /analyze-competition

## Execution Context
**Primary Agent:** Product Strategy Agent
**Required Skills:** ai-market-trends
**Command Category:** Strategy
**Version:** 2.0

## Purpose
Collect competitive intelligence from external sources and generate initial competitive analysis frameworks.

## When to Use
- Entering new markets or launching new products
- Responding to competitive threats or market changes
- Strategic planning cycles (annual/quarterly reviews)
- Creating sales battlecards or investor presentations
- Feature prioritization based on competitive gaps

## What This Command Does
1. **Collects competitive intelligence** from:
   - Competitor websites and product pages
   - Public company filings and investor reports
   - Product reviews (G2, Capterra, TrustRadius)
   - News articles and press releases
   - Social media and community discussions

2. **Generates initial framework files** in `01_Strategy/`:
   - `company-analysis.md` - Your company's competitive position
   - `swot-analysis.md` - Initial competitive SWOT
   - `five-forces-analysis.md` - Initial industry forces analysis
   - `industry-trends.md` - Competitive trends and shifts
   - `competitive-landscape.md` - Detailed competitor profiles
   - `market-sources.md` - All sources with URLs and dates

3. **User adds manual files**: After running this command, you can add:
   - Competitor pitch decks
   - Win/loss reports
   - Sales battlecards
   - Customer feedback about competitors

4. **Next step**: Run `/synthesize-strategy-analysis` to refine SWOT and Five Forces with all inputs

## Example Usage
```
/analyze-competition

Market: AI-powered project management tools
Our product: Notion-like workspace with AI automation
Competitors: Notion, Monday.com, ClickUp, Asana, Linear

Purpose: Define positioning for Series A pitch and prioritize Q1 roadmap
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
- `/analyze-market` - Similar workflow focused on market analysis

---

*Command Category: Strategy*
*Version: 2.0*
*Last Updated: October 2025*
