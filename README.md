### Work first, then toys

Hiring managers: start at **[helix-qms-desk](https://github.com/Coinupbtc/helix-qms-desk)** (90-second Monday). Spark owners: **[dream-stack](https://github.com/Coinupbtc/dream-stack)**. If you cannot run it this week, it is not listed.

Site: **[coinupbtc.com](https://coinupbtc.com)** · Lab: **[coinupbtc.xyz](https://coinupbtc.xyz)** · X: **[@coinupbtc](https://x.com/coinupbtc)**

Every listed repo has **What / For / How** and a **Try it** path.

#### Hire me (quality + systems)

Med-device quality thinking in a plant you can operate. Synthetic data. Not a slide deck.

| Repo | What it is | What it’s for | How to use |
|------|------------|---------------|------------|
| **[helix-qms-desk](https://github.com/Coinupbtc/helix-qms-desk)** | Monday war-room: sticker ≠ cert, CAPA 8D, ISO 14971 residual, IQ/OQ/PQ | Sr QE / SQE / validation screens | `./setup.sh` or [Pages](https://coinupbtc.github.io/helix-qms-desk/) |
| **[build-a-boat](https://github.com/Coinupbtc/build-a-boat)** | Fictional marine electrical package | Drawings + voltage-drop / AC-DC hard stops | `./setup.sh` |
| **[teachers-book](https://github.com/Coinupbtc/teachers-book)** | Offline gradebook PWA | Controlled records on a Chromebook | [Install](https://coinupbtc.github.io/teachers-book/) |

#### Run a Spark

| Repo | What it is | What it’s for | How to use |
|------|------------|---------------|------------|
| **[dream-stack](https://github.com/Coinupbtc/dream-stack)** | 2× DGX Spark occupancy: 0731 + Qwen roommate + baton | Clone, copy `.env`, bring the stack up | `bash scripts/up.sh` |
| **[spark-console](https://github.com/Coinupbtc/spark-console)** | Local GPU/fleet dashboard | One-pane health on localhost | `./setup.sh` → `:8085` |
| **[zwell-bench](https://github.com/Coinupbtc/zwell-bench)** | Local LLM bakeoff harness | Score **your** OpenAI-compatible server | `./setup.sh` then `ZWELL_BASE=… bench_zwell.py` |
| **[spark-training-lab](https://github.com/Coinupbtc/spark-training-lab)** | LoRA/QLoRA lab | Small fine-tunes (weights stay local) | `./setup.sh` |
| **[miaai35-tune](https://github.com/Coinupbtc/miaai35-tune)** | llama.cpp flag bench | Point `bench_v5.py` at **your** `:8889` | `./setup.sh` (not a results museum) |

`miaai35-tune` notes its serving baseline from [MiaAI Labs’ Qwen3.6-35B Spark recipe](https://github.com/MiaAI-Lab/Qwen3.6-35B-A3B-UD-Q8_K_XL_DGX-Spark-Recipe) — that credit is for that tune only.

#### Make something

| Repo | What it is | What it’s for | How to use |
|------|------------|---------------|------------|
| **[stl-sandbox](https://github.com/Coinupbtc/stl-sandbox)** | Prompt → STL/STEP | Printable parts + bed-fit, no cloud | `./install.sh` → `:8050` |
| **[gravity-lander](https://github.com/Coinupbtc/gravity-lander)** | Phone-first Three.js lunar lander | Playable landings on desktop/iPhone | `./setup.sh` → `:8070` |
| **[falling-sand](https://github.com/Coinupbtc/falling-sand)** | Browser falling-sand chemistry sim | Play particle reactions locally | open `index.html` or `./setup.sh` |
| **[bitcoin-blockfield](https://github.com/Coinupbtc/bitcoin-blockfield)** | Live Bitcoin mempool visualizer | Next-block fee wars at a glance | `./setup.sh` or open `index.html` |
| **[ordinookis](https://github.com/Coinupbtc/ordinookis)** | Pixel character + short MP4 gallery | Browse the clips in-browser | open `index.html` or `./setup.sh` |

Homepage: **[Coinupbtc.github.io](https://github.com/Coinupbtc/Coinupbtc.github.io)** → [coinupbtc.com](https://coinupbtc.com)

*Weights stay local. Listed repos are things you run.*
