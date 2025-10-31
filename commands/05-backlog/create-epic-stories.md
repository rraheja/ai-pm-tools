# Command: /create-epic-stories

## Execution Context
**Primary Agent:** Product Manager Agent  
**Required Skills:** requirements-engineering  
**Command Category:** Design & Development  
**Version:** 2.0

## Purpose
Break down epics into detailed user stories with acceptance criteria, ready for sprint planning. This command structures epic requirements into actionable development tasks that teams can estimate, prioritize, and implement incrementally while maintaining clear traceability to business value.

## When to Use
- **Sprint Planning Preparation**: Breaking down epics into sprint-ready user stories
- **Backlog Refinement**: Decomposing high-level requirements into detailed tasks
- **Release Planning**: Creating shippable increments with clear scope boundaries
- **Work Estimation**: Structuring requirements for accurate effort estimation
- **Team Alignment**: Ensuring shared understanding of feature requirements
- **Quality Assurance**: Defining testable acceptance criteria for development validation

## Structure/Components

### Required Information
If any of these are missing, I will ask you to provide them:
- **Epic Title**: Clear, business-value focused name
- **Epic Description**: High-level capability or feature being delivered
- **User Roles**: Specific personas who will interact with the feature

### Optional Information (will enhance the story breakdown)
- **Business Value**: Clear articulation of why this epic matters
- **Target Platforms**: Web, mobile, API specifications
- **Technical Constraints**: Performance, security, compliance requirements
- **Integration Points**: External systems or dependencies
- **Timeline Constraints**: Release deadlines or sequencing requirements
- **Success Metrics**: How epic success will be measured post-release

## Required Skill
**Skill:** `requirements-engineering`

## User Story Format
```
Title: [Action-oriented, user-centric]

As a [specific user role],
I want to [capability/action],
So that [business value/benefit].

Acceptance Criteria:
- Given [precondition], when [action], then [expected outcome]
- [Additional criteria...]

Technical Notes:
- [API endpoints, data requirements, dependencies]

Estimated Effort: [Story points]

Definition of Done:
- Unit tests passing
- Code reviewed
- Documentation updated
- Deployed to staging
```

## Story Breakdown Principles
- Each story should be completable in one sprint
- Stories should deliver user value independently
- Break along vertical slices (full stack)
- Include technical enablers when needed
- Consider edge cases and error handling

## Example Usage
```
/create-epic-stories

Epic: Multi-factor authentication
User roles: End users, IT admins
Platforms: Web, mobile apps
MFA methods: SMS, authenticator app, hardware key
```


## Output Deliverables
- **User Stories Collection**: Complete set of stories following INVEST criteria
- **Acceptance Criteria**: Detailed, testable conditions for each story
- **Story Dependencies**: Technical and logical sequencing requirements
- **Estimation Framework**: Story point guidance and complexity assessment

## Parameter Guidance
If you don't provide all the information I need, I'll guide you through questions like:
- "What's the epic we're breaking down and what business value does it deliver?"
- "Who are the specific user types that will interact with this feature?"
- "Are there any technical constraints or integration requirements?"
- "What platforms or systems need to support this epic?"
- "What does success look like and how will we measure it?"

## Best Practices
- Use INVEST criteria (Independent, Negotiable, Valuable, Estimable, Small, Testable)
- Include happy path and edge cases
- Define clear acceptance criteria
- Add mockups/diagrams where helpful
- Consider non-functional requirements

---
*Command Category: Design & Development*  
*Version: 2.0 - Anthropic Best Practices*  
*Last Updated: October 2025*
