![CursorRIPER](../res/github-header.png)
# CursorRIPER Framework 2.0 - Setup Guide

This guide will help you set up the CursorRIPER Framework 2.0 for your project with the new PRD-driven approach.

## Prerequisites

- [Cursor IDE](https://cursor.sh/) installed
- Git (optional but recommended)
- Basic understanding of your project's requirements

## Installation

1. **Copy the framework files to your project and rename the files to *.mdc**

   Create a `.cursor` directory in your project root and copy the necessary files:

   ```bash
      mkdir -p .cursor/rules
      cp -r /path/to/CursorRIPER/src/.cursor/* .cursor/
      cd .cursor/rules/
      rename 's/\.md$/.mdc/' *.md
   ```

2. **Verify the installation**

   Your project should now have the following structure:

   ```
   your-project/
   └── .cursor/
       ├── rules/
       │   ├── core.mdc
       │   ├── state.mdc
       │   ├── start-phase.mdc
       │   ├── riper-workflow.mdc
       │   └── customization.mdc
       └── cursorignore
   ```

## Starting a New Project

1. **Initialize the framework**

   Open your project in Cursor IDE and use the chat feature to initialize the framework:

   ```
   /start
   ```

   or

   ```
   BEGIN START PHASE
   ```

2. **Follow the PRD-driven START phase**

   The framework will guide you through the START phase:

   1. **PRD Foundation Creation** - Create comprehensive Product Requirements Document
   2. **Technical Architecture Planning** - Design system architecture based on PRD
   3. **Work Plan and Progress Setup** - Break down Epics into implementable Stories
   4. **Project Knowledge Base Initialization** - Set up Best Known Methods documentation
   5. **Session Workbench Setup** - Create active development workspace
   6. **Quality Gates and Checklists Setup** - Establish review standards

3. **Complete the project documentation setup**

   Ensure all required project documentation files are created and populated:
   
   - `dev-docs/00_prd.md` - Product Requirements Document (single source of truth)
   - `dev-docs/01_architecture.md` - Technical architecture and design decisions
   - `dev-docs/02_work_plan_progress.md` - Epic breakdown and progress tracking
   - `dev-docs/03_project_bkm.md` - Best Known Methods and lessons learned
   - `dev-docs/99_session_workbench.md` - Current session workspace
   - `dev-docs/checklists/` - Quality review checklists

## Using the PRD-Driven RIPER Workflow

Once you've completed the START phase, you'll automatically transition to the RIPER workflow. Use the following commands to switch between modes:

- `/research` or `ENTER RESEARCH MODE` - Gather information to inform PRD creation or refinement
- `/innovate` or `ENTER INNOVATE MODE` - Brainstorm solutions for PRD requirements
- `/plan` or `ENTER PLAN MODE` - Create/update PRD, architecture, and work plans
- `/execute` or `ENTER EXECUTE MODE` - Implement Stories following approved plans
- `/review` or `ENTER REVIEW MODE` - Validate work using standardized checklists

## Key Features of 2.0

### 🎯 PRD-Driven Development
- **Single Source of Truth**: Every project starts with a comprehensive PRD
- **Requirements Traceability**: All work traces back to documented requirements
- **Epic-to-Story Breakdown**: Structured decomposition from goals to tasks

### 📋 Quality Gates
- **PRD Review Checklist**: Ensures requirements quality before architecture
- **Architecture Review Checklist**: Validates technical design against requirements
- **Story Definition of Done**: Guarantees implementation quality

### 📚 Comprehensive Documentation
- **Template-Driven**: All documents follow standardized templates
- **Progressive Detail**: From PRD to architecture to implementation
- **Knowledge Accumulation**: BKM captures project experience

## Customization

You can customize the framework behavior by editing `.cursor/rules/customization.mdc`. Some key settings include:

- Response verbosity
- Code style preferences
- Documentation update frequency
- Custom command aliases

See the [Customization Guide](customization-guide.md) for more details.

## Troubleshooting

If you encounter issues with the framework:

1. Verify all required files exist in `.cursor/rules/`
2. Check for state inconsistencies
3. Ensure project documentation files exist and are properly formatted
4. Try restarting Cursor IDE

For more help, refer to the [Troubleshooting Guide](troubleshooting-guide.md).

## Migration from 1.x

If you have an existing CursorRIPER 1.x project:

1. Back up your existing memory-bank files
2. Follow the installation steps above
3. Use the migration guide to convert memory-bank content to the new project documentation structure
4. Run quality checklists to ensure completeness

---

*CursorRIPER Framework 2.0: From Requirements to Reality, with Quality at Every Step*
