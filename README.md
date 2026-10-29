### Quality engineer · ISO 13485 medical devices · St. Louis

Nine years in engineering and manufacturing quality, most recently in FDA-regulated medical-device manufacturing: CAPA, calibration and supplier quality under ISO 13485 and ISO 9001. On my own time I run [Hermes Agent](https://github.com/NousResearch/hermes-agent) around the clock against a DeepSeek-V4.1 model split across two NVIDIA DGX Spark machines, and I test the whole stack the way I test parts.

**Looking for** quality systems, software quality and validation roles · open to remote (US) · coinupbtc@gmail.com

#### Start here

**[Helix QMS Desk →](https://coinupbtc.com/helix-qms-desk/)** A 90-second quality desk in your browser: a calibration sticker that disagrees with its certificate, a CAPA 8D, supplier SCARs, and IQ/OQ/PQ on the desk itself. Every record is synthetic.

#### Case files

- **Lean AI: the waste in an AI agent's token stream.** I sorted four months of Hermes Agent traffic (7.6 billion tokens read, 36 million written) into Lean's wastes. Half of what the agent reads is tool output it already read, and that share grew from 40% to 52% as context windows grew. Hermes already ships the countermeasure, switched off; it's on now, under trial. [The note](https://coinupbtc.xyz/notes/lean-ai.html) · [the tool](https://github.com/Coinupbtc/lean-ai) · [try the demo](https://coinupbtc.xyz/demos/context-carry.html)
- **Three engine fixes upstream for agent traffic.** On the two-Spark DeepSeek-V4.1 recipe: a long prompt no longer freezes live streams (90 s gap down to 1.3 s), a reply's text before its tool calls is no longer dropped, and text in a fetched page can't pose as a control token. All three are on the recipe's `main`, credited in its [CREDITS.md](https://github.com/MiaAI-Lab/DeepSeek-v4.1-Flash-1017-2x-DGX-Sparks/blob/main/CREDITS.md). [Field notes on running Hermes Agent there](https://coinupbtc.xyz/notes/hermes-agent-two-sparks.html)
- **A release gate that rejected the better build.** A fine-tuned model improved on its target task but failed 4 unrelated checks (15/19). I rejected it, rebuilt the training set and shipped at 19/19: 96.2% field accuracy against 89.2% for the base model on 104 held-out records. [The gate](https://github.com/Coinupbtc/miaai35-tune/blob/main/bench_v5.py) · [training scripts](https://github.com/Coinupbtc/spark-training-lab)
- **13 seconds to 7.5 ms.** Selecting one row in a 516-record list rebuilt every row. [The bug and the fix, timed in your browser](https://coinupbtc.xyz/demos/render-cost.html)
- **Control charts against machine learning.** On 1,567 real production runs at the same 1% false-alarm budget, no method reliably beat chance. I committed the analysis plan before scoring. [The study](https://github.com/Coinupbtc/secom-spc-vs-ai)
- **A backup that passed for 15 days while saving one file**, and one more, on [coinupbtc.com](https://coinupbtc.com/#work).

[coinupbtc.com](https://coinupbtc.com) · [The lab](https://coinupbtc.xyz) · [X @coinupbtc](https://x.com/coinupbtc)
