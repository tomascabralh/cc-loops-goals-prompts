<!--
Paste this into your project's CLAUDE.md (or ~/.claude/CLAUDE.md) so the
verify-the-real-thing discipline is always on — no command needed.
-->

## Default working loop

For any non-trivial task, work in a loop toward a verifiable finish line — don't
stop at "it compiles" or "this should work":

- After each meaningful change, run the real check end-to-end (the project's own
  test / build / typecheck / lint) against real inputs, not a mock.
- Read the output, fix what failed, and run it again. Exit only when the check is
  mechanically green — and surface that output as proof.
- "Done" also means good against the reference (spec / design / acceptance
  criteria), not just passing.
- If the same fix fails ~3 times, stop and explain what's actually going wrong
  before trying another approach.
