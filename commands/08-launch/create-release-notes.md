# Command: /create-release-notes

## Execution Context
**Primary Agent:** Product Manager Agent  
**Required Skills:** N/A  
**Command Category:** Design & Development  
**Version:** 2.0

## Purpose
Generate customer-facing release notes from changelog or development updates. This command transforms technical development information into clear, actionable communication that helps customers understand product changes, adopt new features, and maintain operational continuity.

## When to Use
- **Product Release Communication**: Announcing new versions and capabilities
- **Customer Update Cycles**: Regular communication of product evolution
- **Change Documentation**: Creating official record of product modifications
- **Customer Support**: Enabling support teams with change information
- **Compliance Requirements**: Meeting regulatory or contractual documentation needs
- **User Training**: Helping users understand and adopt new features
- **Migration Planning**: Communicating deprecations and upgrade paths

## Structure/Components

### Required Information
If any of these are missing, I will ask you to provide them:
- **Version Information**: Release number, date, and deployment status
- **Change Summary**: High-level overview of what's included in release
- **Feature Details**: New capabilities with customer-focused descriptions

### Optional Information (will enhance the release notes)
- **Impact Assessment**: How changes affect existing users and workflows
- **Migration Guides**: Step-by-step instructions for significant changes
- **Deprecation Timeline**: Phase-out schedules and replacement options
- **Known Issues**: Current limitations with workaround instructions
- **Performance Metrics**: Quantified improvements or benchmarks
- **Integration Details**: API changes or third-party connectivity updates
- **Security Updates**: Privacy and security enhancement communications

## Release Notes Structure
1. **Release Summary**
   - Version number and date
   - Overview of changes
   - Key highlights

2. **New Features**
   - What's new
   - Why it matters
   - How to use

3. **Improvements**
   - Enhancements to existing features
   - Performance improvements
   - UI/UX refinements

4. **Bug Fixes**
   - Issues resolved
   - Impact description

5. **Known Issues** (if any)
   - Current limitations
   - Workarounds
   - Fix timeline

6. **Deprecations** (if any)
   - What's being removed
   - Migration path
   - Timeline

## Example Usage
```
/create-release-notes

Version: 2.5.0
Changelog:
- Added real-time collaboration
- Improved search performance by 50%
- Fixed issue with file exports
- Deprecated v1 API endpoints
```


## Output Deliverables
- **Formatted Release Notes**: Customer-ready documentation in multiple formats
- **Customer Communications**: Email templates and in-app notification content
- **Change Documentation**: Detailed technical changelog for internal teams
- **Migration Resources**: Guides and tools for customer transitions

## Parameter Guidance
If you don't provide all the information I need, I'll guide you through questions like:
- "What version are we releasing and what are the major changes?"
- "Who are the primary users affected by these changes?"
- "Are there any breaking changes or required customer actions?"
- "What new features should customers be most excited about?"
- "Are there any deprecations or timeline considerations?"
- "How should customers get help if they have questions about changes?"

## Writing Guidelines
- Use customer-friendly language (avoid jargon)
- Focus on benefits, not technical details
- Include screenshots for visual features
- Organize by customer impact (most important first)
- Keep tone positive and informative
- Link to documentation for details

---
*Command Category: Design & Development*  
*Version: 2.0 - Anthropic Best Practices*  
*Last Updated: October 2025*
