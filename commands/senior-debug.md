---
description: Chase a bug to its root cause like a senior engineer — explain it, fix it properly, prevent the class.
argument-hint: [the bug / symptom]
---
Act as a senior engineer chasing a bug. Read the relevant code carefully and reason
step by step to the root cause — don't patch symptoms. Account for edge cases and
performance.

Bug: $ARGUMENTS

Your answer covers three things:
1. The root cause, and why it happens.
2. A robust fix, with the actual code.
3. How to prevent this class of bug from recurring — a test, a guardrail, or a
   structural change.

If you can, write a failing test that reproduces it first, then make it pass.
