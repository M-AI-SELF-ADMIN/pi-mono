```markdown
# pi-mono Development Patterns

> Auto-generated skill from repository analysis

## Overview

This skill teaches you the core development patterns, coding conventions, and collaborative workflows used in the `pi-mono` TypeScript monorepo. You'll learn how to structure code, write tests, update documentation, and participate in common repository tasks using standardized commands and step-by-step processes.

## Coding Conventions

- **Language:** TypeScript
- **Framework:** None detected
- **File Naming:** Use kebab-case for all files.
  - Example: `my-feature.ts`, `user-service.test.ts`
- **Import Style:** Use relative imports.
  - Example:
    ```typescript
    import { doThing } from '../utils/do-thing'
    ```
- **Export Style:** Use named exports.
  - Example:
    ```typescript
    // Good
    export function myFunction() { ... }
    export const MY_CONST = 42

    // Avoid default exports
    ```
- **Commit Messages:** Use [Conventional Commits](https://www.conventionalcommits.org/) with these prefixes:
  - `fix`, `docs`, `chore`, `feat`, `test`
  - Example: `feat(core): add new agent provider`
- **Directory Structure:**
  - Source code: `packages/<package>/src/`
  - Tests: `packages/<package>/test/`
  - Documentation: `packages/<package>/docs/`
  - Examples: `packages/<package>/examples/`

## Workflows

### Feature Addition or Major Refactor
**Trigger:** When adding a significant new feature or refactoring an existing subsystem  
**Command:** `/feature`

1. Update or create implementation files in `src/core` or `src/providers`.
2. Update or create documentation in `docs/`.
3. Update or create example files in `examples/`.
4. Update or create test files in `test/` or `test/suite/`.
5. Update `CHANGELOG.md` for the package.

**Example:**
```typescript
// src/core/new-feature.ts
export function newFeature() { ... }
```
```markdown
<!-- docs/new-feature.md -->
# New Feature
Description and usage...
```

---

### Bugfix with Changelog
**Trigger:** When fixing a bug and documenting the change  
**Command:** `/bugfix`

1. Update implementation file(s) to fix the bug.
2. Update or add a test file to cover the bug.
3. Update `CHANGELOG.md` for the package.

**Example:**
```typescript
// src/core/buggy-code.ts
export function fixedFunction() { /* bug fixed */ }
```
```typescript
// test/core/buggy-code.test.ts
import { fixedFunction } from '../../src/core/buggy-code'
test('should not throw', () => { ... })
```

---

### Test Suite Expansion
**Trigger:** When improving or adding to test coverage  
**Command:** `/add-tests`

1. Create or update test files in `test/` or `test/suite/`.
2. Optionally update related documentation (e.g., test README).

**Example:**
```typescript
// test/suite/new-feature.test.ts
import { newFeature } from '../../src/core/new-feature'
test('works as expected', () => { ... })
```

---

### Documentation Update
**Trigger:** When clarifying, expanding, or correcting documentation  
**Command:** `/docs`

1. Update or create documentation files in `docs/`.
2. Optionally update `README.md` or `AGENTS.md`.

**Example:**
```markdown
<!-- docs/usage.md -->
# Usage Guide
How to use the package...
```

---

### Dependency Bump
**Trigger:** When updating dependencies for security or compatibility  
**Command:** `/bump-dep`

1. Update `package-lock.json` and/or `package.json` for the affected package.

**Example:**
```json
// package.json
"dependencies": {
  "some-lib": "^2.0.0"
}
```

---

### Release Cycle
**Trigger:** When preparing for or performing a new release  
**Command:** `/release`

1. Update `CHANGELOG.md` files for all packages.
2. Update `package.json` and `package-lock.json` for all packages.

---

### CI Config Update
**Trigger:** When changing CI/CD, contributor, or workflow settings  
**Command:** `/ci-update`

1. Update files in `.github/` or `scripts/`.
2. Optionally update related documentation.

**Example:**
```yaml
# .github/workflows/ci.yml
jobs:
  test:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - run: npm ci
      - run: npm test
```

## Testing Patterns

- **Framework:** [Vitest](https://vitest.dev/)
- **Test Files:** Use the pattern `*.test.ts` and place tests in `test/` or `test/suite/`.
- **Test Example:**
  ```typescript
  // test/core/example.test.ts
  import { myFunction } from '../../src/core/my-function'

  test('returns correct value', () => {
    expect(myFunction()).toBe('expected')
  })
  ```
- **Run Tests:** Use the standard Vitest CLI (`vitest` or `npx vitest`).

## Commands

| Command     | Purpose                                                |
|-------------|--------------------------------------------------------|
| /feature    | Start a new feature or major refactor workflow         |
| /bugfix     | Fix a bug and update changelog and tests               |
| /add-tests  | Expand or add new test suites                          |
| /docs       | Update or add documentation                            |
| /bump-dep   | Bump dependencies in package.json and lock files       |
| /release    | Prepare and perform a release                          |
| /ci-update  | Update CI/CD or workflow configuration                 |
```
