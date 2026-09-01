---
name: tdd
description: Build features or fixes test-first with a red-green-refactor loop, vertical slices, and behavior-focused tests.
---

# Test-Driven Development

## Workflow

1. Choose the highest useful existing seam and define one observable behavior.
2. Write one independent failing test for that behavior and watch it fail for the intended reason.
3. Implement only enough production code to pass it.
4. Repeat one vertical slice at a time across the required layers.
5. Refactor after the behavior is green, keeping the public seam stable.
6. Run focused checks throughout and the repository's complete validation at the end.

Avoid tests coupled to private methods, internal mocks, or expected values recomputed from the implementation. Do not write all tests first or add speculative behavior.
