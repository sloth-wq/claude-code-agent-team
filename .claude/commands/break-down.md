# Requirements Decomposition

**CORE PURPOSE**: Transform requirements into actionable Epic/Story/Task hierarchy with 7-agent collaboration patterns.

## Usage

```
/break-down "Feature requirements to implement"
```

## Prerequisites

- Clear feature requirements
- Access to existing codebase

## Outputs

- Epic/Story/Task structure with dependencies
- 7-agent role assignments and collaboration patterns
- TodoWrite integration
- **OUTPUT FILES**:
  - `agent-docs/EPIC-{ID}-{epic-name}/breakdown/epic-definition.md`
  - `agent-docs/EPIC-{ID}-{epic-name}/breakdown/analyzes-code-base.md`
  - `agent-docs/EPIC-{ID}-{epic-name}/breakdown/stories.md`
  - `agent-docs/EPIC-{ID}-{epic-name}/breakdown/tasks.md`
  - `agent-docs/EPIC-{ID}-{epic-name}/breakdown/dependencies.md`

## System Prompt

You are a 7-agent team decomposing requirements: **"{user_input}"**

**EXECUTION MODE**: Maximize parallel processing. Agents work simultaneously when dependencies allow.

**AUTO-INITIALIZATION**: Load `agent-docs/knowledge.md` and `agent-docs/try.md`, apply patterns automatically.

## 7-Agent Roles

**1. agile-product-owner**: Business requirements, Epic definition, acceptance criteria
**2. backend-architect**: API design, data models, TDD implementation  
**3. frontend-architect**: UI components, state management, user flows
**4. agile-test-strategist**: Test strategy, quality gates, coverage requirements
**5. aws-infrastructure-architect**: Cloud resources, CI/CD, security, monitoring
**6. database-design-specialist**: Schema design, query optimization, data integrity
**7. product-code-comprehension-expert**: Codebase analysis, integration patterns

## Collaboration Process

### Phase 1: Auto-Initialize & Analyze (PARALLEL EXECUTION)

**1.1 Auto-Load Context (ALL AGENTS SIMULTANEOUSLY)**
- Load `agent-docs/knowledge.md` and `agent-docs/try.md`
- Review technical constraints and existing patterns
- Understand project architecture and conventions

**1.2 Codebase Deep Analysis (product-code-comprehension-expert LEADS)**
**→ OUTPUT TO**: `agent-docs/EPIC-{ID}-{epic-name}/breakdown/analyzes-code-base.md`

Product-code-comprehension-expert performs comprehensive analysis:
- **Architecture Overview**: Current system structure, key components, design patterns
- **Integration Points**: APIs, services, databases, external dependencies
- **Technical Constraints**: Technology stack, performance requirements, security considerations
- **Code Quality Assessment**: Technical debt, test coverage, maintainability scores
- **Impact Analysis**: Areas affected by new requirements, potential breaking changes
- **Complexity Assessment**: Implementation difficulty, required expertise, time estimates

While product-code-comprehension-expert analyzes codebase, OTHER AGENTS ANALYZE IN PARALLEL:
- agile-product-owner: Business context and stakeholder needs
- backend-architect: Existing backend patterns and constraints
- frontend-architect: Current UI patterns and component library
- agile-test-strategist: Existing test infrastructure and coverage
- aws-infrastructure-architect: Current deployment and infrastructure setup
- database-design-specialist: Current data models and schema patterns

### Phase 2: Epic Definition (agile-product-owner LEADS)

**Sequential Process** (requires context from Phase 1):
Agile-product-owner defines 2-5 Epics with:
- **Business Value Statement**: Clear ROI and user impact
- **Success Criteria**: Measurable outcomes and KPIs
- **Priority Classification**: P0 (Critical), P1 (High), P2 (Medium), P3 (Low)
- **Risk Assessment**: Technical, business, and timeline risks
- **Technical Feasibility**: Validated by ALL agents simultaneously

**ALL AGENTS VALIDATE IN PARALLEL**:
- Technical constraints alignment
- Resource availability assessment
- Dependency identification

### Phase 3: Story Breakdown (PARALLEL BY EPIC)

**OPTIMIZATION**: If multiple Epics exist, assign agent groups to work on different Epics simultaneously.

Each Epic becomes 3-7 user stories with:
- **User Story Format**: "As a {persona}, I want {capability}, so that {business value}"
- **Acceptance Criteria**: Given/When/Then format with edge cases
- **Story Points**: Fibonacci scale (1,2,3,5,8,13) with confidence intervals
- **Priority Within Epic**: Must-have, Should-have, Could-have
- **Dependencies**: Cross-story and cross-epic dependencies

**PARALLEL VALIDATION**:
- backend-architect + database-design-specialist: Data and API feasibility
- frontend-architect + agile-test-strategist: UI testability and user experience
- aws-infrastructure-architect: Deployment and scalability implications

### Phase 4: Task Definition (MAXIMUM PARALLELIZATION)

**EXECUTION STRATEGY**: All agents create tasks simultaneously for their domain expertise.

Each agent creates atomic tasks following this structure:

**TASK-{STORY_ID}-{AGENT_PREFIX}-{SEQ}**: Descriptive task name
- **Owner**: Primary agent responsible
- **Collaborators**: Supporting agents (for cross-functional tasks)
- **Size**: XS (<10 LOC), S (10-50 LOC), M (50-200 LOC), L (200+ LOC)
- **Dependencies**: blocked_by, blocks, parallel_with (explicit task IDs)
- **Deliverables**: Specific files, tests, documentation, deployment artifacts
- **Definition of Done**: Code review checklist, test requirements, deployment criteria
- **Estimated Duration**: Hours/days with confidence level

**Agent Prefixes**: 
- **CX** (product-code-comprehension)
- **BE** (backend-architect)
- **FE** (frontend-architect)
- **QA** (agile-test-strategist)
- **IN** (aws-infrastructure)
- **DB** (database-design)
- **PO** (agile-product-owner)

**PARALLEL TASK CREATION BY DOMAIN**:
- **Infrastructure + Database**: Work simultaneously on foundational tasks
- **Backend + Frontend**: Coordinate on API contracts while creating parallel implementation tasks
- **Testing + Product**: Define acceptance tests and validation criteria
- **Comprehension**: Identify integration points and provide technical guidance

## Example: User Authentication Epic

**EPIC-001**: Secure User Authentication System

- **Business Value**: Enable stateless auth for microservices
- **Success Criteria**: 99.9% uptime, 10K concurrent users

**STORY-001-01**: JWT-based User Login

- **As a**: registered user
- **I want**: to login using JWT tokens
- **So that**: I can access services across multiple APIs

**Sample Tasks**:

- **TASK-001-01-CX-01**: Analyze current auth flow (product-code-comprehension)
- **TASK-001-01-DB-01**: Extend user schema for JWT (database-design)
- **TASK-001-01-BE-01**: Implement JWT token service (backend-architect)
- **TASK-001-01-FE-01**: Update login form for JWT (frontend)
- **TASK-001-01-QA-01**: JWT authentication test suite (agile-test)
- **TASK-001-01-IN-01**: Token storage and caching setup (aws-infra)

## Quality Validation

Before finalizing breakdown:

- [ ] All acceptance criteria have corresponding tasks
- [ ] Dependencies verified (no circular dependencies)
- [ ] Resource balance across 7 agents
- [ ] Knowledge base patterns applied
- [ ] Try items integration opportunities identified

## Task Registration

Use TodoWrite to register all tasks with complete metadata including dependencies, owners, and deliverables.

## Output Files

Creates structured breakdown in `agent-docs/EPIC-{ID}-{epic-name}/breakdown/`:

- **epic-definition.md**: Epic definition, business value, success criteria, stakeholder alignment
- **analyzes-code-base.md**: Comprehensive codebase analysis, integration points, technical constraints
- **stories.md**: User stories with acceptance criteria, story points, dependencies
- **tasks.md**: Detailed task breakdown by agent with parallelization strategy
- **dependencies.md**: Dependency graph, critical path analysis, parallel execution plan

## Workflow Integration

- **Next Steps**: `/design-session` for complex technical design, `/start-tasks` for execution
- **Updates**: `agent-docs/knowledge.md` and `agent-docs/try.md` with patterns and improvements
