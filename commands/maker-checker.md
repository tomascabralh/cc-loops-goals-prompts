---
description: Maker-checker loop. One pass writes, a separate fresh-eyes pass reviews, and only what passes gets integrated.
argument-hint: [task or spec]
---
Run this as a maker-checker loop, not a single pass. A writer that grades its own
homework misses its own bugs.

Task: $ARGUMENTS

For each independent unit:
1. Maker: write the code.
2. Checker (fresh eyes, ideally a separate subagent with its own context): verify
   it against the spec, tests, types, and lint. Don't trust the maker's
   self-assessment.
3. If review fails, feed the specific failures back and redo the unit.
4. Only integrate once it passes review and the real flow runs.

Keep a short running log of what's been tried, what passed, and what's still open,
so nothing repeats a dead end. Isolate parallel units (separate git worktrees) so
they never edit the same files at once.

Keep looping until every unit is integrated, the full end-to-end flow passes, and
a final review is clean. Surface blocking decisions; otherwise run to completion.
Hard cap: stop after about 10 rounds and report status.

In Claude Code, use separate subagents for maker and checker. The separate context
windows are what let one catch the other's bugs.
