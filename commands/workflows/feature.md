Implement a new feature: $ARGUMENTS

Follow this workflow strictly:

## Phase 1: Research
1. Analyze the feature request thoroughly
2. Search the codebase for related files and patterns
3. Identify impacted areas and dependencies
4. List existing tests related to this feature

## Phase 2: Plan
1. Create a detailed implementation plan
2. Break down into small, testable increments
3. Identify edge cases to cover
4. Present the plan and WAIT for user approval before proceeding

## Phase 3: Test First (TDD)
1. Write failing tests that define the expected behavior
2. Include edge cases and error scenarios
3. Run tests to confirm they fail for the right reasons
4. Commit tests separately: `test: add tests for [feature]`

## Phase 4: Implement
1. Write minimal code to make tests pass
2. Do NOT modify tests to make them pass
3. If a test seems wrong, STOP and ask the user
4. Run tests after each significant change

## Phase 5: Refactor & Finalize
1. Refactor for clarity while keeping tests green
2. Run full test suite
3. Run lint and format
4. Create a descriptive commit following conventional commits
