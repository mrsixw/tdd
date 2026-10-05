---
name: tdd
description: Build a feature or fix whose desired behaviour is known, test-first, using a red-green-refactor loop, vertical slices, and behaviour-focused tests. Use when the user asks for test-first or TDD development. Not for bugs whose cause is still unknown (start with diagnose-bug).
---

# Test-driven development

Use a red-green-refactor loop to deliver one observable behaviour at a time.
Follow the repository's existing test layout and prefer its documented task
runner or validation commands over introducing new tooling. When a bug's cause
is still unknown, start with `diagnose-bug`.

## Work in vertical slices

1. Choose the highest useful existing seam and state the behaviour in user or
   caller terms. `boundary-testing` identifies that seam and the systems to
   replace beyond it; follow it for the shape of every test in this loop.
2. Add one independent test and run it. Record why it failed so a syntax error,
   fixture problem, or unrelated failure is not mistaken for red.
3. Add only the production code required to make that behaviour green.
4. Run the focused test and nearby regression checks.
5. Refactor names, duplication, and boundaries while keeping the behaviour
   green and the public seam stable.
6. Repeat for the next required behaviour.

`boundary-testing` governs what each test drives and what it fakes. Beyond it,
do not add test-only production interfaces or speculative behaviour, and do not
batch-write the full test suite before producing the first green slice.

## Verify the result

Run the repository's complete applicable validation before completion. Report
the red evidence, green evidence, full checks run, and any check that could not
be run. A test that never demonstrated the intended failure does not establish
the regression guard.
