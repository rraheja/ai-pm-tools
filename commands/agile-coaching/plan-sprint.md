# Command: /plan-sprint

## Execution Context
**Primary Agent:** Agile Coaching Agent  
**Required Skills:** N/A  
**Command Category:** Agile Coaching  
**Version:** 2.0

## Purpose
Guide teams through effective sprint planning to establish clear goals, select appropriate work, and build team commitment to achievable deliverables within sprint capacity.

## When to Use
- Start of each sprint cycle (standard sprint planning)
- New team formation requiring planning process setup
- When teams need improvement in planning effectiveness
- Mid-sprint replanning due to scope changes
- Establishing planning consistency across multiple teams
- When sprint goals are frequently missed or unclear

## Structure/Components

### Required Information
If any of these are missing, I will ask you to provide them:
- **Team Name**: Which team is planning the sprint?
- **Sprint Duration**: How long is your sprint (1-4 weeks)?
- **Sprint Number**: What sprint number is this?

### Optional Information (will enhance sprint planning)
- **Sprint Goal**: What outcome should this sprint achieve?
- **Team Capacity**: Available hours/points for this sprint?
- **Previous Velocity**: Historical velocity data?
- **Backlog Status**: Is the backlog refined and estimated?
- **Dependencies**: Any external dependencies or commitments?

## Sprint Planning Agenda

### Part 1: Sprint Goal & Scope (1 hour)
1. **Review Sprint Goal**
   - What business value will we deliver?
   - How does this align with objectives?

2. **Review Capacity**
   - Team availability
   - Holiday/vacation
   - Known meetings/commitments

3. **Backlog Review**
   - Top priority stories
   - Dependencies
   - Definition of Ready check

### Part 2: Task Breakdown (1 hour)
4. **Story Breakdown**
   - Discuss each story
   - Identify tasks
   - Estimate effort

5. **Commitment**
   - Pull in stories until capacity full
   - Stretch goals (if time permits)

6. **Sprint Backlog Creation**
   - Finalize sprint scope
   - Set up board

## Sprint Planning Outputs
- **Sprint Goal**: One-sentence objective
- **Sprint Backlog**: Committed stories
- **Task Breakdown**: Technical tasks per story
- **Definition of Done**: Acceptance criteria
- **Capacity Plan**: Who's working on what

## Estimation Techniques
- Story points (Fibonacci scale)
- T-shirt sizing (XS, S, M, L, XL)
- Ideal days/hours

## Example Usage
```
/plan-sprint

Team: Backend API team (5 developers)
Sprint length: 2 weeks
Velocity: 30-35 story points
Focus: Payment integration features
Constraints: 2 team members out for 2 days
```


## Output Deliverables
- **Sprint Planning Agenda** with timing and activities
- **Clear Sprint Goal Statement** aligned with product objectives
- **Committed Sprint Backlog** with realistic scope and estimates
- **Team Capacity Analysis** showing available effort and commitments
- **Sprint Success Criteria** with measurable outcomes
- **Planning Retrospective Summary** for continuous improvement
- **Daily Standup Framework** optimized for this sprint

## Parameter Guidance
If you don't provide all the information I need, I'll guide you through questions like:
- "Which team are we planning for and what's your sprint length?"
- "What's the main outcome you want to achieve this sprint?"
- "How many team members will be available and at what capacity?"
- "What's your team's typical velocity or throughput?"
- "Is your product backlog refined with estimates and priorities?"
- "Are there any dependencies or external commitments to consider?"

---
*Command Category: Agile Coaching*  
*Version: 2.0 - Anthropic Best Practices*  
*Last Updated: October 2025*
