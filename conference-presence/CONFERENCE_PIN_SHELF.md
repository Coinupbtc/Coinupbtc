# Conference pin shelf — DRAFT

**Status:** DRAFT for Devil's Advocate review · **No PR, no merge.** Pins, descriptions, and topics are GitHub settings, so the owner applies them by hand. Nothing here changes them.

## Current pins (live, 2026-10-07)

`helix-qms-desk` · `miaai35-tune` · `MiniMax-H3-2x-DGX-Spark` · `spark-console` · `spark-pack` · `stl-sandbox`

These already match the floor set the DA cleared. **No pin swap needed.** Only the order changes, plus one-line descriptions for repos whose current description reads like a form.

`MiniMax-H3-1x-DGX-Spark` vs `-2x`: both are public. Pin **2×**. It carries the original engineering (RoCE bring-up) and the licence notice, while 1× is a 13-file launcher that depends on Joey's repo. 1× stays listed in the README.

## KEEP_HERO — proposed pin order

| # | Repo | Why it's pinned (one line) | Proposed GitHub description (if changing) |
|---|---|---|---|
| 1 | **miaai35-tune** | The single most defensible number on the profile: 35.80 tok/s from a committed JSON, with the faster unsaved lines explicitly refused. | *Keep:* "Measured llama.cpp flag-by-flag bakeoff — numbers instead of vendor claims." |
| 2 | **helix-qms-desk** | The best "I do quality systems" proof: a 90-second browser walk, synthetic plant, sticker ≠ certificate, IQ/OQ/PQ. | *Keep* (already a sentence). |
| 3 | **spark-console** | Shows ops discipline without a score to argue about: local, read-only, DNS-rebinding defence, tests. | *Keep:* "Local GPU and fleet health dashboard. One pane, no cloud." |
| 4 | **spark-pack** | "Will it fit?" in one screen. 121 GB per Spark, FITS / TIGHT / won't start. Prevents real hard-reboots. | "Plan models onto 1–3 DGX Sparks before you start them. 121 GB per Spark. FITS, TIGHT, or won't start." |
| 5 | **MiniMax-H3-2x-DGX-Spark** | Real distributed-systems work (RoCE GID, MTU, memlock), proved by output SHA. **Caveat out loud:** fork of Joey Rodriguez's recipe; model licence is territory-restricted. | *Keep* (already credits Joey and names the RoCE work). |
| 6 | **stl-sandbox** | Local prompt → STL/STEP with an inspection report and an honest "not AS9100" boundary. Ties CAD and AI back to quality. | "Plain-English prompt to printable STL and STEP, fully local, with a dimensional inspection report per part." |

Why this order: the DA floor script leads with "measured, not claimed" (miaai35-tune), then the quality day job (Helix). GitHub shows pins in a 2-column grid, so the first row (miaai35-tune and Helix) carries both stories at once.

## Demote / neutralize

| Repo | Today | Action | Why (one line) |
|---|---|---|---|
| **dream-stack** | Archived, public. Description *"Two-node NVIDIA GB10 inference: Dockerized vLLM TP=2 + llama.cpp roommate."*; topics `llama-cpp vllm llm-inference nvidia-dgx python shell`; homepage points to its own README. | **RETIRE wording.** Description → `RETIRED — see miaai35-tune. Archived for history; not maintained.` · remove all topics · homepage → `https://github.com/Coinupbtc/miaai35-tune`. If GitHub blocks About-box edits on an archived repo: unarchive → edit → re-archive. Stronger option: make it private (drops it from repo lists, search, and topic pages). | DA killer #1. The archived badge is small; the live-sounding description and topics make it look like current work in repo lists and topic search. |
| **build-a-boat** | Not pinned; in the README Quality table | Keep unpinned; README "Also" only | Owner: keep demoted. Good engineering hard stops, but marine electrical is off the conference story. |
| **zwell-bench** | Not pinned; README-listed | Keep unpinned; README Quality row with honest 14/15 wording | Strong method, but the headline result is a published miss. Better as a talking point than a pin card that leads with "15-check gate". |
| **MiniMax-H3-1x-DGX-Spark** | Not pinned; README-listed | Keep README-listed | A launcher on top of Joey's recipe. The 2× pin already carries the story. |
| **spark-training-lab** | Not pinned; README "Also" | **Remove from README** until scrubbed; never pin | Public files contain the owner's first name and unfiltered teacher outputs (audit P1 #1–2). |
| **coinupbtc-xyz** | Not pinned; public; linked from the site | Never pin. Follow-up: move `signals.html` and `signals-checkout.js` out of the public repo | Hosts paid perps-funding and fight-odds signal offers; must not be one click from the face. |
| **spark-ledger** | Archived; description already says "Archived museum…" | Leave as is | Already neutral and points to zwell-bench. |
| **teachers-book** | Not pinned | Keep unlisted | Off-topic for the conference story. |
| **bitcoin-blockfield**, **ordinookis** | Not pinned | Keep unlisted | Crypto and art toys stay off the conference face (DA #11). |
| **gravity-lander**, **falling-sand** | Not pinned | Keep unlisted (gravity-lander removed from the README "Also") | Toys. Fine buried, never heroed. |
| **Coinupbtc.github.io** | Site source | n/a | The site; see `SITE_HERO_GAPS.md`. |

## Follow-up fixes inside pinned repos (not this run)

| Pinned repo | Fix | Why |
|---|---|---|
| spark-pack | Update the "H3 on one Spark won't start" verdict (`js/pack.js:150-155`, README "Won't start" row) with an `as_of` date, now that `MiniMax-H3-1x-DGX-Spark` shows one-Spark H3 at 136.1 s (2026-09-05). | Two of your own listed repos contradict each other, and a curious reviewer will find it. |
| helix-qms-desk | Delete the literal `**GitHub description:** What: … For: … How: …` scaffolding line from the README (it also doesn't match the real description). | Internal template text in a hero README. |
| miaai35-tune | Add one sentence near the top of `REPORT.md` saying "bench_v5 is a separate 19-check personal harness, not zwell-bench's 15". | Stops the "19/19 vs 14/15" confusion before someone asks. |
| zwell-bench | README "What it's for" row: "A candidate ships only if every check passes" → "The bar is all 15 green; the published baseline is 14/15, so it does not pass." | Same honesty fix as the profile and site (DA killer #2). |
