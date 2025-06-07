# {{Project Name}} Work Plan & Progress Tracking

## Overview

This document breaks down the Epics defined in the PRD (`template_00_prd.md`) into detailed, actionable stories. Each story represents a vertical slice of functionality that can be implemented by an AI agent in a single focused session.

**Key Principles:**
- Every story must deliver working, testable functionality
- Stories are sequentially ordered within each Epic
- Each story includes clear acceptance criteria
- Stories are sized for single AI agent execution (2-4 hours of work)

## Epic Progress Summary

| Epic | Status | Stories Complete | Total Stories | % Complete |
|------|--------|------------------|---------------|------------|
| Epic 1: {{Epic Title}} | {{Status}} | {{X}} | {{Y}} | {{Z%}} |
| Epic 2: {{Epic Title}} | {{Status}} | {{X}} | {{Y}} | {{Z%}} |
| Epic 3: {{Epic Title}} | {{Status}} | {{X}} | {{Y}} | {{Z%}} |

**Overall Project Status:** {{X}}/{{Y}} stories complete ({{Z%}})

## Epic 1: {{Epic Title}}

**Goal:** {{Epic goal from PRD}}
**Status:** {{Todo/In Progress/Complete}}
**Architecture Dependencies:** {{Reference relevant architecture components}}

### Story 1.1: {{Story Title}}

**Status:** {{Todo/In Progress/Complete/Blocked}}
**Assigned Session:** {{Session date or "Unassigned"}}
**Estimated Effort:** {{Small/Medium/Large}}

**Story Description:**
As a {{user type}},
I want {{functionality}},
so that {{benefit}}.

**Acceptance Criteria:**
- [ ] **AC1:** {{Specific, testable criterion}}
- [ ] **AC2:** {{Specific, testable criterion}}
- [ ] **AC3:** {{Specific, testable criterion}}

**Technical Notes:**
- {{Technical consideration 1}}
- {{Technical consideration 2}}

**Dependencies:**
- {{Dependency on previous story or external factor}}

**Definition of Done:**
- [ ] All acceptance criteria met
- [ ] Code follows architecture guidelines
- [ ] Unit tests written and passing
- [ ] Integration tests written and passing (if applicable)
- [ ] Documentation updated
- [ ] Story DoD checklist completed

**Implementation Notes:**
{{Add notes during implementation}}

**Session Log:**
{{Track work sessions and decisions}}

---

### Story 1.2: {{Story Title}}

**Status:** {{Todo/In Progress/Complete/Blocked}}
**Assigned Session:** {{Session date or "Unassigned"}}
**Estimated Effort:** {{Small/Medium/Large}}

**Story Description:**
As a {{user type}},
I want {{functionality}},
so that {{benefit}}.

**Acceptance Criteria:**
- [ ] **AC1:** {{Specific, testable criterion}}
- [ ] **AC2:** {{Specific, testable criterion}}
- [ ] **AC3:** {{Specific, testable criterion}}

**Technical Notes:**
- {{Technical consideration 1}}
- {{Technical consideration 2}}

**Dependencies:**
- Requires Story 1.1 to be complete

**Definition of Done:**
- [ ] All acceptance criteria met
- [ ] Code follows architecture guidelines
- [ ] Unit tests written and passing
- [ ] Integration tests written and passing (if applicable)
- [ ] Documentation updated
- [ ] Story DoD checklist completed

**Implementation Notes:**
{{Add notes during implementation}}

**Session Log:**
{{Track work sessions and decisions}}

---

## Epic 2: {{Epic Title}}

**Goal:** {{Epic goal from PRD}}
**Status:** {{Todo/In Progress/Complete}}
**Architecture Dependencies:** {{Reference relevant architecture components}}

### Story 2.1: {{Story Title}}

**Status:** {{Todo/In Progress/Complete/Blocked}}
**Assigned Session:** {{Session date or "Unassigned"}}
**Estimated Effort:** {{Small/Medium/Large}}

**Story Description:**
As a {{user type}},
I want {{functionality}},
so that {{benefit}}.

**Acceptance Criteria:**
- [ ] **AC1:** {{Specific, testable criterion}}
- [ ] **AC2:** {{Specific, testable criterion}}
- [ ] **AC3:** {{Specific, testable criterion}}

**Technical Notes:**
- {{Technical consideration 1}}
- {{Technical consideration 2}}

**Dependencies:**
- {{Dependency on Epic 1 completion or specific stories}}

**Definition of Done:**
- [ ] All acceptance criteria met
- [ ] Code follows architecture guidelines
- [ ] Unit tests written and passing
- [ ] Integration tests written and passing (if applicable)
- [ ] Documentation updated
- [ ] Story DoD checklist completed

**Implementation Notes:**
{{Add notes during implementation}}

**Session Log:**
{{Track work sessions and decisions}}

---

## Epic 3: {{Epic Title}}

**Goal:** {{Epic goal from PRD}}
**Status:** {{Todo/In Progress/Complete}}
**Architecture Dependencies:** {{Reference relevant architecture components}}

### Story 3.1: {{Story Title}}

**Status:** {{Todo/In Progress/Complete/Blocked}}
**Assigned Session:** {{Session date or "Unassigned"}}
**Estimated Effort:** {{Small/Medium/Large}}

**Story Description:**
As a {{user type}},
I want {{functionality}},
so that {{benefit}}.

**Acceptance Criteria:**
- [ ] **AC1:** {{Specific, testable criterion}}
- [ ] **AC2:** {{Specific, testable criterion}}
- [ ] **AC3:** {{Specific, testable criterion}}

**Technical Notes:**
- {{Technical consideration 1}}
- {{Technical consideration 2}}

**Dependencies:**
- {{Dependency on previous epics or stories}}

**Definition of Done:**
- [ ] All acceptance criteria met
- [ ] Code follows architecture guidelines
- [ ] Unit tests written and passing
- [ ] Integration tests written and passing (if applicable)
- [ ] Documentation updated
- [ ] Story DoD checklist completed

**Implementation Notes:**
{{Add notes during implementation}}

**Session Log:**
{{Track work sessions and decisions}}

---

## Story Templates

### New Story Template
```markdown
### Story X.Y: {{Story Title}}

**Status:** Todo
**Assigned Session:** Unassigned
**Estimated Effort:** {{Small/Medium/Large}}

**Story Description:**
As a {{user type}},
I want {{functionality}},
so that {{benefit}}.

**Acceptance Criteria:**
- [ ] **AC1:** {{Specific, testable criterion}}
- [ ] **AC2:** {{Specific, testable criterion}}
- [ ] **AC3:** {{Specific, testable criterion}}

**Technical Notes:**
- {{Technical consideration 1}}
- {{Technical consideration 2}}

**Dependencies:**
- {{Dependency information}}

**Definition of Done:**
- [ ] All acceptance criteria met
- [ ] Code follows architecture guidelines
- [ ] Unit tests written and passing
- [ ] Integration tests written and passing (if applicable)
- [ ] Documentation updated
- [ ] Story DoD checklist completed

**Implementation Notes:**
{{Add notes during implementation}}

**Session Log:**
{{Track work sessions and decisions}}
```

## Risk and Issue Tracking

### Current Risks
| Risk | Impact | Probability | Mitigation | Owner | Status |
|------|--------|-------------|------------|-------|--------|
| {{Risk description}} | {{High/Medium/Low}} | {{High/Medium/Low}} | {{Mitigation strategy}} | {{Owner}} | {{Status}} |

### Current Issues
| Issue | Impact | Blocking Stories | Resolution | Owner | Status |
|-------|--------|------------------|------------|-------|--------|
| {{Issue description}} | {{High/Medium/Low}} | {{Story IDs}} | {{Resolution plan}} | {{Owner}} | {{Status}} |

## Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | {{Date}} | {{Author}} | Initial work plan creation |

---

## Usage Instructions

### For Planning Sessions (Plan Mode)
1. Break down PRD epics into stories using the story template
2. Ensure stories are properly sequenced and sized
3. Update the Epic Progress Summary table
4. Review dependencies and identify any risks

### For Implementation Sessions (Execute Mode)
1. Select the next story in sequence
2. Update story status to "In Progress"
3. Follow the implementation plan
4. Update "Implementation Notes" and "Session Log"
5. Complete the Story DoD checklist before marking as complete

### For Review Sessions (Review Mode)
1. Verify all acceptance criteria are met
2. Run through the Story DoD checklist
3. Update story status to "Complete"
4. Update the Epic Progress Summary
5. Identify any lessons learned for the project BKM

---

*This work plan serves as the tactical execution layer of the PRD. All stories must trace back to PRD requirements and epics.* 