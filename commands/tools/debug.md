Debug this issue: $ARGUMENTS

Follow systematic debugging:

## 1. Gather Information

- What is the expected behavior?
- What is the actual behavior?
- When did it start happening?
- Can it be reproduced consistently?

## 2. Reproduce

- Create a minimal test case that reproduces the issue
- Isolate the problem from other code
- Document exact steps to reproduce

## 3. Analyze

- Add strategic console.log or debugger statements
- Trace the data flow
- Check assumptions at each step
- Look for:
  - Null/undefined values
  - Type mismatches
  - Race conditions (async)
  - State mutations
  - Off-by-one errors

## 4. Hypothesize & Test

- Form a hypothesis about the root cause
- Test the hypothesis with minimal changes
- If wrong, revert and try another hypothesis

## 5. Fix

- Write a failing test that captures the bug
- Implement the fix
- Verify the test passes
- Run full test suite for regressions

## 6. Document

- Explain what caused the bug
- Explain the fix
- Suggest how to prevent similar bugs
