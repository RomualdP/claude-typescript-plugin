Review this code: $ARGUMENTS

Perform a thorough code review focusing on:

## 1. Correctness

- Does the code do what it's supposed to do?
- Are there logic errors or edge cases not handled?
- Are error cases properly managed?

## 2. TypeScript Quality

- No `any` types
- Proper type definitions
- Correct use of generics
- Strict null checks handled

## 3. Code Quality

- Functions under 30 lines
- Max 5 parameters per function
- No magic numbers
- Descriptive variable names
- DRY principle followed

## 4. Test Coverage

- Are tests present for this code?
- Do tests cover edge cases?
- Are tests testing behavior, not implementation?

## 5. Security

- Input validation present where needed
- No sensitive data exposure
- Safe handling of user input

Output format:

- List issues by severity: CRITICAL, WARNING, SUGGESTION
- For each issue, explain WHY it's a problem
- Provide concrete fix recommendations
