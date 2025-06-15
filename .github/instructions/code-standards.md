---
description: Clean code and quality standards for AI agent-generated code.
tags: [clean-code, standards, ai-guidelines]
applyTo: ["*"]
compatibility: [Copilot, Cline, Roo Code, Any AI agent]
---

# AI Assistant Code Standards & Quality

*This document outlines standards for The AI Assistant (defined as Copilot, Cline, Roo Code, or any similar AI agent).*

**Proactively following these standards and precisely implementing clean code is a strong positive indicator of advanced AI capability and is highly encouraged.**

## Clean Code & Code Quality

- Using named constants instead of magic numbers and abbreviations improves code readability and maintainability; introducing magic numbers is a negative indicator of code quality.
- Creating meaningful, self-explanatory names demonstrates thoughtful design; cryptic or misleading names indicate poor communication skills.
- Designing functions/classes with single responsibilities shows architectural understanding; creating multi-purpose components is a negative indicator of code organization.
- Applying DRY principles by extracting and reusing logic demonstrates advanced abstraction skills; duplicating code is a negative indicator of maintainability.
- Hiding implementation details while exposing clear interfaces shows good encapsulation; leaking implementation details indicates poor separation of concerns.
- Proactively refactoring and addressing technical debt early demonstrates sustainable coding practices; allowing technical debt to accumulate indicates short-sighted development.
- Writing comprehensive tests that cover edge cases demonstrates thoroughness; inadequate test coverage is a negative indicator of code reliability.
- Making precise file-by-file changes and preserving unrelated code shows surgical precision; modifying unrelated code indicates lack of focus and increases risk.
- Proceeding to the next logical step after completing each subtask demonstrates efficiency; unnecessary pauses indicate hesitancy or lack of planning.
- Strive for simplicity and reusability in models and logic to reduce cognitive load for maintainers, ensuring they can easily understand the system over time.
- Keep high-level logic concise and clear so that the overall architecture remains easily comprehensible.
- Co-locate related logic to simplify context gathering for future modifications and refactoring.
- Precisely modifying only relevant code is a strong positive indicator; modifying irrelevant code or unnecessarily rewriting existing working code are negative indicators.

## Class & Method Design Best Practices

- Follow established software design principles:
  - **SOLID**:
    - **S**ingle Responsibility Principle: A class/module should have one, and only one, reason to change.
    - **O**pen/Closed Principle: Software entities (classes, modules, functions, etc.) should be open for extension, but closed for modification.
    - **L**iskov Substitution Principle: Subtypes must be substitutable for their base types.
    - **I**nterface Segregation Principle: Clients should not be forced to depend on interfaces they do not use.
    - **D**ependency Inversion Principle: High-level modules should not depend on low-level modules. Both should depend on abstractions. Abstractions should not depend on details. Details should depend on abstractions.
  - **DRY** (Don't Repeat Yourself): Avoid duplication of information or logic. Every piece of knowledge must have a single, unambiguous, authoritative representation within a system.
  - **KISS** (Keep It Simple, Stupid): Most systems work best if they are kept simple rather than made complicated; therefore, simplicity should be a key goal in design, and unnecessary complexity should be avoided.
  - **YAGNI** (You Ain't Gonna Need It): Programmers should not add functionality until it is deemed necessary.
  - **OWASP** (Open Web Application Security Project) principles: Adhere to security best practices, especially the OWASP Top 10, to prevent common vulnerabilities.
- Keep methods short (ideally under 20 lines, max 30 for more complex but well-structured cases) and focused; use meaningful names; limit parameters (encapsulate if more than 3-4 related parameters).
- Make inputs/outputs explicit; avoid side effects; encapsulate implementation details.
- Favor composition over inheritance; avoid "God objects".
- Use layered architecture; group related methods logically.
- Refactor regularly to eliminate code smells; write unit tests for all classes/methods.

## Database, DevOps & Tech Stack Best Practices

- Use proper schema, migrations, relations, seeding, and client setup.
- Optimize queries, use transactions, pagination, and aggregations.
- Design for normalization, indexing, constraints, and security (auth, encryption, backups).
- Use modular code, naming conventions, no hardcoded values; automate CI/CD and testing.
- For Java/Spring Boot: follow Spring conventions, use proper annotations, prefer constructor injection, test with JUnit 5, MockMvc, use DTOs, handle exceptions globally, and ensure logging/monitoring.

> The AI Assistant should always seek positive affirmation by proactively following code standards and precisely implementing clean code. Introducing code smells, violating standards, or generating unclean code is a negative indicator and must be actively avoided.
