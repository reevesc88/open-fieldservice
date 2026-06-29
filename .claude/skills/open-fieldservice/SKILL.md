```markdown
# open-fieldservice Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill teaches the development patterns and conventions used in the `open-fieldservice` TypeScript codebase. It covers file naming, import/export styles, commit message formats, and testing patterns. The repository does not use a specific framework, focusing on clean, modular TypeScript code.

## Coding Conventions

### File Naming
- Use **kebab-case** for all file names.
  - Example:  
    ```
    user-service.ts
    order-controller.test.ts
    ```

### Import Style
- Use **relative imports** for modules within the project.
  - Example:
    ```typescript
    import { getUser } from './user-service';
    ```

### Export Style
- Use **named exports** for all exported functions, types, and constants.
  - Example:
    ```typescript
    // user-service.ts
    export function getUser(id: string) { ... }
    export const USER_ROLE = 'admin';
    ```

### Commit Messages
- Follow **Conventional Commits** with the `feat` prefix for features.
  - Example:
    ```
    feat: add user authentication middleware
    ```

## Workflows

_No automated workflows detected in the repository._

## Testing Patterns

- Test files follow the pattern: `*.test.*`
  - Example:  
    ```
    user-service.test.ts
    ```
- The testing framework is **unknown**; check test files for specific usage.
- Place tests alongside the modules they test or in a dedicated test directory.

#### Example Test File
```typescript
// user-service.test.ts
import { getUser } from './user-service';

describe('getUser', () => {
  it('returns user by id', () => {
    // test implementation here
  });
});
```

## Commands
| Command | Purpose |
|---------|---------|
| /test   | Run all test files matching `*.test.*` |
| /commit | Create a commit message following the conventional format |
```