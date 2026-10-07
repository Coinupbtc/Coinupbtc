# Proposed profile README — DRAFT

**Status:** DRAFT for Devil's Advocate review · **No PR, no merge.** `README.md` at the repo root is untouched.
**How to use:** everything between the two `COPY` markers is the full proposed `README.md`. The notes below the second marker are for reviewers and are not part of the README.

---

<!-- ===== COPY START ===== -->

**Quality systems engineer** — ISO 13485, CAPA, metrology, validation (IQ/OQ/PQ).
I also run AI models on my own hardware, and I hold them to the rule I use on a plant floor: **presence is not integrity.** A green light, an HTTP 200, or a fast number only counts if there is a file behind it.

**Start here**

- **Hiring for quality or validation?** Open **[Helix QMS Desk](https://coinupbtc.github.io/helix-qms-desk/)**: a 90-second walk through a fictional biomedical plant, in your browser.
- **Hiring for on-prem AI or inference ops?** Read **[miaai35-tune → RESULTS](https://github.com/Coinupbtc/miaai35-tune/blob/main/RESULTS.md#primary-coding-decode-9-july-2026)**: 35.80 tok/s, copied from a committed results file.

[coinupbtc.com](https://coinupbtc.com) · X [@coinupbtc](https://x.com/coinupbtc)
<!-- OWNER CONFIRM before publish — optional line, supported by helix-qms-desk's own "For:" row:
Open to Senior Quality Engineer, Supplier Quality, and validation roles, and to on-prem AI operations work.
-->

---

### Quality systems

| Repo | What it shows |
|------|---------------|
| **[helix-qms-desk](https://github.com/Coinupbtc/helix-qms-desk)** | An interactive ISO 13485 quality desk for a fictional plant: a calibration sticker that disagrees with its certificate, a CAPA 8D, supplier SCARs, an ISO 14971 risk that got *worse* after a "control", and IQ/OQ/PQ run against the desk itself. All records are synthetic. [Open it in the browser](https://coinupbtc.github.io/helix-qms-desk/). |
| **[zwell-bench](https://github.com/Coinupbtc/zwell-bench)** | A 15-check release gate for local AI models: executed coding tests, exact JSON extraction, vision reads, tool choice, and agentic ordering. The bar is all 15 green. The published 16 July 2026 baseline scored **14 of 15** (weighted 95.0; missed `schedule_math`), so by its own rule it does not pass. The miss is published, not hidden. |
| **[stl-sandbox](https://github.com/Coinupbtc/stl-sandbox)** | A plain-English prompt becomes a printable STL and a STEP file, fully local. Each mechanical part gets an ISO 2768-style dimensional inspection report. The README states that this is not AS9100 qualification. |

### On-prem inference

Two NVIDIA DGX Sparks on a desk. Weights stay local.

| Repo | What it shows |
|------|---------------|
| **[miaai35-tune](https://github.com/Coinupbtc/miaai35-tune)** | A flag-by-flag llama.cpp bakeoff for Qwen3.6-35B-A3B. Headline: **35.80 tok/s** coding decode on 9 July 2026 (thinking off, speculative decode off, clean restart), copied from a [committed results file](https://github.com/Coinupbtc/miaai35-tune/blob/main/results/bench-original-rerun-think-off-20260709-203311.json). Faster figures in the lab log that have no saved file are not quoted. |
| **[spark-console](https://github.com/Coinupbtc/spark-console)** | One local page for GPU, memory, model, and service health. Binds to localhost, blocks DNS-rebinding and cross-origin writes, never starts or stops anything, never phones home. `./setup.sh` → `:8085` |
| **[spark-pack](https://github.com/Coinupbtc/spark-pack)** | Plan which models fit on 1–3 Sparks *before* you start them. 121 GB is per Spark, not one shared pool. The verdict is FITS, TIGHT, or won't start. |
| **[MiniMax-H3-2x-DGX-Spark](https://github.com/Coinupbtc/MiniMax-H3-2x-DGX-Spark)** | A public fork of [Joey Rodriguez's](https://github.com/joeynyc/MiniMax-H3-2x-DGX-Spark) two-Spark video-model recipe. My addition is the RoCE network bring-up, so both machines use the fast link instead of falling back to TCP. Same clip: 90.5 s → **55.5 s** warm, output SHA identical. |
| **[MiniMax-H3-1x-DGX-Spark](https://github.com/Coinupbtc/MiniMax-H3-1x-DGX-Spark)** | A one-Spark launcher for the same quality profile, built on Joey's one-Spark recipe. Same output SHA as the two-Spark clip, 136.1 s warm. |

MiniMax H3 weights and outputs are covered by MiniMax's own territory-restricted Community License, not by these repos' code licences. The repos ship no weights and no generated media. Read that licence before you run them.

`miaai35-tune` credits [MiaAI Labs' Qwen3.6-35B Spark recipe](https://github.com/MiaAI-Lab/Qwen3.6-35B-A3B-UD-Q8_K_XL_DGX-Spark-Recipe) for its serving baseline.

### Also

[build-a-boat](https://github.com/Coinupbtc/build-a-boat): a fictional marine electrical package whose voltage-drop and AC/DC checks fail before a drawing can pass. [Open it in the browser](https://coinupbtc.github.io/build-a-boat/).

Every repo above has a **Try it** section, and each one states the hardware it needs at the top.

<!-- ===== COPY END ===== -->

---

## Reviewer notes (not part of the README)

### Claim ledger — every number in the copy, and its source

| Number in copy | Source file (public) | Checked 2026-10-07 |
|---|---|---|
| 35.80 tok/s, 9 July 2026, thinking off, spec decode off, clean restart | `miaai35-tune/results/bench-original-rerun-think-off-20260709-203311.json` (`tokens_per_sec: 35.8`, `predicted_per_second: 35.8029`); conditions in `RESULTS.md` | ✅ |
| 15 checks; 14 of 15; weighted 95.0; missed `schedule_math`; 16 July 2026 | `zwell-bench/README.md`, `results/miaai35-v8-baseline.json` | ✅ |
| 90 seconds (Helix walk) | `helix-qms-desk/README.md` "Monday path (90 seconds)" | ✅ (author's estimate, not a measurement) |
| 121 GB per Spark; 1–3 Sparks; FITS / TIGHT / won't start | `spark-pack/README.md` | ✅ |
| 90.5 s → 55.5 s warm, SHA identical | `MiniMax-H3-2x-DGX-Spark/README.md` §"GB10 CX7 RoCE (this fork, 2026-09-04)" | ✅ |
| 136.1 s warm, same SHA | `MiniMax-H3-1x-DGX-Spark/README.md`; 2× README §"One Spark, same quality SHA" | ✅ |
| ISO 2768-style inspection; not AS9100 | `stl-sandbox/README.md` §"ISO-style inspection" | ✅ |
| `:8085`; localhost bind; DNS-rebinding / Origin defences | `spark-console/README.md` §Security | ✅ |
| "Two NVIDIA DGX Sparks" | H3 2× measured topology; site photo | ✅ |

**Deliberately not quoted:**
- 169.4 t/s (no saved file; the repo itself says not to quote it).
- 68.69 tok/s (saved, but speculative decode is on — a different setup; fine in conversation, not as a headline).
- "19/19" (a different, 19-check harness inside miaai35-tune's REPORT.md).
- The 46.6 s H3 figure (Joey's August acceptance run, not this fork's).
- dream-stack's "69" tool-eval score (retired repo).

**Gap — do not paper over:** the zwell 14/15 run is tag `miaai35-v8-baseline` (16 July). The 35.80 tok/s figure is the ORIGINAL profile (9 July). No public file shows the 35.80 configuration going through the 15-check gate. The copy keeps them in separate rows and never says "35.80 and gated".

### What changed vs. the current README, and why

| Change | Why |
|---|---|
| Opening slogan → one plain sentence on role and method | A recruiter needs "who / what job" in the first line. "Presence is not integrity" comes from Helix's own README and ties the QMS and AI work together. |
| Added a two-door "Start here" (quality vs. on-prem AI) | Conference traffic is mixed. Route each reader to the one link that matters to them. |
| zwell: "ships only if every check passes" → "the bar is all 15 green … does not pass" | Removes the slogan that its own published 14/15 contradicts (DA killer #2). |
| stl-sandbox moved from "Also" into Quality systems | It's a pinned hero, and its inspection-report-with-honest-boundary fits the quality story. |
| build-a-boat moved from the Quality table to "Also" | Owner: keep demoted. Still shows engineering hard stops, so it stays listed, but low. |
| spark-training-lab removed | Public files contain the owner's first name and unfiltered teacher outputs (audit P1 #1–2). Re-add only after a scrub, and only as "configs + scripts; weights stay local". |
| gravity-lander removed | A toy; DA says keep toys unlisted on the conference face. |
| H3 rows credit Joey Rodriguez by name and add a licence line | DA: "credit Joey + licence territory on the first breath". |
| "If it cannot be run this week, it is not listed" → "each one states the hardware it needs" | The old line was false for H3 (needs Sparks, weights, and licence clearance). |
| Added X `@coinupbtc` | Owner ruling: one handle everywhere, `@coinupbtc`. The current README has no X link. |
| Email kept out of the README | Matches the earlier owner decision (commit 279ca5f) to drop the public Gmail from the README. It stays in the GitHub sidebar and on the site. |
| dream-stack: not mentioned | Retired. Its neutralization is a repo-settings change; see `CONFERENCE_PIN_SHELF.md`. |

### GitHub profile sidebar (owner settings, not a file change)

| Field | Today | Proposed |
|---|---|---|
| Bio | Quality systems engineer. ISO 13485, CAPA, metrology. On-prem inference with measured gates. | **Keep.** It's already the best line on the profile. |
| Location | `St.Louis , MO` | `St. Louis, MO` |
| X / Twitter | `CoinUpBTC` | `coinupbtc` (matches site, social card, and this README) |
| Website | `https://coinupbtc.com` | Keep, *after* the site fixes in `SITE_HERO_GAPS.md` |
| Email | `coinupbtc@gmail.com` (public) | Owner decision. Fine for a hiring profile; it's already on the site and social card. |
| Hireable | ✅ | Keep |

### Hard-fail self-check on this copy

- Legal name: absent (searched the draft; only the alias appears).
- Live-GLM serving claim: absent.
- Traders, trading, betting, signals: absent.
- Factory-style slogan: absent.
- tok/s: only 35.80, with its date, conditions, and source file.
- dream-stack: not mentioned.
- X handle: only `@coinupbtc`.
