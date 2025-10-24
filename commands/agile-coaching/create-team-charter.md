# Command: /create-team-charter

## Execution Context
**Primary Agent:** Agile Coach Agent  
**Required Skills:** agile-ceremonies  
**Command Category:** Agile Coaching  
**Version:** 2.0

## Purpose
Establish team working agreements, norms, and values to foster healthy collaboration and high performance. This command helps new or restructured teams define how they will work together.

## When to Use
- **New team formation**: Setting up foundations for a new product team
- **Team restructuring**: Major changes in team composition or reporting structure
- **Culture issues**: Team experiencing communication problems or conflict
- **Team health improvement**: Proactive investment in team dynamics
- **Distributed teams**: Establishing clear norms for remote/hybrid work

## Required Context from User

Before executing, gather:
1. **Team Composition**: Size, roles (eng, PM, design, QA, etc.), seniority levels
2. **Geographic Distribution**: Time zones, office locations, remote work setup
3. **Current Challenges**: Any known pain points or team health issues (optional)
4. **Team Maturity**: Is this a new team or established team?
5. **Organizational Context**: Company culture, existing standards/policies
6. **Timeline**: When the charter needs to be complete

## Task Execution Framework

### Step 1: Discovery & Assessment
- Review provided team context
- Identify any team-specific constraints or requirements
- Determine appropriate level of detail based on team maturity

### Step 2: Charter Structure
Create a comprehensive team charter covering these components:

**1. Team Purpose & Mission**
   - Why does this team exist?
   - What value do we deliver to the organization?
   - How do we measure success?

**2. Team Members & Roles**
   - Who is on the team and what are their roles?
   - What expertise does each person bring?
   - How do we contact each other?

**3. Working Agreements**
   - Core working hours and availability expectations
   - Communication channels and when to use them (Slack, email, meetings)
   - Response time expectations
   - Meeting norms (cameras on, punctuality, preparation)
   - Focus time and interruption policies

**4. Decision-Making Protocols**
   - How do we make decisions? (consensus, consent, delegation, voting)
   - When do we need to escalate?
   - Who has final say on what types of decisions?
   - How do we document decisions?

**5. Team Values & Principles**
   - What behaviors do we value?
   - How do we want to treat each other?
   - How do we handle conflict?
   - How do we give and receive feedback?

**6. Tools & Development Process**
   - What tools do we use? (Jira, GitHub, Figma, etc.)
   - What is our development workflow?
   - Documentation standards and locations
   - Code review and approval processes

**7. Definition of Done (DoD)**
   - What does "done" mean for our work?
   - Code quality standards
   - Testing requirements
   - Documentation requirements
   - Deployment criteria

**8. Definition of Ready (DoR)**
   - When is a story ready to be worked on?
   - What information needs to be available?
   - Who needs to approve stories?
   - Design and technical clarity requirements

### Step 3: Adaptation Based on Context

**For New Teams:**
- Include more prescriptive guidelines initially
- Plan for a review after first sprint/month
- Keep language welcoming and inclusive

**For Distributed Teams:**
- Emphasize asynchronous communication norms
- Define overlap hours for real-time collaboration
- Address time zone considerations explicitly

**For Experienced Teams:**
- Focus on gaps and improvement areas
- Reference existing company standards
- Emphasize team-specific agreements

### Step 4: Output Generation
Create the following deliverables:

1. **Team Charter Document** (Google Doc format)
   - Comprehensive 4-6 page document
   - Professional formatting with sections and examples
   - Editable template for team to customize

2. **Working Agreements Poster** (1-page summary)
   - Visual reference of key agreements
   - Can be printed or shared digitally
   - Focus on most critical norms

3. **Communication Guide** (Quick reference)
   - Channel matrix (what tool for what purpose)
   - Response time expectations
   - Escalation paths

4. **Implementation Recommendations**
   - How to socialize the charter with the team
   - Facilitation approach for team review
   - Suggested review cadence (quarterly)
   - Metrics to track charter effectiveness

## Quality Criteria

The charter should be:
- ✅ **Specific**: Concrete behaviors, not vague aspirations
- ✅ **Actionable**: Clear enough that team can follow it
- ✅ **Measurable**: Where possible, define observable behaviors
- ✅ **Realistic**: Achievable given team constraints
- ✅ **Team-owned**: Invite team input and customization
- ✅ **Living document**: Designed to evolve with team

## Example Usage

```
/create-team-charter

Team: Product Platform API Team
Size: 8 people (5 backend engineers, 1 PM, 1 designer, 1 QA)
Distribution: 3 time zones (PST, EST, UTC+1)
Context: Newly formed team combining members from 2 legacy teams
Challenges: Different code review standards, unclear prioritization process
Goal: Establish clear working norms and rebuild team cohesion
Timeline: Need charter by next sprint (2 weeks)
```

## Follow-up Recommendations

After creating the charter:
1. **Facilitate a team review session** (suggest 90-minute workshop format)
2. **Set up a 30-day check-in** to adjust based on what's working
3. **Establish quarterly review** as part of retrospective
4. **Create measurement plan** for charter effectiveness
5. **Share with stakeholders** who interact with the team

## Notes for Execution

- Load the Agile Coach Agent persona fully before beginning
- Reference agile-ceremonies skill for best practices
- Tailor tone to team maturity (newer teams need more structure)
- If geographic distribution is complex, emphasize async practices
- Consider company culture and existing policies when making recommendations
- Always provide concrete examples for each section
- Leave room for team to customize and make it their own

---

*Command Category: Agile Coaching*  
*Version: 2.0 - Anthropic Best Practices*  
*Last Updated: October 2025*
