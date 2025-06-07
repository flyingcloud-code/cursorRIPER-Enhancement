# {{Project Name}} Architecture Document

## Introduction

This document outlines the technical architecture for {{Project Name}}, serving as the implementation blueprint for the requirements defined in the PRD (`template_00_prd.md`). All technical decisions documented here must directly support the functional and non-functional requirements specified in the PRD.

## Technical Summary

{{Provide a brief overview of the system's architecture, key components, technology choices, and architectural patterns. Reference the goals and requirements from the PRD.}}

## High-Level Architecture

### Architectural Style
{{Based on PRD Technical Assumptions: Monolith, Microservices, Serverless, Event-Driven, etc.}}

### Repository Structure
{{Based on PRD Technical Assumptions: Monorepo, Polyrepo, etc.}}

### System Context Diagram

```mermaid
{{Insert high-level system context diagram showing external systems, users, and main components}}
```

## Technology Stack

### Definitive Technology Selections

**Backend:**
- Language: {{Language from PRD}}
- Framework: {{Framework from PRD}}
- Runtime: {{Runtime version}}

**Frontend:** {{If applicable}}
- Framework: {{Framework from PRD}}
- Build Tool: {{Build tool}}
- State Management: {{State management solution}}

**Database:**
- Primary Database: {{Database from PRD}}
- Connection Library: {{ORM/Database client}}

**Infrastructure:**
- Deployment Platform: {{Platform from PRD}}
- CI/CD: {{CI/CD platform}}
- Monitoring: {{Monitoring tools}}

### Rationale for Technology Choices

{{Explain why these technologies were chosen based on PRD requirements and constraints}}

## Component Architecture

### Core Components

{{List the major logical components and their responsibilities}}

- **{{Component 1}}:** {{Responsibility and role}}
- **{{Component 2}}:** {{Responsibility and role}}
- **{{Component 3}}:** {{Responsibility and role}}

### Component Interaction Diagram

```mermaid
{{Insert component interaction diagram}}
```

## Project Structure

```
{{project-name}}/
├── .github/                    # CI/CD workflows
│   └── workflows/
│       └── ci.yml
├── docs/                       # Project documentation
│   ├── 00_prd.md
│   ├── 01_architecture.md
│   └── 02_work_plan_progress.md
├── src/                        # Application source code
│   ├── {{main-module}}/        # Core application logic
│   ├── {{module-2}}/           # Secondary modules
│   └── {{shared}}/             # Shared utilities and types
├── tests/                      # Test files
│   ├── unit/
│   ├── integration/
│   └── e2e/
├── config/                     # Configuration files
├── scripts/                    # Build and deployment scripts
├── {{package-manager-file}}    # Dependencies (package.json, requirements.txt, etc.)
├── {{config-file}}             # Language-specific config
├── .env.example                # Environment variables template
├── Dockerfile                  # Container configuration
└── README.md                   # Project setup instructions
```

### Key Directory Descriptions

- **src/{{main-module}}/**: {{Description of main application code}}
- **src/{{shared}}/**: {{Description of shared utilities}}
- **tests/**: {{Description of testing strategy and organization}}
- **config/**: {{Description of configuration management}}

## Data Architecture

### Data Models

{{Reference core entities from PRD and define their technical implementation}}

#### {{Entity 1}}
```typescript
// Example interface
interface {{Entity1}} {
  id: string;
  {{property1}}: {{type}};
  {{property2}}: {{type}};
  createdAt: Date;
  updatedAt: Date;
}
```

#### {{Entity 2}}
```typescript
interface {{Entity2}} {
  id: string;
  {{property1}}: {{type}};
  {{property2}}: {{type}};
}
```

### Database Schema

{{If using a relational database}}

#### {{Table 1}}
```sql
CREATE TABLE {{table_name}} (
  id UUID PRIMARY KEY DEFAULT gen_random_uuid(),
  {{column1}} {{type}} NOT NULL,
  {{column2}} {{type}},
  created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
  updated_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);
```

## API Design

### API Architecture

{{Describe the API architecture: REST, GraphQL, gRPC, etc.}}

### Endpoint Structure

#### {{API Group 1}}
- `GET /api/v1/{{resource}}` - {{Description}}
- `POST /api/v1/{{resource}}` - {{Description}}
- `PUT /api/v1/{{resource}}/:id` - {{Description}}
- `DELETE /api/v1/{{resource}}/:id` - {{Description}}

#### {{API Group 2}}
- `GET /api/v1/{{resource2}}` - {{Description}}
- `POST /api/v1/{{resource2}}` - {{Description}}

### Request/Response Schemas

{{Define key API schemas}}

#### {{Request Schema}}
```json
{
  "{{field1}}": "{{type}}",
  "{{field2}}": "{{type}}"
}
```

#### {{Response Schema}}
```json
{
  "id": "string",
  "{{field1}}": "{{type}}",
  "{{field2}}": "{{type}}",
  "createdAt": "ISO 8601 timestamp"
}
```

## Security Architecture

### Authentication Strategy
{{Based on PRD security requirements}}

### Authorization Model
{{Define roles, permissions, and access control}}

### Security Measures
- {{Security measure 1}}
- {{Security measure 2}}
- {{Security measure 3}}

## Performance & Scalability

### Performance Requirements
{{Reference NFRs from PRD}}

### Scalability Strategy
{{How the system will handle growth}}

### Monitoring & Observability
- **Logging:** {{Logging strategy}}
- **Metrics:** {{Metrics collection}}
- **Tracing:** {{Distributed tracing if applicable}}

## Development Guidelines

### Code Standards
- {{Coding standard 1}}
- {{Coding standard 2}}
- {{Linting and formatting tools}}

### Testing Strategy
{{Based on PRD testing requirements}}

- **Unit Tests:** {{Coverage and tools}}
- **Integration Tests:** {{Scope and tools}}
- **E2E Tests:** {{Scope and tools}}

### Development Workflow
1. {{Step 1}}
2. {{Step 2}}
3. {{Step 3}}

## Deployment Architecture

### Environment Strategy
- **Development:** {{Configuration}}
- **Staging:** {{Configuration}}
- **Production:** {{Configuration}}

### CI/CD Pipeline
{{Describe the build, test, and deployment pipeline}}

### Infrastructure as Code
{{If applicable, describe IaC approach}}

## Risk Mitigation

### Technical Risks
{{Based on risks identified in PRD}}

- **Risk:** {{Technical risk}}
  - **Mitigation:** {{Technical mitigation strategy}}

### Performance Risks
- **Risk:** {{Performance risk}}
  - **Mitigation:** {{Performance mitigation strategy}}

## Integration Points

### External Services
{{List and describe external API integrations}}

#### {{External Service 1}}
- **Purpose:** {{Why we integrate with this service}}
- **Integration Pattern:** {{REST, SDK, etc.}}
- **Error Handling:** {{How we handle failures}}

### Third-Party Libraries
{{List major dependencies and their purposes}}

## Change Log

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | {{Date}} | {{Author}} | Initial architecture document |

---

## Next Steps

After completing this architecture document:
1. Run the Architecture Review Checklist (`checklists/template_architecture_review_checklist.md`)
2. Begin detailed story planning in the Work Plan (`template_02_work_plan_progress.md`)
3. Set up the initial project structure and development environment

---

*This architecture document must be kept in sync with the PRD. Any changes to requirements should trigger a review of this document.* 