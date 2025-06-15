# LLM Agent Instructions Overview

This document provides an overview of the LLM agent instruction files located in this directory. These instructions are designed to guide the AI agent in performing complex software development tasks, from understanding initial ideas to implementing and testing code, while adhering to specific quality standards and workflows.

## Instruction Modules and Relationships

The instruction files are highly interconnected modules, forming a comprehensive and cohesive guide for the LLM agent. Understanding their relationships is key to leveraging them effectively.

## Module Categories and Descriptions

### 1. Core Behavior Definition

These modules define the fundamental operational principles and core systems for the LLM agent.

*   **`memory-bank.instructions.md` (Memory System)**: Describes the Memory Bank system, crucial for maintaining project knowledge across sessions. Referenced by `programming-workflow.md` and `shortcut-system-instruction.md` as a foundational element for context retention.
*   **`response-and-prompt-guidelines.md` (Interaction Model)**: Outlines how the LLM agent should structure its responses and interact with users. It's a key input for `req.md` (influencing the "Core Interaction Model") and `shortcut-system-instruction.md`. It also implicitly guides how `sequential-thinking.md` outputs are formulated.
*   **`programming-workflow.md` (Development Workflow)**: Defines the mandatory, structured, test-driven approach for all programming tasks. This is a central orchestrator, referencing `memory-bank.instructions.md`, `code-standards.md`, `avoid-bad-smells.md`, `testing-guidelines.md`, and `workflow-and-task-splitting.md`.
*   **`workflow-and-task-splitting.md` (Task Splitting Methodology)**: Provides principles for decomposing complex requirements into manageable tasks. Referenced by `req.md` and `programming-workflow.md`.

### 2. Standards & Quality Specifications

This category includes guidelines that ensure the quality, maintainability, and robustness of the code and designs produced by the LLM agent.

*   **`code-standards.md` (Code Quality Standards)**: Details clean code principles and quality standards. It's intrinsically linked with `avoid-bad-smells.md` and is a core reference for `programming-workflow.md`, `req.md`, and `shortcut-system-instruction.md`.
*   **`avoid-bad-smells.md` (Code Smell Prevention)**: Lists code smells and anti-patterns to be strictly avoided. Complements `code-standards.md` and is referenced by `programming-workflow.md`, `req.md`, and `shortcut-system-instruction.md`.
*   **`testing-guidelines.md` (Testing Methodology)**: Outlines best practices for designing and implementing tests. Referenced by `programming-workflow.md`, `req.md`, and `shortcut-system-instruction.md`.

### 3. Process Templates

These modules define structured processes for transforming ideas into actionable plans and implementations.

*   **`req.md` (Idea to Implementation Process)**: Defines a workflow for taking vague ideas through requirements, task definition, design, and test case creation. It acts as a high-level process guide, referencing `workflow-and-task-splitting.md` and `response-and-prompt-guidelines.md`. Its later stages for design and testing directly integrate guidelines from `programming-workflow.md`, `code-standards.md`, `avoid-bad-smells.md`, and `testing-guidelines.md`.

### 4. Tool Usage Guides

This category provides instructions on how to use specific tools or commands that aid the LLM agent's operation.

*   **`sequential-thinking.md` (Sequential Thinking Tool Guide)**: Guides the use of the `sequentialthinking` MCP tool for complex problem-solving. Its usage would be implicitly guided by `response-and-prompt-guidelines.md` for structuring its output.
*   **`shortcut-system-instruction.md` (Shortcut Commands)**: Defines a set of shortcut commands for efficient interaction. This module references many others (`req.md`, `programming-workflow.md`, `code-standards.md`, `avoid-bad-smells.md`, `testing-guidelines.md`, `memory-bank.instructions.md`, `response-and-prompt-guidelines.md`) as it provides quick access to their respective functionalities.

## How to Use These Instructions

When tasking the LLM agent, referencing the relevant instruction modules can help ensure that the agent understands the expected process, quality standards, and interaction model. This overview and the detailed instruction files are intended for both human developers seeking to guide the LLM agent and for the agent itself to ensure consistent, high-quality performance and adherence to project standards. These documents are intended to be a comprehensive resource for both human users guiding the LLM and for the LLM agent itself to maintain consistent and high-quality performance.

**Note on Location**: These files are located in the `.github/instructions` directory. While this is a common path for GitHub-related templates, these specific files serve as operational instructions for the LLM agent.
