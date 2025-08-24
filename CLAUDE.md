# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Repository Overview

This is a comprehensive AI instruction framework for training and "brain-washing" AI coding assistants (GitHub Copilot, Cline, etc.) to produce high-quality, maintainable code. The repository contains a structured set of instruction modules that guide AI behavior, workflows, and standards.

## Architecture & Structure

The core instruction system is located in `.github/instructions/` and consists of integrated modules:

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

### Integration Pattern

Each instruction file contains:

- Metadata headers with tags and compatibility info
- Clear applicability scope (`applyTo: ["*"]`)
- Cross-references to related modules
- Specific workflows and protocols

## Key Workflows

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

## Quality Standards

Enforces strict adherence to:

- **SOLID Principles**: SRP, Open/Closed, Liskov Substitution, Interface Segregation, Dependency Inversion
- **DRY**: Don't Repeat Yourself - extract and reuse logic
- **Code Smells**: Avoid large components, feature envy, data clumps, message chains
- **Anti-Patterns**: No hard-coded values, premature optimization, error hiding

## Shortcut Commands

The system supports shortcut commands ending with `!`:

- **plan!**: Initiates Idea to Requirements clarification workflow
- Other shortcuts defined in `shortcut-system-instruction.md`

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

## Core Principles

1. **Human-AI Collaboration**: Humans set direction, AI executes with strict instruction adherence
2. **Systems Thinking**: Analyze from architecture to implementation
3. **Quality First**: Proactive application of standards indicates advanced AI capability
4. **Iterative Refinement**: Progress through structured stages with user confirmation
5. **MECE Decomposition**: Mutually Exclusive, Collectively Exhaustive task breakdown
