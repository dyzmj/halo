```markdown
# halo Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill provides guidance on the development patterns used in the `halo` TypeScript codebase. It covers file naming, import/export conventions, commit message style, and testing patterns. By following these conventions, contributors can ensure consistency and maintainability across the project.

## Coding Conventions

### File Naming
- **Pattern:** PascalCase  
  All files should be named using PascalCase (each word capitalized, no separators).
  
  **Example:**  
  ```
  UserService.ts
  AuthController.ts
  ```

### Import Style
- **Pattern:** Relative imports  
  Modules are imported using relative paths.

  **Example:**  
  ```typescript
  import { UserService } from './UserService';
  import { AuthController } from '../controllers/AuthController';
  ```

### Export Style
- **Pattern:** Named exports  
  Functions, classes, or constants are exported using named exports.

  **Example:**  
  ```typescript
  // UserService.ts
  export class UserService { ... }

  // AuthController.ts
  export function authenticate() { ... }
  ```

### Commit Messages
- **Pattern:** Conventional Commits  
  Commit messages use the conventional commit format, with the prefix `feat` for new features. Average message length is 69 characters.

  **Example:**  
  ```
  feat: add user authentication middleware to AuthController
  ```

## Workflows

### Feature Development
**Trigger:** When implementing a new feature  
**Command:** `/feature-development`

1. Create a new file using PascalCase for the feature.
2. Implement the feature using TypeScript.
3. Use relative imports to include dependencies.
4. Export your classes/functions using named exports.
5. Write or update corresponding test files (`*.test.*`).
6. Commit changes using the conventional commit format with `feat` prefix.

### Testing
**Trigger:** When verifying code correctness  
**Command:** `/run-tests`

1. Identify or create test files matching the `*.test.*` pattern.
2. Run the test suite using your preferred test runner.
3. Review test results and fix any failing tests.
4. Commit any necessary fixes using the conventional commit format.

## Testing Patterns

- **Test File Naming:**  
  Test files follow the `*.test.*` pattern (e.g., `UserService.test.ts`).
- **Framework:**  
  No specific testing framework detected; use your preferred TypeScript-compatible test runner.
- **Example:**  
  ```typescript
  // UserService.test.ts
  import { UserService } from './UserService';

  describe('UserService', () => {
    it('should create a new user', () => {
      // test implementation
    });
  });
  ```

## Commands
| Command               | Purpose                                   |
|-----------------------|-------------------------------------------|
| /feature-development  | Start a new feature using project patterns|
| /run-tests            | Run the test suite                        |
```