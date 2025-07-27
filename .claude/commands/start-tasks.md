# Autonomous Multi-Agent Task Execution

**CORE PURPOSE**: Orchestrate intelligent parallel task execution with autonomous 7-agent coordination.

## Usage
```
/start-tasks [--mode=autonomous|guided] [--agents=all|selected]
```

## Prerequisites
- `/break-down` completed with task hierarchy and dependencies
- Optional `/design-session` for complex technical specifications
- TodoWrite integration with agent assignments

## Outputs
- Real-time execution dashboard with progress tracking
- Autonomous task progression with conflict resolution
- Performance metrics and bottleneck analysis
- **OUTPUT FILES**: 
  - `agent-docs/EPIC-{ID}-{epic-name}/execution/progress-tracking.md`
  - `agent-docs/EPIC-{ID}-{epic-name}/execution/execution-logs.md`

## Execution Intelligence

Auto-load `agent-docs/knowledge.md` and `agent-docs/try.md` for:
- Smart task selection with AI-driven priority optimization
- Real-time conflict resolution and resource balancing
- Dynamic bottleneck detection and mitigation
- Knowledge pattern matching and application

## Task Selection Algorithm

### Priority Matrix
1. Business Value × Urgency = Base Priority
2. Dependency unblocking = +50% weight
3. Agent expertise match = 0.8-1.2x multiplier
4. Parallel execution potential = +20% weight

### 7-Agent Execution Flow
```
FOR EACH AGENT:
  1. Extract specialized tasks from TodoWrite
  2. Apply knowledge base patterns
  3. Analyze dependencies dynamically
  4. Select optimal task with priority matrix
  5. Update status to in_progress
  6. Notify dependent agents automatically
```

## Agent Communication

### Communication Types
- **Blocking**: Immediate response required (timeout: 30s)
- **Async**: Batch processing (5min intervals)
- **Broadcast**: Critical updates to all agents

## Parallel Execution Management

### Execution Patterns
1. **Full Parallel**: Independent tasks across all 7 agents
2. **Pipeline**: Sequential with dependency optimization
3. **Phased**: Feature-based phases with synchronized handoffs
4. **Cross-functional**: Clustered collaboration

### Synchronization Points
- API specification finalized → Frontend implementation
- Database schema ready → Backend implementation  
- Infrastructure prepared → Deployment ready
- All components complete → Integration testing

## Conflict Resolution

### Conflict Types & Auto-Resolution
- **Resource Conflicts**: Merge by timestamp + auto-test
- **Design Conflicts**: Product-owner arbitration
- **Priority Conflicts**: Business value matrix application

### Bottleneck Detection
Monitor agent wait times (>10min), dependency chains (>5 levels), critical path delays (>150% planned), and resource usage (>80%).

## Progress Management

### Task Lifecycle Automation
```
Task Selection → In Progress → (Blocked) → Completed → Next Task
```

### Real-Time Dashboard
```
Agent Status    | Task Pipeline      | Performance
🟢 Backend API  | ⏳ Pending: 12     | Avg Duration: 23min
🟢 Frontend UI  | 🔄 Progress: 7     | Efficiency: 85%
🟡 Test Wait    | ✅ Complete: 23    | Auto-Resolution: 91%
🟢 AWS Setup    | 📊 Overall: 67%    | Collaboration: 89%
```

## Execution Phases

### Phase 1: Initialize (0-5min)
1. Auto-load knowledge base and try items
2. Get task list from TodoWrite
3. Build dependency graph and optimize initial distribution

### Phase 2: Parallel Execution (5min-completion)
```
WHILE tasks_remaining > 0:
  FOR EACH AGENT IN parallel:
    1. Scan available tasks
    2. Apply knowledge patterns
    3. Select optimal task
    4. Report progress and notify dependencies
```

### Phase 3: Integration & Validation (auto-trigger)
Auto-run integration tests, performance tests, security scans, and quality gates when all implementation tasks complete.

## Success Metrics

### Real-Time KPIs
- Task completion rate: >90%
- Average wait time: <5 minutes
- Parallel efficiency: >80%
- Auto-resolution rate: >85%

## Output Files

Creates execution tracking in `agent-docs/EPIC-{ID}-{epic-name}/execution/`:
- **progress-tracking.md**: Real-time progress dashboard
- **execution-logs.md**: Detailed execution logs and bottleneck analysis

## Workflow Integration

- **From**: `/break-down` task hierarchy, optional `/design-session`
- **To**: `/task-done` for completion notifications
- **Updates**: Continuous TodoWrite status updates, knowledge base usage tracking