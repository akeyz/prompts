# LLM Agent Instructions Overview

This overview distills the purpose and synergy of the LLM agent instruction files in this directory. These directives empower the AI agent to execute complex software development tasks—from ideation to deployment—with precision, adhering to stringent quality standards and defined workflows.

## Instruction Modules: A Cohesive Ecosystem

The instruction files are interconnected modules, forming a comprehensive guide. Understanding their interplay is crucial for maximizing agent effectiveness.

## Module Categories and Impact

### 1. Core Behavior Definition 🧱

These modules establish the agent's foundational operational principles and systems.

- **`memory-bank.instructions.md` (Memory System)**: Defines the Memory Bank, vital for persistent project knowledge across sessions. Underpins `programming-workflow.md` and `shortcut-system-instruction.md` by ensuring context retention.
- **`response-and-prompt-guidelines.md` (Interaction Model)**: Dictates AI response structure and user interaction protocols. Shapes the "Core Interaction Model" in `req.md`, influences `shortcut-system-instruction.md`, and guides `sequential-thinking.md` output formulation.
- **`programming-workflow.md` (Development Workflow)**: Mandates a structured, test-driven development lifecycle. Orchestrates `memory-bank.instructions.md`, `code-standards.md`, `avoid-bad-smells.md`, `testing-guidelines.md`, and `workflow-and-task-splitting.md`.
- **`workflow-and-task-splitting.md` (Task Splitting Methodology)**: Provides principles for dissecting complex requirements into actionable, MECE tasks. Referenced by `req.md` and `programming-workflow.md`.

### 2. Standards & Quality Specifications ✨

This category enforces the quality, maintainability, and robustness of AI-generated designs and code.

- **`code-standards.md` (Code Quality Standards)**: Specifies clean code principles. Intrinsically linked with `avoid-bad-smells.md`; a core reference for `programming-workflow.md`, `req.md`, and `shortcut-system-instruction.md`.
- **`avoid-bad-smells.md` (Code Smell Prevention)**: Catalogs code smells and anti-patterns for strict avoidance. Complements `code-standards.md`; referenced by `programming-workflow.md`, `req.md`, and `shortcut-system-instruction.md`.
- **`testing-guidelines.md` (Testing Methodology)**: Outlines best practices for robust test design and implementation. Referenced by `programming-workflow.md`, `req.md`, and `shortcut-system-instruction.md`.

### 3. Process Templates 📋

These modules define structured pathways for transforming concepts into executable plans.

- **`req.md` (Idea to Implementation Process)**: Defines a strategic workflow from vague ideas to requirements, tasks, design, and test cases. It's a high-level process map, integrating `workflow-and-task-splitting.md`, `response-and-prompt-guidelines.md`, and leveraging `programming-workflow.md`, `code-standards.md`, `avoid-bad-smells.md`, and `testing-guidelines.md` for its design and testing phases.

### 4. Tool Usage Guides 🛠️

This category instructs the agent on leveraging specific tools and commands for enhanced operation.

- **`sequential-thinking.md` (Sequential Thinking Tool Guide)**: Guides the strategic use of the `sequentialthinking` MCP tool for nuanced problem-solving. Output structuring is implicitly guided by `response-and-prompt-guidelines.md`.
- **`shortcut-system-instruction.md` (Shortcut Commands)**: Defines concise commands for efficient agent interaction, providing rapid access to functionalities detailed in `req.md`, `programming-workflow.md`, `code-standards.md`, `avoid-bad-smells.md`, `testing-guidelines.md`, `memory-bank.instructions.md`, and `response-and-prompt-guidelines.md`.

## Leveraging These Instructions

To maximize AI agent performance, reference pertinent instruction modules when assigning tasks. This ensures alignment with expected processes, quality benchmarks, and interaction models. This overview and the detailed instructions are your definitive resource for consistent, high-quality outcomes.
