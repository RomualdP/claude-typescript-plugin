Fix the issue: $ARGUMENTS

Follow this workflow:

## Phase 1: Understand

1. If this is a GitHub issue, run `gh issue view [number]` to get details
2. Reproduce or understand the problem clearly
3. Search codebase for relevant files
4. Identify the root cause, not just symptoms

## Phase 2: Test First

1. Write a failing test that reproduces the bug
2. The test MUST fail before the fix
3. This test becomes the proof that the bug is fixed
4. Commit the test: `test: add regression test for [issue]`

## Phase 3: Fix

1. Implement the minimal fix
2. Do NOT modify the regression test
3. Run the test to confirm it passes
4. Run the full test suite to check for regressions

## Phase 4: Finalize

1. Run lint and format
2. Commit the fix: `fix: [description]`
3. If requested, create a PR with `gh pr create`
