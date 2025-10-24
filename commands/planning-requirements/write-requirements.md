# Command: /write-requirements

## Purpose
Create a comprehensive Product Requirements Document (PRD) for development teams with structured acceptance criteria, user stories, and technical specifications that enable clear communication and successful feature delivery.

## When to Use
- Defining new features or products requiring detailed specifications
- Communicating requirements to engineering teams
- Creating shared understanding of scope and acceptance criteria
- Documenting functional and non-functional requirements
- Establishing clear success metrics and validation criteria
- When stakeholders need alignment on what success looks like

## Structure/Components

### Required Information
If any of these are missing, I will ask you to provide them:
- **Feature Name**: What are we building?
- **Target Users**: Who will use this and in what context?
- **Problem Statement**: What specific problem does this solve?

### Optional Information (will enhance the PRD)
- **Success Metrics**: How will we measure success?
- **Technical Constraints**: Any platform, performance, or integration requirements?
- **Timeline**: Expected delivery milestones?
- **Out of Scope**: What are we explicitly NOT building?

### PRD Structure Generated
1. **Executive Summary** - Problem, solution, success metrics
2. **User Personas & Scenarios** - Target users, key use cases, workflows
3. **Functional Requirements** - Features, capabilities, acceptance criteria
4. **Non-Functional Requirements** - Performance, security, scalability
5. **Technical Requirements** - APIs, integrations, data model
6. **Out of Scope** - What we're NOT building
7. **Success Metrics** - KPIs and measurement plan
8. **Open Questions** - Items needing resolution
9. **Appendix** - Mockups, diagrams, research

## PRD Structure
1. **Executive Summary**
   - Problem statement
   - Solution overview
   - Success metrics

2. **User Personas & Scenarios**
   - Target users
   - Key use cases
   - User workflows

3. **Functional Requirements**
   - Features and capabilities
   - Acceptance criteria
   - Edge cases

4. **Non-Functional Requirements**
   - Performance
   - Security
   - Scalability
   - Accessibility

5. **Technical Requirements**
   - APIs and integrations
   - Data model
   - Platform requirements

6. **Out of Scope**
   - What we're NOT building

7. **Success Metrics**
   - KPIs and measurement plan

8. **Open Questions**
   - Items needing resolution

9. **Appendix**
   - Mockups, diagrams, research

## Example Usage

### Basic Usage
```
/write-requirements feature_name="Multi-factor Authentication" target_users="Enterprise IT administrators and end users" problem_statement="Current single-factor authentication creates security vulnerabilities for enterprise accounts"
```

### Advanced Usage
```
/write-requirements feature_name="Smart Meeting Scheduler" target_users="Busy executives and their assistants" problem_statement="Manual meeting scheduling creates 2-3 hours of back-and-forth emails weekly" success_metrics="Reduce scheduling time by 80%, increase meeting completion rate by 20%" technical_constraints="Must integrate with Google Calendar, Outlook, and Zoom" timeline="Q2 2024 delivery" out_of_scope="Room booking, catering coordination"
```


## Output Deliverables
- Comprehensive PRD (DOCX format)
- Acceptance criteria document
- Technical specifications

## Output Deliverables
- **Comprehensive PRD Document** (DOCX format)
- **User Story Collection** with acceptance criteria
- **Technical Specification Outline** for engineering collaboration
- **Success Metrics Dashboard Design** with KPIs
- **Stakeholder Review Checklist** for validation

## Parameter Guidance
If you don't provide all the information I need, I'll guide you through questions like:
- "Can you describe the specific user problem we're solving?"
- "Who are the primary users and what's their context?"
- "What would success look like for this feature?"
- "Are there any technical constraints I should know about?"
- "What's explicitly out of scope for this release?"

## Best Practices
- Start with the "why" (problem statement) before defining "what"
- Be specific about outcomes but flexible on implementation approach
- Include user workflows, mockups, and interaction patterns
- Define edge cases, error states, and failure scenarios
- Review with engineering and design teams before finalizing
- Validate assumptions with user research and data when possible

---
*Command Category: Planning & Requirements*  
*Version: 1.0*
