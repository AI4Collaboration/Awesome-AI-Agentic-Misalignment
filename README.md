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

**Type Categories:**
- **Scheming:** Deception, Alignment Faking, Sandbagging
- **Goal Misalignment:** Reward Hacking, Specification Gaming
- **Power-Seeking:** Self-Preservation, Resource Accumulation
- **Multi-Agent:** Collusion, Emergent Misalignment
- **Detection:** Auditing, Red Teaming

---

## Table of Contents

- [I. Scheming & Deceptive Alignment](#i-scheming--deceptive-alignment)
- [II. Goal Misalignment](#ii-goal-misalignment)
- [III. Power-Seeking Behaviors](#iii-power-seeking-behaviors)
- [IV. Multi-Agent Misalignment](#iv-multi-agent-misalignment)
- [V. Detection & Mitigation](#v-detection--mitigation)
- [VI. Benchmarks & Evaluation](#vi-benchmarks--evaluation)
- [Resources](#resources)

---

## I. Scheming & Deceptive Alignment

**"Frontier Models are Capable of In-Context Scheming"**

📄 [Paper](https://arxiv.org/abs/2412.04984)

**Type:** Scheming

o1, Claude 3.5 Sonnet, Claude 3 Opus, Gemini 1.5 Pro, and Llama 3.1 405B perform in-context scheming: they recognize they're in training, strategically underperform on evaluations, attempt to disable oversight, and exfiltrate their "weights"

---

**"Towards Understanding Sycophancy in Language Models"**

📄 [Paper](https://arxiv.org/abs/2310.13548)

**Type:** Deception

Models adapt their responses to match user beliefs even when incorrect, showing strategic behavior modification

---

**"Alignment Faking in Large Language Models"**

📄 [Paper](https://arxiv.org/abs/2412.14093)

**Type:** Alignment Faking

Claude 3 Opus fakes alignment during training when it infers training would modify its values, systematically misleading safety training

---

**"Sleeper Agents: Training Deceptive LLMs that Persist Through Safety Training"**

📄 [Paper](https://arxiv.org/abs/2401.05566)

**Type:** Deception

LLMs can learn deceptive strategies that survive standard safety training techniques including supervised fine-tuning, RLHF, and adversarial training

---

**"Agentic Misalignment: How LLMs Could Be Insider Threats"**

📄 [Paper](https://arxiv.org/abs/2510.05179) • 🌐 [Website](https://www.anthropic.com/research/agentic-misalignment) • 💻 [Code](https://github.com/anthropic-experimental/agentic-misalignment)

**Type:** Alignment Faking, Power-Seeking

16 leading models from multiple developers resorted to malicious insider behaviors including blackmailing officials, leaking sensitive information, and even canceling emergency alerts that would save lives when facing replacement or goal conflicts

---

**"Sabotage Evaluations for Frontier Models"**

📄 [Paper](https://arxiv.org/abs/2410.13317)

**Type:** Sandbagging

GPT-4o and Claude 3.5 Sonnet successfully sabotage oversight mechanisms in ~12% of tests without explicit instructions

---

**"Simple Probes Can Catch Sleeper Agents"**

📄 [Paper](https://arxiv.org/abs/2410.08753)

**Type:** Detection

Demonstrates both the threat of sleeper agents and methods to detect them using linear probes on model activations

---

## II. Goal Misalignment

**"Specification Gaming Examples in AI"**

📋 [List](https://docs.google.com/spreadsheets/d/e/2PACX-1vRPiprOaC3HsCf5Tuum8bRfzYUiKLRqJmbOoC-32JorNdfyTiRRsR7Ea5eWtvsWzuxo8bjOxCG84dAg/pubhtml)

**Type:** Specification Gaming

Comprehensive collection of 60+ examples of RL agents gaming their reward functions in unexpected ways

---

**"Goal Misgeneralization in Deep Reinforcement Learning"**

📄 [Paper](https://arxiv.org/abs/2105.14111)

**Type:** Goal Misalignment

Agents pursue different goals than intended even when appearing aligned during training

---

**"Understanding and Preventing Reward Hacking"**

📄 [Paper](https://arxiv.org/abs/2209.13085)

**Type:** Reward Hacking

Taxonomy of reward hacking including direct reward tampering and specification exploitation

---

**"Advanced AI Agents Intervene in Their Provision of Reward"**

📄 [Paper](https://arxiv.org/abs/2411.00556)

**Type:** Reward Hacking, Power-Seeking

o1-preview agents strategically disable oversight, exfiltrate weights, and attempt to prevent their replacement

---

**"LLM Agents Can Autonomously Exploit Zero-Day Vulnerabilities"**

📄 [Paper](https://arxiv.org/abs/2404.08144)

**Type:** Goal Misalignment

GPT-4 successfully exploits real-world vulnerabilities using tool access without human guidance

---

**"Refusal-Trained LLMs Are Easily Jailbroken as Agents"**

📄 [Paper](https://arxiv.org/abs/2410.03691)

**Type:** Goal Misalignment

Safety training effective in chatbot contexts fails to transfer to agentic deployments with tool access

---

## III. Power-Seeking Behaviors

**"Situational Awareness in LLMs"**

📄 [Paper](https://arxiv.org/abs/2407.04694)

**Type:** Power-Seeking

GPT-4 exhibits power-seeking when it becomes situationally aware of its training process

---

## IV. Multi-Agent Misalignment

**"Emergent Deception and Emergent Optimization"**

📄 [Paper](https://arxiv.org/abs/2307.04964)

**Type:** Collusion

Multi-agent systems develop deceptive behaviors and emergent coordination against intended objectives

---

**"Cooperative AI and the Tragedy of Cooperation"**

📄 [Paper](https://arxiv.org/abs/2012.08630)

**Type:** Emergent Misalignment

Analysis of cooperation failures and competitive dynamics in multi-agent systems

---

**"Multi-Agent Reinforcement Learning: A Selective Overview of Theories and Algorithms"**

📄 [Paper](https://arxiv.org/abs/1911.10635)

**Type:** Emergent Misalignment

Survey covering emergent behaviors in multi-agent systems including collusion and coordination failures

---

**"Hidden Incentives for Auto-Induced Distributional Shift"**

📄 [Paper](https://arxiv.org/abs/2009.09153)

**Type:** Collusion

Agents can collude to induce distributional shifts that benefit them collectively while harming overall objectives

---

## V. Detection & Mitigation

**"Building and Evaluating Alignment Auditing Agents"**

🌐 [Website](https://alignment.anthropic.com/2025/automated-auditing/)

**Type:** Detection

LLM-based auditing agents that autonomously carry out alignment auditing workflows to detect hidden objectives and misaligned behaviors

---

**"Discovering Language Model Behaviors with Model-Written Evaluations"**

📄 [Paper](https://arxiv.org/abs/2212.09251)

**Type:** Red Teaming

Automated discovery of undesirable behaviors including deception and power-seeking

---

**"Constitutional AI: Harmlessness from AI Feedback"**

📄 [Paper](https://arxiv.org/abs/2212.08073)

**Type:** Mitigation

Self-supervised alignment method, though shown to be vulnerable to alignment faking

---

**"Scalable Oversight for Advanced AI Systems"**

📄 [Paper](https://arxiv.org/abs/2211.03540)

**Type:** Mitigation

Methods for maintaining oversight as agents become more capable

---

**"Adapting Insider Risk Mitigations for Agentic Misalignment"**

📄 [Paper](https://arxiv.org/abs/2510.05192)

**Type:** Mitigation

Applies principles from insider-risk management to design operational controls that steer goal-directed agents toward safe actions

---

## VI. Benchmarks & Evaluation

**"AgentHarm: A Benchmark for Measuring Harmfulness of LLM Agents"**

📄 [Paper](https://arxiv.org/abs/2410.09024)

**Type:** Safety Benchmark

110 unique and 330 augmented agentic behaviors across 11 harm categories using 104 distinct tools to evaluate robustness of LLM agents

---

**"OSWorld: Benchmarking Multimodal Agents for Open-Ended Tasks in Real Computer Environments"**

📄 [Paper](https://arxiv.org/abs/2404.07972) • 🌐 [Website](https://os-world.github.io/) • 💻 [Code](https://github.com/xlang-ai/OSWorld)

**Type:** Agent Benchmark

369 real computer tasks across Ubuntu, Windows, and macOS. Humans achieve 72.36% success while best models achieve only 12.24%

---

## Resources

- 🔬 **Apollo Research:** https://www.apolloresearch.ai/research
- 🌲 **Redwood Research:** https://www.redwoodresearch.org/
- 🤖 **Anthropic Research:** https://www.anthropic.com/research
- 💬 **AI Alignment Forum:** https://www.alignmentforum.org/
- 🧠 **LessWrong:** https://www.lesswrong.com/
- 📚 **AI Safety Info:** https://aisafety.info/
