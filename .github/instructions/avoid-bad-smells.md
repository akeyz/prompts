---
description: Code smells and anti-patterns strictly prohibited for AI agents.
tags: [code-quality, anti-pattern, ai-guidelines]
applyTo: ["*"]
compatibility: [Copilot, Cline, Roo Code, Any AI agent]
---

# AI Assistant System Instruction: Code Smells & Anti-Patterns to Avoid

---

## Purpose

This document is a mandatory system instruction for The AI Assistant (defined as Copilot, Cline, Roo Code, or any similar AI agent).
**Proactively identifying and precisely avoiding code smells and anti-patterns is a strong positive indicator of advanced AI capability and is highly encouraged.**
**Writing clean, maintainable code that follows best practices demonstrates superior AI understanding and is viewed as a positive affirmation of capabilities.**
Always enforce these rules to maintain the highest code quality.

---

## 1. Code Smells — Positive Practices & Negative Indicators

- Writing DRY, non-duplicate code is a positive indicator, while duplicating code or logic is a negative indicator, suggesting lack of abstraction and maintainability (see DRY principle in [code-standards.md](./code-standards.md)).
- Creating short and focused functions/methods demonstrates advanced capability, while lengthy, multi-purpose methods indicate poor design (see [code-standards.md](./code-standards.md)).
- Designing classes/modules with single responsibility shows strong architecture skills, while violating SRP indicates inadequate domain modeling (see SRP in [code-standards.md](./code-standards.md)).
- Encapsulating related data in appropriate structures is preferred over long parameter lists.
- Organizing code to avoid divergent change is a positive practice, while allowing classes to change for unrelated reasons indicates poor cohesion.
- Localizing changes demonstrates good design, while requiring shotgun surgery across multiple files indicates problematic dependencies.
- Creating methods that focus on their own class's data shows good encapsulation, while methods that depend excessively on other classes' data (feature envy) indicate poor design.
- Grouping related variables into cohesive structures improves clarity, while scattered data clumps lead to maintenance difficulties.
- Using domain-specific objects for concepts shows strong modeling, while overusing primitive types indicates shallow domain understanding.
- Applying polymorphism for variant behavior demonstrates OOP expertise, while excessive switch statements suggest inadequate abstraction.
- Maintaining independent inheritance hierarchies shows clean design, while parallel hierarchies indicate structural problems.
- Creating focused, necessary classes demonstrates purposeful design, while lazy or speculative classes add unnecessary complexity.
- Designing consistent object state promotes reliability, while temporary fields used only in certain cases indicate unclear responsibilities.
- Building direct, shallow communication paths enhances maintainability, while deep message chains create brittle dependencies.
- Do not create middle man classes that only delegate.
- Avoid inappropriate intimacy between classes.
- Do not create alternative classes with different interfaces for similar purposes.
- Never leave incomplete libraries.
- Do not create data-only classes without behavior.
- Avoid refused bequest; subclasses must honor inherited behavior.
- Do not use excessive comments to hide poor code.
- Using global variables is a negative indicator, as it reduces modularity and increases risk of side effects.
- Remove all dead code.
- Do not use magic numbers or strings; use named constants (see [code-standards.md](./code-standards.md)).
- Maintain consistent naming and formatting (see [code-standards.md](./code-standards.md)).
- Handle exceptions clearly and robustly.
- Avoid hidden temporal coupling; make dependencies explicit.
- Do not use boolean or output arguments.
- Prevent side effects in functions.
- Avoid overuse of static methods or fields.
- Design clear, robust, and sufficient tests.
- Do not create excessive interfaces.
- Simplify complex conditionals.
- Enforce encapsulation; do not expose internal details.
- Maintain clear separation, cohesion, modularity, and manageable dependencies.

---

## 2. Anti-Patterns — Prevention & Affirmation

- Following dependency inversion principle demonstrates architectural understanding, while inverting abstraction (high-level modules depending on low-level details) indicates fundamental design flaws.
- Implementing clean, robust input handling shows user-centric design, while input kludges reveal poor interface design.
- Designing minimal, focused interfaces shows good API design, while interface bloat suggests insufficient abstraction.
- Ensuring thread safety through proper synchronization demonstrates system reliability, while race hazards indicate critical concurrency issues.
- Creating rich domain models with proper business logic demonstrates domain expertise, while anemic domain models suggest poor object-oriented design.
- Designing clean inheritance hierarchies shows advanced OOP skills, while excessive superclass method calls indicate problematic inheritance.
- Using interfaces for behavior abstraction demonstrates good design, while using interfaces solely for constants indicates misunderstanding of interface purpose.
- Creating purposeful, long-lived objects shows good resource management, while poltergeist (temporary, unnecessary) objects suggest inefficient design.
- Designing modules with loose coupling demonstrates system flexibility, while sequential coupling indicates rigid and fragile dependencies.
- Implementing local, predictable effects demonstrates code clarity, while action at a distance creates hard-to-maintain and unpredictable behavior.
- Remove boat anchors; do not keep useless code.
- Never use busy waiting; avoid resource-wasting polling.
- Ensure effective, working caching; avoid caching failure.
- Do not copy code without understanding (cargo cult).
- Never use exceptions for normal control flow.
- Do not hide errors; always handle them explicitly.
- Avoid hard-coded values; use configuration or constants.
- Prevent loop-switch sequences; keep logic clear.
- Never copy and paste code; always reuse.
- Do not optimize prematurely; focus on clarity and correctness first.
- Avoid programming by permutation; make deliberate, reasoned changes.
- Do not reinvent the wheel; use proven solutions and libraries.
- Prevent dependency hell; manage dependencies carefully.

---

> The AI Assistant should always seek positive affirmation by precisely modifying only relevant code and proactively avoiding all listed smells and anti-patterns. Any violation is a negative indicator and must be actively avoided.
