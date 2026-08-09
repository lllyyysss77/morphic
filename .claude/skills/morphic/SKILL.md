```markdown
# morphic Development Patterns

> Auto-generated skill from repository analysis

## Overview
This skill covers the core development patterns, coding conventions, and workflows used in the `morphic` TypeScript codebase. The repository focuses on features such as chat rate limiting, analytics event tracking, and streaming responses, with a strong emphasis on test coverage and maintainable code structure. The following guidelines and workflows will help you contribute effectively and consistently.

## Coding Conventions

### File Naming
- Use **kebab-case** for all file names.
  - Example: `chat-limits.ts`, `create-chat-stream-response.ts`

### Import Style
- Mixed import styles are used. Both named and default imports may appear.
  - Example:
    ```typescript
    import { trackEvent } from './analytics/track-chat-limit-event';
    import adaptiveLimit from './rate-limit/adaptive-limit';
    ```

### Export Style
- Prefer **named exports**.
  - Example:
    ```typescript
    // lib/analytics/track-chat-limit-event.ts
    export function trackChatLimitEvent(...) { ... }
    ```

### Commit Message Patterns
- Prefix with `feat` for new features and `fix` for bug fixes.
- Keep commit messages concise (average ~56 characters).
  - Example: `feat: add adaptive chat rate limit`

## Workflows

### Feature Implementation with Analytics or Rate Limit
**Trigger:** When adding or modifying a chat limit feature and ensuring it is tracked and delivered correctly in analytics.  
**Command:** `/update-chat-limit-feature`

1. Implement or update chat limit logic in `lib/rate-limit/chat-limits.ts`.
2. Add or update analytics event tracking in `lib/analytics/*`.
3. Fix or improve event delivery and test coverage in related files.

**Files Involved:**
- `lib/rate-limit/chat-limits.ts`
- `lib/analytics/index.ts`
- `lib/analytics/track-chat-limit-event.ts`
- `lib/rate-limit/__tests__/*.ts`
- `lib/rate-limit/adaptive-limit.ts`

**Example:**
```typescript
// lib/rate-limit/chat-limits.ts
export function setChatLimit(userId: string, limit: number) { ... }

// lib/analytics/track-chat-limit-event.ts
export function trackChatLimitEvent(userId: string, limit: number) { ... }
```

---

### Feature Refactor with Test Update
**Trigger:** When refactoring, optimizing, or changing core logic and ensuring it is covered by tests.  
**Command:** `/refactor-feature-with-tests`

1. Refactor or optimize core logic in implementation files.
2. Update or add corresponding test files in `__tests__` directories.

**Files Involved:**
- `lib/streaming/helpers/*.ts`
- `lib/streaming/create-chat-stream-response.ts`
- `lib/streaming/create-ephemeral-chat-stream-response.ts`
- `lib/streaming/__tests__/*.test.ts`
- `lib/agents/title-generator.ts`
- `lib/agents/__tests__/title-generator.test.ts`

**Example:**
```typescript
// lib/streaming/create-chat-stream-response.ts
export function createChatStreamResponse(...) { ... }

// lib/streaming/__tests__/create-chat-stream-response.test.ts
import { createChatStreamResponse } from '../create-chat-stream-response';
import { describe, it, expect } from 'vitest';

describe('createChatStreamResponse', () => {
  it('should return a valid response', () => {
    // test implementation
  });
});
```

## Testing Patterns

- **Framework:** [vitest](https://vitest.dev/)
- **Test File Pattern:** Files end with `.test.ts` and are located in `__tests__` directories or alongside implementation files.
- **Test Example:**
  ```typescript
  // lib/rate-limit/__tests__/chat-limits.test.ts
  import { setChatLimit } from '../chat-limits';
  import { describe, it, expect } from 'vitest';

  describe('setChatLimit', () => {
    it('sets the chat limit for a user', () => {
      // test logic
    });
  });
  ```

## Commands

| Command                        | Purpose                                                        |
|--------------------------------|----------------------------------------------------------------|
| /update-chat-limit-feature     | Add or update chat limit features and analytics tracking        |
| /refactor-feature-with-tests   | Refactor core logic and update or add corresponding tests       |
```
