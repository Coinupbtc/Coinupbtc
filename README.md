### DGX Spark — local inference & fine-tunes

I build and measure **NVIDIA DGX Spark** stacks (Grace Blackwell, unified memory): llama.cpp serving,
LoRA adapters, and bakeoffs with real tok/s and quality numbers — methods and results, not just checkpoints.

Site: **[coinupbtc.com](https://coinupbtc.com)** · X: **[@coinupbtc](https://x.com/coinupbtc)** · Email: **[coinupbtc@gmail.com](mailto:coinupbtc@gmail.com)**

Every public repo includes an **At a glance** table (what / what for / how) and a **Try it** one-command path.

#### Spotlight

| Repo | What it is | What it’s for | How to use |
|------|------------|---------------|------------|
| **[miaai35-tune](https://github.com/Coinupbtc/miaai35-tune)** | Measured llama.cpp tune for Qwen3.6-35B | Pick serving flags with real tok/s & quality | `./setup.sh` or read `REPORT.md` |
| **[spark-training-lab](https://github.com/Coinupbtc/spark-training-lab)** | LoRA/QLoRA lab (adapters + datasets) | Small Spark fine-tunes without multi-GB weights in git | `./setup.sh` |
| **[zwell-bench](https://github.com/Coinupbtc/zwell-bench)** | Local LLM bakeoff harness | Objective model comparisons | `./setup.sh` then `bench_zwell.py` |
| **[spark-console](https://github.com/Coinupbtc/spark-console)** | Local GPU/fleet dashboard | One-pane Spark health on localhost | `./setup.sh` → `:8085` |

`miaai35-tune` notes its serving baseline from [MiaAI Labs’ Qwen3.6-35B Spark recipe](https://github.com/MiaAI-Lab/Qwen3.6-35B-A3B-UD-Q8_K_XL_DGX-Spark-Recipe) — that credit is for that tune only, not the other repos.

#### Also

| Repo | What it is | What it’s for | How to use |
|------|------------|---------------|------------|
| **[Coinupbtc.github.io](https://github.com/Coinupbtc/Coinupbtc.github.io)** | Portfolio site | One hiring-friendly link for GitHub + X + builds | [coinupbtc.com](https://coinupbtc.com) or `./setup.sh` |
| [stl-sandbox](https://github.com/Coinupbtc/stl-sandbox) | Prompt → STL/STEP sandbox | Local printable CAD + bed-fit checks | `./install.sh` → `:8050` |
| [bitcoin-blockfield](https://github.com/Coinupbtc/bitcoin-blockfield) | Mempool visualizer | See next-block fee wars at a glance | `./setup.sh` or open `index.html` |
| [teachers-book](https://github.com/Coinupbtc/teachers-book) | Browser gradebook | Fast local-first grade entry | `./setup.sh` → `:8010` |

*Weights stay local. Repos ship methods, adapters, and measured results.*
