```markdown
# suna Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the core development patterns used in the `suna` TypeScript codebase. You'll learn about file naming conventions, import/export styles, commit message habits, and how to write and run tests. While no specific framework is detected, the repository follows consistent TypeScript best practices and uses relative imports and named exports throughout.

## Coding Conventions

### File Naming
- Use **camelCase** for file names.
  - Example: `userProfile.ts`, `dataFetcher.ts`

### Import Style
- Use **relative imports** for modules within the codebase.
  - Example:
    ```typescript
    import { fetchData } from './dataFetcher';
    ```

### Export Style
- Use **named exports**.
  - Example:
    ```typescript
    // In dataFetcher.ts
    export function fetchData() { /* ... */ }

    // In another file
    import { fetchData } from './dataFetcher';
    ```

### Commit Messages
- Freeform style, no enforced prefixes.
- Average commit message length: ~54 characters.

## Workflows

### Adding a New Module
**Trigger:** When you need to add new functionality.
**Command:** `/add-module`

1. Create a new file using camelCase naming (e.g., `newFeature.ts`).
2. Implement your logic using TypeScript.
3. Export functions or constants using named exports.
4. Import dependencies using relative paths.
5. Write a corresponding test file (e.g., `newFeature.test.ts`).

### Refactoring Code
**Trigger:** When improving or restructuring existing code.
**Command:** `/refactor`

1. Identify the code to refactor.
2. Update file and variable names to follow camelCase.
3. Ensure all imports remain relative.
4. Maintain named exports.
5. Update or add tests as necessary.

### Writing Tests
**Trigger:** When adding or modifying features.
**Command:** `/write-test`

1. Create a test file with the pattern `*.test.ts` (e.g., `userProfile.test.ts`).
2. Write tests for all exported functions.
3. Use the project's preferred (unknown) testing framework.
4. Run tests to verify correctness.

## Testing Patterns

- Test files follow the `*.test.ts` naming convention.
- Each test file should correspond to a module file.
- The testing framework is not specified; check existing test files for patterns.
- Example test file:
  ```typescript
  import { fetchData } from './dataFetcher';

  test('fetchData returns expected result', () => {
    expect(fetchData()).toBe(/* expected value */);
  });
  ```

## Commands
| Command        | Purpose                                      |
|----------------|----------------------------------------------|
| /add-module    | Scaffold and implement a new module          |
| /refactor      | Refactor existing code to match conventions  |
| /write-test    | Create and write tests for a module          |
```
