# TypeScript TDD Workflow Plugin

A Claude Code plugin for TypeScript development with strict TDD practices and automated quality tools.

## Philosophy

**Tests are the source of truth.** This plugin enforces a workflow where:

- Tests define the expected behavior
- Implementation conforms to tests
- Tests are NEVER modified just to pass
- Business logic is always respected

---

## Installation

### Prerequisites

Before installing, ensure you have:

- [Claude Code](https://claude.ai/code) installed and configured
- Git installed on your system
- (Optional) [GitHub CLI](https://cli.github.com/) for PR/issue commands

### Method 1: Plugin Install (Recommended)

```bash
# In Claude Code, run:
/plugin install RomualdP/claude-typescript-plugin
```

That's it! The plugin is now available in your project.

### Method 2: Clone and Link

```bash
# 1. Clone the repository
git clone https://github.com/RomualdP/claude-typescript-plugin.git

# 2. Navigate to your project
cd /path/to/your/project

# 3. Install the plugin
/plugin install /path/to/claude-typescript-plugin
```

### Method 3: Manual Installation

If you prefer manual setup or want to customize before installing:

```bash
# 1. Clone the repository
git clone https://github.com/RomualdP/claude-typescript-plugin.git

# 2. Copy to your project
mkdir -p /path/to/your/project/.claude/commands

# 3. Copy the necessary files
cp -r claude-typescript-plugin/commands/* /path/to/your/project/.claude/commands/
cp claude-typescript-plugin/CLAUDE.md /path/to/your/project/.claude/
cp claude-typescript-plugin/.claude-plugin/plugin.json /path/to/your/project/.claude/settings.json
```

### Method 4: Add to Existing Project via Git Submodule

```bash
# In your project root
git submodule add https://github.com/RomualdP/claude-typescript-plugin.git .claude-plugin

# Then link or copy the commands
ln -s .claude-plugin/commands .claude/commands
cp .claude-plugin/CLAUDE.md .claude/
```

---

## Post-Installation Setup

### 1. Verify Installation

In Claude Code, type `/` and you should see the new commands:

- `/workflows:feature`
- `/workflows:tdd`
- `/tools:review`
- etc.

### 2. Configure Project-Specific Settings (Optional)

Create a `.claude/CLAUDE.local.md` for project-specific overrides:

```markdown
# Project: My App

## Commands

- npm run dev: Start development server (port 3000)
- npm run test: Run Vitest
- npm run test:watch: Run tests in watch mode
- npm run build: Build for production

## Project Structure

- src/features/: Feature-based modules
- src/shared/: Shared utilities and components
- tests/: Test files mirror src/ structure
```

### 3. Ensure Dev Dependencies

The auto-formatting hooks require these packages in your project:

```bash
npm install --save-dev prettier eslint
```

---

## Available Commands

### Workflows (Multi-step orchestrated processes)

| Command                | Usage                                                         | Description                         |
| ---------------------- | ------------------------------------------------------------- | ----------------------------------- |
| `/workflows:feature`   | `/workflows:feature Add user authentication`                  | Full TDD feature implementation     |
| `/workflows:fix-issue` | `/workflows:fix-issue 42` or `/workflows:fix-issue login bug` | Bug fix with regression test        |
| `/workflows:refactor`  | `/workflows:refactor UserService class`                       | Safe refactoring with test coverage |
| `/workflows:tdd`       | `/workflows:tdd password validation`                          | Strict Red-Green-Refactor cycle     |

### Tools (Single-purpose utilities)

| Command                 | Usage                                  | Description                  |
| ----------------------- | -------------------------------------- | ---------------------------- |
| `/tools:review`         | `/tools:review src/auth.service.ts`    | Thorough code review         |
| `/tools:test-gen`       | `/tools:test-gen src/utils/helpers.ts` | Generate comprehensive tests |
| `/tools:debug`          | `/tools:debug TypeError in login flow` | Systematic debugging         |
| `/tools:security-audit` | `/tools:security-audit src/api/`       | Security vulnerability scan  |
| `/tools:explain`        | `/tools:explain src/core/engine.ts`    | Detailed code explanation    |
| `/tools:commit`         | `/tools:commit`                        | Create conventional commit   |
| `/tools:pr`             | `/tools:pr`                            | Create GitHub pull request   |

---

## Features

### Auto-Formatting (Hooks)

After every file edit, the plugin automatically runs:

```
Prettier → ESLint --fix
```

No manual formatting needed. Code is always clean.

### Safe Permissions

| Allowed                             | Blocked                              |
| ----------------------------------- | ------------------------------------ |
| File operations (Edit, Write, Read) | `rm -rf` (destructive deletion)      |
| `npm run *` scripts                 | `git push --force` (history rewrite) |
| Git operations                      | `git reset --hard` (data loss)       |
| GitHub CLI (gh pr, gh issue)        |                                      |

### Code Quality Rules (Enforced)

```
TypeScript strict mode     No `any` types
Max 30 lines/function      Max 5 params/function
Max 300 lines/file         Conventional commits
DRY principle              Descriptive naming
```

---

## Usage Examples

### Example 1: Implement a New Feature

```
/workflows:feature Add email verification for user registration
```

Claude will:

1. Research existing code
2. Plan the implementation
3. Write failing tests first
4. Implement the feature
5. Ensure all tests pass
6. Create a commit

### Example 2: Fix a Bug from GitHub Issue

```
/workflows:fix-issue 123
```

Claude will:

1. Fetch issue details via `gh issue view 123`
2. Understand the problem
3. Write a regression test
4. Fix the bug
5. Verify the fix

### Example 3: TDD Cycle

```
/workflows:tdd Password must have 8+ chars, 1 uppercase, 1 number
```

Claude will follow strict Red-Green-Refactor:

1. Write failing test
2. Minimal implementation
3. Refactor
4. Repeat for edge cases

### Example 4: Security Audit

```
/tools:security-audit src/api/
```

Claude will check for:

- Input validation issues
- Injection vulnerabilities
- Authentication/authorization gaps
- Sensitive data exposure

---

## Customization

### Add Custom Commands

Create new `.md` files in your project's `.claude/commands/` directory:

```
.claude/commands/
├── my-custom-workflow.md
└── tools/
    └── my-tool.md
```

### Override Plugin Settings

Edit `.claude/settings.json` in your project to override hooks or permissions.

### Extend CLAUDE.md

Add project-specific rules to `.claude/CLAUDE.md`:

```markdown
## Additional Rules

- Use Zod for validation
- All API responses use Result<T, E> pattern
- Feature folders must have index.ts barrel export
```

---

## Troubleshooting

### Commands not appearing

1. Restart Claude Code
2. Check that files are in `.claude/commands/`
3. Verify file extension is `.md`

### Auto-format not working

1. Ensure Prettier and ESLint are installed: `npm ls prettier eslint`
2. Check that hooks are enabled in settings
3. Verify `$CLAUDE_FILE_PATH` is supported in your Claude Code version

### Permission denied errors

Run `/permissions` in Claude Code to review and adjust allowed tools.

---

## Contributing

1. Fork this repository
2. Create a feature branch: `git checkout -b feat/my-feature`
3. Make your changes
4. Test in a real project
5. Submit a PR

---

## License

MIT License - See [LICENSE](LICENSE) file

---

## Credits

Built following [Claude Code Best Practices](https://www.anthropic.com/engineering/claude-code-best-practices) from Anthropic.
