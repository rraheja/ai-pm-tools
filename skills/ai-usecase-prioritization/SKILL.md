---
name: ai-usecase-prioritization
description: Enterprise AI use case prioritization framework using VALUE/(RISK+COST) formula. Helps product managers score, rank, and visualize AI initiatives. Use when asked to prioritize AI projects, evaluate AI use cases, create AI portfolio strategies, or generate prioritization frameworks.
allowed-tools: Read, Write, Edit, Grep, Glob
license: Apache-2.0
---

# AI Use Case Prioritization Framework

## Purpose

Systematic value-based methodology for evaluating AI initiatives to generate risk-adjusted priority scores with Excel dashboards.

**Core Formula:**
```
Priority Score = VALUE / (RISK + COST)

VALUE = Impact × Adoption × Differentiation (range: 1-27)
RISK = Consequence × Probability × Cost-to-Fix (range: 1-27)
COST = Cost-to-Implement (range: 1-3)

Normalized Score = (Priority Score / 13.5) × 100
```

**Priority Tiers based on Normalized Score:**
- 100-60: 🟢 Strategic Priority (pursue aggressively)
- 59-20: 🟡 Opportunity (solid execution bet)
- 19-10: 🟠 Caution (only if Consequence ≤ 2)
- <10: 🔴 Deprioritize (avoid unless strategic)

## When to Use

- **Portfolio planning**: Multiple AI projects competing for limited resources
- **Vendor evaluation**: Comparing build vs. buy vs. partner options for AI capabilities  
- **Strategic planning**: Creating multi-year AI investment roadmaps
- **Stakeholder alignment**: Need objective framework for prioritization discussions
- **Budget justification**: Building business cases for AI investments
- **Quarterly planning**: Re-evaluating and re-prioritizing existing AI initiatives

### When NOT to Use

- The use cases are not AI related, because the formula components are aimed at AI considerations

---

## Scoring Framework

### VALUE (Numerator - Multiply)

#### Impact (1-3): Business value and strategic importance
- **3**: Transformative (30%+ improvement), CEO priority, enables new business model, $B+ market
- **2**: Significant (10-25% improvement), clear ROI, important but not critical, $50M-$1B market
- **1**: Incremental (<10% improvement), nice-to-have, limited strategic value, <=$50M market

**Examples:** Netflix recommendations (3), Operational efficiency (2), UI polish (1)

**Checklist:** Top-line metrics? New business model? CEO priority? Force competitors to respond?

---

#### Adoption (1-3): Expected 12-18 month user base and frequency
- **3**: >75% of audience, cross-platform, daily usage, network effects (e.g. Grammarly daily users)
- **2**: 25-75% of audience, multiple departments, weekly usage (e.g. GitHub Copilot adoption)
- **1**: <25% of audience, single department, occasional usage, niche

**Checklist:** User base size? Switching costs? Behavior change needed? Brand trust? Pricing model?

**Avoid:** Penalizing for launch constraints, overweighting privacy without data, ignoring parent platform users

---

#### Differentiation (1-3): Competitive uniqueness and sustainability
- **3**: 1-2+ year lead, proprietary tech, patents, data moats, first-mover sustained (e.g. Tesla FSD)
- **2**: Some unique elements, 1-2 year advantage, better execution, quality-based (e.g. Netflix recommendations)
- **1**: Me-too solution, commodity, table stakes, following competitors

**Checklist:** Technology advantage? Sustainable? Alternatives? Can competitors copy in 6 months? Proprietary assets?

**Avoid:** Scoring UI vs capability, ignoring model quality, treating "first" as sustainable, confusing features with moats

---

### RISK (Denominator - Multiply)

#### Consequence (1-3): **SCALE-AWARE** - Severity at expected adoption level
**⚠️ CRITICAL:** Ask "If this fails with millions of users, what happens?"

- **3**: Unacceptable at any scale - deaths, major harm, lawsuits, headlines (e.g. Tesla Autopilot, IBM Watson oncology)
- **2**: Scale amplifies - annoying per-user but significant at millions of users scale (e.g. Alexa privacy, billing errors)
- **1**: Trivial even at massive scale - user ignores/overrides, self-correcting (e.g. Grammarly auto-correct, Spotify, Netflix recommendations)

**Checklist:** Failure scenario? Core business threat? Regulatory/legal? Reputational damage? Block initiatives?

**Avoid:** "Competitive market" ≠ catastrophic, bigger company ≠ higher consequence, high-impact ≠ high-consequence

**Governance for High Consequence (3)**: Require C-suite oversight regardless of priority score, especially since it may include safety (autonomous vehicles, medical), financial exposure, regulatory/legal implications, or brand risk. Even if approved, these may need continuous monitoring, incident response plans, and regular governance reviews.

**Example:** Tesla FSD scores low but strategically important → Framework correctly flags for special governance, not automatic "no-go"


---

#### Probability (1-3): Likelihood of errors using Data + Tech + Org Readiness
- **3**: Immature tech, poor data, complex integration, no experience (e.g. Google Flu Trends, Watson oncology)
- **2**: Proven tech with gaps, acceptable data, some experience, occasional errors (e.g. Github Copilot, Tesla FSD)
- **1**: Mature/battle-tested, excellent data, years of production, strong expertise (e.g. Grammarly, Netflix, Spotify recommendations)

**Readiness Check:**
- Data: Have/Good/Missing, presence of data engineerig or data science initiatives
- Tech: Production/Beta/Prototype, MLOps and other data/AI/ML technologies
- Org: Experienced/Learning/No experience within the teams

---

#### Cost-to-Fix (1-3): Recovery difficulty and timeline
- **3**: Hardware recalls, complete retraining, legal remediation, months (Tesla, Watson)
- **2**: Model adjustments, manual review, customer support, weeks (Copilot, Google Translate)
- **1**: Config changes, automated rollback, human-in-loop design, days (Grammarly, Spotify, Netflix)

**Checklist:** Easy rollback? Customer impact? Systems affected? Data/reputation damage? Recovery time?

---

### COST (Denominator - Single Factor)

#### Cost-to-Implement (1-3): Launch barriers + Economic sustainability
**Ask: "Given our capabilities and business model, how hard to launch sustainably?"**

- **1**: Ready to launch, pricing covers costs, existing infrastructure, clear ROI <1 year
  - Examples: GitHub Copilot (subscription covers API costs), Grammarly (freemium→premium), Spotify DW (subscription)
  - ✓ Data/Tech/Org ready, ✓ Revenue covers LLM/GPU costs day 1

- **2**: Some gaps, focused investment, break-even uncertain 1-2 years
  - Examples: New product lines, data acquisition needed, new team skills
  - ⚠ Need data/tech/org improvements, ⚠ ROI uncertain but plausible

- **3**: Low readiness, no path to profitability, major transformation, losses expected
  - Examples: Amazon Alexa ($10B losses), Amazon Go ($1M+/store), IBM Watson ($62M+)
  - ❌ Missing data/tech/org readiness, major talent up-skilling, ❌ No revenue model

**Ecosystem Plays:** High Cost (3) is CORRECT for strategic loss-leaders. Framework flags economics while acknowledging strategic value via high VALUE scores → "Strategic Bet" tier requiring executive approval. e.g. Amazon Alexa is strategic for ecosystem value despite losses.

**Checklist:** Data/Tech/Org readiness? Pricing model covers costs? Time to market?

---

## Structure/Components

### Execution Workflow

1. **Read this SKILL.md** - Understand formula, tiers, criteria
2. **Gather context** - Ask about vision, initiatives, OKRs, strategy, users, resources, risk tolerance
3. **Create comparison matrix** (`docs/comparison_matrix.md`) - List initiatives side-by-side with factual differences before scoring
4. **Score systematically** - Use criteria and checklists above
5. **Validate** - Challenge scores e.g. If Initiative A > Impact, why lower Adoption? Equal scores = document why
6. **Document rationale** - Complete justification template (`docs/scoring_justification.md`) for transparency
7. **Generate Excel** - Use Template.xlsx, fill yellow cells only (A, B-H, O), run recalc.py
8. **Provide analysis** - Explain scores, compare strengths/weaknesses, recommend by tier

---

## Template Usage

### Files

**Excel Assets:**
- `assets/AI_Use_Case_Prioritization_Template.xlsx` - Blank (use this)
- `assets/AI_Use_Case_Prioritization_Example.xlsx` - Reference for examples only (do not use)

**Documentation Templates:**
- `docs/scoring_justification.md` - Systematic score documentation
- `docs/comparison_matrix.md` - Side-by-side initiative comparison

### Excel Template Structure
**Data Tab - Fill yellow cells only:**
- **Row 4+**: Your initiatives
- **A**: Use Case Name
- **B**: Impact (1-3)
- **C**: Adoption (1-3)
- **D**: Differentiation (1-3)
- **E**: Consequence (1-3)
- **F**: Probability (1-3)
- **G**: Cost-to-Fix (1-3)
- **H**: Cost-to-Implement (1-3)
**I-N are AUTO CALCULATED, DO NOT EDIT):**
- **O**: Notes/Justification

**Dashboard Tab**: Auto-generates visualizations after recalc.py

**Instructions Tab**: Scoring rubrics (manual reference only - do not use or edit)

### Process
```
1. Load the template spreadsheet
2. Go to Data tab
3. Fill yellow cells (rows 4+, columns A, B-H, O)
4. Save file
5. Run Claude's native xlsx skill's recalc.py
6. Review Dashboard tab
```

---

## Common Scenarios

**User has 5-10 initiatives:** Ask questions → Compare → Score collaboratively → Generate spreadsheet → Discuss portfolio

**User wants framework only:** Explain methodology → Provide template → Offer scoring help

**Strategic decision support:** Score initiatives → Compare to benchmarks → Highlight governance needs → Generate memo

**Portfolio review:** Gather AI docs → Score all active initiatives → Generate dashboard → Categorize (Quick wins, Strategic bets, At-risk) → Recommend rebalancing

---

## Best Practices

### For Product Managers
- Don't game scores - Use judgment
- Phase-appropriate scoring - Pilot ≠ scale
- Update as you learn - Reassess readiness
- Framework informs, doesn't decide
- Flag strategic exceptions
- Document assumptions

### For Claude
- Ask clarifying questions - Don't guess
- Explain trade-offs clearly
- Reference real-world benchmarks
- Generate comprehensive rationales
- Use Template.xlsx (don't create from scratch)
- Complete documentation templates
- Validate with recalc.py
- Challenge counterintuitive scores

---

## Common Pitfalls

### Scoring Errors
1. Temporal bias - Don't penalize temporary launch constraints
2. Size bias - Bigger ≠ higher risk/cost
3. Feature parity trap - UI ≠ capability
4. First-mover fallacy - First ≠ sustainable
5. Consequence inflation - Competitive ≠ catastrophic
6. Ignoring scale effects - 1M vs 100M users matters
7. Conflating potential and actual - Adoption = realistic 12-18mo

### Technical Errors
1. Don't recreate Excel - Use template
2. Don't write custom formulas - Pre-configured
3. Don't skip validation - Run recalc.py
4. Don't forget justifications - Use templates
5. Only edit yellow cells - White cells auto-calculate

---

## Quick Reference

```
FORMULA: Priority = VALUE/(RISK+COST) → Normalize to 0-100

VALUE = Impact(1-3) × Adoption(1-3) × Differentiation(1-3)
RISK = Consequence(1-3) × Probability(1-3) × Cost-to-Fix(1-3)
COST = Cost-to-Implement(1-3)

TIERS: 🟢60-100 | 🟡20-59 | 🟠10-19 | 🔴<10

EXAMPLES (purely for illustrative scoring use, please verify independently):
- Grammarly: VALUE=27, RISK=1, COST=1 → 100 (perfect)
- GitHub Copilot: VALUE=27, RISK=4, COST=1 → 60 (successful)
- Amazon Alexa: VALUE=27, RISK=8, COST=3 → 27 (strategic bet)
- Tesla FSD: VALUE=18, RISK=18, COST=2 → 10 (executive oversight)
- Watson oncology: VALUE=6, RISK=27, COST=3 → 2 (catastrophic)
```

---

## Example Usage

```
User: "As OpenAI, should we build our own AI browser or integrate with existing ones?"

Claude:
1. Reads SKILL.md
2. Asks: user base, models, differentiation, resources, timeline
3. Creates comparison matrix
4. Scores using checklists:
   - Build Own: 3,2,2 | 3,2,3,3 → High risk/cost but strategic
   - Integrate: 2,3,1 | 1,1,1,1 → Lower risk/cost, faster
5. Loads Template.xlsx → Data tab
6. Fills yellow cells (rows 4-5)
7. Runs recalc.py
8. Delivers spreadsheet + analysis with rationale
```

## Output Deliverables

- **Prioritized AI Initiative Ranking** with objective 0-100 scores
- **Excel Dashboard** with automatic visualizations and priority tiers
- **Comparative Analysis Matrix** showing factual differences between initiatives
- **Detailed Scoring Rationale** documenting all scoring decisions and assumptions
- **Strategic Recommendations** by priority tier with clear next steps
- **Executive Summary** suitable for C-level stakeholder communication
- **Risk Assessment** highlighting governance needs for high-consequence initiatives

---
*Skill Category: Discovery & Strategy*  
*Version: 2.0 - Anthropic Best Practices*  