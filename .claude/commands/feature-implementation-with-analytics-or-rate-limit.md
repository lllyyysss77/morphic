---
name: feature-implementation-with-analytics-or-rate-limit
description: Workflow command scaffold for feature-implementation-with-analytics-or-rate-limit in morphic.
allowed_tools: ["Bash", "Read", "Write", "Grep", "Glob"]
---

# /feature-implementation-with-analytics-or-rate-limit

Use this workflow when working on **feature-implementation-with-analytics-or-rate-limit** in `morphic`.

## Goal

Implements or updates a feature related to chat limits or analytics, then follows up with analytics tracking and/or bugfixes for event delivery.

## Common Files

- `lib/rate-limit/chat-limits.ts`
- `lib/analytics/index.ts`
- `lib/analytics/track-chat-limit-event.ts`
- `lib/rate-limit/__tests__/*.ts`
- `lib/rate-limit/adaptive-limit.ts`

## Suggested Sequence

1. Understand the current state and failure mode before editing.
2. Make the smallest coherent change that satisfies the workflow goal.
3. Run the most relevant verification for touched files.
4. Summarize what changed and what still needs review.

## Typical Commit Signals

- Implement or update chat limit logic in lib/rate-limit/chat-limits.ts
- Add or update analytics event tracking in lib/analytics/*
- Fix or improve event delivery and test coverage in related files

## Notes

- Treat this as a scaffold, not a hard-coded script.
- Update the command if the workflow evolves materially.