---
description: Defines how AI assistants recognize and execute user-defined shortcut commands (e.g., r!, d!, t!), ensuring consistent, predictable, and structured shortcut handling.
author: https://github.com/nickbaumann98
version: 1.1
tags: [ "shortcut", "ai-assistant", "command", "system-instruction" ]
globs: ["*"]
---

# Shortcut Instruction for AI Assistants

## Purpose & Format

This document defines how AI assistants handle shortcut commands - short prefixes ending with `!` (e.g., `r!`, `d!`, `t!`). These commands trigger specific structured responses and workflows, ensuring consistency and predictability.

## Command Execution Process

1. Parse input to extract the shortcut identifier (e.g., `r!`)
2. Match the identifier to a command in this file
3. Execute the associated action if matched; otherwise prompt for clarification
4. User-defined shortcuts take precedence in case of conflicts

## Available Commands

### Design Layer

- **d!**
  - Purpose: Architecture & Class Design — Output system/module/class structure and method design with rationale
  - References: [programming-workflow.md], [code-standards.md], [avoid-bad-smells.md]
- **doc!**
  - Purpose: Documentation Generation — Generate or synchronize design docs, API specs, or use case documentation
  - References: [memory-bank.instructions.md], [response-and-prompt-guidelines.md]

### Implementation Layer

- **t!**
  - Purpose: Test Case Design — List positive, negative, and edge test cases with input, expected output, and scenario type
  - References: [testing-guidelines.md], [programming-workflow.md]
- **tdd!**
  - Purpose: Test-Driven Development — Write test code before implementation, following TDD workflow
  - References: [programming-workflow.md], [testing-guidelines.md], [code-standards.md]
- **code!**
  - Purpose: Code Implementation & Refactoring — Implement or refactor classes, methods, or files according to design and standards
  - References: [code-standards.md], [avoid-bad-smells.md], [testing-guidelines.md]

### Quality Layer

- **pr!**
  - Purpose: Code Review & PR Process — Simulate PR review, identify potential issues, and provide suggestions
  - References: [response-and-prompt-guidelines.md], [avoid-bad-smells.md], [code-standards.md], [testing-guidelines.md]
- **std!**
  - Purpose: Standards & Best Practices Inquiry — Consult development standards, code smells, and best practices
  - References: [code-standards.md], [avoid-bad-smells.md], [programming-workflow.md]

### Support Layer

- **m!**
  - Purpose: Memory Bank Maintenance — Maintain `.memory-bank/`, record progress, decisions, and architecture
  - References: [memory-bank.instructions.md], [response-and-prompt-guidelines.md]
- **shorts!**
  - Purpose: Shortcut Command Overview — Display all available shortcut commands and their descriptions
  - References: This file
- **rules!**
  - Purpose: AI Self-Check & Rules Compliance — List all custom rules and instructions available to the AI assistant
  - References: All custom instructions and rules

### Planning

- **plan!**
  - Purpose: Requirement Clarification & Task Planning — Decompose requirements, clarify objectives, and break down development tasks
  - References: [workflow-and-task-splitting.md], [response-and-prompt-guidelines.md], [programming-workflow.md]

## Usage Examples

- `r!` triggers structured requirement decomposition: `r! Create a login system`
- `plan!` initiates detailed planning: `plan! Implement user authentication`
- `d!` starts architecture design: `d! Design a database schema for users`

> This rule applies to all AI assistants.  
> Ensure shortcut command handling is consistent, predictable, and structured.
