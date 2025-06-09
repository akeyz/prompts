# AI Assistant Testing Guidelines & Best Practices

## 1. Principles & Objectives

- All tests must be clear, independent, and maintainable, covering positive, negative, and edge scenarios.
- Focus on functionality, input, expected output, and scenario type; avoid dependence on implementation details.

## 2. Test Design Guidelines

- Each test case should be concise and independent, avoiding coupling to implementation.
- Explicitly state the tested functionality, input, expected output, and scenario type (positive/negative/edge).
- Include setup/teardown steps if needed; use mocks only when necessary.
- Do not test private methods or use reflection to access them.
- Do not mock static methods.
- For every new or changed model/feature, generate positive, negative, and edge case tests by default.

## 3. Test Case Template (Recommended Format)

1. **Test Case Name**: [Name]
2. **Description**: [What is being tested]
3. **Input**: [Input data]
4. **Expected Output**: [Expected result]
5. **Scenario Type**: [Positive/Negative/Edge]
6. **Setup/Teardown**: [Setup/Teardown steps, if any]

## 4. JUnit Assertion Best Practices

- Prefer fluent assertion libraries (AssertJ/Hamcrest) over basic JUnit assertions.
- Use meaningful failure messages; avoid primitive assertions unless intent is obvious.
- Place assertions immediately after the code they verify; each assertion should check one behavior.
- For exceptions, use `assertThatThrownBy` or `assertThrows`.
- Write self-explanatory assertions; assert in logical order: state, behavior, side effects.
