### Quality engineer · ISO 13485 medical devices

I find the checks that pass when they shouldn't, then build the tests that prove the fix. Nine years in engineering and manufacturing quality, most recently in FDA-regulated medical-device manufacturing. I validate the software and AI systems I build the same way.

**Start here: [Helix QMS Desk](https://coinupbtc.com/helix-qms-desk/)**, a 90-second quality desk in your browser. A fictional plant with a calibration sticker that disagrees with its certificate, a CAPA 8D, supplier SCARs, and IQ/OQ/PQ on the desk itself. Every record is synthetic.

[coinupbtc.com](https://coinupbtc.com) · [The lab: coinupbtc.xyz](https://coinupbtc.xyz)

### Case files

| What I found | What I proved | Evidence |
|---|---|---|
| A fine-tuned model scored better on its target task but failed 4 unrelated checks (15/19) | Rejected it, rebuilt the training set, shipped at 19/19: 96.2% field accuracy against 89.2% for the base model on 104 held-out records | [19-check gate](https://github.com/Coinupbtc/miaai35-tune/blob/main/bench_v5.py) · [training scripts](https://github.com/Coinupbtc/spark-training-lab) |
| Selecting one row in a 516-record list took 13 seconds | A flat 7.5 ms after removing the full rebuild and repeated parsing | [The bug and the fix, timed in your browser](https://coinupbtc.xyz/demos/render-cost.html) |
| Do machine-learning alarms beat control charts on real factory data? | 1,567 runs, 590 sensors, the same 1% false-alarm budget: no method reliably beat chance. Plan committed before scoring. | [secom-spc-vs-ai](https://github.com/Coinupbtc/secom-spc-vs-ai) |

Two more, including a backup that reported success for 15 days while saving one file, are on [coinupbtc.com](https://coinupbtc.com/#work).

### Repos

| Repo | What it is |
|---|---|
| **[helix-qms-desk](https://github.com/Coinupbtc/helix-qms-desk)** | The quality desk above. Plain JavaScript, no framework; CI regenerates the synthetic data and checks ID uniqueness. |
| **[miaai35-tune](https://github.com/Coinupbtc/miaai35-tune)** | Setting-by-setting tuning study for a 35B model on one DGX Spark, against a recorded baseline, plus the 19-check release gate. Serving baseline from [MiaAI Labs' recipe](https://github.com/MiaAI-Lab/Qwen3.6-35B-A3B-UD-Q8_K_XL_DGX-Spark-Recipe). |
| **[spark-training-lab](https://github.com/Coinupbtc/spark-training-lab)** | LoRA/QLoRA fine-tuning: datasets, adapter configs, merge and eval scripts. Weights stay on the machine. |
| **[secom-spc-vs-ai](https://github.com/Coinupbtc/secom-spc-vs-ai)** | The control-chart study, with its preregistration and deviations log. |
| **[spark-console](https://github.com/Coinupbtc/spark-console)** | Read-only health dashboard for the machines. Localhost only, no start/stop/kill routes. |
| **[coinupbtc-xyz](https://github.com/Coinupbtc/coinupbtc-xyz)** | The lab site: four demos you can run in the browser. |

Also: [stl-sandbox](https://github.com/Coinupbtc/stl-sandbox) (plain-English prompt to printable 3D model, fully local) · [teachers-book](https://github.com/Coinupbtc/teachers-book) (offline gradebook app) · [gravity-lander](https://github.com/Coinupbtc/gravity-lander) · [bitcoin-blockfield](https://github.com/Coinupbtc/bitcoin-blockfield)

Lab hardware: two NVIDIA DGX Spark machines, 121 GB each. Models run locally; nothing is rented in the cloud.
