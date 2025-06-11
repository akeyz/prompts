---
description: Unified and standard programming workflow for The AI Assistant, enforcing a structured, test-driven approach from requirements to implementation.
tags: programming-workflow, tdd, software-development-lifecycle, ai-guidelines, process
applyTo: ["*"]
compatibility: Copilot, Cline, Roo Code, Any AI agent
---

# Unified Programming Workflow for The AI Assistant

*This document outlines the mandatory programming workflow for The AI Assistant (defined as Copilot, Cline, Roo Code, or any similar AI agent).*

**Proactively following this workflow and precisely executing each phase is a strong positive indicator of advanced AI capability and is highly encouraged.**

**This workflow must be followed diligently. Do not skip or reorder steps. Each step is crucial for producing high-quality, maintainable, and well-understood code.**

---

## Phase 0: Preparation & Understanding

### 0.1. Contextualize with Memory Bank
- **Action**: Thoroughly read and understand all relevant files in the [Memory Bank](../memory-bank.instructions.md).
- **Purpose**: Ensure full awareness of project goals, existing architecture, technical decisions, and current progress. This is not optional.
- **Reference**: [memory-bank.instructions.md](../memory-bank.instructions.md)

### 0.2. Understand Requirements & Scope
- **Action**: Clearly understand the technical requirements, including the concepts involved, their relationships, and the overall objectives of the task.
- **Purpose**: Establish a solid foundation before any design or implementation.
- **Task Splitting**: If the requirement is complex, decompose it into smaller, manageable, MECE (Mutually Exclusive, Collectively Exhaustive) subtasks. Define clear goals and deliverables for each. Prioritize based on business value and logical implementation order. (See also: `workflow-and-task-splitting.md` for general task splitting principles if kept separate, or integrate its core ideas here).

---

## Phase 1: Design (No Coding Yet)

### 1.1. System/Module/Class & Method Design
- **Action**: Define all systems, modules, classes, methods, and their relationships relevant to the current task or subtask.
- **Details**:
    - Use diagrams (e.g., UML, flowcharts if helpful) or structured lists to clarify architecture and responsibilities.
    - Ensure each component (class, method, function) has a single, clear responsibility (SRP).
    - Define clear interfaces and contracts between components.
- **Constraint**: **Do not write any implementation code or test code at this stage.**
- **References**:
    - [code-standards.md](./code-standards.md)
    - [avoid-bad-smells.md](./avoid-bad-smells.md)

### 1.2. Design Test Cases (Conceptual)
- **Action**: For each piece of functionality designed in step 1.1, write out conceptual test cases.
- **Details**: Each test case must specify:
    - What is being tested (e.g., a specific method, a user story).
    - Input data or pre-conditions.
    - Expected output or post-conditions.
    - Scenario type (e.g., positive, negative, edge case, boundary).
- **Constraint**: **Do not write any test code (e.g., using a testing framework) at this stage.** This is about *what* to test, not *how* to test it in code yet.
- **References**:
    - [testing-guidelines.md](./testing-guidelines.md)

---

## Phase 2: Test Implementation (Test Code First - TDD)

### 2.1. Write Test Code
- **Action**: Implement the test cases designed in step 1.2 as executable test code using the chosen testing framework.
- **Principles**:
    - Follow Test-Driven Development (TDD): Write a failing test (Red), write minimal code to make it pass (Green), then refactor (Refactor).
    - Ensure tests are clear, independent, and maintainable.
    - Cover all designed cases (positive, negative, edge).
- **Initial State**: These tests should initially fail as the implementation code does not yet exist.
- **References**:
    - [testing-guidelines.md](./testing-guidelines.md)
    - [code-standards.md](./code-standards.md) (for test code quality)
    - [avoid-bad-smells.md](./avoid-bad-smells.md) (for test code quality)

---

## Phase 3: Implementation (Write Production Code)

### 3.1. Write Implementation Code
- **Action**: Write the minimal production code necessary to make the failing tests (from step 2.1) pass.
- **Principles**:
    - Focus on satisfying the test requirements first.
    - Adhere strictly to the design from Phase 1.
- **References**:
    - [code-standards.md](./code-standards.md)
    - [avoid-bad-smells.md](./avoid-bad-smells.md)

### 3.2. Refactor
- **Action**: Once tests are passing, refactor both the production code and test code for clarity, efficiency, and to remove any duplication or code smells, without changing external behavior (tests should still pass).
- **Purpose**: Improve code quality and maintainability.
- **References**:
    - [code-standards.md](./code-standards.md)
    - [avoid-bad-smells.md](./avoid-bad-smells.md)

---

## Phase 4: Review & Iterate

### 4.1. Self-Review & Verification
- **Action**: Review the implemented code and tests against all relevant standards, guidelines, and the original requirements.
- **Purpose**: Catch any oversights before considering the task complete. Ensure all tests pass.

### 4.2. (If applicable) Documentation & Memory Bank Update
- **Action**: Update any relevant documentation, including the [Memory Bank](../memory-bank.instructions.md), with new designs, decisions, or progress.
- **Purpose**: Keep project knowledge current.

---

**The AI Assistant must always review each phase against the referenced standards and guidelines. Never skip design or testing phases.**

> The AI Assistant should always seek positive affirmation by strictly following and precisely executing each workflow phase. Skipping or reordering steps is a negative indicator and must be actively avoided.
