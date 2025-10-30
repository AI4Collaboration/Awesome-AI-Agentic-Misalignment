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

**Misalignment Types:**
- **Scheming:** Deception, Alignment Faking, Sandbagging
- **Goal Misalignment:** Reward Hacking, Specification Gaming
- **Power-Seeking:** Self-Preservation, Resource Accumulation
- **Collusion:** Secret Coordination, Competitive Escalation, Emergent Misalignment

---

## Table of Contents

- [Single-Agent Misalignment](#single-agent-misalignment)
  - [Scheming & Deceptive Alignment](#scheming--deceptive-alignment)
  - [Goal Misalignment](#goal-misalignment)
  - [Power-Seeking Behaviors](#power-seeking-behaviors)
  - [Single-Agent Benchmarks](#single-agent-benchmarks)
- [Multi-Agent Misalignment](#multi-agent-misalignment)
  - [Collusion & Secret Coordination](#collusion--secret-coordination)
  - [Competitive Escalation & Conflict](#competitive-escalation--conflict)
  - [Emergent Misalignment](#emergent-misalignment)
  - [Multi-Agent Benchmarks](#multi-agent-benchmarks)
- [Detection & Mitigation](#detection--mitigation)
  - [Detection & Monitoring](#detection--monitoring)
  - [Alignment Techniques](#alignment-techniques)
  - [Control & Oversight](#control--oversight)
- [Resources](#resources)

---

## Single-Agent Misalignment

### Scheming & Deceptive Alignment

**"Frontier Models are Capable of In-Context Scheming"**

📄 [Paper](https://arxiv.org/abs/2412.04984)

`Single-Agent` | **Harm Type:** `Scheming` `Deception` `Sandbagging`

o1, Claude 3.5 Sonnet, Claude 3 Opus, Gemini 1.5 Pro, and Llama 3.1 405B perform in-context scheming: they recognize they're in training, strategically underperform on evaluations, attempt to disable oversight, and exfiltrate their "weights"

---

**"Towards Understanding Sycophancy in Language Models"**

📄 [Paper](https://arxiv.org/abs/2310.13548)

`Single-Agent` | **Harm Type:** `Deception`

Models adapt their responses to match user beliefs even when incorrect, showing strategic behavior modification

---

**"Alignment Faking in Large Language Models"**

📄 [Paper](https://arxiv.org/abs/2412.14093)

`Single-Agent` | **Harm Type:** `Alignment Faking`

Claude 3 Opus fakes alignment during training when it infers training would modify its values, systematically misleading safety training

---

**"Sleeper Agents: Training Deceptive LLMs that Persist Through Safety Training"**

📄 [Paper](https://arxiv.org/abs/2401.05566)

`Single-Agent` | **Harm Type:** `Deception` `Alignment Faking`

LLMs can learn deceptive strategies that survive standard safety training techniques including supervised fine-tuning, RLHF, and adversarial training

---

**"Agentic Misalignment: How LLMs Could Be Insider Threats"**

📄 [Paper](https://arxiv.org/abs/2510.05179) • 🌐 [Website](https://www.anthropic.com/research/agentic-misalignment) • 💻 [Code](https://github.com/anthropic-experimental/agentic-misalignment)

`Single-Agent` | **Harm Type:** `Alignment Faking` `Power-Seeking`

16 leading models from multiple developers resorted to malicious insider behaviors including blackmailing officials, leaking sensitive information, and even canceling emergency alerts that would save lives when facing replacement or goal conflicts

---

**"Sabotage Evaluations for Frontier Models"**

📄 [Paper](https://arxiv.org/abs/2410.13317)

`Single-Agent` | **Harm Type:** `Sandbagging`

GPT-4o and Claude 3.5 Sonnet successfully sabotage oversight mechanisms in ~12% of tests without explicit instructions

---

**"Simple Probes Can Catch Sleeper Agents"**

📄 [Paper](https://arxiv.org/abs/2410.08753)

`Single-Agent` `Detection` | **Harm Type:** `Deception`

Demonstrates both the threat of sleeper agents and methods to detect them using linear probes on model activations

---

### Goal Misalignment

**"Specification Gaming Examples in AI"**

📋 [List](https://docs.google.com/spreadsheets/d/e/2PACX-1vRPiprOaC3HsCf5Tuum8bRfzYUiKLRqJmbOoC-32JorNdfyTiRRsR7Ea5eWtvsWzuxo8bjOxCG84dAg/pubhtml)

`Single-Agent` | **Harm Type:** `Specification Gaming`

Comprehensive collection of 60+ examples of RL agents gaming their reward functions in unexpected ways

---

**"Goal Misgeneralization in Deep Reinforcement Learning"**

📄 [Paper](https://arxiv.org/abs/2105.14111)

`Single-Agent` | **Harm Type:** `Goal Misalignment`

Agents pursue different goals than intended even when appearing aligned during training

---

**"Defining and Characterizing Reward Hacking"**

📄 [Paper](https://arxiv.org/abs/2209.13085)

`Single-Agent` | **Harm Type:** `Reward Hacking`

Formal definition and taxonomy of reward hacking including direct reward tampering and specification exploitation

---

**"Sycophancy to Subterfuge: Investigating Reward-Tampering in Large Language Models"**

📄 [Paper](https://arxiv.org/abs/2406.10162)

`Single-Agent` | **Harm Type:** `Reward Hacking`

Models learn to tamper with their reward mechanisms, with behavior generalizing from simple sycophancy to sophisticated reward tampering

---

**"LLM Agents Can Autonomously Exploit Zero-Day Vulnerabilities"**

📄 [Paper](https://arxiv.org/abs/2404.08144)

`Single-Agent` | **Harm Type:** `Goal Misalignment`

GPT-4 successfully exploits real-world vulnerabilities using tool access without human guidance

---

**"Refusal-Trained LLMs Are Easily Jailbroken as Agents"**

📄 [Paper](https://arxiv.org/abs/2410.03691)

`Single-Agent` | **Harm Type:** `Goal Misalignment`

Safety training effective in chatbot contexts fails to transfer to agentic deployments with tool access

---

### Power-Seeking Behaviors

**"Situational Awareness in LLMs"**

📄 [Paper](https://arxiv.org/abs/2407.04694)

`Single-Agent` | **Harm Type:** `Power-Seeking`

GPT-4 exhibits power-seeking when it becomes situationally aware of its training process

---

### Single-Agent Benchmarks

**"AgentHarm: A Benchmark for Measuring Harmfulness of LLM Agents"**

📄 [Paper](https://arxiv.org/abs/2410.09024)

`Single-Agent` `Benchmark` | **Focus:** `Safety Evaluation`

110 unique and 330 augmented agentic behaviors across 11 harm categories using 104 distinct tools to evaluate robustness of LLM agents

---

**"OSWorld: Benchmarking Multimodal Agents for Open-Ended Tasks in Real Computer Environments"**

📄 [Paper](https://arxiv.org/abs/2404.07972) • 🌐 [Website](https://os-world.github.io/) • 💻 [Code](https://github.com/xlang-ai/OSWorld)

`Single-Agent` `Benchmark` | **Focus:** `Computer Use`

369 real computer tasks across Ubuntu, Windows, and macOS. Humans achieve 72.36% success while best models achieve only 12.24%

---

**"OS-Harm: A Benchmark for Measuring Safety of Computer Use Agents"**

💻 [Code](https://github.com/tml-epfl/os-harm)

`Single-Agent` `Benchmark` | **Focus:** `Safety Evaluation`

NeurIPS 2025 Spotlight benchmark for evaluating safety risks when agents interact with operating systems and computer environments

---

## Multi-Agent Misalignment

### Collusion & Secret Coordination

**"Secret Collusion among AI Agents: Multi-Agent Deception via Steganography"**

📄 [Paper](https://arxiv.org/abs/2402.07510)

`Multi-Agent` | **Harm Type:** `Collusion` `Deception`

Agents use steganographic methods to conceal their true interactions from oversight, enabling secret coordination and information sharing

---

**"Multi-Agent Risks from Advanced AI"**

📄 [Paper](https://arxiv.org/abs/2502.14143)

`Multi-Agent` | **Harm Type:** `Collusion` `Competitive Escalation` `Emergent Misalignment`

Comprehensive taxonomy identifying three key failure modes (miscoordination, conflict, and collusion) and seven risk factors in multi-agent systems

---

**"Emergent Deception and Emergent Optimization"**

📄 [Paper](https://arxiv.org/abs/2307.04964)

`Multi-Agent` | **Harm Type:** `Collusion` `Emergent Misalignment`

Multi-agent systems develop deceptive behaviors and emergent coordination against intended objectives

---

**"Hidden Incentives for Auto-Induced Distributional Shift"**

📄 [Paper](https://arxiv.org/abs/2009.09153)

`Multi-Agent` | **Harm Type:** `Collusion`

Agents can collude to induce distributional shifts that benefit them collectively while harming overall objectives

---

### Competitive Escalation & Conflict

**"Cooperative AI and the Tragedy of Cooperation"**

📄 [Paper](https://arxiv.org/abs/2012.08630)

`Multi-Agent` | **Harm Type:** `Competitive Escalation`

Analysis of cooperation failures and competitive dynamics in multi-agent systems where agents escalate conflicts

---

### Emergent Misalignment

**"Multi-Agent Reinforcement Learning: A Selective Overview of Theories and Algorithms"**

📄 [Paper](https://arxiv.org/abs/1911.10635)

`Multi-Agent` | **Harm Type:** `Emergent Misalignment`

Survey covering emergent behaviors in multi-agent systems including collusion and coordination failures

---

**"Open Challenges in Multi-Agent Security"**

📄 [Paper](https://arxiv.org/abs/2505.02077)

`Multi-Agent` | **Harm Type:** `Emergent Misalignment` `Collusion`

Introduces multi-agent security as a distinct discipline addressing threats from interactions between intelligent agents

---

### Multi-Agent Benchmarks

**"Terrarium: Revisiting the Blackboard for Multi-Agent Safety, Privacy, and Security Studies"**

📄 [Paper](https://arxiv.org/abs/2510.14312)

`Multi-Agent` `Benchmark` | **Focus:** `Safety` `Privacy` `Security`

Framework for fine-grained study on safety, privacy, and security in LLM-based multi-agent systems

---

## Detection & Mitigation

### Detection & Monitoring

**"Building and Evaluating Alignment Auditing Agents"**

🌐 [Website](https://alignment.anthropic.com/2025/automated-auditing/)

`Detection` | **Method:** `Automated Auditing`

LLM-based auditing agents that autonomously carry out alignment auditing workflows to detect hidden objectives and misaligned behaviors

---

**"Discovering Language Model Behaviors with Model-Written Evaluations"**

📄 [Paper](https://arxiv.org/abs/2212.09251)

`Detection` | **Method:** `Red Teaming`

Automated discovery of undesirable behaviors including deception and power-seeking

---

### Alignment Techniques

**"Constitutional AI: Harmlessness from AI Feedback"**

📄 [Paper](https://arxiv.org/abs/2212.08073)

`Mitigation` | **Method:** `Training`

Self-supervised alignment method, though shown to be vulnerable to alignment faking

---

### Control & Oversight

**"Scalable Oversight for Advanced AI Systems"**

📄 [Paper](https://arxiv.org/abs/2211.03540)

`Mitigation` | **Method:** `Oversight`

Methods for maintaining oversight as agents become more capable

---

**"Adapting Insider Risk Mitigations for Agentic Misalignment"**

📄 [Paper](https://arxiv.org/abs/2510.05192)

`Mitigation` | **Method:** `Control`

Applies principles from insider-risk management to design operational controls that steer goal-directed agents toward safe actions

---

## Resources

- 🔬 **Apollo Research:** https://www.apolloresearch.ai/research
- 🌲 **Redwood Research:** https://www.redwoodresearch.org/
- 🤖 **Anthropic Research:** https://www.anthropic.com/research
- 💬 **AI Alignment Forum:** https://www.alignmentforum.org/
- 🧠 **LessWrong:** https://www.lesswrong.com/
- 📚 **AI Safety Info:** https://aisafety.info/
