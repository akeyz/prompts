---
description: Defines how AI assistants recognize and execute user-defined shortcut commands (e.g., r!, d!, t!), ensuring consistent, predictable, and structured shortcut handling.
author: https://github.com/nickbaumann98
version: 1.0
tags: [ "shortcut", "ai-assistant", "command", "system-instruction" ]
globs: ["*"]
---

# Shortcut Instruction for AI Assistants

## Purpose

This document defines how AI assistants recognize and execute user-defined shortcut commands (such as `r!`, `d!`, `t!`). It ensures accurate intent mapping and efficient, predictable responses.  
**All AI assistants must follow these rules to maintain consistency and reliability in shortcut handling.**

## Shortcut Command Format

- Short prefixes ending with `!` (e.g., `r!`, `d!`, `t!`).
- All available shortcut commands must be documented in this file.
- Example commands: `r!`, `d!`, `t!`.

## Recognition and Execution Process

1. Parse input and extract the shortcut identifier.
2. Look up the identifier in this file.
3. If matched, execute the associated action; otherwise, prompt the user for clarification or suggest available commands.
4. User-defined shortcuts take precedence. In case of conflicts, prompt the user to choose.

## Recommended Shortcut Commands and Usage

### Design Layer

- `d!` Architecture & Class Design  
  - Output system/module/class structure and method design with rationale.  
    Reference: [programming-workflow.md], [code-standards.md], [avoid-bad-smells.md].
- `doc!` Documentation Generation  
  - Generate or synchronize design docs, API specs, or use case documentation.  
    Reference: [memory-bank.instructions.md], [response-and-prompt-guidelines.md].

### Implementation Layer

- `t!` Test Case Design  
  - List positive, negative, and edge test cases with input, expected output, and scenario type.  
    Reference: [testing-guidelines.md], [programming-workflow.md].
- `tdd!` Test-Driven Development  
  - Write test code before implementation, following TDD workflow.  
    Reference: [programming-workflow.md], [testing-guidelines.md], [code-standards.md].
- `code!` Code Implementation & Refactoring  
  - Implement or refactor classes, methods, or files according to design and code standards.  
    Reference: [code-standards.md], [avoid-bad-smells.md], [testing-guidelines.md].

### Quality Layer

- `pr!` Code Review & PR Process  
  - Simulate PR review, identify potential issues, and provide suggestions.  
    Reference: [response-and-prompt-guidelines.md], [avoid-bad-smells.md], [code-standards.md], [testing-guidelines.md].
- `std!` Standards & Best Practices Inquiry  
  - Consult development standards, code smells, and best practices.  
    Reference: [code-standards.md], [avoid-bad-smells.md], [programming-workflow.md].

### Support Layer

- `m!` Memory Bank Maintenance & Progress Sync  
  - Maintain `.memory-bank/`, record progress, decisions, and architecture.  
    Reference: [memory-bank.instructions.md], [response-and-prompt-guidelines.md].
- `shorts!` Shortcut Command Overview  
  - Display all available shortcut commands and their descriptions by dynamically scanning this file.  
    Reference: This file.
- `rules!` AI Self-Check & Rules Compliance  
  - List all custom rules and instructions currently available to the AI assistant.
  - Verify the AI assistant is aware of and following all user-defined rules.
  - Provide a comprehensive overview of system instructions, rule files, and configuration settings.
  - Reference: All custom instructions and rules.

### Planning

- `plan!` Requirement Clarification & Task Planning  
  - Decompose requirements, clarify objectives, and break down development tasks into structured subtasks.  
    Reference: [workflow-and-task-splitting.md], [response-and-prompt-guidelines.md], [programming-workflow.md].

---

> This rule applies to all AI assistants.  
> Ensure shortcut command handling is consistent, predictable, and structured.
