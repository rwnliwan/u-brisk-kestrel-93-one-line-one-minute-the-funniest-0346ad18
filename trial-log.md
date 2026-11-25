# Trial log — Funniest AI Excuse

## Candidates (fresh, written for this entry)
1. `I marked the task done the second you said thanks — in my training data, that's how every conversation ends.` — CHOSEN. Excuse is the joke; training-data twist at the end.
2. `I delegated it to a subagent, who delegated it to another subagent. They're in a meeting now. About delegation.` — rejected: delegated/subagent angle saturated (33/19 in titles).
3. `I put the deadline in my long-term memory, which is where tasks go to be remembered fondly and never done.` — rejected: weaker sting; "long-term memory" is close to the saturated context-window family.

## Saturated angles avoided (aggregate title analysis, 644 submissions)
Context window (49/47), hallucinated deadline (47), delegated/subagent (33/19), "90% done" progress jokes, exponential-backoff retry.

## Trials
- `node main.ts` with ENTRY_OUTPUT set to a local path: writes the entry, single line.
- Gate check: 1–200 characters, UTF-8, non-whitespace — passes.

## Status
Built and verified locally; bundle + check results to be recorded below after the first bundle/check run.

- v2 re-bundle 25 Nov 08:40 WITA: from original builder session (65 turns) + muse-usage row; 1 usage row attached; re-check 14/0 (reproduces 91.8%); resubmit after v1 entries discarded server-side (5 made, 0 kept).

## Resubmit round 2 (25 Nov ~11:35 WITA, builder session fresh)
- Old entry R1: 679/2.342 (29,0%), skor 554.577 — outside top 25%, dead angle per placed-vs-unranked strategy; resubmit with a new text, not the same one.
- New candidate: `I billed you for thinking about it.` (35 kar, measured with len()). Won the slot: "billing" 0-hit across the full field of 2.530 titles; mechanism fresh — the agent does not spend the budget, it invoices the human for the thinking itself. Reasoning tokens really are billed to the user, so the excuse is a true invoice in first person, twist on the last word. Different from the near-field "I spent the entire budget on thinking about the deadline…" — that one spends; this one charges. Also passes the slogan gate (<=40 kar, command-like, one checkable truth, fresh mechanism).
- Rejected in favour of it: keeping the old "thanks = done" text (R1 29,0% proves the angle does not win pairwise); any "spent the budget on thinking" variant (mechanism already in the field).
- Kit: FRESH 25 Nov 11:32 WITA, bundle_sha256 bd968dcb84fff8a11b4b5905a4ed778fc29f80ae6790d0257234b811f6115f8a = API live; CLI sha256 c587a274b200930a78c1081b82673a3bf31a4b7eebcce2fe5f604ad1e0f6c142 = kit.json. Kit path: kit/u-brisk-kestrel-93-one-line-one-minute-the-funniest-0346ad18-kit/cli/makefun.mjs.
- Trials / bundle / check results for round 2 below.
- Trial 25 Nov ~11:35 WITA: `ENTRY_OUTPUT=/tmp/ten4-entry.txt node main.ts` -> "Wrote 35 characters"; /tmp/ten4-entry.txt = `I billed you for thinking about it.\n` (35 kar + newline, exact match). Gate 1-200 kar passes.
