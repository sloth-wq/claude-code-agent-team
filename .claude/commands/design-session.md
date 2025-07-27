# Visual Design Session

**CORE PURPOSE**: Create comprehensive visual designs and technical specifications for complex Epic/Stories.

## Usage
```
/design-session "Epic or Story requiring design"
```

## Prerequisites
- `/break-down` completed with Epic/Story/Task structure
- Complex technical requirements identified

## Outputs
- Visual architecture diagrams, component designs, data flows
- Implementation blueprints and technical decisions
- **OUTPUT FILES**: 
  - `agent-docs/EPIC-{ID}-{epic-name}/design/architecture-diagrams.md`
  - `agent-docs/EPIC-{ID}-{epic-name}/design/component-designs.md`
  - `agent-docs/EPIC-{ID}-{epic-name}/design/data-flows.md`

## Design Protocol

**7-AGENT COLLABORATION**: Auto-load `agent-docs/knowledge.md` and `agent-docs/try.md` for pattern application.

### Phase 1: Context & Analysis (5min)
1. Product-code-comprehension-expert analyzes existing architecture and constraints
2. Agile-product-owner clarifies business requirements and design constraints
3. All agents establish common understanding of design scope

### Phase 2: Parallel Design Creation (15min)
All 7 agents create specialized designs:

- **Backend-tdd-architect**: API specifications, data flows, service contracts
- **Frontend-architect**: Component hierarchy, user flows, state management
- **Database-design-specialist**: ER diagrams, schema design, optimization
- **AWS-infrastructure-architect**: Cloud architecture, CI/CD, security
- **Agile-test-strategist**: Test strategy, coverage plans, quality gates

### Phase 3: Integration Review (10min)
Cross-validation across all agents for design consistency and integration points.

## Design Deliverables by Domain

- **System Architecture**: Component interaction & deployment topology
- **API Contracts**: Endpoint specifications & data schemas  
- **UI/UX Flows**: Component hierarchies & user journeys
- **Data Models**: Entity relationships & query patterns
- **Test Strategies**: Validation flows & coverage maps
- **Infrastructure**: Security, monitoring, CI/CD pipelines

## Design Templates

### System Architecture Diagram
```
[Client Layer] -> [API Gateway] -> [Services] -> [Data Layer]
```

### Data Flow Diagram  
```
[Request] -> [Service] -> [Database] -> [Response]
```

### Component Hierarchy
```
App -> Layout -> Components -> UI Elements
```

### Database Schema
```
Tables with relationships, indexes, constraints
```

## Quality Validation

- [ ] Knowledge base patterns applied
- [ ] Visual clarity with proper titles and directions
- [ ] Technical constraints considered
- [ ] Agent designs are consistent and integrated
- [ ] Implementation feasibility confirmed

## Output Files

Creates design documentation in `agent-docs/EPIC-{ID}-{epic-name}/design/`:
- **architecture-diagrams.md**: System architecture and infrastructure design
- **component-designs.md**: UI/UX components and functional design
- **data-flows.md**: Data flows and API specifications

## Workflow Integration

- **From**: `/break-down` Epic/Story/Task structure
- **To**: `/start-tasks` for implementation, `/task-done` for validation
- **Updates**: `agent-docs/knowledge.md` and `agent-docs/try.md`