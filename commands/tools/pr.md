Create a Pull Request for the current branch.

## Steps

1. Run `git status` to check current state
2. Run `git log main..HEAD` (or appropriate base branch) to see all commits
3. Run `git diff main..HEAD` to see all changes
4. Ensure all changes are committed
5. Push the branch if needed: `git push -u origin [branch]`

## PR Content

Create PR with `gh pr create` including:

### Title

- Follow conventional commit format: `type(scope): description`
- Be specific but concise

### Body Structure

```markdown
## Summary

[2-3 bullet points describing WHAT and WHY]

## Changes

- [List of significant changes]

## Testing

- [ ] Unit tests added/updated
- [ ] Integration tests pass
- [ ] Manual testing completed

## Checklist

- [ ] Code follows project conventions
- [ ] No `any` types introduced
- [ ] Tests cover edge cases
- [ ] Documentation updated if needed
```

## Before Creating

- Verify tests pass
- Verify lint passes
- Verify build succeeds
