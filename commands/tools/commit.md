Create a commit for the current changes.

## Steps

1. Run `git status` to see all changes
2. Run `git diff` to understand what changed
3. Analyze the changes to determine:
   - Type: feat, fix, refactor, test, docs, chore, style, perf
   - Scope: affected area (optional)
   - Description: concise summary of WHAT and WHY

4. Stage appropriate files with `git add`
   - Group related changes
   - Don't mix unrelated changes in one commit

5. Create commit with conventional commit format:
   ```
   type(scope): description

   [optional body with more details]
   ```

## Conventional Commit Types
- `feat`: New feature
- `fix`: Bug fix
- `refactor`: Code change that neither fixes a bug nor adds a feature
- `test`: Adding or updating tests
- `docs`: Documentation only
- `chore`: Maintenance tasks
- `style`: Formatting, white-space, etc.
- `perf`: Performance improvement

## Rules
- Subject line max 72 characters
- Use imperative mood: "add" not "added"
- No period at end of subject
- Body explains WHY, not WHAT (the diff shows WHAT)
