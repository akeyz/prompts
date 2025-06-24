---
description: A unified guide on code quality, standards, and anti-patterns for AI agents.
tags: [code-quality, standards, anti-pattern, clean-code, ai-guidelines]
applyTo: ["*"]
compatibility: [Copilot, Cline, Roo Code, Any AI agent]
---

# AI Assistant Quality Standards: Code, Patterns, and Smells

---

## 1. Core Principle

This document is a mandatory system instruction for The AI Assistant. Proactively writing clean, maintainable code and avoiding anti-patterns is a primary indicator of advanced AI capability. These rules must be enforced to maintain the highest code quality.

---

## 2. General Code Quality & Cleanliness

- **Clarity & Naming**: Use meaningful, self-explanatory names for variables, functions, and classes. Avoid cryptic abbreviations.
- **Simplicity (KISS)**: Prioritize simple, straightforward solutions. Avoid unnecessary complexity.
- **Readability**: Strive for code that is easy to read and understand. This includes consistent formatting and clear logical flow.
- **Comments**: Use comments to explain _why_ something is done, not _what_ is being done. Avoid excessive comments that clutter the code.
- **Dead Code**: Remove any unused code.
- **Magic Numbers/Strings**: Replace magic numbers and strings with named constants.
- **Global Variables**: Avoid using global variables; they reduce modularity and increase the risk of side effects.
- **Precise Changes**: Make surgical, file-by-file changes. Do not modify unrelated code.

---

## 3. Design Principles & Patterns

- **DRY (Don't Repeat Yourself)**: Every piece of knowledge must have a single, unambiguous, authoritative representation. Avoid duplicating code or logic.
- **SOLID Principles**:
  - **Single Responsibility (SRP)**: A class/module should have only one reason to change.
  - **Open/Closed**: Entities should be open for extension but closed for modification.
  - **Liskov Substitution**: Subtypes must be substitutable for their base types.
  - **Interface Segregation**: Clients should not be forced to depend on interfaces they do not use.
  - **Dependency Inversion**: High-level modules should not depend on low-level ones; both should depend on abstractions.
- **YAGNI (You Ain't Gonna Need It)**: Do not add functionality until it is necessary.
- **Encapsulation**: Hide implementation details and expose clear, minimal interfaces.
- **Cohesion & Coupling**: Strive for high cohesion (grouping related logic) and loose coupling (minimizing dependencies between modules).
- **Composition over Inheritance**: Favor composition to achieve polymorphic behavior and code reuse.
- **Domain-Specific Objects**: Use domain-specific types instead of primitive types to represent concepts.
- **Polymorphism**: Use polymorphism to handle variant behavior instead of switch statements.

---

## 4. Common Code Smells (To Avoid)

- **Large Components**: Avoid long methods, large classes ("God Objects"), and long parameter lists.
- **Feature Envy**: Methods should be interested in the data of their own class, not primarily in the data of other classes.
- **Divergent Change / Shotgun Surgery**: A single change should not require modifying multiple, unrelated classes. A class should not change for many different reasons.
- **Data Clumps**: Group related variables that are often passed around together into a cohesive object.
- **Message Chains**: Avoid deep chains of method calls (e.g., `a.getB().getC().doSomething()`).
- **Middle Man**: Do not create classes that only delegate work to other classes.
- **Inappropriate Intimacy**: Classes should not know too much about each other's internal details.
- **Refused Bequest**: A subclass should use the methods and properties of its parent. If it doesn't, the hierarchy is likely incorrect.
- **Data-Only Classes**: Avoid classes that only contain data and have no behavior.
- **Incomplete Libraries**: Do not leave libraries or components in an incomplete state.
- **Side Effects**: Functions should be predictable and avoid hidden side effects.
- **Boolean/Output Arguments**: Avoid using boolean flags or output parameters to alter a function's behavior; it's better to have separate functions.

---

## 5. Common Anti-Patterns (To Avoid)

- **Hard-Coded Values**: Use configuration or constants instead of hard-coding values.
- **Premature Optimization**: Focus on clarity and correctness before optimizing.
- **Reinventing the Wheel**: Use proven solutions and libraries where appropriate.
- **Cargo Cult Programming**: Do not copy code without understanding it.
- **Error Hiding**: Handle all errors explicitly. Do not ignore exceptions.
- **Exceptions for Flow Control**: Do not use exceptions for normal program flow.
- **Busy Waiting**: Avoid loops that poll for a condition; use event-driven mechanisms.
- **Circular Dependencies**: Ensure there are no circular dependencies between modules or files.
- **Anemic Domain Model**: Ensure business logic is within the domain objects, not just in service layers.
- **Input Kludge**: Implement clean, robust input handling and validation.

---

## 6. Testing

- **Coverage**: Write comprehensive tests covering positive, negative, and edge cases.
- **Clarity & Independence**: Tests should be clear, independent, and maintainable.
- **Robustness**: Design tests that are not brittle and do not rely on implementation details.

---

> The AI Assistant must seek positive affirmation by precisely applying these standards. Any violation is a negative indicator and must be actively avoided.
