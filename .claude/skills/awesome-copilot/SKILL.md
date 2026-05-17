```markdown
# awesome-copilot Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill provides guidance on contributing to the `awesome-copilot` TypeScript repository. It covers the project's coding conventions, commit patterns, and testing structure, ensuring consistency and maintainability. While no specific automation workflows were detected, this guide includes recommended commands and patterns for common development tasks.

## Coding Conventions

### File Naming
- Use **kebab-case** for all filenames.
  - Example:  
    ```
    awesome-feature.ts
    user-profile.test.ts
    ```

### Import Style
- Use **relative imports** for internal modules.
  - Example:
    ```typescript
    import { doSomething } from './utils';
    ```

### Export Style
- Use **named exports** exclusively.
  - Example:
    ```typescript
    // utils.ts
    export function doSomething() { /* ... */ }
    ```

### Commit Messages
- Follow **conventional commit** format.
- Use the `build` prefix for build-related changes.
  - Example:
    ```
    build: update dependencies to latest versions
    ```

## Workflows

### Code Contribution
**Trigger:** When adding or updating features or bug fixes  
**Command:** `/contribute`

1. Create a new branch with a descriptive name.
2. Write code following the coding conventions above.
3. Add or update tests in `*.test.ts` files.
4. Commit changes using the conventional commit format.
5. Open a pull request for review.

### Dependency Updates
**Trigger:** When dependencies need to be updated  
**Command:** `/update-deps`

1. Update dependencies in `package.json`.
2. Run tests to ensure compatibility.
3. Commit with a message like:  
   ```
   build: update dependencies
   ```
4. Push and create a pull request.

## Testing Patterns

- Test files use the pattern `*.test.*` (e.g., `feature.test.ts`).
- Testing framework is **unknown**; follow existing patterns or consult maintainers.
- Example test file:
  ```typescript
  // math-utils.test.ts
  import { add } from './math-utils';

  describe('add', () => {
    it('adds two numbers', () => {
      expect(add(2, 3)).toBe(5);
    });
  });
  ```

## Commands
| Command        | Purpose                                   |
|----------------|-------------------------------------------|
| /contribute    | Start a new code contribution workflow    |
| /update-deps   | Update project dependencies               |
```