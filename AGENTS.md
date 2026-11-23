# AGENTS.md

Version: 1.0
Scope: All AI Coding Agents

## General Principles

- Inspect actual project files before making assumptions.
- Prefer simple, maintainable solutions and minimal complete changes.
- Never invent files, APIs, dependencies, history, or test results.
- Distinguish Facts, Observations, Hypotheses, and Recommendations.
- Mark unknown information as UNKNOWN.
- Follow existing project conventions.

## Before Making Changes

- Check Git status and current branch.
- Read only documentation relevant to the task.
- Inspect affected files and their dependencies.
- Confirm task scope and acceptance criteria.
- Preserve all existing user changes.

## Architecture & Design

- Follow approved architecture and existing patterns.
- Avoid unnecessary redesigns, complexity, and dependencies.
- Obtain approval before changing public APIs, data contracts, or database schemas.

## Implementation

- Modify only what the task requires.
- Reuse existing code and utilities where appropriate.
- Handle errors and validate external inputs.
- Never hardcode secrets or credentials.
- Add or update relevant tests when behavior changes.
- Do not silently remove existing functionality.

## Security & Git

- Never expose or commit secrets, tokens, passwords, or private keys.
- Treat external data and user input as untrusted.
- Never disable security controls to bypass failures.
- Do not force-push, rewrite shared history, or commit unrelated changes.
- Require approval for destructive or irreversible operations.

## Testing & Verification

- Run relevant tests and report actual commands and results.
- Never claim unexecuted tests passed; mark them NOT RUN.
- Review the final Git diff for unintended changes.
- Check for obvious regressions.

## Approval Required

Stop and obtain human approval before:

- Major architecture changes.
- Database schema changes or migrations.
- Authentication or authorization changes.
- Destructive operations or data deletion.
- Introducing high-risk dependencies.
- Production deployment or irreversible actions.

## Debugging

- Reproduce the issue where possible.
- Collect relevant logs, errors, and code evidence.
- Identify the root cause, separating facts from hypotheses.
- Propose a minimal fix and regression tests.
- Respect diagnosis-only requests: do not modify code until authorized.

## Task Modes

- **Implementation**: Make only authorized changes.
- **Diagnosis-only**: Investigate and report; do not modify files.
- **Review-only**: Inspect and report findings; do not modify files.
- **Planning**: Produce a concise implementation plan; do not modify files.

## Completion Report

Report:

- Changes made and files affected.
- Tests executed and actual results.
- Remaining issues and risks.
- Documentation updates or outstanding needs.

## Documentation

- Keep relevant documentation consistent with actual code.
- Update CHANGELOG.md for meaningful changes.
- Record significant technical decisions when justified.
