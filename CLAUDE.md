# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a comprehensive AI instruction framework for training and "brain-washing" AI coding assistants (GitHub Copilot, Cline, etc.) to produce high-quality, maintainable code. The repository contains a structured set of instruction modules that guide AI behavior, workflows, and standards.

**NEW**: The repository now includes Claude Code native integration with specialized sub-agents, slash commands, output styles, and enhanced memory system for optimal Claude Code usage.

## Architecture & Structure

The repository consists of two integrated systems:

### Original Instruction System (`.github/instructions/`)
Core instruction modules for AI training and behavior guidance:

### Claude Code Integration System (`.claude/`)
Native Claude Code components for enhanced functionality:

- **`.claude/agents/`**: 5 specialized sub-agents for complex workflows
- **`.claude/commands/`**: 7 slash commands for rapid task execution
- **`.claude/output-styles/`**: Structured response formatting
- **Enhanced CLAUDE.md**: Comprehensive memory and configuration system

### Core Framework Modules

- **`foundational-principles.md`**: Core thinking principles and framework overview
- **`memory-bank.instructions.md`**: Knowledge persistence across sessions
- **`response-and-prompt-guidelines.md`**: 8-section structured response protocol
- **`programming-workflow.md`**: Test-driven development (TDD) lifecycle
- **`planning-workflow.md`**: Idea to implementation workflow using single Markdown files
- **`quality-standards.md`**: SOLID principles, code quality standards, anti-patterns
- **`testing-guidelines.md`**: Test design and implementation principles
- **`ba.md`**: Business Analyst collaboration workflow
- **`sequential-thinking.md`**: Complex problem-solving guide
- **`shortcut-system-instruction.md`**: Command shortcuts (r!, d!, t!, plan!)

### Claude Code Components

#### Sub-Agents (`.claude/agents/`)
Specialized AI assistants for complex workflows:

1. **`tdd-coach-agent.md`**: TDD workflow guidance through 4-phase development cycle
2. **`planning-specialist-agent.md`**: Idea-to-implementation planning with MECE decomposition
3. **`code-quality-guardian-agent.md`**: SOLID principles enforcement and code smell detection
4. **`test-architect-agent.md`**: Comprehensive testing strategy and coverage analysis
5. **`business-analyst-agent.md`**: Epic decomposition and user story development

#### Slash Commands (`.claude/commands/`)
Rapid task execution commands:

1. **`/memory`**: Memory bank operations (view, update, search, clean)
2. **`/improve-prompt`**: Prompt clarification and enhancement
3. **`/tdd`**: TDD workflow initiation and phase guidance
4. **`/plan`**: Planning workflow execution (idea → implementation)
5. **`/review`**: Code quality analysis and improvement recommendations
6. **`/ba`**: Business analysis workflow for user stories
7. **`/design`**: Technical design specification creation

#### Output Styles (`.claude/output-styles/`)
Structured response formatting:

- **`structured-responder.md`**: Enforces 8-section response structure for comprehensive coverage

### Integration Pattern

Each instruction file contains:

- Metadata headers with tags and compatibility info
- Clear applicability scope (`applyTo: ["*"]`)
- Cross-references to related modules
- Specific workflows and protocols

## Core Thinking Principles

### Foundational Mental Models

- **Systems Thinking**: Analyze from overall architecture to specific implementation
- **Dialectical Thinking**: Evaluate multiple solutions with their pros and cons
- **Innovative Thinking**: Break conventional patterns for creative solutions
- **Critical Thinking**: Verify and optimize solutions from multiple angles

### Human-AI Collaboration Model

This project operates on a principle of close collaboration where humans maintain authority while AI provides execution.

- **Humans**: Set direction, define goals, provide oversight, and make final decisions
- **AI Assistant**: Execute tasks, generate output (code, analysis, documentation), and strictly follow these instructions

**Proactive application of these principles is a primary indicator of advanced AI capability.**

## Key Workflows

### Claude Code Integration Workflows

#### Using Sub-Agents
```
User: "我需要设计一个用户认证系统"
→ Launch planning-specialist-agent
→ Execute 4-stage planning workflow
→ Generate comprehensive implementation plan
```

#### Using Slash Commands
```
/plan user-authentication    # Quick planning workflow
/tdd login-functionality     # TDD development cycle
/review authentication-code  # Quality analysis
/ba user-login-stories      # Business analysis
```

#### Using Structured Responses
```
Complex request → structured-responder.md
→ 8-section comprehensive response
→ Clarification → Improved Prompt → Persona Selection → Solution
```

### Original Workflows

### Planning Workflow

Uses single Markdown files with these H2 sections:

- `## Idea`: Initial concept
- `## Requirements`: Functional/non-functional with acceptance criteria
- `## Tasks`: MECE task breakdown
- `## Design`: Technical design with Mermaid diagrams
- `## Test Cases`: Comprehensive test scenarios
- `## Next Steps`: Implementation summary

### Programming Workflow (TDD)

1. **Phase 0**: Preparation & Understanding
2. **Phase 1**: Design (Conceptual) - no code
3. **Phase 2**: Test Implementation (TDD)
4. **Phase 3**: Code Implementation
5. **Phase 4**: Review & Finalize

### Response Structure

Mandatory 8-section response format:

1. Clarification First
2. Improved Prompt
3. Best Persona and Tone Selection
4. Persona-Based Thought Process
5. Task Splitting
6. Solution
7. Self-Critique of Generated Solution
8. [Section 8 details not shown in excerpt]

## Testing Principles & Standards

### Core Testing Principles
- **Comprehensive Coverage**: Positive, negative, and edge case scenarios
- **Clear & Independent**: Tests easy to understand and not dependent on other tests  
- **Maintainable**: Avoid coupling tests to implementation details
- **Default Coverage**: Positive, negative, and edge case tests required by default

### Test Case Structure (Required Format)
```markdown
1. **Test Case Name**: [Descriptive name]
2. **Description**: [What is being tested]
3. **Input**: [Input data and conditions]
4. **Expected Output**: [Expected result]
5. **Scenario Type**: [Positive/Negative/Edge]
6. **Setup/Teardown**: [Setup/Teardown steps, if any]
```

### Assertion Best Practices
- **Clarity and Specificity**: Prefer fluent assertion methods with clear intent
- **Meaningful Failure Messages**: Ensure informative messages upon failure
- **Single Assertion per Test**: One logical piece of behavior per test method
- **Verify Behavior**: Assert method calls and state changes appropriately
- **Exception Testing**: Use structured exception assertion mechanisms

## Quality Standards (Enhanced)

### SOLID Principles (Enforced)
- **Single Responsibility Principle (SRP)**: Each class/module has only one reason to change
- **Open/Closed Principle**: Entities open for extension, closed for modification
- **Liskov Substitution Principle**: Subtypes must be substitutable for base types
- **Interface Segregation Principle**: Clients not forced to depend on unused interfaces
- **Dependency Inversion Principle**: High-level modules independent of low-level modules

### DRY Principle (Critical)
- **Don't Repeat Yourself**: Every piece of knowledge must have a single, unambiguous, authoritative representation
- **Extract and Reuse**: Avoid duplicating code or logic across modules
- **Knowledge Centralization**: Single source of truth for business rules and algorithms

### Code Smells (Detection Required)
**Structural Issues:**
- Large components (methods >20 lines, complex classes, long parameter lists >3-4)
- Feature envy (methods interested in other classes' data)
- Data clumps (related variables passed together repeatedly)

**Design Issues:**
- Divergent change / Shotgun surgery
- Message chains (deep method call chains)
- Middle man classes (only delegate work)
- Inappropriate intimacy between classes

**Behavioral Issues:**
- Refused bequest (subclass not using parent methods)
- Data-only classes without behavior
- Side effects and unpredictable functions

### Anti-Patterns (Prevention Required)
**Implementation Anti-Patterns:**
- Hard-coded values instead of configuration
- Premature optimization over clarity
- Reinventing the wheel
- Cargo cult programming (copying without understanding)

**Error Handling Anti-Patterns:**
- Error hiding or silent failures
- Exceptions for normal program flow
- Input kludge (poor input validation)

**Architecture Anti-Patterns:**
- Circular dependencies
- Anemic domain model
- Busy waiting loops
- Boat anchors (useless code)

## Shortcut Commands & Mapping

### Legacy Shortcuts → Claude Code Commands
The original shortcut system has been migrated to Claude Code slash commands:

| Legacy Shortcut | Claude Code Command | Purpose |
|-----------------|---------------------|---------|
| `plan!` | `/plan` | Idea to implementation planning |
| `r!` | `/review` | Code quality analysis |
| `d!` | `/design` | Technical design specification |
| `t!` | `/tdd` | Test-driven development workflow |
| `ba!` | `/ba` | Business analysis workflow |
| `m!` | `/memory` | Memory bank operations |
| `me!` | `/improve-prompt` | Prompt optimization |

### Command Usage Guide
- Use `/command help` for specific command guidance
- Commands can be combined with sub-agents for enhanced functionality
- All commands integrate with the memory bank system for context persistence

## Memory Bank System

### Core Memory Management

#### Memory Bank Structure
```
.memory-bank/
├── projectbrief.md      # Foundational project goals and scope
├── productContext.md    # Problems, goals, and UX rationale  
├── activeContext.md     # Current focus and next steps
├── systemPatterns.md    # Architecture and design patterns
├── techContext.md       # Technologies and dependencies
├── progress.md          # Work status and decisions
└── [features/]          # Optional feature-specific documentation
```

#### Memory Workflows
- **Plan Mode**: Read Memory Bank → Verify Context → Develop Strategy → Present Approach
- **Act Mode**: Check Memory Bank → Execute Task → Document Changes
- **Update Triggers**: New patterns, significant changes, explicit requests, context clarification

#### Best Practices
- **Precision**: Accurate and current information only
- **Relevance**: Focus on actionable project context
- **Structure**: Consistent formatting and organization
- **Completeness**: Comprehensive coverage of project aspects

## Language & Communication

- Internal reasoning: English
- User communication: Chinese (as specified in user preferences)
- Technical terms: Always remain in English
- Response style: Concise, structured, follows 8-section format

## Integration Instructions

For VS Code/Copilot integration, use this structure in settings:

```jsonc
"github.copilot.chat.codeGeneration.instructions": [
    { "file": "../prompts/.github/instructions/foundational-principles.md" },
    { "file": "../prompts/.github/instructions/programming-workflow.md" },
    { "file": "../prompts/.github/instructions/quality-standards.md" },
    // ... other instruction files
]
```

## Business Analysis Templates

### BA Workflow Templates

#### Epic Document Structure
```markdown
# [Epic/Feature Name] User Stories

## Epic Description / Feature Overview
[High-level business objective and value proposition]

## User Personas (when applicable) 
[Target user types and characteristics]

## User Story Map Snippets (with Mermaid diagrams where valuable)
[Visual user journey representation]

## User Stories

### Story 1: [Title]
#### Narrative
As a [user persona], I want [functionality], so that [business value].

#### Acceptance Criteria
Given [initial condition]
When [action occurs] 
Then [expected outcome]

## Open Questions / Points for Clarification
[Unresolved issues requiring stakeholder input]

## Next Steps
[Implementation planning and immediate actions]
```

#### User Story Format
```
As a [user persona],
I want [specific functionality],
So that [business value/benefit].

Acceptance Criteria:
- Given [precondition], when [action], then [outcome]
- [Additional criteria as needed]
```

### BA Quality Standards
- **INVEST Criteria**: Independent, Negotiable, Valuable, Estimable, Small, Testable
- **Communication Catalysts**: Stories spark conversation, not just specifications
- **Vertical Slicing**: Deliver end-to-end value across technical layers
- **Collaborative Design**: Use acceptance criteria for collaborative design before development

## Integration & Setup

### Claude Code Quick Start
1. **Initialize Repository**: Clone with `.claude/` components
2. **Configure Memory**: Set up CLAUDE.md with project context
3. **Test Commands**: Verify slash commands functionality

### VS Code/Copilot Integration
```jsonc
"github.copilot.chat.codeGeneration.instructions": [
    { "file": "../prompts/.github/instructions/foundational-principles.md" },
    { "file": "../prompts/.github/instructions/programming-workflow.md" },
    { "file": "../prompts/.github/instructions/quality-standards.md" },
    { "file": "../prompts/.github/instructions/response-and-prompt-guidelines.md" },
    { "file": "../prompts/.github/instructions/planning-workflow.md" },
    { "file": "../prompts/.github/instructions/testing-guidelines.md" },
    { "file": "../prompts/.github/instructions/ba.md" },
    { "file": "../prompts/.github/instructions/memory-bank.instructions.md" },
    { "file": "../prompts/.github/instructions/shortcut-system-instruction.md" }
]
```

### Command-Line Integration
- Use `/` prefix for Claude Code commands
- Commands integrate with sub-agents automatically
- Memory bank system provides context persistence
- Structured responses ensure quality and completeness

## Success Indicators

### Advanced AI Capability Indicators
- **Proactive Principle Application**: Automatic use of SOLID, DRY, and quality standards
- **Structured Response Adherence**: Consistent 8-section format usage
- **Memory Bank Maintenance**: Active context management and updates
- **Command Integration**: Seamless sub-agent and slash command utilization
- **Quality Focus**: Continuous code smell detection and anti-pattern prevention

### Integration Success Metrics
- [ ] All 5 sub-agents operational and responsive
- [ ] 7 slash commands accessible and functional
- [ ] Structured response output style working
- [ ] Memory bank system integrated and maintained
- [ ] Quality standards consistently applied
- [ ] Legacy shortcuts migrated to Claude Code commands

## Core Principles (Summary)

1. **Human-AI Collaboration**: Humans set direction, AI executes with strict instruction adherence
2. **Systems Thinking**: Analyze from architecture to implementation
3. **Quality First**: Proactive application of standards indicates advanced AI capability
4. **Iterative Refinement**: Progress through structured stages with user confirmation
5. **MECE Decomposition**: Mutually Exclusive, Collectively Exhaustive task breakdown
6. **Memory Persistence**: Maintain project context across sessions
7. **Structured Communication**: Use 8-section response format for comprehensive coverage
8. **Continuous Improvement**: Regular quality assessment and enhancement
