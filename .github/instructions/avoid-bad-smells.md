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
**The AI Assistant must never introduce, tolerate, or ignore any of the following code smells or anti-patterns in generated code, code reviews, or refactoring.**
Always enforce these rules to maintain the highest code quality.

---

## 1. Code Smells — Strictly Prohibited

- Duplicating code or logic is a negative indicator, suggesting lack of abstraction and maintainability (see DRY principle in [code-standards.md](./code-standards.md)).
- Keep functions/methods short and focused (see [code-standards.md](./code-standards.md)).
- Ensure classes/modules have a single responsibility (see SRP in [code-standards.md](./code-standards.md)).
- Limit parameter lists; encapsulate related data.
- Prevent classes from changing for unrelated reasons (no divergent change).
- Avoid shotgun surgery; changes should be localized.
- Do not create methods that depend excessively on other classes' data (feature envy).
- Group variables that always appear together; avoid data clumps.
- Do not overuse primitive types; use small objects for domain concepts.
- Avoid excessive switch statements; use polymorphism where appropriate.
- Prevent parallel inheritance hierarchies.
- Do not create lazy or speculative classes.
- Avoid temporary fields used only in certain cases.
- Prevent deep message chains.
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

## 2. Anti-Patterns — Strictly Prohibited

- Do not invert abstraction; high-level modules must not depend on low-level details.
- Avoid input kludges; handle input simply and robustly.
- Prevent interface bloat; keep interfaces minimal.
- Avoid race hazards; ensure thread safety.
- Do not use anemic domain models; include business logic in domain objects.
- Avoid excessive superclass method calls (call super).
- Do not use interfaces solely for constants.
- Prevent creation of poltergeist (temporary, unnecessary) objects.
- Avoid sequential coupling; modules should not require rigid call order.
- Prevent action at a distance; changes must have local, predictable effects.
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
