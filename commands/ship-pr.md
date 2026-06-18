---
description: Finalize work into a clean PR — tidy the diff, run the checks, write the commit message and PR body.
argument-hint: [optional: PR title or focus]
---
Get this work ready to merge.

Context: $ARGUMENTS

1. Review the diff yourself first — remove debug code, stray logs, commented-out
   blocks, and anything unrelated to this change.
2. Run the real checks (test / build / typecheck / lint) and confirm they pass.
   Show the output. Don't proceed on red.
3. Write a commit message: one concise summary line, then a short body only if it
   adds something the diff doesn't.
4. Write a PR description: what changed and why, anything reviewers should look at,
   and how it was verified. Keep it tight.
5. Flag anything risky or deferred so it isn't a surprise in review.

Match the repo's existing commit and PR conventions. Don't push or open the PR
until I confirm.
