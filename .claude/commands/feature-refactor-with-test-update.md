---
name: feature-refactor-with-test-update
description: Workflow command scaffold for feature-refactor-with-test-update in morphic.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /feature-refactor-with-test-update

Use this workflow when working on **feature-refactor-with-test-update** in `morphic`.

## Goal

Refactors or optimizes a core feature and updates or adds corresponding tests to ensure correctness.

## Common Files

- `lib/streaming/helpers/*.ts`
- `lib/streaming/create-chat-stream-response.ts`
- `lib/streaming/create-ephemeral-chat-stream-response.ts`
- `lib/streaming/__tests__/*.test.ts`
- `lib/agents/title-generator.ts`
- `lib/agents/__tests__/title-generator.test.ts`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Refactor or optimize core logic in implementation files
- Update or add corresponding test files in __tests__ directories

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.