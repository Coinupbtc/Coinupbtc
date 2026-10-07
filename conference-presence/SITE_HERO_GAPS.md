# Site hero gaps — handoff note for a follow-up agent

**Status:** DRAFT · **This run did not edit the site repos.** No PR, no merge.
**Surfaces:** `coinupbtc.com` (repo `Coinupbtc/Coinupbtc.github.io`) and `coinupbtc.xyz` (repo `Coinupbtc/coinupbtc-xyz`), which the site links as "Lab".
**Checked:** 2026-10-07, shallow clones plus live fetches. Every URL below returned HTTP 200.
**Alias only.** Same hard constraints as the profile pack: no legal name, no live-GLM claim, no trading or betting as the face, no factory-style slogan, honest tok/s, dream-stack not heroed, X handle `@coinupbtc`.

Ranked by what blocks a conference push.

---

## 1. X handle — `@coinupbtc` everywhere (DA killer #3, owner ruling)

**Site and lab are already consistent. Don't change them.** All 19 references use `@coinupbtc` / `x.com/coinupbtc`:

| File | Lines |
|---|---|
| `Coinupbtc.github.io/index.html` | 22 (`twitter:site`), 23 (`twitter:creator`), 58 (JSON-LD `sameAs`), 359 (footer) |
| `Coinupbtc.github.io/README.md` | 29 |
| `Coinupbtc.github.io/assets/og-image.png` | baked-in text `x.com/coinupbtc` ✅ |
| `coinupbtc-xyz/index.html` | 27, 29, 30, 32, 371 |
| `coinupbtc-xyz/training.html` | 23, 187, 200 |
| `coinupbtc-xyz/README.md` | 72 |

**The only drift is GitHub:** the profile X field is `CoinUpBTC`. The owner should change it to `coinupbtc` in GitHub settings. Use no other handle in any new copy.

## 2. Trading/betting one click from the homepage — BLOCKER

- Path: `coinupbtc.com` → nav **Lab** (also the "the lab" card and JSON-LD `sameAs`) → `coinupbtc.xyz`.
- `https://coinupbtc.xyz/signals.html` is live (200). Its source is in the **public** repo `coinupbtc-xyz` (`signals.html`, `signals-checkout.js`).
- It sells perps funding signals, a DeFi yield digest, and a UFC fair-odds-vs-book-lines / Polymarket feed ($5–$9/mo via Telegram).
- `robots.txt` disallows it and the lab index doesn't link it. Hiding it from crawlers doesn't hide it from someone browsing the public repo.
- The homepage lab card says **"No account. No checkout."**, which `signals-checkout.js` contradicts.

**Fix options, best first:**
- (a) Remove `signals.html` and `signals-checkout.js` from `coinupbtc-xyz` and the `.xyz` domain. Host them under a separate, unlinked identity, if at all.
- (b) Drop `coinupbtc.xyz` from the homepage nav, the lab card, and `sameAs` until (a) is done.

Either way, the "No checkout" claim must be true.

## 3. zwell gate wording (DA killer #2)

`Coinupbtc.github.io/index.html:183`, current:
> Release gate for local LLMs — coding, vision, tools, and agentic checks. A build ships only if every check passes. The published run from 16 July 2026 is **14 of 15**, one agentic miss.

Proposed:
> Release gate for local AI models: coding, vision, tools, and agentic checks. The bar is all 15 green. The published 16 July 2026 baseline is **14 of 15** (one agentic miss), so by its own rule it does not pass.

The marquee item "15-check gate" (`index.html` ~122, ~126) is fine; it doesn't claim a pass. Apply the same wording to `zwell-bench/README.md` line 27 ("A candidate ships only if every check passes").

## 4. MiniMax H3 media on the site — OWNER DECISION before any traffic push

- The site autoplays `assets/video/hero-street.mp4` (an H3 clip, per the HTML comment at `index.html:89`) as the hero backplate. It shows an eight-clip H3 gallery ("Made on the machine"), and `og-image.png` appears to use an H3 frame (the astronaut clip).
- The owner's own `MiniMax-H3-2x-DGX-Spark/MODEL-LICENSE.md` summarises the H3 Community License as excluding the **United States**, EU, UK, and Republic of Korea. It says displaying the model's outputs outside that territory is not authorized, and that published model output needs prominent disclosure.
- The GitHub location is St. Louis, MO.

That's a visible contradiction between the owner's repo and the owner's site. The DA's suggested one-line caveat ("community license ≠ commercial free-for-all") doesn't resolve it. A caveat that names the US exclusion, sitting under US-hosted outputs, makes it *more* noticeable.

**Not legal advice. The owner chooses one:**
- (a) Confirm written authorization from MiniMax and add the disclosure line.
- (b) Replace the hero backplate, the gallery, and the social-card background with non-H3 media (for example ComfyUI stills already described on the site as "on-metal", or the `setup-cluster.webp` photo) and regenerate `og-image.png`.

Until then, don't print the site URL on conference material.

## 5. Hero copy — role first, number second

Current hero (`index.html:100-111`): the eyebrow is "miaai35-tune · measured llama.cpp", the H1 is the handle, then the lede *"I don't rent intelligence — I host it."*, then CTAs miaai35-tune / Helix / spark-console, then the 35.80 line. It's honest, but it never says what job the person does, and the QMS story only appears as the second button.

Proposed (keep the lede; the DA likes it):

| Element | Proposed |
|---|---|
| Eyebrow | `Quality systems engineer · on-prem AI` |
| H1 | `Coinupbtc` (unchanged) |
| Lede | *I don't rent intelligence — I host it.* (unchanged) |
| New line under lede | `ISO 13485, CAPA, metrology, validation. I hold my own AI hardware to the same rule: presence is not integrity.` |
| CTAs (order) | `Helix QMS desk ↗` · `miaai35-tune ↗` · `spark-console ↗` |
| Use-line | Keep as is: "Primary coding decode is **35.80 tok/s** on 9 July 2026, from the committed bench JSON. The same file is the ~35–38 band." |
| Foot meta | Replace "Pseudonymous · hiring-friendly" with a contact action, e.g. `Hiring? GitHub · X @coinupbtc · email` |

## 6. Smaller accuracy and consistency fixes

| Where | Issue | Fix |
|---|---|---|
| `index.html` systems grid, "GPU memory 121 GB · unified CPU+RAM, on-box" | The site photo and H3 work are two Sparks; 121 GB is **per Spark**. spark-pack is careful about this; the site isn't. | `121 GB per Spark` |
| `index.html` spark-console card badge "**121** GB" and "121 GB unified memory" | 121 GB is hardware, not a spark-console feature. | Badge → something spark-console actually does (e.g. `read-only`, `:8085`); drop the 121 GB sentence. |
| `index.html` lab card "Browser mechanisms — memory packer, speculative decoding, render-cost timer. No account. No checkout." | False while `signals.html` exists on the same domain (§2). | Keep the text only after §2 (a). |
| `coinupbtc-xyz/training.html` "We train your team", $1,200 / $4,500 flat | A paid-services page with "we" (company voice) one click from a hireable profile. Not a hard fail, but it muddies "is this person job-hunting or selling?" | Owner decision: keep it under Lab only, or remove the nav link from the homepage path during the conference. |
| Social-card PNG | Correct handle and email, but likely an H3 background (§4). The headline is "Local AI · measured builds · open repos", with no quality role. | Regenerate with the role line (`Quality systems engineer · on-prem AI`) and a non-H3 background, if §4 (b). |
| `index.html` JSON-LD `sameAs` includes `https://coinupbtc.xyz/` | Ties the lab domain, and so the signals page, to the person entity in search. | Drop until §2 is done. |

## 7. Verified OK — don't "fix"

- 35.80 tok/s everywhere on the site matches `results/bench-original-rerun-think-off-20260709-203311.json`, with date and conditions.
- No dream-stack mention anywhere on either site.
- No legal name, no live-GLM claim, and no factory-style slogan on either site's pages.
- The Helix Pages link and the build-a-boat Pages link both resolve (200).
