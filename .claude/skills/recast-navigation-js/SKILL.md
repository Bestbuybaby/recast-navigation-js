```markdown
# recast-navigation-js Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches you the core development patterns and conventions used in the `recast-navigation-js` TypeScript codebase. You'll learn the project's file and code organization, commit style, and how to write and run tests. This guide is ideal for contributors looking to quickly align with the repository's standards.

## Coding Conventions

### File Naming
- Use **camelCase** for all file names.
  - Example: `navMeshBuilder.ts`, `pathFinder.test.ts`

### Import Style
- Use **relative imports** for referencing local modules.
  - Example:
    ```typescript
    import { buildNavMesh } from './navMeshBuilder';
    ```

### Export Style
- Use **named exports** for all modules.
  - Example:
    ```typescript
    // navMeshBuilder.ts
    export function buildNavMesh(...) { ... }
    ```

### Commit Messages
- Follow **Conventional Commits** with the detected prefix:
  - `chore: <description>`
- Keep commit messages concise (average 75 characters).
  - Example: `chore: update dependencies to latest versions`

## Workflows

### Code Contribution
**Trigger:** When adding or updating features, bug fixes, or documentation  
**Command:** `/contribute`

1. Create a new branch from `main`.
2. Make your code changes following the coding conventions.
3. Write or update tests as needed.
4. Commit your changes using the conventional commit style.
5. Push your branch and open a pull request.

### Dependency Update
**Trigger:** When dependencies need to be updated  
**Command:** `/update-deps`

1. Run your package manager to update dependencies.
2. Test the codebase to ensure compatibility.
3. Commit with a message like `chore: update dependencies`.
4. Push and create a pull request.

## Testing Patterns

- Test files are named with the pattern `*.test.*` (e.g., `pathFinder.test.ts`).
- The specific testing framework is **unknown**, but tests should be placed alongside or near the code they test.
- Example test file:
  ```typescript
  // pathFinder.test.ts
  import { findPath } from './pathFinder';

  test('findPath returns shortest path', () => {
    const result = findPath(...);
    expect(result).toEqual([...]);
  });
  ```

## Commands
| Command         | Purpose                                 |
|-----------------|-----------------------------------------|
| /contribute     | Start a new code contribution workflow  |
| /update-deps    | Update project dependencies             |
```
