---
description: Drive a task to a verified finish line — implement, run the real check, fix, repeat until green.
argument-hint: [task or spec]
---
Goal: $ARGUMENTS

Keep going until both the implementation and the result clear the bar — not just
until it compiles or runs. Loop, don't single-pass:

1. Implement the next meaningful slice.
2. Run the real check end-to-end — real inputs, real data, the actual flow, not a
   mock (use the project's own test / build / typecheck / lint).
3. Read the output. Fix what failed. Run it again.

Exit only when the check is mechanically, visibly green — e.g. tests exit 0 and
the typecheck reports 0 errors — and surface that output as proof each round.
"Green" also means good against the reference (design / example / acceptance
criteria), not just passing: a result that passes the checks but is useless
doesn't count.

Guardrails:
- Don't change unrelated behavior or break a contract while fixing.
- If the same fix fails ~3 times, stop thrashing: step back, explain what's
  actually going wrong, and ask before trying a different approach.
- Safety cap: stop after ~10 rounds and report what's left if it isn't green.
