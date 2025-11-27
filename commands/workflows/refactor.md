Refactor: $ARGUMENTS

Follow this workflow:

## Phase 1: Analyze

1. Identify what needs refactoring and why
2. Search for all usages and dependencies
3. Review existing tests for the affected code
4. Ensure tests provide sufficient coverage BEFORE refactoring

## Phase 2: Ensure Test Coverage

1. If tests are missing, write them FIRST
2. Tests must pass before any refactoring begins
3. Commit new tests separately: `test: add coverage for [area]`

## Phase 3: Refactor

1. Make incremental changes
2. Run tests after EACH change
3. If tests fail, STOP - something broke
4. Never change tests during refactoring (unless fixing test code itself)

## Phase 4: Validate

1. All original tests must still pass
2. Behavior must be identical (unless intentionally changed)
3. Run lint and format
4. Commit: `refactor: [description]`

IMPORTANT: If tests fail during refactoring, the refactor introduced a bug. Fix the implementation, NOT the tests.
