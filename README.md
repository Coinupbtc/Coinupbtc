Quality systems. On-prem inference. Measured, not claimed.

**[Helix QMS Desk](https://coinupbtc.github.io/helix-qms-desk/)** (90 seconds in the browser). A fictional biomedical plant: calibration sticker ≠ certificate, CAPA 8D, supplier SCARs, fail-closed integrity checks. All records are synthetic.

Homepage: **[coinupbtc.com](https://coinupbtc.com)**

---

### Quality & systems

| Repo | What you get |
|------|----------------|
| **[helix-qms-desk](https://github.com/Coinupbtc/helix-qms-desk)** | Interactive ISO 13485 quality desk. [Open the Pages build](https://coinupbtc.github.io/helix-qms-desk/). |
| **[build-a-boat](https://github.com/Coinupbtc/build-a-boat)** | Marine electrical package — voltage-drop and AC/DC hard stops. [Pages](https://coinupbtc.github.io/build-a-boat/). |
| **[zwell-bench](https://github.com/Coinupbtc/zwell-bench)** | 19-test release gate. A candidate ships only at 19/19. |

### On-prem inference

Dual NVIDIA DGX Spark. Weights stay local.

| Repo | What you get |
|------|----------------|
| **[dream-stack](https://github.com/Coinupbtc/dream-stack)** | Two-node serving: vLLM TP=2 + llama.cpp roommate. `./setup.sh && ./setup.sh --up` |
| **[spark-console](https://github.com/Coinupbtc/spark-console)** | Local fleet health dashboard. `./setup.sh` → `:8085` |
| **[miaai35-tune](https://github.com/Coinupbtc/miaai35-tune)** | Flag-by-flag llama.cpp bakeoff — numbers instead of vendor slides. |
| **[spark-training-lab](https://github.com/Coinupbtc/spark-training-lab)** | Small QLoRA runs with held-out evaluation. Weights never leave the box. |

`miaai35-tune` credits [MiaAI Labs’ Qwen3.6-35B Spark recipe](https://github.com/MiaAI-Lab/Qwen3.6-35B-A3B-UD-Q8_K_XL_DGX-Spark-Recipe) for the serving baseline of that tune only.

### Also 

[gravity-lander](https://github.com/Coinupbtc/gravity-lander) · [stl-sandbox](https://github.com/Coinupbtc/stl-sandbox) · [bitcoin-blockfield](https://github.com/Coinupbtc/bitcoin-blockfield) · [teachers-book](https://github.com/Coinupbtc/teachers-book)

Every listed repo has a **Try it** path. If it cannot be run this week, it is not listed.
