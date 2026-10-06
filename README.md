Quality systems. On-prem inference. Measured, not claimed.

**[Helix QMS Desk](https://coinupbtc.github.io/helix-qms-desk/)** (90 seconds in the browser). A fictional biomedical plant: calibration sticker ≠ certificate, CAPA 8D, supplier SCARs, fail-closed integrity checks. All records are synthetic.

Homepage: **[coinupbtc.com](https://coinupbtc.com)**

---

### Quality & systems

| Repo | What you get |
|------|----------------|
| **[helix-qms-desk](https://github.com/Coinupbtc/helix-qms-desk)** | Interactive ISO 13485 quality desk. [Open the Pages build](https://coinupbtc.github.io/helix-qms-desk/). |
| **[build-a-boat](https://github.com/Coinupbtc/build-a-boat)** | Marine electrical package — voltage-drop and AC/DC hard stops. [Pages](https://coinupbtc.github.io/build-a-boat/). |
| **[zwell-bench](https://github.com/Coinupbtc/zwell-bench)** | 15-check release gate. A build ships only if every check passes. The published 16 July 2026 run is 14 of 15. |

### On-prem inference

Dual NVIDIA DGX Spark. Weights stay local. The public throughput number is the bakeoff.

| Repo | What you get |
|------|----------------|
| **[miaai35-tune](https://github.com/Coinupbtc/miaai35-tune)** | Flagship llama.cpp bakeoff. Coding decode **35.80 tok/s** (9 July 2026; thinking off, speculative decode off). |
| **[spark-console](https://github.com/Coinupbtc/spark-console)** | Local fleet health dashboard. `./setup.sh` → `:8085` |
| **[spark-training-lab](https://github.com/Coinupbtc/spark-training-lab)** | Small QLoRA runs with held-out evaluation. Weights never leave the box. |
| **[MiniMax-H3-2x-DGX-Spark](https://github.com/Coinupbtc/MiniMax-H3-2x-DGX-Spark)** | Two-Spark H3 over RoCE IB. Same-seed quality SHA + 55.5 s eager clip. |
| **[MiniMax-H3-1x-DGX-Spark](https://github.com/Coinupbtc/MiniMax-H3-1x-DGX-Spark)** | One-Spark H3 CUDNN eager — SHA-identical to the 2× clip, slower. `./setup.sh && ./start.sh` |
| **[dream-stack](https://github.com/Coinupbtc/dream-stack)** | Supporting occupancy around the public MiaAI / Anemll 0731 TP=2 brain, plus a llama.cpp roommate. `./setup.sh && ./setup.sh --up` |

`miaai35-tune` credits [MiaAI Labs’ Qwen3.6-35B Spark recipe](https://github.com/MiaAI-Lab/Qwen3.6-35B-A3B-UD-Q8_K_XL_DGX-Spark-Recipe) for the serving baseline of that tune only. The **35.80 tok/s** figure is the committed 9 July 2026 coding decode in that repo.

`dream-stack` credits the public [MiaAI / Anemll DeepSeek-V4-Flash-0731 DSpark TP=2](https://github.com/MiaAI-Lab/DeepSeek-v4-Flash-DSpark-2x-DGX-Spark) pair as the chat brain. This repo is the occupancy and the roommate.

### Also 

[gravity-lander](https://github.com/Coinupbtc/gravity-lander) · [stl-sandbox](https://github.com/Coinupbtc/stl-sandbox) · [bitcoin-blockfield](https://github.com/Coinupbtc/bitcoin-blockfield) · [teachers-book](https://github.com/Coinupbtc/teachers-book)

Every listed repo has a **Try it** path. If it cannot be run this week, it is not listed.
