# TypeScript TDD Workflow Plugin

## Stack
- TypeScript strict mode only
- No `any` types allowed
- Explicit return types on functions

## Code Quality
- Max 30 lines per function
- Max 5 parameters per function
- Max 300 lines per file
- Use explicit constants, no magic numbers
- Long, descriptive variable names
- DRY: eliminate duplication

## Testing - CRITICAL
**IMPORTANT: Tests are the source of truth.**

YOU MUST:
- NEVER modify tests just to make them pass
- ALWAYS respect business cases in tests
- ALWAYS cover edge cases
- If a test fails, fix the implementation, NOT the test
- Only modify a test if the business requirement changed (confirmed by user)

Testing workflow:
1. Write/review tests first (TDD)
2. Understand what the test expects
3. Implement code to satisfy the test
4. If test fails, analyze WHY before touching anything

## Error Handling
- Fail fast, throw early
- Use custom domain errors
- Log errors in English with error codes

## Git Conventions
- Commit messages: conventional commits format
- Branch naming: `type/short-description`

## Workflow
1. Understand the requirement fully before coding
2. Write/review tests first
3. Implement minimal code to pass tests
4. Refactor if needed
5. Run lint and format before committing
