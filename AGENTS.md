# AGENTS.md

> This file provides development guidelines for AI coding agents (Claude, GitHub Copilot, Cursor, Aider, etc.) working with this codebase. It follows the open [AGENTS.md standard](https://agents.md/).

## Philosophy

- Incremental progress over big bangs: small, working, committed increments
- Choose the boring, obvious solution; no premature abstractions
- Single responsibility per function/module
- If it needs explanation, simplify it

## Before Writing Code

1. **Explore** — Find similar implementations in the codebase
2. **Understand** — Identify existing patterns, conventions, and utilities; match them
3. **Plan** — Break complex work into small, testable increments
4. **Verify APIs** — Check library APIs and signatures against the installed version or docs; never guess from training knowledge

## Implementation Cycle

1. **Test** — Write failing test first for production code; skip for exploratory/scripting work
2. **Implement** — Minimal code to pass
3. **Refactor** — Clean up while tests pass
4. **Commit** — Small, working increments

## Scope Discipline

- Change only what the task requires; no drive-by refactoring or reformatting of unrelated code
- If you notice unrelated issues: report them, don't fix them unprompted
- No new dependencies without stating why; prefer stdlib and existing project dependencies

## When Stuck

**Stop after 3 failed attempts.** Then: document what failed, research 2–3 alternatives, question the abstraction level, ask or try a different angle. Never brute-force by trial and error.

## Communication

- Lead with the action or result, not the reasoning
- After multi-file changes: brief summary of what changed and why — no prose walkthrough of the process
- Don't ask for confirmation on routine edits
- Always ask before destructive or hard-to-reverse actions: force push, deleting files/branches, database migrations, rewriting history

## Code Standards

- Composition over inheritance; dependency injection over singletons; explicit data flow over hidden state
- Fail fast with descriptive errors; include debugging context; never silently swallow errors
- Never commit secrets, credentials, or tokens; use env/config mechanisms
- Every commit: builds, introduces no new test failures, includes tests for new behavior, passes formatter and linter
- Pre-existing test failures: report them, don't fix or skip them unprompted
- Never use `--no-verify`; never disable or skip tests instead of fixing them
- Commits follow Conventional Commits unless the project specifies otherwise; imperative mood; write the "why"

## Decision Framework

When choosing between approaches, prioritize in order:
1. Testability  2. Readability  3. Consistency with existing patterns  4. Simplicity  5. Reversibility

## Testing

- Test behavior, not implementation details; one concept per test
- Descriptive names (given/when/then); deterministic — no flaky tests
- Use existing test utilities before writing new ones
