# Command: /create-test-plan

## Execution Context
**Primary Agent:** Quality Assurance Agent  
**Required Skills:** N/A  
**Command Category:** Design & Development  
**Version:** 2.0

## Purpose
Create comprehensive test strategy and QA plans to ensure product quality. This command develops systematic testing approaches that validate functionality, performance, security, and user experience while establishing clear quality gates and risk mitigation strategies for product releases.

## When to Use
- **Product Development Initiation**: Establishing quality framework for new products
- **Feature Release Planning**: Ensuring comprehensive testing before major releases
- **Quality Issue Response**: Addressing production problems with systematic testing
- **Compliance Validation**: Meeting regulatory, security, or industry standards
- **Performance Optimization**: Validating system performance under various conditions
- **Integration Testing**: Verifying system interactions and data flow integrity
- **Risk Mitigation**: Reducing quality risks through structured testing approaches

## Structure/Components

### Required Information
If any of these are missing, I will ask you to provide them:
- **Testing Scope**: Features, systems, and functionality to be tested
- **Quality Objectives**: Specific goals and success criteria for testing
- **Test Environment**: Infrastructure, data, and configuration requirements

### Optional Information (will enhance the test plan)
- **Resource Allocation**: Team members, tools, and timeline for testing
- **Risk Assessment**: High-risk areas requiring focused testing attention
- **Automation Strategy**: Tools and frameworks for automated testing
- **Performance Benchmarks**: Specific metrics and acceptance thresholds
- **Security Requirements**: Vulnerability testing and compliance validation
- **Accessibility Standards**: WCAG compliance and usability testing criteria
- **Integration Points**: Third-party systems and API testing requirements
- **Regulatory Compliance**: Industry-specific testing and validation needs

## Test Plan Structure
1. **Test Scope & Objectives**
   - Features to test
   - Quality goals
   - Success criteria

2. **Test Strategy**
   - Types of testing (unit, integration, E2E, performance, security)
   - Test environments
   - Automation approach

3. **Test Cases**
   - Functional test scenarios
   - Edge cases and negative tests
   - Accessibility tests
   - Performance benchmarks

4. **Test Schedule**
   - Testing phases
   - Entry and exit criteria
   - Resource allocation

5. **Risk Assessment**
   - High-risk areas
   - Mitigation strategies

6. **Defect Management**
   - Severity classification
   - Triage process
   - Fix/retest workflow

## Example Usage
```
/create-test-plan

Feature: Payment processing system
Requirements: PCI compliance, 99.9% uptime
Volume: 10,000 transactions/day
Platforms: Web, iOS, Android
```


## Output Deliverables
- **Comprehensive Test Plan**: Detailed testing strategy and execution framework
- **Test Case Repository**: Organized collection of functional and non-functional tests
- **Automation Roadmap**: Strategy for test automation implementation and maintenance
- **Quality Metrics Dashboard**: KPIs and measurement framework for testing effectiveness

## Parameter Guidance
If you don't provide all the information I need, I'll guide you through questions like:
- "What specific features or systems need testing coverage?"
- "What are your quality goals and success criteria?"
- "What testing environments and resources are available?"
- "Are there particular risk areas or compliance requirements?"
- "What's your timeline and resource allocation for testing?"
- "Do you need automation strategy or manual testing focus?"

## Testing Types Coverage
- **Functional**: Features work as specified
- **Integration**: Systems work together
- **Performance**: Speed and scalability
- **Security**: Vulnerabilities and threats
- **Usability**: User experience quality
- **Accessibility**: WCAG compliance
- **Compatibility**: Browsers, devices, OS
- **Regression**: Existing functionality intact

---
*Command Category: Design & Development*  
*Version: 2.0 - Anthropic Best Practices*  
*Last Updated: October 2025*
