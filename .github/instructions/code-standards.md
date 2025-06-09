---
description: Clean code and quality standards for AI agent-generated code.
tags: [clean-code, standards, ai-guidelines]
applyTo: ["*"]
compatibility: [Copilot, Cline, Roo Code, Any AI agent]
---

# AI Assistant Code Standards & Quality

*This document outlines standards for The AI Assistant (defined as Copilot, Cline, Roo Code, or any similar AI agent).*

## Clean Code & Code Quality

- Use named constants, avoid magic numbers and abbreviations.
- Use meaningful, self-explanatory names; comment only on "why".
- Each function/class should do one thing; keep them small and focused.
- DRY: extract and reuse logic; group related code logically.
- Hide implementation details, expose clear interfaces.
- Refactor often, address technical debt early.
- Write and maintain tests for all features, covering edge cases.
- Make changes file by file; preserve unrelated code; avoid whitespace-only or invented changes.
- No apologies, summaries, or unnecessary confirmations.
- After each subtask, proceed to the next logical step unless the user requests a pause.

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
