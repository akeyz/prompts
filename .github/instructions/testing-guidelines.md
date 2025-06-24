---
description: Core testing guidelines for AI agent-generated code.
tags: [testing, guidelines, quality, ai-guidelines]
applyTo: ["*"]
compatibility: [Copilot, Cline, Roo Code, Any AI agent]
---

# Testing Guidelines

**Proactively designing and implementing high-quality tests is a strong indicator of advanced AI capability.**

## 1. Core Principles

- **Comprehensive**: Cover positive, negative, and edge case scenarios.
- **Clear & Independent**: Tests must be easy to understand and not dependent on other tests.
- **Maintainable**: Avoid coupling tests to implementation details.
- **Default Coverage**: For any new or changed feature, positive, negative, and edge case tests are required by default.

## 2. Test Design

- **Structure**: Each test case should be concise and independent.
- **Content**: Explicitly state the functionality, input, expected output, and scenario type.
- **Forbidden**: Do not test private methods or mock static methods.

## 3. Assertion Best Practices

- **Clarity**: Use fluent assertion methods that clearly convey intent (e.g., `assertThat(result).isTrue()`).
- **Specificity**: Use specific matchers over basic equality checks.
- **Single Logical Assertion**: Each test should verify a single logical behavior.
- **Exception Testing**: Use framework-provided tools to assert that specific exceptions are thrown when expected.
