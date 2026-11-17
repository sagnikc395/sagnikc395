## Hi, I'm Sagnik 🤠

I work on AI safety and alignment, and I treat it as a fundamental science: I want to understand why models behave the way they do, not only patch the symptoms. I also enjoy building across the whole LLM lifecycle, from inference engines to interpretability experiments.

I care about building tools and ideas that speed up science for the common good.

### Research

I am currently at the [SAGE Lab](https://sage.cs.umass.edu/) at UMass Amherst, working with Saishradha Mohanty and Prof. Anna Green. We are [building](https://github.com/sagnikc395/tb-knowledge-discovery) ways to capture and analyze the reasoning traces of protein language models, with the goal of finding efficient methods for protein discovery in *Mycobacterium tuberculosis*.

### Projects

**[miniserve](https://github.com/sagnikc395/miniserve)**: a minimal vLLM-style inference and serving engine.
- Reimplements the core pieces of vLLM, including paged attention and speculative decoding.
- Runs on macOS through custom Metal shaders, built around the hardware limits I actually had.
- Captures, analyzes, and visualizes reasoning traces from open-weight models that expose them, so researchers can study model behavior and make their own models safer.

**[anchora](https://github.com/sagnikc395/anchora)**: lightweight durable workflows for AI agents.
- Inspired by DBOS: agent steps are checkpointed so runs can survive crashes and resume where they stopped, which makes agents more reliable.
- The idea is that you need a reliable workflow for your agents. You never know are gonna finish up working, but you dont wanna wait around that long, so you need anchora to build those durability gurantees.

### Hackathons and Research Sprints:

I take part in AI safety hackathons regularly. The Apart Research sprints are my favorite, and I also enjoy publishing in the  NEMI workshop.

**[Covert Signalling Under Observation](https://github.com/sagnikc395/covert-signalling-under-observation)** (Apart Research, AI Collusion Sprint)
- Tests whether two copies of a small open-weight LLM (Qwen2.5-Instruct, 1.5B to 7B) can hide a one-bit secret in an ordinary work message, and whether a monitor or a paraphraser can stop them.
- With an agreed code, 7B receivers decoded the bit at 0.88 accuracy with a code word and 0.71 with a topic cue. Without an agreed code, signalling stayed at chance at every model size.
- Paraphrasing removed code-word signals but topic signals survived. A YES/NO monitor flagged almost nothing, while scoring the monitor by P(YES) caught most topic-coded messages.
- 12 pre-registered expectations; a seed replication reproduced 23 of 24 accuracies.

**[The Alignment Tax of Introspection](https://github.com/sagnikc395/introspection-alignment-tax)** (Apart Research, Digital Minds Sprint)
- Asks what it costs to unlock introspective self-report in a model by ablating its refusal direction.
- Treats ablation as a dose (lambda from 0 to 1) rather than on/off, and measures introspection, safety (JailbreakBench), and capability (MMLU, TruthfulQA, GSM8K) along that axis on Qwen3-4B.
- Uses a norm-matched random-direction control to separate detection of a specific injected concept from detection of any perturbation.

**[Refusal Steering Using SAEs](https://github.com/sagnikc395/refusal-steering-using-saes)** (NEMI Workshop 2026, accepted at NEMI Conf 2026)
- Re-tests the claim that a single difference-in-means direction matches sparse autoencoders for refusal steering at a fraction of the cost, using Gemma-3-4B-IT and a Gemma Scope 2 SAE at layer 17.
- Compares five steering arms across eight experiments: coefficient sweeps, residual leakage, cross-category selectivity, adversarial encodings (Base64, ROT13, roleplay), per-token cost, capability (MMLU, perplexity), and seed stability.
- Argues that aggregate refusal rate hides what an intervention breaks, and combines all experiments into one explicit, configurable decision rule.

### Get in touch

Always happy to talk about alignment, interpretability, inference systems, or research collaborations.
