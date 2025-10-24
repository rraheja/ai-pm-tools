# Command: /create-roadmap-epics

## Execution Context
**Primary Agent:** Product Manager Agent  
**Required Skills:** product-roadmapping  
**Command Category:** Planning & Requirements  
**Version:** 2.0

## Purpose
Generate epics from a strategic roadmap, breaking down themes into actionable bodies of work.

## When to Use
- Translating strategy into execution
- Planning quarterly objectives
- Breaking down large initiatives
- Preparing for sprint planning

## Required Skill
**Skill:** `product-roadmapping`

## How It Works
1. **Roadmap Analysis**: Reviews strategic roadmap and themes
2. **Epic Definition**: Creates epics for each roadmap item
3. **Value Articulation**: Defines business value and user impact
4. **Scope Sizing**: Estimates epic size and complexity
5. **Dependency Mapping**: Identifies cross-epic dependencies
6. **Prioritization**: Recommends sequencing

## Epic Format
```
Epic Name: [Action-oriented title]

Description:
Clear description of the epic's purpose and scope

Business Value:
Why this matters and expected impact

User Stories (High-Level):
- As a [user], I want [capability]...
- As a [user], I want [capability]...

Acceptance Criteria:
- What defines "done" for this epic

Dependencies:
- Other epics or systems required

Estimated Effort: [T-shirt size: XS/S/M/L/XL]

Priority: [High/Medium/Low]
```

## Example Usage
```
/create-roadmap-epics

Roadmap theme: "AI-Powered Insights"
Timeline: Q2 2025
Goal: Enable customers to get automated insights from their data
```


## Output Deliverables
- **Epic Collection**: Detailed epic descriptions with clear business value statements
- **Acceptance Criteria**: Comprehensive success conditions for each epic
- **Implementation Guidance**: Technical approach and sequencing recommendations
- **Effort Estimation**: Sizing guidance and complexity assessment for each epic
- **Dependency Map**: Cross-epic and external dependencies clearly identified
- **User Story Templates**: Foundation stories ready for further decomposition

## Parameter Guidance
If you don't provide all the information I need, I'll guide you through questions like:
- "What roadmap theme or strategic initiative are we breaking down into epics?"
- "What business goals should these epics achieve?"
- "Who are the target users and what value will they get?"
- "Are there technical constraints or platform requirements to consider?"
- "What timeline or delivery expectations exist for this theme?"
- "How will we measure success for these epics?"

---
*Command Category: Planning & Requirements*  
*Version: 2.0 - Anthropic Best Practices*
*Last Updated: October 2025*
