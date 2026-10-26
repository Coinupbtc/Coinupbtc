Quality systems. On-prem inference. Measured, not claimed.

**[Helix QMS Desk](https://coinupbtc.com/helix-qms-desk/)** (90 seconds in the browser). A fictional biomedical plant: calibration sticker ≠ certificate, CAPA 8D, supplier SCARs, fail-closed integrity checks. All records are synthetic.

Homepage: **[coinupbtc.com](https://coinupbtc.com)**

---

### Quality & systems

| Repo | What you get |
|------|----------------|
| **[helix-qms-desk](https://github.com/Coinupbtc/helix-qms-desk)** | Interactive ISO 13485 quality desk. [Open it in the browser](https://coinupbtc.com/helix-qms-desk/). |
| **[secom-spc-vs-ai](https://github.com/Coinupbtc/secom-spc-vs-ai)** | Control charts vs ML on public UCI SECOM fab data, preregistered. At a 1% false-alarm budget no method reliably beat chance. |
| **[zwell-bench](https://github.com/Coinupbtc/zwell-bench)** | 15-check local-LLM bakeoff: coding, tools, vision, agentic. Latest committed run: 14/15. |

### On-prem inference

Dual NVIDIA DGX Spark. Weights stay local. The public throughput number is the bakeoff.

| Repo | What you get |
|------|----------------|
| **[miaai35-tune](https://github.com/Coinupbtc/miaai35-tune)** | Flagship llama.cpp bakeoff and the 19-check `bench_v5` release gate. Coding decode **35.80 tok/s** (9 July 2026; thinking off, speculative decode off). |
| **[spark-console](https://github.com/Coinupbtc/spark-console)** | Local fleet health dashboard. `./setup.sh` → `:8085` |
| **[MiniMax-H3-2x-DGX-Spark](https://github.com/Coinupbtc/MiniMax-H3-2x-DGX-Spark)** | Two-Spark H3 over RoCE IB. Same-seed quality SHA + 55.5 s eager clip. |
| **[MiniMax-H3-1x-DGX-Spark](https://github.com/Coinupbtc/MiniMax-H3-1x-DGX-Spark)** | One-Spark H3 CUDNN eager — SHA-identical to the 2× clip, slower. `./setup.sh && ./start.sh` |

`miaai35-tune` credits [MiaAI Labs’ Qwen3.6-35B Spark recipe](https://github.com/MiaAI-Lab/Qwen3.6-35B-A3B-UD-Q8_K_XL_DGX-Spark-Recipe) for the serving baseline of that tune only. The **35.80 tok/s** figure is the committed 9 July 2026 coding decode in that repo.

### Also

[gravity-lander](https://github.com/Coinupbtc/gravity-lander) · [stl-sandbox](https://github.com/Coinupbtc/stl-sandbox) · [spark-training-lab](https://github.com/Coinupbtc/spark-training-lab) (configs + scripts only; adapters stay on the box — not a public weight dump)

Every listed repo has a **Try it** path. If it cannot be run this week, it is not listed.
