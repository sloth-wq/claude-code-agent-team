# Epic Retrospective Analysis

**Purpose**: Conduct comprehensive Epic retrospective with data-driven insights and improvement recommendations.

## Usage
```
/retrospective [epic-name]
```

## Prerequisites
- Epic tasks completed via `/task-done`
- Performance data from `/start-tasks` execution
- Quality metrics from validation phase

## Outputs
- Data-driven improvement recommendations
- Collaboration efficiency analysis
- Process optimization proposals
- **Files**: 
  - `agent-docs/EPIC-{ID}-{name}/analysis/retrospective-data.md`
  - `agent-docs/EPIC-{ID}-{name}/analysis/metrics.md`

## Agent Collaboration

### Automatic Knowledge Integration
- Load `agent-docs/knowledge.md` for pattern analysis
- Load `agent-docs/try.md` for improvement tracking
- Apply learned patterns to retrospective insights

### 7-Agent Analysis Framework
All agents contribute specialized retrospective insights:

- **agile-product-owner**: Business value realization, stakeholder satisfaction
- **backend-tdd-architect**: API quality, TDD effectiveness, technical metrics
- **frontend-architect**: UI/UX outcomes, component reusability, performance
- **agile-test-strategist**: Quality metrics, test effectiveness, risk mitigation
- **aws-infrastructure-architect**: Infrastructure efficiency, deployment success
- **database-design-specialist**: Data model effectiveness, query performance
- **product-code-comprehension-expert**: Code quality, technical debt, architecture

## Analysis Process

### Phase 1: Performance Metrics Collection (Auto)
```
Epic Completion Analysis:
- Task completion rates and timing
- Quality gate pass/fail rates
- Agent collaboration efficiency scores
- Bottleneck identification and resolution times
- Knowledge base usage statistics
- Try item implementation success rates
```

### Phase 2: Multi-Agent Insights Gathering
Each agent provides domain-specific retrospective analysis:
- What worked well in their specialty area
- Challenges encountered and solutions found
- Improvement opportunities identified
- Knowledge gained for future application

### Phase 3: Cross-Agent Pattern Recognition
Identify collaboration patterns and optimization opportunities:
- High-efficiency agent pairing patterns
- Successful dependency resolution strategies
- Effective knowledge sharing approaches
- Process bottlenecks requiring cross-functional solutions

### Phase 4: Data-Driven KPT Analysis

**Keep** (Quantified Success Factors):
- Effective practices with measured impact
- Successful collaboration patterns
- Knowledge applications that accelerated delivery
- Quality improvements achieved

**Problem** (Measured Issues):
- Bottlenecks with time impact analysis
- Quality issues and root causes
- Collaboration friction points
- Resource utilization inefficiencies

**Try** (Improvement Proposals):
- Specific, measurable improvement initiatives
- Process optimization opportunities
- Tool/technology enhancement proposals
- Knowledge gap filling strategies

## Output Generation

### Comprehensive Analysis Reports
Generate structured retrospective documentation covering:

1. **Epic Performance Summary**
   - Overall completion metrics vs targets
   - Quality achievements and gaps
   - Business value delivery assessment

2. **Agent Collaboration Analysis**
   - Individual agent contribution metrics
   - Cross-agent efficiency patterns
   - Communication and handoff effectiveness

3. **Process Optimization Recommendations**
   - Immediate improvements for next Epic
   - Medium-term process evolution proposals
   - Long-term strategic recommendations

4. **Knowledge Base Updates**
   - New learnings captured in `agent-docs/knowledge.md`
   - Try item progress updates in `agent-docs/try.md`
   - Usage statistics and effectiveness ratings

### Actionable Next Steps
Provide concrete, prioritized recommendations:
- Process adjustments for immediate implementation
- Tool/technique experiments to try
- Knowledge areas requiring development
- Collaboration pattern refinements

## Success Metrics

Track retrospective effectiveness:
- Implementation rate of Try items from previous retrospectives
- Process efficiency improvements measured
- Quality metric trends over time
- Team satisfaction and learning velocity

## Knowledge Integration

**Automatic Knowledge Usage Tracking**:
- Which knowledge patterns were most valuable
- Knowledge gaps identified during Epic execution
- New patterns discovered worth capturing
- Try item effectiveness and continuation decisions

**Knowledge Base Evolution**:
- Update usage statistics for knowledge entries
- Add new discoveries and learnings
- Retire outdated or ineffective knowledge
- Enhance successful patterns with more detail

The retrospective leverages the full 7-agent collaboration model to provide comprehensive, actionable insights for continuous improvement while maintaining the knowledge-driven development approach established in previous commands.