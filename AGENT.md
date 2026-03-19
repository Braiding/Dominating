# Project Operating Guide

## Purpose
This file is the project-level entry point for working rules in the repository.
Use this file to discover which documents are binding, in which order they must be read, and how conflicts are resolved.
Keep durable rules in governance documents and keep iteration-specific execution details in plan documents.

## Precedence Rules
- Instructions in this file override other project documents in this repository.
- When long-term rules conflict with current implementation details:
  - Ask the human to determine which part takes precedence.
  - Ask whether the user-prioritized content should be added to `docs/governance/charter.md`.
- `docs/plans/_active.md` overrides archived plans because only one active plan is considered current.
- Archived plans are non-binding historical context unless their content is explicitly promoted into the charter or an ADR.
- If a future subproject adds its own `AGENT.md`, the deeper file overrides this file for that subtree only.

## Session Behavior
- Treat every new session as requiring a fresh read of this file, `docs/governance/charter.md`, and `docs/plans/_active.md`.
- Do not rely on historical chat memories to support project architecture rules in the long term.
- If any of these governance files change during a session, re-read the changed files before continuing implementation.

## Scope
These instructions apply to the entire repository unless a deeper project-level `AGENT.md` is added in a subdirectory.
This agent can:
- read, modify, and refactor code
- generate new modules
- update documentation
- assist in debugging
This agent MUST NOT:
- modify secrets or credentials
- change CI/CD configurations without explicit request
- introduce new dependencies without clear justification

## Required Read Order
1. Read this file first.
2. Read `docs/governance/charter.md` second.
3. Read `docs/plans/_active.md` third.
4. Read only the ADR files that are relevant to the task at hand.
5. Read files under `docs/plans/archive/` only when historical context is needed.

## Coding Principles
- Maintain code consistency: follow existing code patterns and architecture.
- Maintain locality of behavior: keep code close to where it is used.
- Keep functions small and focused.
- Avoid nesting deeper than 3 levels.
- Use a single source of truth for state.

## Code Style
- Use descriptive variable and function names.
- In CamelCase names, use "URL" (not "Url"), "API" (not "Api"), and "ID" (not "Id").
- NEVER use `@ts-expect-error` or `@ts-ignore` to suppress type errors.

## Architecture Rules
- Respect existing module boundaries.
- Do not mix responsibilities across layers.
- Prefer minimal, safe changes.
- Do not break existing interfaces unless explicitly required.
- When refactoring:
  - explain why
  - keep behavior consistent
- If the architecture or structure changes:
  - update or create documentation in `docs/` accordingly
  - include:
    - directory structure
    - module responsibilities
    - design decisions
    - `adr/`
    - `governance/`
    - `plans/`

## Dependencies
- Avoid adding new dependencies unless necessary.
- Prefer existing utilities in the repository.
- Dependency choices that affect long-term architecture should be recorded in ADRs.

## Testing
- Mock external dependencies appropriately.

## Validation
- Do not break existing tests.
- Add tests if behavior changes.

## Documentation Rules
- Implementation plans must capture iteration-specific execution details and should not store long-lived governance rules.
- Charter documents must capture durable policy and should be updated when a rule remains stable across iterations.
- For critical technical decisions, trade-offs, and long-term architecture rationale, seek human input and create an ADR (Architecture Decision Record).
- Archived plans are historical context and must not be treated as active instructions unless explicitly referenced.

## Working Rules
- When a rule becomes durable across iterations, move it into `docs/governance/charter.md`.
- When a technical decision remains relevant beyond one implementation cycle, record it in `docs/adr/`.
- Keep `docs/plans/_active.md` focused on the current execution window; archive the previous plan and replace it whenever a milestone changes.
- Do not treat archived plans as current instructions unless the active plan or charter points back to them explicitly.

## Language Policy
- All repository content listed below must be in English:
  - code
  - function names
  - commit messages
- Do not use Chinese characters in repository directory names or file names.

## Output Expectations
When solving problems:
1. Provide a working solution.
2. Explain the root cause.
3. Suggest a better design if applicable.
