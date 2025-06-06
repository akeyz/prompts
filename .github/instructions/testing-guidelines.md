# Testing Guidelines & Best Practices

## Test Design Guidelines

- Each test case must be clear, concise, and independent of implementation details.
- State functionality, input, expected output, and scenario type (positive/negative/edge).
- Include setup/teardown if needed; mock only when necessary.
- Do not test private methods or use reflection to access them.
- Do not mock static methods.
- For every new/changed model/feature, generate positive, negative, and edge case tests by default.

### Test Case Template

| Test Case | Description            | Input        | Expected Output   | Scenario Type            | Setup/Teardown         |
| --------- | ---------------------- | ------------ | ----------------- | ------------------------ | ---------------------- |
| [Name]    | [What is being tested] | [Input data] | [Expected result] | [Positive/Negative/Edge] | [Setup/Teardown steps] |

## JUnit Assertion Best Practices

- Prefer fluent assertion libraries (AssertJ/Hamcrest) over basic JUnit assertions.
- Use meaningful failure messages; avoid primitive assertions unless intent is obvious.
- Place assertions immediately after the code they verify; each assertion checks one behavior.
- For exceptions, use `assertThatThrownBy` or `assertThrows`.
- Write self-explanatory assertions; assert in logical order: state, behavior, side effects.
