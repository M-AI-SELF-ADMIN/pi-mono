---
name: bugfix-with-changelog
description: Workflow command scaffold for bugfix-with-changelog in pi-mono.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /bugfix-with-changelog

Use this workflow when working on **bugfix-with-changelog** in `pi-mono`.

## Goal

Fixes a bug and records the change in the changelog, often with a test update.

## Common Files

- `packages/*/src/**/*.ts`
- `packages/*/test/**/*.test.ts`
- `packages/*/CHANGELOG.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update implementation file(s) to fix the bug
- Update or add a test file to cover the bug
- Update CHANGELOG.md

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.