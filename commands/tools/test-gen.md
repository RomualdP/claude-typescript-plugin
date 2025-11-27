Generate tests for: $ARGUMENTS

Follow these guidelines:

## Analysis First
1. Read and understand the code to test
2. Identify all public functions/methods
3. Identify dependencies that need mocking
4. List all possible scenarios and edge cases

## Test Structure
Use this pattern for each test file:
```typescript
describe('[UnitName]', () => {
  describe('[methodName]', () => {
    it('should [expected behavior] when [condition]', () => {
      // Arrange
      // Act
      // Assert
    });
  });
});
```

## Coverage Requirements
For each function, cover:
- Happy path (normal expected input)
- Edge cases (empty, null, undefined, boundary values)
- Error cases (invalid input, failures)
- Async behavior if applicable

## Test Quality Rules
- Test behavior, NOT implementation details
- One assertion concept per test
- Descriptive test names that explain the scenario
- No test interdependence
- Minimal mocking - prefer real implementations when possible

## Output
Generate complete, runnable test files. Include necessary imports and setup.
