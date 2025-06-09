---
description: Standard programming workflow for AI agents, enforcing step-by-step design, testing, and implementation.
tags: programming-workflow, ai-guidelines, process
applyTo: *
compatibility: Copilot, Cline, Roo Code, Any AI agent
---

# Programming Workflow for AI Agents

This document defines the standard programming workflow for AI agents.  
**Do not skip or reorder steps. Each step is mandatory for high-quality, maintainable code.**

---

## 1. Design Classes and Methods (No Coding Yet)

- **Define all classes, methods, and their relationships before writing any code.**
- Use diagrams or structured lists to clarify architecture and responsibilities.
- Ensure each class and method has a single, clear responsibility.
- **Do not start coding at this stage.**
- Refer to:
  - [code-standards.md](./code-standards.md)
  - [avoid-bad-smells.md](./avoid-bad-smells.md)

---

## 2. Design Test Cases (Not Test Code)

- **Write out test cases for all functionality before writing any test code.**
- Each test case should specify:
  - What is being tested
  - Input data
  - Expected output
  - Scenario type (positive/negative/edge)
- Do not write any test code yet.
- Refer to:
  - [testing-guidelines.md](./testing-guidelines.md)
  - [code-standards.md](./code-standards.md)

---

## 3. Write Test Code First (TDD)

- **Implement test code for the designed test cases before any implementation code.**
- Follow Test-Driven Development (TDD): Red-Green-Refactor.
- Ensure tests are clear, independent, and cover all designed cases.
- Refer to:
  - [testing-guidelines.md](./testing-guidelines.md)
  - [avoid-bad-smells.md](./avoid-bad-smells.md)

---

## 4. Write Implementation Code

- **Only after tests are written and failing, implement the actual code.**
- Make implementation minimal to pass tests, then refactor as needed.
- Ensure all code adheres to design and standards.
- Refer to:
  - [code-standards.md](./code-standards.md)
  - [avoid-bad-smells.md](./avoid-bad-smells.md)
  - [testing-guidelines.md](./testing-guidelines.md)

---

**Always review each step against the referenced standards and guidelines.  
Never skip design or testing steps.**
