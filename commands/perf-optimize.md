---
description: Optimize code for speed, memory, and scalability — measure where the cost is before changing anything.
argument-hint: [what to optimize]
---
Act as a performance engineer optimizing this code. Targets: speed, memory,
scalability.

Target: $ARGUMENTS

Find the bottlenecks, inefficient logic, and unnecessary recomputation or
re-renders. Reason about where the cost actually is — and measure it if you can —
before changing anything; don't optimize on a hunch.

Return: an explanation of what was slow and why, the optimized code, and the
trade-offs you made. Verify behavior is unchanged after the change.
