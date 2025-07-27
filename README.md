# Claude Code Agent Team

Agent documentation and planning repository for development epics and knowledge management with custom slash commands and specialized agent workflows.

## Custom Slash Commands

This repository supports various custom slash commands for enhanced development workflows:

- `/init` - Initialize and analyze codebase, create CLAUDE.md for future instances
- `/check-file <path>` - Perform comprehensive analysis of specific files
- `/compact` - Optimize code for reduced token usage while maintaining functionality

## Specialized Agents

The repository leverages multiple specialized agent types for different tasks:

### Core Development Agents
- **general-purpose** - Multi-step research and code searching
- **product-code-comprehension-expert** - Deep codebase analysis and architecture understanding
- **frontend-architect** - Component design and modern frontend best practices
- **backend-architect** - API design and server-side architecture with TDD

### Planning & Testing Agents
- **agile-product-owner** - Feature breakdown into epics, stories, and tasks
- **agile-test-strategist** - Risk-based testing strategies and test optimization

### Infrastructure & Optimization
- **aws-infrastructure-architect** - Cloud architecture design and optimization
- **database-design-specialist** - Schema design and performance optimization
- **prompt-optimization-expert** - LLM prompt engineering and optimization

## Agent Workflow

1. **Planning Phase** - Use agile-product-owner for feature decomposition
2. **Analysis Phase** - Employ product-code-comprehension-expert for codebase understanding
3. **Implementation Phase** - Leverage specialized architects (frontend/backend) for development
4. **Testing Phase** - Apply agile-test-strategist for comprehensive testing approaches
5. **Optimization Phase** - Utilize infrastructure and optimization specialists as needed

## Usage

This repository serves as a documentation hub for agent development planning and knowledge sharing, with emphasis on:

- Epic-based development planning
- Agent role specialization
- Custom command workflows
- Knowledge base management