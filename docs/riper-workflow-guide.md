![CursorRIPER](../res/github-header.png)
# CursorRIPER Framework 2.0 - PRD-Driven RIPER Workflow Guide

The RIPER workflow is the core component of the CursorRIPER Framework 2.0, providing a structured, PRD-driven approach to software development through five distinct operational modes. This guide explains how to use each mode effectively in the new PRD-centric paradigm.

## RIPER Workflow Overview

```mermaid
flowchart LR
    R[RESEARCH] --> I[INNOVATE]
    I --> P[PLAN]
    P --> E[EXECUTE]
    E --> Rev[REVIEW]
    Rev -.-> R
    
    style R fill:#e6f3ff,stroke:#0066cc
    style I fill:#e6ffe6,stroke:#006600
    style P fill:#fff0e6,stroke:#cc6600
    style E fill:#ffe6e6,stroke:#cc0000
    style Rev fill:#f0e6ff,stroke:#6600cc
```

## Mode 1: RESEARCH

### Purpose
Information gathering to inform PRD creation or refinement.

### When to Use
- When creating a new PRD and need to understand user needs
- When researching market requirements or competitive analysis
- When gathering technical constraints for PRD requirements
- When understanding existing systems for PRD context

### Commands
- `/research` or `ENTER RESEARCH MODE`

### Example Prompts
- "Research user authentication patterns for our PRD requirements."
- "Analyze competitor features for the task management Epic."
- "Investigate technical constraints for the real-time notification requirement."
- "Research user needs for the mobile app Epic."

### Best Practices
1. Focus research on informing PRD requirements
2. Gather information that helps define user needs and acceptance criteria
3. Document findings that will influence Epic definitions
4. Consider both functional and non-functional requirements
5. Research should contribute to PRD quality and completeness

### PRD Context
All research should contribute to understanding requirements, user needs, or technical constraints that will be documented in the PRD.

## Mode 2: INNOVATE

### Purpose
Brainstorming solutions for PRD requirements or technical challenges.

### When to Use
- After defining PRD requirements, explore implementation approaches
- When solving technical challenges for specific Epics
- When exploring creative solutions for PRD objectives
- When considering alternative approaches to meet acceptance criteria

### Commands
- `/innovate` or `ENTER INNOVATE MODE`

### Example Prompts
- "Brainstorm approaches for the user authentication Epic."
- "Explore solutions for the real-time notification requirements."
- "Consider different architectures for the mobile app Epic."
- "Innovate solutions for the performance requirements in the PRD."

### Best Practices
1. All innovations must serve PRD goals and requirements
2. Consider multiple approaches for each Epic
3. Evaluate solutions against PRD acceptance criteria
4. Explore trade-offs between different approaches
5. Ensure innovations are traceable to specific PRD requirements

### PRD Alignment
All innovations must be traceable to specific PRD requirements or Epic goals.

## Mode 3: PLAN

### Purpose
Project total designer - create/update PRD, architecture, and work plans.

### Strategic Planning Priority Order
1. **PRD Creation/Revision**: Collaborate to create/refine 00_prd.md (highest priority)
2. **Architecture Planning**: Create/update 01_architecture.md based on approved PRD
3. **Work Breakdown**: Create/update 02_work_plan_progress.md with Epic-to-Story decomposition
4. **Task Planning**: Generate Implementation Plans for specific Stories in 99_session_workbench.md

### When to Use
- When creating or updating the PRD
- When designing technical architecture based on PRD
- When breaking down Epics into implementable Stories
- When planning specific Story implementations

### Commands
- `/plan` or `ENTER PLAN MODE`

### Example Prompts
- "Let's create the PRD for our task management application."
- "Update the architecture based on our approved PRD."
- "Break down the user authentication Epic into Stories."
- "Plan the implementation for Story: User Login Form."

### Quality Gates
Use checklists after each major planning deliverable:
- `prd_review_checklist.md` after PRD work
- `architecture_review_checklist.md` after architecture work
- `story_dod_checklist.md` for story planning

### Planning Process
1. Identify planning level (PRD, Architecture, Work Plan, or Task)
2. Review existing documentation for context
3. Create or update relevant documentation
4. Run appropriate checklist for self-validation
5. Present results for approval

### Best Practices
1. Always start with PRD if it doesn't exist or needs updates
2. Ensure architecture serves PRD requirements
3. Break Epics into 3-8 implementable Stories
4. Define clear acceptance criteria for each Story
5. Maintain traceability from PRD to Stories

## Mode 4: EXECUTE

### Purpose
PRD implementation - execute approved Implementation Plans from session workbench.

### When to Use
- When implementing Stories as defined in the work plan
- When you have an approved Implementation Plan for a Story
- When executing specific tasks that trace back to PRD requirements

### Commands
- `/execute` or `ENTER EXECUTE MODE`

### Context Requirements
- Clear Story selected in 99_session_workbench.md
- Approved Implementation Plan exists for the Story
- Story requirements trace back to PRD Epics

### Example Prompts
- "Execute the implementation plan for Story: User Login Form."
- "Implement the database schema for the user management Story."
- "Execute the API endpoints for the task creation Epic."

### Best Practices
1. Only implement Stories defined in 02_work_plan_progress.md
2. Follow approved Implementation Plans exactly
3. Update Story status as you progress
4. Document implementation decisions in 03_project_bkm.md
5. If plan changes are needed, return to PLAN mode

### Progress Tracking
- Update Story status in 02_work_plan_progress.md
- Update session context in 99_session_workbench.md
- Document implementation decisions in 03_project_bkm.md

### PRD Traceability
All implementation must serve documented PRD requirements and be traceable to specific Epics and Stories.

## Mode 5: REVIEW

### Purpose
PRD requirements validator and quality assurance using standardized checklists.

### Review Levels
1. **Story Review**: Use story_dod_checklist.md to validate completed Stories
2. **Architecture Review**: Use architecture_review_checklist.md for technical design
3. **PRD Review**: Use prd_review_checklist.md for requirements quality

### When to Use
- After completing Story implementation
- When validating architecture against PRD requirements
- When reviewing PRD quality and completeness
- Before marking any work as complete

### Commands
- `/review` or `ENTER REVIEW MODE`

### Example Prompts
- "Review the completed user login Story using the DoD checklist."
- "Validate our architecture against the PRD using the architecture checklist."
- "Review our PRD quality using the PRD review checklist."

### Required Process
MUST execute appropriate checklist systematically:
- No Story can be marked complete without passing DoD checklist
- Architecture must pass review before implementation begins
- PRD must pass review before architecture planning

### Best Practices
1. Use the appropriate checklist for each review type
2. Verify Story completion against acceptance criteria from PRD
3. Document review findings in 03_project_bkm.md
4. Ensure all reviewed work traces back to documented requirements
5. Address any checklist failures before proceeding

## Mode Transitions

You can transition between modes at any time using the appropriate command. The typical PRD-driven workflow follows:

1. **RESEARCH** to gather information for PRD creation
2. **PLAN** to create comprehensive PRD and architecture
3. **INNOVATE** to explore solutions for PRD requirements
4. **PLAN** to break down Epics into Stories and create implementation plans
5. **EXECUTE** to implement approved Stories
6. **REVIEW** to validate implementation using checklists

The key difference in 2.0 is that PLAN mode is central to the workflow, serving as the strategic planning hub for all PRD-driven activities.

## Documentation Updates

As you progress through the RIPER workflow, the framework will automatically update project documentation:

- `00_prd.md` - Updated with research findings and requirement refinements
- `01_architecture.md` - Updated with technical design decisions
- `02_work_plan_progress.md` - Updated with Story progress and completion
- `03_project_bkm.md` - Updated with lessons learned and decisions
- `99_session_workbench.md` - Updated with current session context

## PRD-Driven Principles

The 2.0 workflow is built on these core principles:

1. **PRD as Single Source of Truth**: All work traces back to documented requirements
2. **Epic-to-Story Traceability**: Clear path from high-level goals to implementable tasks
3. **Quality Gates**: Standardized review processes at each level
4. **Documentation-Driven Development**: Comprehensive planning before implementation
5. **Continuous Learning**: BKM captures decisions and lessons for future reference

---

*CursorRIPER Framework 2.0: From Requirements to Reality, with Quality at Every Step*
