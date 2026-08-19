### Work first, then toys

Hiring managers: start at **[helix-qms-desk](https://github.com/Coinupbtc/helix-qms-desk)** (browser JS, 90-second Monday). Spark owners: **[dream-stack](https://github.com/Coinupbtc/dream-stack)** (Python + shell). If you cannot run it this week, it is not listed.

Site: **[coinupbtc.com](https://coinupbtc.com)** · Lab: **[coinupbtc.xyz](https://coinupbtc.xyz)** · X: **[@coinupbtc](https://x.com/coinupbtc)**

Python is the **ops glue** (serve, bench, seed). The things a stranger clicks are **JavaScript / HTML**. That split is on purpose.

#### Stack (what is actually in the repos)

| Layer | Proof | What it is not |
|-------|--------|----------------|
| **Browser JS + CSS** | helix, lander, boat, mempool, .com | No React/Next résumé-spam |
| **Python** | benches, Spark glue, gradebook | Not notebooks-as-the-product |
| **Shell** | dream-stack `up.sh`, keep-warm, heal | Not a Kubernetes museum |
| **Systems / inference** | Dual DGX Spark, TP=2, KV/context math, on-prem only | Not “I wrote a CUDA kernel” |
| **Quality / CSV** | ISO 13485 + 14971 desk, IQ/OQ/PQ, fail-closed | Not a slide deck |

Every listed repo has **What / For / How** and a **Try it** path.

#### Hire me (quality + systems)

Med-device quality thinking in a plant you can operate. Synthetic data.

| Repo | Lang | What it is | How |
|------|------|------------|-----|
| **[helix-qms-desk](https://github.com/Coinupbtc/helix-qms-desk)** | JS | Monday: sticker ≠ cert, CAPA 8D, ISO 14971 residual, IQ/OQ/PQ | `./setup.sh` or [Pages](https://coinupbtc.github.io/helix-qms-desk/) |
| **[build-a-boat](https://github.com/Coinupbtc/build-a-boat)** | JS | Marine electrical package — voltage-drop / AC-DC hard stops | `./setup.sh` |
| **[teachers-book](https://github.com/Coinupbtc/teachers-book)** | Python | Offline gradebook PWA — controlled records | [Install](https://coinupbtc.github.io/teachers-book/) |

#### Run a Spark

| Repo | Lang | What it is | How |
|------|------|------------|-----|
| **[dream-stack](https://github.com/Coinupbtc/dream-stack)** | Python + shell | 2× Spark occupancy: 0731 + Qwen roommate + baton | `bash scripts/up.sh` |
| **[spark-console](https://github.com/Coinupbtc/spark-console)** | Python + HTML | One-pane fleet health on localhost | `./setup.sh` → `:8085` |
| **[zwell-bench](https://github.com/Coinupbtc/zwell-bench)** | Python | Score **your** OpenAI-compatible server | `ZWELL_BASE=… bench_zwell.py` |
| **[spark-training-lab](https://github.com/Coinupbtc/spark-training-lab)** | Python + shell | Small LoRA/QLoRA (weights stay local) | `./setup.sh` |
| **[miaai35-tune](https://github.com/Coinupbtc/miaai35-tune)** | Python | llama.cpp flag bench on **your** `:8889` | `./setup.sh` |

`miaai35-tune` notes its serving baseline from [MiaAI Labs’ Qwen3.6-35B Spark recipe](https://github.com/MiaAI-Lab/Qwen3.6-35B-A3B-UD-Q8_K_XL_DGX-Spark-Recipe) — that credit is for that tune only.

#### Make something

| Repo | Lang | What it is | How |
|------|------|------------|-----|
| **[gravity-lander](https://github.com/Coinupbtc/gravity-lander)** | JS (Three.js) | Phone-first lunar lander | `./setup.sh` → `:8070` |
| **[bitcoin-blockfield](https://github.com/Coinupbtc/bitcoin-blockfield)** | JS | Live mempool / fee wars | `./setup.sh` or `index.html` |
| **[stl-sandbox](https://github.com/Coinupbtc/stl-sandbox)** | Python | Prompt → STL/STEP, no cloud | `./install.sh` → `:8050` |
| **[falling-sand](https://github.com/Coinupbtc/falling-sand)** | HTML | Particle chemistry in the browser | `index.html` |
| **[ordinookis](https://github.com/Coinupbtc/ordinookis)** | HTML | Pixel characters + clips | `index.html` |

Homepage: **[Coinupbtc.github.io](https://github.com/Coinupbtc/Coinupbtc.github.io)** → [coinupbtc.com](https://coinupbtc.com)

*Weights stay local. Listed repos are things you run.*
