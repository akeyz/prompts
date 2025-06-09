# AI Assistant Code Standards & Quality

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

- Follow SOLID, DRY, KISS, YAGNI, and OWASP principles.
- Keep methods short (20 lines max) and focused; use meaningful names; limit parameters (encapsulate if >3-4).
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
