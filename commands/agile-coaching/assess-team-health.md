# Command: /assess-team-health

## Execution Context
**Primary Agent:** Agile Coaching Agent  
**Required Skills:** N/A  
**Command Category:** Agile Coaching  
**Version:** 2.0

## Purpose
Conduct comprehensive team health assessments to identify strengths, challenges, and improvement opportunities across delivery, collaboration, technical practices, and team dynamics.

## When to Use
- Quarterly team reviews and health check-ins
- New team formation (establishing baseline metrics)
- After organizational changes or restructuring
- When performance issues or velocity decline is observed
- Low morale indicators or team dysfunction symptoms
- Before implementing process or tooling changes
- Annual team development planning

## Structure/Components

### Required Information
If any of these are missing, I will ask you to provide them:
- **Team Name**: Which specific team are we assessing?
- **Team Size**: How many people and what roles?
- **Assessment Context**: What triggered this health check?

### Optional Information (will enhance the assessment)
- **Previous Assessments**: Any baseline data or historical trends?
- **Specific Concerns**: Areas you want to focus on?
- **Recent Changes**: Organizational, process, or team changes?
- **Timeline**: How urgently do you need results and improvements?

## Health Assessment Dimensions

1. **Delivery**
   - Meeting commitments
   - Velocity trends
   - Quality metrics

2. **Collaboration**
   - Cross-functional partnership
   - Communication effectiveness
   - Knowledge sharing

3. **Technical Practices**
   - Code quality
   - Test automation
   - CI/CD maturity

4. **Learning & Growth**
   - Skill development
   - Innovation time
   - Career progression

5. **Work/Life Balance**
   - Sustainable pace
   - Overtime frequency
   - Burnout indicators

6. **Psychological Safety**
   - Speak up comfort
   - Mistake tolerance
   - Feedback culture

7. **Purpose & Engagement**
   - Clarity of goals
   - Work meaningfulness
   - Team morale

## Assessment Methods
- Anonymous surveys
- Team discussions
- One-on-ones
- Metric analysis
- Observation

## Scoring
Each dimension rated 1-5:
- 🔴 1-2: Needs immediate attention
- 🟡 3: Room for improvement
- 🟢 4-5: Healthy

## Example Usage
```
/assess-team-health

Team: Mobile engineering team
Size: 6 developers
Context: Recent leadership change, velocity declining
Concerns: Morale and technical debt
```


## Output Deliverables
- **Comprehensive Health Assessment Report** with scores across all 7 dimensions
- **Visual Radar Chart** showing team strengths and improvement areas
- **Prioritized Action Plan** with specific, measurable improvement steps
- **Trend Analysis** comparing to previous assessments (if available)
- **Team Discussion Guide** for sharing results and building consensus
- **90-Day Improvement Roadmap** with milestones and success metrics

## Parameter Guidance
If you don't provide all the information I need, I'll guide you through questions like:
- "Which team would you like to assess and how many members?"
- "What specific concerns or symptoms prompted this assessment?"
- "Have you done team health assessments before with this group?"
- "Are there particular areas you want to focus on (delivery, morale, technical practices)?"
- "What timeline do you have for implementing improvements?"

---
*Command Category: Agile Coaching*  
*Version: 2.0 - Anthropic Best Practices*  
*Last Updated: October 2025*
