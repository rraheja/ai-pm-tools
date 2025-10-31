# Command: /analyze-customer-feedback

## Execution Context
**Primary Agent:** Customer Success Agent
**Required Skills:** None (web research)
**Command Category:** Feedback
**Version:** 2.0

## Purpose
Collect customer feedback data from public sources (G2, Reddit, app reviews, social media) to understand user sentiment, pain points, and feature requests.

## When to Use
- Quarterly product reviews
- Feature prioritization decisions
- Understanding competitive positioning from customer perspective
- Identifying product gaps or issues
- Planning product roadmap based on voice of customer

## What This Command Does
1. **Collects feedback** from:
   - **Review sites**: G2, Capterra, TrustRadius, Gartner Peer Insights
   - **Social media**: Reddit, Twitter/X, LinkedIn discussions
   - **App stores**: iOS App Store, Google Play Store reviews
   - **Community forums**: Product Hunt, Hacker News, Discord, Slack communities
   - **Support channels**: Public support forums, status pages

2. **Organizes feedback** by:
   - Sentiment (positive, neutral, negative)
   - Feature requests and pain points
   - Use case patterns
   - Competitive mentions
   - User personas and segments

3. **Generates initial output** in `09_Feedback/`:
   - `customer-feedback.md` - Raw feedback organized by source and theme

4. **User adds internal data**: After running this command, you can add:
   - Support tickets
   - NPS survey results
   - Customer interviews transcripts
   - Churn feedback
   - Success team notes

5. **Next step**: Run `/synthesize-customer-feedback` to extract insights and patterns

## What to Provide
- **Product name**: What product to research?
- **Competitors** (optional): Include competitor feedback for comparison?
- **Time range** (optional): Last 3 months, 6 months, 1 year?
- **Focus areas** (optional): Specific features or pain points to investigate?

## Example Usage
```
/analyze-customer-feedback

Product: Notion
Competitors: Monday.com, ClickUp, Asana
Time range: Last 6 months
Focus: AI features, collaboration capabilities, mobile app experience
```

## Output Files
- `09_Feedback/customer-feedback.md` (organized raw feedback with sources)

## Related Commands
- `/synthesize-customer-feedback` - Analyze feedback to extract insights and recommendations
- `/analyze-win-loss` - Competitive win/loss analysis

---

*Command Category: Feedback*
*Version: 2.0*
*Last Updated: October 2025*
