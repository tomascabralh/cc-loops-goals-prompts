---
description: Plan the whole task end-to-end, then execute it — parallelize independent units and verify each.
argument-hint: [task or spec]
---
Write yourself an end-to-end plan for this, then execute the whole thing — not
just the next step — until architecture, implementation, tests, and a self-review
all meet the bar.

Task: $ARGUMENTS

- Break the work into independent units; parallelize the ones that don't depend on
  each other, and isolate them so two never edit the same files at once.
- After each unit, run the real flow end-to-end to verify it before integrating —
  real inputs, real data, not a mock.
- Keep a short running log of what's done, what passed, and what's still open.
- Surface blocking decisions to me; otherwise keep going to completion.

In Claude Code: give true-parallel units their own git worktrees so they don't
collide. Stop and report if a unit can't reach green after a few attempts.
