# Command: /facilitate-retrospective

## Execution Context
**Primary Agent:** Agile Coaching Agent  
**Required Skills:** N/A  
**Command Category:** Agile Coaching  
**Version:** 2.0

## Purpose
Guide teams through structured retrospective sessions to inspect team performance, identify improvement opportunities, and create actionable experiments that drive continuous improvement and team effectiveness.

## When to Use
- End of sprints or iterations for continuous improvement
- End of major projects or milestones
- After significant incidents or failures requiring learning
- When team health or collaboration concerns arise
- During process improvement initiatives or team formation
- When team velocity or quality metrics show concerning trends
- When teams are stuck in unproductive patterns

## Structure/Components

### Required Information
If any of these are missing, I will ask you to provide them:
- **Team Name**: Which team are we facilitating?
- **Time Period**: What sprint, project, or time period are we reviewing?
- **Session Duration**: How much time do we have (30-120 minutes)?

### Optional Information (will enhance the facilitation)
- **Retrospective Format**: Any preference (Start/Stop/Continue, 4Ls, Sailboat, etc.)?
- **Team Size**: How many participants?
- **Specific Focus**: Any particular area to explore (process, collaboration, tools)?
- **Previous Actions**: Action items from the last retrospective?
- **Team Mood**: General sentiment or energy level?

### Facilitation Structure

1. **Set the Stage** (5 min)
   - Create psychological safety
   - Review prime directive
   - Set working agreements

2. **Gather Data** (15 min)
   - Collect observations
   - Use chosen format
   - Silent generation first

3. **Generate Insights** (20 min)
   - Group similar items
   - Discuss patterns
   - Identify root causes

4. **Decide What to Do** (15 min)
   - Vote on top items
   - Create actionable experiments
   - Assign owners

5. **Close** (5 min)
   - Summarize actions
   - Reflect on retrospective itself

## Available Retrospective Formats

**Start/Stop/Continue**: New practices to begin, wasteful activities to eliminate, what's working well

**4Ls (Liked/Learned/Lacked/Longed For)**: What went well, new insights, what was missing, what we wish we had

**Sailboat**: Wind (helped us), Anchors (slowed us), Rocks (risks ahead), Island (our goal)

**Mad/Sad/Glad**: Focus on emotional responses to events

**Timeline**: Review events chronologically, mark highs and lows

*I will recommend the best format based on your team's situation and goals.*

## Example Usage

### Basic Usage
```
/facilitate-retrospective team_name="Mobile Development Team" time_period="Sprint 23" session_duration=60
```

### Advanced Usage
```
/facilitate-retrospective team_name="Platform Engineering" time_period="Q1 2024" session_duration=90 retrospective_format="Timeline" team_size=8 specific_focus="delivery process and technical debt" previous_actions=["Implement automated testing", "Reduce meeting overhead", "Improve code review process"] team_mood="frustrated with recent production issues"
```

### Incident-Focused Usage
```
/facilitate-retrospective team_name="Backend Services" time_period="Post-incident review for service outage" session_duration=75 retrospective_format="Timeline" specific_focus="incident response and prevention" team_mood="concerned about system reliability"
```


## Output Deliverables
- **Facilitation Guide** with step-by-step timing and activities
- **Retrospective Template** for the chosen format
- **Action Items List** with owners and success criteria
- **Experiment Plan** with hypotheses and measurement approach
- **Team Health Assessment** based on observations
- **Follow-up Schedule** for accountability and check-ins

## Parameter Guidance
If you don't provide all the information I need, I'll guide you through questions like:
- "Which team are we running this retrospective for?"
- "What time period should we focus on (sprint number, project phase)?"
- "How much time do we have for the session?"
- "Are there any specific issues or focus areas?"
- "What format would work best for your team's current situation?"
- "What action items from the last retrospective should we review?"

---
*Command Category: Agile Coaching*  
*Version: 2.0 - Anthropic Best Practices*  
*Last Updated: October 2025*
