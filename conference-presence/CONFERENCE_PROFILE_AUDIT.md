# Conference profile audit — github.com/Coinupbtc

**Date:** 2026-10-07 · **Status:** DRAFT for Devil's Advocate review · **No PR, no merge.**
**Scope:** what a hiring manager sees in the first 30 seconds on the GitHub profile today, checked against the public repos (shallow clones on 2026-10-07) and the live URLs.
**Alias only.** This pack uses Coinupbtc / Coin Up. It quotes no number that a committed README or results file does not support.

---

## 1. The 30-second read, as it stands

A hiring manager lands on `github.com/Coinupbtc` from a badge QR code or a business card. In order, they see:

| Order | What they see | Read | Verdict |
|---|---|---|---|
| 1 | Sidebar: name `Coinupbtc`, bio *"Quality systems engineer. ISO 13485, CAPA, metrology. On-prem inference with measured gates."*, `St.Louis , MO`, `coinupbtc.com`, X `@CoinUpBTC`, `coinupbtc@gmail.com`, **Hireable**, 4 followers | Clear role and domain. The location has a stray space and comma. The X field shows `CoinUpBTC`, while the owner's public handle is **@coinupbtc** and every site and meta surface writes it in lowercase. X handles are case-insensitive, so the link works, but the profile is the one place that disagrees. | **Fix** (X field case, location typo) |
| 2 | README line 1: *"Quality systems. On-prem inference. Measured, not claimed."* | Good hook, but no "who / what role / why hire". It's a slogan, not a sentence. | **Rewrite** |
| 3 | README hero: Helix QMS Desk with a working Pages link | The strongest hiring asset. Opens in under 90 seconds; Pages returns 200. | **Keep** |
| 4 | "Quality & systems" table: helix, **build-a-boat**, zwell-bench | build-a-boat sits at hero level although the owner wants it demoted. zwell row says *"A build ships only if every check passes"*, then *"14 of 15"* in the next sentence. A sharp reader asks whether it shipped. | **Demote build-a-boat; reword zwell** |
| 5 | "On-prem inference" table: miaai35-tune 35.80 tok/s, spark-console, H3 2×, H3 1× | The numbers are honest and dated. The H3 rows don't mention the model licence, and the H3 2× row doesn't credit Joey Rodriguez in the README (the repo itself does). | **Keep, add credit + licence line** |
| 6 | "Also": gravity-lander, stl-sandbox, spark-training-lab | stl-sandbox is a pinned hero but appears here as an "also". spark-training-lab has public-data problems (section 3). | **Reorder; drop training-lab until scrubbed** |
| 7 | Closing line: *"If it cannot be run this week, it is not listed."* | Too absolute. Both H3 repos need two (or one) DGX Sparks, the FL2VA weights, and a model licence that excludes the US. Most visitors cannot run them this week. | **Rewrite** |
| 8 | Pinned shelf (6) | helix-qms-desk, miaai35-tune, MiniMax-H3-2x-DGX-Spark, spark-console, spark-pack, stl-sandbox. **Already matches the target floor set.** | **Keep set; reorder** (see `CONFERENCE_PIN_SHELF.md`) |

**Honest 30-second summary today:** *"Quality engineer who also runs serious local AI hardware and publishes real, dated numbers — but I'm not sure which job they want, and a couple of lines read like slogans that their own results contradict."* That's a conditional pass. The substance is there; the framing and three or four loose ends cost credibility.

---

## 2. What is actually strong (verified)

| Claim on the face | Evidence checked | Holds? |
|---|---|---|
| miaai35-tune **35.80 tok/s** coding decode, 9 July 2026, thinking off, speculative decode off | `results/bench-original-rerun-think-off-20260709-203311.json`: `tokens_per_sec: 35.8`, `predicted_per_second: 35.80288970455151`. `RESULTS.md` states the same conditions (ORIGINAL profile, clean restart). | **Yes** |
| Same run is a ~35–38 tok/s band | RESULTS.md: short 38.23 · reasoning 35.29 · long 35.45; coding quality 9/10 | **Yes** |
| zwell-bench: 15 checks, 16 July 2026 run 14/15 | README + committed `results/miaai35-v8-baseline.json`: 14/15, weighted 95.0, failed `agentic/schedule_math`. No committed run is 15/15. | **Yes** (the slogan is the problem, not the data) |
| H3 2× RoCE: 55.5 s warm, SHA-identical to Socket TCP eager (90.5 s) | MiniMax-H3-2x README §"GB10 CX7 RoCE", 2026-09-04; repeat 58.4 s | **Yes** |
| H3 1×: same seed-42 SHA as 2× IB, slower | MiniMax-H3-1x README: 136.1 s warm vs 55.5 s, SSIM 1.0, 2026-09-05 | **Yes** |
| Helix QMS Desk opens in the browser | `https://coinupbtc.github.io/helix-qms-desk/` → 200. CI green (2026-09-02). | **Yes** |
| spark-console is local and read-only | README: binds 127.0.0.1, `Host` allowlist (DNS rebinding), `Origin` check on writes, no start/stop routes, pytest suite. CI green. | **Yes** (and under-sold; security is a hiring signal) |
| stl-sandbox works offline for primitives | README + CI green (2026-10-05). Explicitly "not AS9100 / flight / NADCAP". | **Yes** |

**Under-sold:** the profile never says *why* these repos belong together. The through-line, written in each README but never on the profile, is **"presence is not integrity."**
- Helix treats HTTP 200 with empty content as a failed check.
- zwell publishes its own miss.
- miaai35-tune refuses to quote its unsaved 169.4 t/s line.
- H3 proves quality by SHA, not by eye.

That's a quality engineer's habit applied to AI infrastructure, and it is the hiring story.

---

## 3. Problems a hiring manager (or a DA) will find by clicking once

Ranked by damage.

### P1 — Public exposure risks (fix before the conference)

1. **The owner's first name appears in five public files in `spark-training-lab`.** It shows up as a style label ("…in [first name]'s short ops style") in:
   - `docs/first-lora-plan.md` (line 4)
   - `datasets/distill_task_pack_v1.jsonl` (line 22)
   - `datasets/continuous/glm52-teacher-20260727-140033.jsonl` (line 22)
   - `datasets/continuous/ds4f-20260727-223634.jsonl` (line 22)
   - `datasets/continuous/ds4f-combined-20260727-231210.jsonl` (line 1054)

   The surname appears nowhere (searched all 16 cloned public repos). A first name next to a city and an employer-type bio is still an identity bridge. The current profile README links this repo under "Also". **Action:** drop it from the README now. Then scrub the files (rewriting history if the owner wants it fully gone) or make the repo private.
2. **`spark-training-lab` publishes degenerate teacher outputs as training data.** For example, `glm52-teacher-…jsonl` contains a bash answer that collapses into hundreds of `&&` tokens, and a curl answer with invented flags. A reviewer who opens the dataset sees unfiltered garbage labelled as distillation data. That undercuts "measured, not claimed". It also names a GLM teacher model. That isn't a live-serving claim, but it invites the question. **Action:** same as above; keep the repo off the face.
3. **The live trading/betting product is one click from the homepage.** `coinupbtc.com` → nav "Lab" → `coinupbtc.xyz`. The `.xyz` repo (`Coinupbtc/coinupbtc-xyz`, public) and the live domain both serve `signals.html`, which returns 200. It sells:
   - perps funding signals and a DeFi yield digest ($5–$9/mo, Telegram)
   - a UFC "model fair odds vs book lines, Polymarket" feed

   `robots.txt` disallows the page, but the source is public and the URL is guessable. The homepage card for the lab says *"No account. No checkout."*, which `signals-checkout.js` contradicts. This breaks the "no traders / live betting as public face" constraint. Not on the GitHub profile itself, but reachable from it. **Action:** see `SITE_HERO_GAPS.md` §2.
4. **MiniMax H3 licence vs. where the owner says they are.** The H3 2× repo's own `MODEL-LICENSE.md` summarises the Community License as excluding the United States, EU, UK and Republic of Korea, and says that "using, reproducing, modifying, distributing, or displaying the model or its outputs outside that applicable territory is not authorized". The GitHub location says St. Louis, MO. `coinupbtc.com` autoplays an H3 clip as the hero backplate and shows an eight-clip H3 gallery; the social-card image also appears to use an H3 frame. Pinning the H3 repos is defensible (they ship no weights and no media, and they warn loudly). The site displaying outputs is a different matter. **This needs an owner decision (and possibly MiniMax authorization or legal advice) before a conference that drives traffic to the site.** I am not giving legal advice. I'm flagging that the repo's own text and the site's behaviour disagree, and a sharp reviewer will notice.

### P2 — Credibility leaks (fix in the profile README pass)

5. **dream-stack still reads as live.** It's archived and absent from the README and pins (good). But its GitHub description is *"Two-node NVIDIA GB10 inference: Dockerized vLLM TP=2 + llama.cpp roommate."*, its topics are `llm-inference`, `vllm`, `nvidia-dgx`…, and its README hero alt text is "Tool-eval-bench 69 on 2× DGX Spark". It surfaces in topic search and the repo list, and it reads like current work. **Action:** set the description to `RETIRED — see miaai35-tune. Archived for history; not maintained.`, remove the topics, and point the homepage at miaai35-tune. If GitHub blocks About-box edits on an archived repo: unarchive → edit → re-archive. Alternative: make it private. (DA killer #1.)
6. **X handle drift.** The owner's ruling (2026-10-07) is that the public handle is **@coinupbtc** everywhere. This overrides the DA roast's alternate handle, which must not appear in any copy. Here is where things stand:
   - The site and lab already use `@coinupbtc` / `x.com/coinupbtc` in **19 places** (list in `SITE_HERO_GAPS.md` §1), and the social-card PNG shows `x.com/coinupbtc`. All correct; no change needed.
   - **The GitHub profile `twitter_username` is `CoinUpBTC`.** It's the only surface with different casing. The link resolves, but the sidebar shows a different-looking handle from the site, card, and README.
   - The current profile README doesn't mention X at all.

   **Action:** set the GitHub profile X field to `coinupbtc` (a manual settings change by the owner), and use `@coinupbtc` / `https://x.com/coinupbtc` in the proposed README. I did not query X to confirm the account. (DA killer #3, as restated by the owner.)
7. **The gate slogan contradicts the gate's own result.** "A build ships only if every check passes", followed immediately by "14 of 15", appears in the profile README (zwell row), the site card (`index.html:183`), and the zwell README "What it's for" row. Reword to: *"The bar is all 15 green. The published 16 July 2026 baseline is 14/15, so by its own rule it does not pass."* (DA killer #2. The site line is handed to the follow-up agent in `SITE_HERO_GAPS.md` §3; the proposed README already uses the honest wording.)
8. **The gate and the headline number come from different configurations; don't let them blur.** The zwell run is tag `miaai35-v8-baseline` (16 July). The 35.80 tok/s figure is the ORIGINAL profile (9 July). No public file shows the 35.80 configuration going through the 15-check gate. **Gap:** don't write "35.80 tok/s and passed the gate". The proposed README keeps them in separate rows.
9. **"19/19" ghost.** `miaai35-tune/REPORT.md` (lines ~361, 394, 420) reports "19/19 on bench_v5". That's a *different*, 19-check personal harness, not zwell's 15. The archived spark-ledger also says "bench_v5 19/19". Someone who reads REPORT then zwell ("not 19/19") will think the numbers conflict. **Action (follow-up, not this run):** add one sentence near the top of REPORT.md naming bench_v5 as a separate harness. On the floor: never say "19/19".
10. **Pinned repos disagree about H3 on one Spark.** `spark-pack` (last commit 2026-08-13), `js/pack.js:150-155`: *"H3 wants both Sparks … the worker never comes up."*; the README's "Won't start" row says "H3 on one Spark". `MiniMax-H3-1x-DGX-Spark` (2026-09-05) shows H3 running on one Spark in 136.1 s with an identical SHA. Both are pinned or listed. **Action (follow-up):** update spark-pack's verdict and catalog row with an `as_of` date (the README promises every row has one).

### P3 — Polish

11. Helix and build-a-boat READMEs contain a literal `**GitHub description:** What: … For: … How: …` line, which is internal scaffolding showing in the README. Helix's line also doesn't match its real GitHub description.
12. Several GitHub descriptions use the `What: … For: … How: …` template (spark-pack, stl-sandbox, the H3 1× repo). In a pin card that reads like a form, not a sentence. Proposed one-liners are in `CONFERENCE_PIN_SHELF.md`.
13. The site's spark-console card shows "**121** GB" as its badge. 121 GB is per-Spark hardware, not a spark-console feature, and "per Spark" is missing (spark-pack is careful about this; the site isn't).
14. The profile README has no "open to" line and no résumé or contact path except the homepage. That's fine for pseudonymity, but a recruiter needs *one* obvious next step.

---

## 4. Hard-constraint check on today's public face

| Constraint | Profile README | Pins | Site (`coinupbtc.com`) | One click out |
|---|---|---|---|---|
| Legal name absent | ✅ | ✅ | ✅ | ⚠️ first name in `spark-training-lab` (linked from README "Also") |
| dream-stack not heroed | ✅ removed in #3 | ✅ | ✅ | ⚠️ live-sounding archived description and topics |
| No live-GLM serving claim | ✅ | ✅ | ✅ | ⚠️ GLM teacher datasets in `spark-training-lab` (data, not a serving claim) |
| No traders / betting as face | ✅ | ✅ | ✅ on page | ❌ `coinupbtc.xyz/signals.html` live, public repo, linked via "Lab" |
| No invented benchmarks | ✅ | ✅ | ⚠️ gate slogan | ⚠️ "19/19" in REPORT (different harness) |
| One X handle (`@coinupbtc`) | ⚠️ profile field `CoinUpBTC` (case drift); README has none | n/a | ✅ `@coinupbtc` ×19 + PNG | ✅ lab uses `@coinupbtc` |

The proposed drafts in this folder fix every ❌/⚠️ that lives on the **profile** surface. Site and other-repo fixes are listed for a follow-up agent; this run doesn't edit them.
