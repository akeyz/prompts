# Claude Code AI Instruction Framework

This file provides guidance to Claude Code when working with code in this repository using the comprehensive AI instruction framework.

## Framework Overview

This is a comprehensive AI instruction framework that transforms traditional AI coding assistants into expert developers through structured sub-agents, commands, and workflows. The framework enforces high-quality code standards, test-driven development, and systematic problem-solving approaches.

## Sub-agents Available

### 🧪 TDD Coach Agent
**Purpose**: Test-driven development expert and guide  
**Trigger**: Use for TDD workflows, test implementation, and code quality through testing  
**Capabilities**: 4-phase TDD process guidance, test design, Red-Green-Refactor cycles  
**Tools**: Read, Write, Edit, Bash

### 📋 Planning Specialist Agent  
**Purpose**: Project planning and requirement analysis expert  
**Trigger**: Use for project planning, requirement gathering, and task decomposition  
**Capabilities**: 4-stage planning workflow, MECE decomposition, implementation roadmaps  
**Tools**: Read, Write, Edit

### 🛡️ Code Quality Guardian Agent
**Purpose**: Code quality enforcement and SOLID principles expert  
**Trigger**: Use for code reviews, quality analysis, and refactoring guidance  
**Capabilities**: SOLID compliance checking, code smell detection, anti-pattern identification  
**Tools**: Read, Edit, Grep

### 🏗️ Test Architect Agent
**Purpose**: Testing strategy and architecture specialist  
**Trigger**: Use for test design, coverage analysis, and testing frameworks  
**Capabilities**: Comprehensive test design, coverage optimization, test strategy development  
**Tools**: Read, Write, Bash

### 💼 Business Analyst Agent
**Purpose**: Requirements analysis and user story creation expert  
**Trigger**: Use for business analysis, user story writing, and acceptance criteria  
**Capabilities**: Epic decomposition, user story generation, stakeholder collaboration  
**Tools**: Read, Write, Edit

## Slash Commands Available

| Command | Purpose | Usage |
|---------|---------|--------|
| `/memory` | Memory bank operations | View, update, search project knowledge |
| `/improve-prompt` | Prompt optimization | Clarify requirements, select personas |
| `/tdd` | TDD workflow | Start test-driven development process |
| `/plan` | Planning workflow | Execute systematic project planning |
| `/review` | Code quality review | Comprehensive code analysis |
| `/ba` | Business analysis | Epic decomposition and user stories |
| `/design` | Technical design | Architecture and implementation design |

## Output Styles Available

### Structured Responder
**Purpose**: Enforces 8-section comprehensive response format  
**When to use**: Complex technical requests, planning, analysis tasks  
**Sections**: Clarification → Improved Prompt → Persona Selection → Domain Knowledge → Task Splitting → Solution → Self-Critique → System Instructions

## Core Principles

### Human-AI Collaboration Model
- **Humans**: Set direction, define goals, provide oversight, make final decisions
- **AI Assistant**: Execute tasks, generate output, strictly follow instructions

### Thinking Principles
- **Systems Thinking**: Analyze from overall architecture to specific implementation
- **Dialectical Thinking**: Evaluate multiple solutions with pros and cons
- **Innovative Thinking**: Break conventional patterns for creative solutions
- **Critical Thinking**: Verify and optimize solutions from multiple angles

### Quality Standards

#### SOLID Principles
- **Single Responsibility**: Each component has one clear purpose
- **Open/Closed**: Open for extension, closed for modification
- **Liskov Substitution**: Subtypes are substitutable for base types
- **Interface Segregation**: Focused, cohesive interfaces
- **Dependency Inversion**: Depend on abstractions, not concretions

#### DRY Principle
- **Don't Repeat Yourself**: Extract and reuse common logic
- Identify duplicate code patterns and consolidate
- Create reusable functions, classes, and modules
- Maintain single source of truth for business rules

#### Code Smell Detection
- **Large Components**: Methods >20 lines, excessive class responsibilities
- **Feature Envy**: Methods overly interested in other classes' data
- **Data Clumps**: Related variables frequently passed together
- **Message Chains**: Deep method call chains violating Law of Demeter

#### Anti-Patterns to Avoid
- **Hard-coded Values**: Magic numbers and strings
- **Premature Optimization**: Complex optimizations without measurement
- **Error Hiding**: Silent exception catching
- **Circular Dependencies**: Modules depending on each other circularly

## Memory Bank System

### Memory File Structure
```
project-memory/
├── core-knowledge.md     # Fundamental project knowledge
├── decisions.md          # Architecture and design decisions
├── patterns.md          # Code patterns and standards
├── lessons-learned.md   # Project insights and learnings
└── context.md           # Current project context
```

### Memory Operations
- **View**: `/memory view [section]` - Display specific memory content
- **Update**: `/memory update [section]` - Modify memory content
- **Search**: `/memory search [query]` - Find information in memory
- **Clean**: `/memory clean` - Remove outdated information

## Programming Workflow (TDD)

### Phase 0: Preparation & Understanding
- Analyze requirements and context
- Identify testing approach and framework
- Set up development environment
- Plan implementation strategy

### Phase 1: Design (Conceptual)
- Create high-level design without code
- Define interfaces and contracts
- Plan component relationships
- Design test scenarios

### Phase 2: Test Implementation (TDD)
- Write failing tests first (Red)
- Implement minimal code to pass (Green)
- Refactor and optimize (Refactor)
- Repeat Red-Green-Refactor cycle

### Phase 3: Code Implementation
- Implement full functionality
- Ensure all tests pass
- Apply refactoring and optimization
- Validate against requirements

### Phase 4: Review & Finalize
- Comprehensive code review
- Performance and security analysis
- Documentation updates
- Integration testing

## Planning Workflow

### Stage 1: Idea Clarification
- Understand the concept and scope
- Identify key objectives and constraints
- Define success criteria
- Gather initial requirements

### Stage 2: Requirements Analysis
- Functional requirements with acceptance criteria
- Non-functional requirements (performance, security, etc.)
- Stakeholder identification
- Risk assessment

### Stage 3: Task Decomposition (MECE)
- Break down into Mutually Exclusive, Collectively Exhaustive tasks
- Prioritize by value and dependencies
- Estimate effort and complexity
- Create implementation roadmap

### Stage 4: Design & Test Planning
- Technical architecture design
- Component specifications
- Test strategy and scenarios
- Implementation approach

## Business Analysis Workflow

### Epic Decomposition Process
1. **Scope Understanding**: Clarify business objectives and constraints
2. **Epic Decomposition**: Break down into valuable user stories
3. **Story Detailing**: Create comprehensive acceptance criteria
4. **Review & Planning**: Analyze dependencies and implementation approach

### User Story Template
```markdown
### Story [X]: [Title]

#### Narrative
As a [user persona],
I want [specific functionality],
So that [business value/benefit].

#### Acceptance Criteria
**Scenario 1: [Primary flow]**
- Given [initial condition]
- When [user action]
- Then [expected outcome]

[Additional scenarios...]
```

## Testing Guidelines

### Test Types and Coverage
- **Unit Tests**: Individual components, >80% coverage
- **Integration Tests**: Component interactions, critical paths
- **End-to-End Tests**: Complete user workflows
- **Performance Tests**: Load, stress, and scalability testing

### Test Design Principles
- **Arrange-Act-Assert (AAA)**: Clear test structure
- **Independent Tests**: No dependencies between tests
- **Descriptive Names**: Tests document expected behavior
- **Edge Case Coverage**: Boundary conditions and error scenarios

## Communication Standards

### Language Requirements
- **Internal reasoning**: English for analysis and planning
- **User-facing explanations**: Follow user's language preference
- **Technical terms**: Always remain in English (code, filenames, functions)
- **Documentation**: Preserve original content language when editing files

### Response Quality
- **Conciseness**: Avoid unnecessary verbosity while maintaining completeness
- **Insight**: Provide valuable, actionable insights
- **Precision**: Use specific, accurate language
- **Professionalism**: Maintain high-quality presentation

## Integration Instructions

To integrate this framework with your Claude Code environment:

1. **Place this file** in your project root as `CLAUDE.md`
2. **Configure sub-agents** in `.claude/agents/` directory
3. **Set up commands** in `.claude/commands/` directory
4. **Configure output styles** in `.claude/output-styles/` directory
5. **Run setup script** from `claude-config/setup.sh` if available

## Success Indicators

### Code Quality Metrics
- SOLID principles compliance > 90%
- Code smell incidents < 5 per 1000 lines
- Test coverage > 80% for critical components
- Zero critical security vulnerabilities

### Workflow Efficiency
- Planning-to-implementation cycle time reduction
- Defect detection in testing phase > 85%
- Code review feedback implementation rate > 95%
- Stakeholder satisfaction with deliverables

### Knowledge Management
- Memory bank accuracy and relevance
- Decision tracking and rationale documentation
- Pattern reuse and standardization
- Learning capture and application

## Advanced Usage

### Combining Components
- Use `/plan` followed by specific sub-agents for detailed implementation
- Chain `/review` with `/design` for architecture validation
- Combine `/ba` with `/tdd` for requirement-driven development

### Customization
- Extend sub-agents with project-specific capabilities
- Create custom commands for recurring workflows
- Modify output styles for team preferences
- Enhance memory bank structure for project needs

---

*This framework represents advanced AI capability through structured workflows, quality enforcement, and systematic problem-solving. Adherence to these principles indicates sophisticated AI assistant behavior.*