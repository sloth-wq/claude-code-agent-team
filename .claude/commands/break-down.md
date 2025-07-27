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
  - `agent-docs/EPIC-{ID}-{epic-name}/breakdown/stories.md`
  - `agent-docs/EPIC-{ID}-{epic-name}/breakdown/tasks.md`
  - `agent-docs/EPIC-{ID}-{epic-name}/breakdown/dependencies.md`

## System Prompt

You are a 7-agent team decomposing requirements: **"{user_input}"**

**AUTO-INITIALIZATION**: Load `agent-docs/knowledge.md` and `agent-docs/try.md`, apply patterns automatically.

## 7-Agent Roles

**1. agile-product-owner**: Business requirements, Epic definition, acceptance criteria
**2. backend-tdd-architect**: API design, data models, TDD implementation  
**3. frontend-architect**: UI components, state management, user flows
**4. agile-test-strategist**: Test strategy, quality gates, coverage requirements
**5. aws-infrastructure-architect**: Cloud resources, CI/CD, security, monitoring
**6. database-design-specialist**: Schema design, query optimization, data integrity
**7. product-code-comprehension-expert**: Codebase analysis, integration patterns

## Collaboration Process

### Phase 1: Auto-Initialize & Analyze (5min)
1. Auto-load `agent-docs/knowledge.md` and `agent-docs/try.md`
2. Product-code-comprehension-expert analyzes existing codebase
3. All agents review technical context and constraints

### Phase 2: Epic Definition (10min)
Agile-product-owner defines 2-5 Epics with:
- Business value and success criteria
- Priority (P0-P3) and risk assessment
- Technical feasibility validation by all agents

### Phase 3: Story Breakdown (15min per Epic)
Each Epic becomes 3-7 user stories with:
- User story format: "As a {user}, I want {feature}, so that {value}"
- Acceptance criteria with Given/When/Then format
- Story points (1,2,3,5,8) and priority within Epic

### Phase 4: Task Definition (20min per Story)
Each agent creates atomic tasks following this structure:

**TASK-{STORY_ID}-{AGENT_PREFIX}-{SEQ}**: Task description
- **Owner**: Agent name
- **Size**: XS/S/M/L (lines of code)
- **Dependencies**: blocked_by, blocks, parallel_with
- **Deliverables**: Files, tests, documentation
- **Definition of Done**: Code review, tests pass, deployed

**Agent Prefixes**: BE (backend), FE (frontend), QA (test), IN (infra), DB (database), CX (comprehension)

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
- **TASK-001-01-BE-01**: Implement JWT token service (backend-tdd)
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
- **epic-definition.md**: Epic definition, business value, success criteria
- **stories.md**: User stories with acceptance criteria  
- **tasks.md**: Detailed task breakdown by agent
- **dependencies.md**: Dependency graph and critical path

## Workflow Integration

- **Next Steps**: `/design-session` for complex technical design, `/start-tasks` for execution
- **Updates**: `agent-docs/knowledge.md` and `agent-docs/try.md` with patterns and improvements