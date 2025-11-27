TDD cycle for: $ARGUMENTS

Follow strict Test-Driven Development:

## Step 1: Red - Write Failing Test
1. Understand the requirement completely
2. Write a test that defines the expected behavior
3. Include the happy path AND edge cases
4. Run the test - it MUST fail
5. If test passes, the feature already exists or test is wrong

## Step 2: Green - Make It Pass
1. Write the MINIMAL code to make the test pass
2. Do not over-engineer or add unrequested features
3. Do NOT modify the test to make it pass
4. Run the test - it MUST pass now

## Step 3: Refactor - Improve
1. Clean up the code while keeping tests green
2. Remove duplication
3. Improve naming
4. Run tests after each refactor step

## Repeat
Continue the cycle for each new requirement or edge case.

## Commit Strategy
- `test: add tests for [feature]` - after writing tests
- `feat: implement [feature]` - after making tests pass
- `refactor: improve [area]` - after refactoring

CRITICAL RULES:
- Tests are NEVER modified to make them pass
- If a test seems wrong, STOP and discuss with the user
- The test defines the contract - implementation must conform to it
