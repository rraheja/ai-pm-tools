# Command: /create-ux-design

## Execution Context
**Primary Agent:** Product Design Agent
**Required Skills:** None (prompt-based)
**Command Category:** Design
**Version:** 2.0

## Purpose
Design user interface, interaction flows, and UX patterns for product features.

## When to Use
- Creating new feature designs
- Redesigning existing interfaces
- Defining user interaction patterns
- Planning user journeys and flows

## What to Provide
- **Feature description**: What are we designing?
- **User personas**: Who will use this?
- **Key user goals**: What are users trying to accomplish?
- **Constraints** (optional): Platform, technical, brand guidelines

## What You'll Get
Generated in `03_Design/design.md`:
- **User Journey**: Step-by-step user flow with decision points
- **Interface Layout**: Screen structure and component hierarchy
- **Interaction Patterns**: How users interact with the interface
- **UX Principles**: Accessibility, usability, and design best practices
- **Design Tokens** (optional): Colors, spacing, typography suggestions

## Example Usage
```
/create-ux-design

Feature: AI-powered meeting scheduler
Users: Busy executives and their assistants
Goals: Schedule meetings in <30 seconds with zero email back-and-forth
Constraints: Mobile-first, must integrate with Google/Outlook calendars
```

## Output File
- `03_Design/design.md`

---

*Command Category: Design*
*Version: 2.0*
*Last Updated: October 2025*
