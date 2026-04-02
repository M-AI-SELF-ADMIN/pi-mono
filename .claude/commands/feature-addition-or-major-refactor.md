---
name: feature-addition-or-major-refactor
description: Workflow command scaffold for feature-addition-or-major-refactor in pi-mono.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /feature-addition-or-major-refactor

Use this workflow when working on **feature-addition-or-major-refactor** in `pi-mono`.

## Goal

Implements a new feature or major refactor, typically involving changes to implementation code, documentation, examples, and tests.

## Common Files

- `packages/coding-agent/src/core/**/*.ts`
- `packages/coding-agent/docs/**/*.md`
- `packages/coding-agent/examples/**/*.ts`
- `packages/coding-agent/test/**/*.test.ts`
- `packages/coding-agent/CHANGELOG.md`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Update or create implementation files in src/core or src/providers
- Update or create documentation files in docs/
- Update or create example files in examples/
- Update or create test files in test/ or test/suite/
- Update CHANGELOG.md

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.