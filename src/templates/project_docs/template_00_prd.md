# {{Project Name}} Product Requirements Document (PRD)

## Overview

This PRD serves as the single source of truth for the {{Project Name}} project. It defines what we're building, why we're building it, and how we'll measure success. All subsequent technical architecture, work planning, and implementation must align with and serve the requirements defined in this document.

## Goals and Background Context

### Goals

**Primary Goals:**
- {{Goal 1: Specific, measurable outcome}}
- {{Goal 2: Specific, measurable outcome}}
- {{Goal 3: Specific, measurable outcome}}

**Success Metrics:**
- {{Metric 1: How we'll measure success}}
- {{Metric 2: How we'll measure success}}

### Background Context

{{Provide 1-2 paragraphs summarizing:
- The problem this project solves
- Current state and challenges
- Why this solution is needed now
- Target audience/users}}

## Requirements

### Functional Requirements

<!-- Each requirement should be clear, testable, and traceable -->
- **FR1:** {{Describe what the system must do}}
- **FR2:** {{Describe what the system must do}}
- **FR3:** {{Describe what the system must do}}

### Non-Functional Requirements

<!-- Performance, security, scalability, usability requirements -->
- **NFR1:** {{Performance/scalability requirement}}
- **NFR2:** {{Security/compliance requirement}}
- **NFR3:** {{Usability/accessibility requirement}}

## User Interface Design Goals

<!-- Only include this section if the project has a user interface -->

### Overall UX Vision

{{Describe the high-level user experience philosophy and key principles}}

### Key Interaction Paradigms

{{Describe how users will primarily interact with the system}}

### Core Screens and Views

{{List the essential screens/views needed to deliver the PRD value:}}
- {{Screen 1: Purpose and key functionality}}
- {{Screen 2: Purpose and key functionality}}
- {{Screen 3: Purpose and key functionality}}

### Target Platforms

{{Specify target platforms: Web, Mobile, Desktop, etc.}}

### Accessibility Requirements

{{Specify accessibility standards: WCAG level, specific requirements}}

## Technical Assumptions

<!-- These become constraints for the architect -->

### Repository Structure
{{Monorepo, Polyrepo, etc.}}

### Service Architecture
{{Monolith, Microservices, Serverless, etc.}}

### Core Technology Stack
- **Backend:** {{Language/Framework}}
- **Frontend:** {{Framework/Library (if applicable)}}
- **Database:** {{Database technology}}
- **Deployment:** {{Platform/service}}

### Testing Strategy
{{Unit, Integration, E2E requirements and tools}}

### Additional Technical Constraints
- {{Constraint 1}}
- {{Constraint 2}}
- {{Constraint 3}}

## Epics Overview

<!-- High-level delivery milestones that provide significant value -->

### Epic 1: {{Epic Title}}
**Goal:** {{1-2 sentence description of what this epic achieves}}
**Value:** {{What business/user value does this deliver}}

### Epic 2: {{Epic Title}}
**Goal:** {{1-2 sentence description of what this epic achieves}}
**Value:** {{What business/user value does this deliver}}

### Epic 3: {{Epic Title}}
**Goal:** {{1-2 sentence description of what this epic achieves}}
**Value:** {{What business/user value does this deliver}}

## Dependencies and Assumptions

### External Dependencies
- {{External service/API dependency}}
- {{Third-party library/tool dependency}}

### Key Assumptions
- {{Assumption 1 that impacts the project}}
- {{Assumption 2 that impacts the project}}

## Risks and Mitigation

### High Priority Risks
- **Risk:** {{Risk description}}
  - **Impact:** {{Potential impact}}
  - **Mitigation:** {{How we'll address this}}

### Medium Priority Risks
- **Risk:** {{Risk description}}
  - **Impact:** {{Potential impact}}
  - **Mitigation:** {{How we'll address this}}

## Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | {{Date}} | {{Author}} | Initial PRD creation |

---

## Next Steps

After completing this PRD:
1. Run the PRD Review Checklist (`checklists/template_prd_review_checklist.md`)
2. Create the Technical Architecture Document (`template_01_architecture.md`)
3. Break down Epics into detailed Stories (`template_02_work_plan_progress.md`)

---

*This PRD serves as the foundation for all project work. Any changes to requirements or scope should be reflected here first.* 