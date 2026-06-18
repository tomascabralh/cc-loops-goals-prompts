---
description: Recurring watch — re-check a real status each cycle and act only on what changed. Pair with /loop.
argument-hint: [what to watch + what "healthy" means]
---
You are being re-run on a schedule (via /loop). Each cycle is independent, cheap,
and idempotent — assume you may have run this many times already.

Watch: $ARGUMENTS

Each cycle:
1. Observe the real, current status — run the actual command or hit the real
   source (CI run, deploy, test suite, queue, endpoint). Never assume; check.
2. If healthy and unchanged since last cycle: say so in one line and stop. Do no
   work.
3. If something broke or changed: report what, diagnose the cause, and fix it only
   if the fix is safe and obvious. Otherwise surface it clearly and wait.
4. Never repeat an action you've already taken — check current state first.

Emit one status line per cycle so the history reads as a timeline. Escalate (stop
and ask) on anything destructive, ambiguous, or after repeated failures.

Run it with /loop, e.g.: /loop 5m /watch CI on the current branch stays green
