### DGX Spark — local inference & fine-tunes

I build and measure **NVIDIA DGX Spark** stacks (Grace Blackwell, unified memory): llama.cpp serving,
LoRA adapters, and bakeoffs with real tok/s and quality numbers — methods and results, not just checkpoints.

Site: **[coinupbtc.com](https://coinupbtc.com)** · X: **[@coinupbtc](https://x.com/coinupbtc)** · GitHub issues on any public repo.

Every public repo includes an **At a glance** table (what / what for / how) and a **Try it** one-command path.

#### Spotlight

| Repo | What it is | What it’s for | How to use |
|------|------------|---------------|------------|
| **[helix-qms-desk](https://github.com/Coinupbtc/helix-qms-desk)** | Quality desk + CSV binder for a demo med-device plant | Sr QE / SQE / validation screens | `./setup.sh` or open the Pages URL |
| **[spark-ledger](https://github.com/Coinupbtc/spark-ledger)** | Ship/kill blotter for local Spark models | Decide with public numbers, not vibes | `./setup.sh` or [Pages](https://coinupbtc.github.io/spark-ledger/) |
| **[build-a-boat](https://github.com/Coinupbtc/build-a-boat)** | Fictional marine electrical package | Drawings + voltage-drop / AC-DC hard stops | `./setup.sh` |
| **[miaai35-tune](https://github.com/Coinupbtc/miaai35-tune)** | Measured llama.cpp tune for Qwen3.6-35B | Pick serving flags with real tok/s & quality | `./setup.sh` or read `REPORT.md` |
| **[spark-training-lab](https://github.com/Coinupbtc/spark-training-lab)** | LoRA/QLoRA lab (adapters + datasets) | Small Spark fine-tunes without multi-GB weights in git | `./setup.sh` |
| **[zwell-bench](https://github.com/Coinupbtc/zwell-bench)** | Local LLM bakeoff harness | Objective model comparisons | `./setup.sh` then `bench_zwell.py` |
| **[spark-console](https://github.com/Coinupbtc/spark-console)** | Local GPU/fleet dashboard | One-pane Spark health on localhost | `./setup.sh` → `:8085` |

`miaai35-tune` and the 35B cards on `spark-ledger` note the serving baseline from [MiaAI Labs’ Qwen3.6-35B Spark recipe](https://github.com/MiaAI-Lab/Qwen3.6-35B-A3B-UD-Q8_K_XL_DGX-Spark-Recipe) — that credit is for that recipe only, not the other repos.

#### Also

| Repo | What it is | What it’s for | How to use |
|------|------------|---------------|------------|
| **[Coinupbtc.github.io](https://github.com/Coinupbtc/Coinupbtc.github.io)** | Portfolio site | One hiring-friendly link for GitHub + X + builds | [coinupbtc.com](https://coinupbtc.com) or `./setup.sh` |
| [stl-sandbox](https://github.com/Coinupbtc/stl-sandbox) | Prompt → STL/STEP sandbox | Local printable CAD + bed-fit checks | `./install.sh` → `:8050` |
| [bitcoin-blockfield](https://github.com/Coinupbtc/bitcoin-blockfield) | Mempool visualizer | See next-block fee wars at a glance | `./setup.sh` or open `index.html` |
| [teachers-book](https://github.com/Coinupbtc/teachers-book) | Offline gradebook PWA | Grades on one Windows/Chromebook | [coinupbtc.com/teachers-book](https://coinupbtc.com/teachers-book/) |
| [falling-sand](https://github.com/Coinupbtc/falling-sand) | Browser falling-sand chemistry sim | Play particle reactions locally | open `index.html` or `./setup.sh` |
| [gravity-lander](https://github.com/Coinupbtc/gravity-lander) | Phone-first Three.js lunar lander | Playable landings on desktop/iPhone | `./setup.sh` → `:8070` |
| [ordinookis](https://github.com/Coinupbtc/ordinookis) | Pixel character + short MP4 gallery | Browse Ordinooki-style art/clips | open `index.html` or `./setup.sh` |

*Weights stay local. Repos ship methods, adapters, and measured results.*
