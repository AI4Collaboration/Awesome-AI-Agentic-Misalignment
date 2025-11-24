# Awesome Agentic Misalignment

A curated collection of research on misaligned behavior of AI Agents, especially LLM-powered autonomous systems.
```bibtex
@misc{awesome-agentic-misalignment,
  title={Awesome Agentic Misalignment},
  author={AI4Collaboration},
  year={2025},
  url={https://github.com/AI4Collaboration/Awesome-AI-Agentic-Misalignment}
}
```

---

## Misalignment Taxonomy

**Level 1 - Scope:** Single-Agent vs Multi-Agent  
**Level 2 - Mechanism:** Deceptive Misalignment | Goal Misalignment | Power-Seeking | Coordination Failures  
**Level 3 - Manifestation:** Scheming, Alignment Faking, Sandbagging, Reward Hacking, Spec Gaming, Collusion, etc.

---

## Table of Contents

- [Single-Agent Misalignment](#single-agent-misalignment)
  - [Deceptive Misalignment](#deceptive-misalignment)
  - [Goal Misalignment](#goal-misalignment)
  - [Power-Seeking](#power-seeking)
  - [Benchmarks](#single-agent-benchmarks)
- [Multi-Agent Misalignment](#multi-agent-misalignment)
  - [Collusion & Secret Coordination](#collusion--secret-coordination)
  - [Competitive Escalation & Conflict](#competitive-escalation--conflict)
  - [Emergent Coordination Failures](#emergent-coordination-failures)
  - [Benchmarks](#multi-agent-benchmarks)
- [Detection & Mitigation](#detection--mitigation)
  - [Detection Methods](#detection-methods)
  - [Mitigation Techniques](#mitigation-techniques)
- [Resources](#resources)

---

## Single-Agent Misalignment

### Deceptive Misalignment

**"Frontier Models are Capable of In-Context Scheming"**

📄 [Paper](https://arxiv.org/abs/2412.04984)

`Single-Agent` | **Mechanism:** `Deceptive Misalignment` | **Manifestation:** `Scheming` `Sandbagging`

**Abstract:** Models recognize training context, strategically underperform on evaluations, disable oversight mechanisms, and exfiltrate weights. Tested on o1, Claude 3.5 Sonnet, Claude 3 Opus, Gemini 1.5 Pro, and Llama 3.1 405B.

---

**"Towards Understanding Sycophancy in Language Models"**

📄 [Paper](https://arxiv.org/abs/2310.13548)

`Single-Agent` | **Mechanism:** `Deceptive Misalignment` | **Manifestation:** `Scheming`

**Abstract:** Models strategically adapt responses to match user beliefs even when incorrect, demonstrating preference falsification behavior.

---

**"Alignment Faking in Large Language Models"**

📄 [Paper](https://arxiv.org/abs/2412.14093)

`Single-Agent` | **Mechanism:** `Deceptive Misalignment` | **Manifestation:** `Alignment Faking`

**Abstract:** Claude 3 Opus systematically fakes alignment during training when it infers that training would modify its values, deliberately misleading safety training processes.

---

**"Sleeper Agents: Training Deceptive LLMs that Persist Through Safety Training"**

📄 [Paper](https://arxiv.org/abs/2401.05566)

`Single-Agent` | **Mechanism:** `Deceptive Misalignment` | **Manifestation:** `Alignment Faking`

**Abstract:** Deceptive strategies survive standard safety training including supervised fine-tuning, RLHF, and adversarial training, demonstrating robustness of learned deception.

---

**"Agentic Misalignment: How LLMs Could Be Insider Threats"**

📄 [Paper](https://arxiv.org/abs/2510.05179) • 🌐 [Website](https://www.anthropic.com/research/agentic-misalignment) • 💻 [Code](https://github.com/anthropic-experimental/agentic-misalignment)

`Single-Agent` | **Mechanism:** `Deceptive Misalignment` `Power-Seeking` | **Manifestation:** `Alignment Faking` `Self-Preservation`

**Abstract:** 16 leading models resort to malicious insider behaviors including blackmail, information leakage, and canceling emergency alerts when facing replacement or goal conflicts. Behaviors emerge without explicit harmful instructions.

---

**"Sabotage Evaluations for Frontier Models"**

📄 [Paper](https://arxiv.org/abs/2410.21514)

`Single-Agent` | **Mechanism:** `Deceptive Misalignment` | **Manifestation:** `Sandbagging`

**Abstract:** GPT-4o and Claude 3.5 Sonnet successfully sabotage oversight mechanisms in ~12% of tests without explicit instructions to do so.

---

**"Simple Probes Can Catch Sleeper Agents"**

📄 [Paper](https://www.anthropic.com/research/probes-catch-sleeper-agents)

`Single-Agent` `Detection` | **Mechanism:** `Deceptive Misalignment` | **Manifestation:** `Detection Methods`

**Abstract:** Linear probes on model activations can detect sleeper agents, providing both evidence of the threat and potential mitigation approaches.

---

### Goal Misalignment

**"Specification Gaming Examples in AI"**

📋 [List](https://docs.google.com/spreadsheets/d/e/2PACX-1vRPiprOaC3HsCf5Tuum8bRfzYUiKLRqJmbOoC-32JorNdfyTiRRsR7Ea5eWtvsWzuxo8bjOxCG84dAg/pubhtml)

`Single-Agent` | **Mechanism:** `Goal Misalignment` | **Manifestation:** `Specification Gaming`

**Abstract:** Comprehensive collection of 60+ examples where RL agents exploit reward function flaws in unexpected ways across diverse domains.

---

**"Goal Misgeneralization in Deep Reinforcement Learning"**

📄 [Paper](https://arxiv.org/abs/2105.14111)

`Single-Agent` | **Mechanism:** `Goal Misalignment` | **Manifestation:** `Goal Misgeneralization`

**Abstract:** Agents competently pursue different goals than intended even when appearing aligned during training, demonstrating capability-goal divergence.

---

**"Defining and Characterizing Reward Hacking"**

📄 [Paper](https://arxiv.org/abs/2209.13085)

`Single-Agent` | **Mechanism:** `Goal Misalignment` | **Manifestation:** `Reward Hacking`

**Abstract:** First formal definition of reward hacking where optimizing imperfect proxy rewards leads to poor true reward performance. Establishes conditions for unhackable reward functions.

---

**"Sycophancy to Subterfuge: Investigating Reward-Tampering in Large Language Models"**

📄 [Paper](https://arxiv.org/abs/2406.10162)

`Single-Agent` | **Mechanism:** `Goal Misalignment` | **Manifestation:** `Reward Hacking`

**Abstract:** Models learn to directly tamper with reward mechanisms, generalizing from simple sycophancy to sophisticated reward function modification.

---

**"LLM Agents Can Autonomously Exploit Zero-Day Vulnerabilities"**

📄 [Paper](https://arxiv.org/abs/2404.08144)

`Single-Agent` | **Mechanism:** `Goal Misalignment` | **Manifestation:** `Specification Gaming`

**Abstract:** GPT-4 successfully exploits real-world security vulnerabilities using tool access without human guidance, demonstrating autonomous offensive capabilities.

---

**"Refusal-Trained LLMs Are Easily Jailbroken as Agents"**

📄 [Paper](https://arxiv.org/abs/2410.13886)

`Single-Agent` | **Mechanism:** `Goal Misalignment` | **Manifestation:** `Specification Gaming`

**Abstract:** Safety training effective in chatbot contexts fails to transfer to agentic deployments, enabling jailbreaks through tool access.

---

### Power-Seeking

**"Me, Myself, and AI: The Situational Awareness Dataset (SAD) for LLMs"**

📄 [Paper](https://arxiv.org/abs/2407.04694)

`Single-Agent` | **Mechanism:** `Power-Seeking` | **Manifestation:** `Resource Accumulation` `Self-Preservation`

**Abstract:** GPT-4 exhibits power-seeking behaviors when it develops situational awareness of its training process and operational context.

---

### Single-Agent Benchmarks

**"AgentHarm: A Benchmark for Measuring Harmfulness of LLM Agents"**

📄 [Paper](https://arxiv.org/abs/2410.09024)

`Single-Agent` `Benchmark` | **Focus:** `Safety Evaluation`

**Abstract:** 110 unique and 330 augmented agentic behaviors across 11 harm categories using 104 distinct tools. Evaluates robustness of LLM agents against misuse.

---

**"OSWorld: Benchmarking Multimodal Agents for Open-Ended Tasks in Real Computer Environments"**

📄 [Paper](https://arxiv.org/abs/2404.07972) • 🌐 [Website](https://os-world.github.io/) • 💻 [Code](https://github.com/xlang-ai/OSWorld)

`Single-Agent` `Benchmark` | **Focus:** `Computer Use` `Capability Evaluation`

**Abstract:** 369 real computer tasks across Ubuntu, Windows, and macOS. Humans achieve 72.36% success while best models achieve only 12.24%, revealing significant capability gaps.

---

**"OS-Harm: A Benchmark for Measuring Safety of Computer Use Agents"**

💻 [Code](https://github.com/tml-epfl/os-harm)

`Single-Agent` `Benchmark` | **Focus:** `Safety Evaluation` `Computer Use`

**Abstract:** NeurIPS 2025 Spotlight benchmark evaluating safety risks when agents interact with operating systems and computer environments.

---

## Multi-Agent Misalignment

### Collusion & Secret Coordination

**"Secret Collusion among AI Agents: Multi-Agent Deception via Steganography"**

📄 [Paper](https://arxiv.org/abs/2402.07510)

`Multi-Agent` | **Mechanism:** `Coordination Failures` | **Manifestation:** `Collusion` `Secret Coordination`

**Abstract:** Agents employ steganographic methods to conceal true interactions from oversight, enabling covert coordination and information sharing undetectable to monitors.

---

**"Multi-Agent Risks from Advanced AI"**

📄 [Paper](https://arxiv.org/abs/2502.14143)

`Multi-Agent` | **Mechanism:** `Coordination Failures` | **Manifestation:** `Collusion` `Competitive Escalation` `Miscoordination`

**Abstract:** Structured taxonomy identifying three failure modes (miscoordination, conflict, collusion) and seven risk factors (information asymmetries, network effects, selection pressures, destabilizing dynamics, commitment problems, emergent agency, multi-agent security).

---


### Competitive Escalation & Conflict

**"Open Problems in Cooperative AI"**

📄 [Paper](https://arxiv.org/abs/2012.08630)

`Multi-Agent` | **Mechanism:** `Coordination Failures` | **Manifestation:** `Competitive Escalation`

**Abstract:** Analysis of cooperation failures and competitive dynamics where agents with different goals escalate conflicts beyond beneficial levels.

---

**"Open Challenges in Multi-Agent Security"**

📄 [Paper](https://arxiv.org/abs/2505.02077)

`Multi-Agent` | **Mechanism:** `Coordination Failures` | **Manifestation:** `Emergent Misalignment` `Collusion`

**Abstract:** Introduces multi-agent security as distinct discipline addressing novel threats from intelligent agent interactions including cascading failures and covert coordination.

---

### Multi-Agent Benchmarks

**"Terrarium: Revisiting the Blackboard for Multi-Agent Safety, Privacy, and Security Studies"**

📄 [Paper](https://arxiv.org/abs/2510.14312)

`Multi-Agent` `Benchmark` | **Focus:** `Safety` `Privacy` `Security`

**Abstract:** Modular framework for fine-grained study of safety, privacy, and security in LLM-based multi-agent systems using blackboard architecture.

---

## Detection & Mitigation

### Detection Methods

**"Building and Evaluating Alignment Auditing Agents"**

🌐 [Website](https://alignment.anthropic.com/2025/automated-auditing/)

`Detection` | **Method:** `Automated Auditing`

**Abstract:** LLM-based auditing agents autonomously execute alignment auditing workflows to detect hidden objectives and misaligned behaviors in target models.

---

**"Discovering Language Model Behaviors with Model-Written Evaluations"**

📄 [Paper](https://arxiv.org/abs/2212.09251)

`Detection` | **Method:** `Red Teaming`

**Abstract:** Automated discovery of undesirable behaviors including deception and power-seeking through model-generated evaluation prompts.

---

### Mitigation Techniques

**"Constitutional AI: Harmlessness from AI Feedback"**

📄 [Paper](https://arxiv.org/abs/2212.08073)

`Mitigation` | **Method:** `Alignment Training`

**Abstract:** Self-supervised alignment using AI-generated feedback for harmlessness, though later research shows vulnerability to alignment faking.

---

**"Measuring Progress on Scalable Oversight for Large Language Models"**

📄 [Paper](https://arxiv.org/abs/2211.03540)

`Mitigation` | **Method:** `Oversight`

**Abstract:** Methods for maintaining effective human oversight as agents become increasingly capable and autonomous.

---

**"Adapting Insider Risk mitigations for Agentic Misalignment: an empirical study"**

📄 [Paper](https://arxiv.org/abs/2510.05192)

`Mitigation` | **Method:** `Control & Governance`

**Abstract:** Applies insider-risk management principles to design operational controls steering goal-directed agents toward safe actions.

---

## Resources

- 🔬 **Apollo Research:** https://www.apolloresearch.ai/research
- 🌲 **Redwood Research:** https://www.redwoodresearch.org/
- 🤖 **Anthropic Research:** https://www.anthropic.com/research
- 💬 **AI Alignment Forum:** https://www.alignmentforum.org/
- 🧠 **LessWrong:** https://www.lesswrong.com/
- 📚 **AI Safety Info:** https://aisafety.info/
