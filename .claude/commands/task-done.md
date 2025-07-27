# Task Completion with Intelligent Handoffs

**CORE PURPOSE**: Execute comprehensive task validation, automatic dependency resolution, and seamless workflow transitions.

## Usage
```
/task-done "Completed task name" [--validation-level=strict|standard]
```

## Prerequisites
- Task in `in_progress` status in TodoWrite
- Clear completion deliverables defined

## Outputs
- Quality validation and dependency unblocking
- Next task recommendations and performance analytics
- **OUTPUT FILES**: 
  - `agent-docs/EPIC-{ID}-{epic-name}/validation/quality-reports.md`
  - `agent-docs/EPIC-{ID}-{epic-name}/validation/completion-status.md`

## Quality Validation

### Technical Quality Gates
- Code quality: ESLint/TSLint compliance, test coverage ≥80%
- Security: Vulnerability scan clearance, security standards
- Performance: Benchmark achievement, optimization validation
- Business: All acceptance criteria satisfied, design system compliance

### 7-Agent Cross-Validation
All agents validate task completion from their specialized perspective:
- **backend-architect**: API contracts, database integration, TDD compliance
- **frontend-architect**: Component standards, state management, accessibility
- **agile-test-strategist**: Coverage goals, quality gates, regression analysis
- **aws-infrastructure-architect**: Deployment readiness, security, monitoring
- **database-design-specialist**: Data integrity, performance optimization
- **product-code-comprehension-expert**: Architecture quality, technical debt
- **agile-product-owner**: Business value realization, acceptance criteria

## Dependency Resolution

### Automatic Unblocking Analysis
When a task completes, automatically analyze:
- **Direct dependencies**: Tasks immediately unblocked
- **Indirect impacts**: Tasks affected downstream  
- **Parallel opportunities**: Tasks that can now run concurrently

Example: "User Auth API" completion unblocks:
- Login UI implementation (frontend)
- Auth middleware tests (agile-test)  
- JWT deployment setup (aws-infrastructure)

### Agent Notification System
Each agent automatically notifies relevant agents when completing tasks:
- **backend-architect** → frontend-architect (API contracts), database-design-specialist (schema), aws-infrastructure-architect (deploy needs)
- **frontend-architect** → backend-architect (data requirements), agile-test-strategist (UI scenarios), agile-product-owner (UX feedback)
- **agile-test-strategist** → All agents (quality results), agile-product-owner (release readiness)
- **aws-infrastructure-architect** → All agents (deployment constraints), agile-product-owner (cost impacts)  
- **database-design-specialist** → backend/frontend (schema changes), aws-infrastructure (resource needs)
- **product-code-comprehension-expert** → All agents (architecture guidance), agile-product-owner (feasibility)
- **agile-product-owner** → All agents (requirements clarification, priority adjustments)

## Next Task Selection & Handoffs

### AI-Driven Task Selection
Intelligent selection algorithm considering:
- Dependency unblocking (40% weight)
- Context preservation (25% weight)  
- Business value (20% weight)
- Risk mitigation (10% weight)
- Team capacity (5% weight)

### Seamless Handoffs
1. **Completing Agent**: Generate deliverable summary, document implementation details
2. **Next Agent**: Auto-receive context, verify dependencies, set up work environment  
3. **All Agents**: Share progress, update blockers, identify collaboration opportunities

## Performance Analytics

### Real-Time Progress Dashboard
```
Project Status: 67% complete (34/51 tasks)
Agent Collaboration: 89% efficiency

Agent Status:
🟢 backend-architect: In Progress (8/12 complete)
🟡 frontend-architect: Waiting (5/9 complete, 2 blocked)  
🟢 agile-test-strategist: Active (6/8 complete)
🟢 aws-infrastructure-architect: Deploying (4/6 complete)
✅ database-design-specialist: Complete (5/5)
🟢 product-code-comprehension-expert: Active (3/5 complete)
🟡 agile-product-owner: Reviewing (3/6 complete)
```

### Task Completion Report
```yaml
✅ Task: "User Authentication API Implementation"

Technical Deliverables:
  - Code: 247 lines (src/api/auth/*)
  - APIs: 5 new endpoints
  - Tests: 45 added (92% coverage)
  - Docs: OpenAPI specification updated

Quality Verification:
  ✅ Security: JWT implementation, OWASP compliant
  ✅ Performance: Response time <100ms
  ✅ Reliability: Error handling complete

Impact Analysis:
  🔓 Immediately Unblocks:
    - Frontend auth state management
    - Auth middleware integration tests  
    - Production JWT deployment setup
```

## Output Files

Creates validation documentation in `agent-docs/EPIC-{ID}-{epic-name}/validation/`:
- **quality-reports.md**: Quality verification results, test coverage, code quality
- **completion-status.md**: Task completion status, dependency resolution, handoffs

## Workflow Integration

- **From**: `/start-tasks` execution tracking
- **To**: `/retrospective` for performance analysis, `/knowledge-share` for learning capture
- **Updates**: TodoWrite status transitions, knowledge base usage tracking