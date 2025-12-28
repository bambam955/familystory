# AGENTS.md

## Specture System

This project uses the Specture System for managing specifications and design documents. When you ask about planned features, architectural decisions, or implementation details, refer to the `specs/` directory in the repository. Each spec file (`specs/NNN-name.md`) contains:

- Design rationale and decisions
- Task lists for implementation
- Requirements and acceptance criteria

The `specs/` directory also contains a `README.md` with complete guidelines on how the spec system works.

**Important**: Before editing the design in any spec file, prompt the user for explicit permission.

When implementing a spec, follow this workflow for each task:

1. Complete a single task from the task list
2. Update the spec file by changing `- [ ]` to `- [x]` for that task
3. Commit both the implementation and spec update together with a conventional commit message (e.g., `feat: implement feature X`)
4. Push the changes

This keeps the spec file as a living document that tracks implementation progress, with each task corresponding to one commit.

### Key Concepts

- **Specs as living documents**: Specs are continually improved during design and implementation, but left static after completion
- **Scope**: Specs cover planned changes—new features, major refactors, redesigns, tooling improvements. Use the issue tracker for bugs
- **Status workflow**: draft → approved → in-progress → completed (or rejected)
- **Precedence**: Higher-numbered specs take precedence when conflicts arise. Once a spec is completed, treat it as historical record; don't retroactively update it (fix only typos/factual errors)
- **Task organization**: Tasks are grouped into logical sections (e.g., Foundation, Core Implementation, Polish and Documentation)
- **File naming**: Numeric prefix with kebab-case (e.g., `000-mvp.md`, `013-refactor-database.md`). Higher numbers have higher precedence

### Directory Structure

- **`specs/`**: Markdown spec files for planned changes (features, refactors, improvements)
- **`specs/README.md`**: Complete spec guidelines, workflow, and best practices
- **`AGENTS.md`**: This file, for agentic coding tools

## Development Environment

TBD...ignore this section for now

## Code Style and Organization

- **Naming**: Kebab-case with numeric prefix for specs and files
- **Documentation**: Prioritize clarity; explain "why" in specs; code shows "how"
- **Commits**: Use conventional commits (feat:, fix:, test:, refactor:, etc.)

## Testing

TBD...ignore this section for now

## GitHub Workflow

**Creating issues and PRs:**

```bash
# View issue details
gh issue view <number>

# Create PR with conventional commit format (required)
gh pr create --title "feat: add new feature" --body "Description of changes"
```

**PR Title Format**: PRs are squashed on merge to main, so PR titles become commit messages. Use conventional commit format:

- `feat:` for features
- `fix:` for bug fixes
- `refactor:` for refactoring
- `docs:` for documentation
- `test:` for test changes
