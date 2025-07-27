# Knowledge Sharing & Learning Capture

**CORE PURPOSE**: Systematically capture and share domain expertise gained during Epic development for continuous team learning.

## Usage
```
/knowledge-share [--domain=technical|business|process]
```

## Prerequisites
- Epic or Sprint completion with lessons learned
- Agent experiences from workflow execution
- Clear insights or discoveries worth sharing

## Outputs
- Structured knowledge entries and cross-domain learning recommendations
- **OUTPUT FILES**: 
  - `agent-docs/knowledge.md` (unified knowledge base updates)
  - `agent-docs/try.md` (new improvement proposals)

## Knowledge Capture Framework

**7-AGENT COLLABORATION**: All agents contribute knowledge leveraging roles from `/break-down`

### Knowledge Categories

**A. Business & Domain Knowledge**: Business rules, user patterns, market insights
**B. Technical Patterns**: Architecture decisions, code patterns, best practices  
**C. Integration Solutions**: System connectivity, API design, dependency management
**D. Performance & Security**: Optimization techniques, security implementations
**E. Agent Collaboration**: Cross-functional workflows, decision processes

## Knowledge Entry Template

```markdown
## Knowledge: {Title}

**Category**: {A-E}  
**Priority**: {High/Medium/Low}  
**Contributing Agent**: {Agent Role}  
**Date**: {YYYY-MM-DD}

### Context & Background
{Why this knowledge is important, discovery situation}

### Knowledge Content
{Specific findings, methods, patterns, solutions}

### Implementation Example
```{language}
{Code examples or configuration}
```

### Impact & Effects
- **Technical**: {System impact}
- **Business**: {Business value impact}  
- **Team**: {Process/efficiency impact}

### Tags
{Keywords for searchability}
```

## 7-Agent Learning Facilitation

### Cross-Agent Value Proposition
Define how knowledge applies to each agent's domain:
- **Backend/Frontend**: API design, component patterns, integration points
- **Test**: Quality strategies, validation approaches  
- **Infrastructure**: Deployment, security, monitoring considerations
- **Database**: Data modeling, performance optimization
- **Code Comprehension**: Architecture insights, technical debt management
- **Product Owner**: Business value realization, user impact

## Quality Validation

### Knowledge Quality Checklist
- [ ] Reproducible and includes concrete implementation examples
- [ ] Business value clearly articulated
- [ ] Applicable across agent domains
- [ ] Searchable with appropriate tags
- [ ] Cross-agent collaboration patterns defined

## Continuous Improvement

### Success Metrics
- Knowledge reuse rate: >60%
- Problem-solving effectiveness (time reduction)
- Usage frequency and knowledge gap reduction

## Output Files

Updates knowledge base directly:
- **`agent-docs/knowledge.md`**: Add new entries, usage statistics, effectiveness ratings  
- **`agent-docs/try.md`**: Add improvement proposals, update implementation progress

## Workflow Integration

- **From**: `/retrospective`, `/task-done`, entire workflow learnings
- **To**: Enhanced `/break-down` processes, continuous knowledge evolution
- **Structure**: Simple 2-file system for maximum efficiency