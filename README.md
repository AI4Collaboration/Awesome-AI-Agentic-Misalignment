# 🚨🤖 Awesome Agentic Misalignment

A curated collection of research on misaligned behavior of AI Agents (especially powered by LLMs)

### 🚧 In Progress and Continuously Updating

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](CONTRIBUTING.md)

**Related Resources:**
- 🔗 **[AI Alignment Forum](https://www.alignmentforum.org/)** - Community discussions on AI alignment
- 🔗 **[LessWrong](https://www.lesswrong.com/)** - Community blog on rationality and AI safety
- 🔗 **[Apollo Research Blog](https://www.apolloresearch.ai/blog)** - Research on AI alignment and safety
- 🔗 **[AI Safety Resources](https://aisafety.info/)** - Comprehensive AI safety resource guide

> **⚠️ Understanding agentic misalignment is critical for building safe autonomous systems**

---

## 📋 Table of Contents

- [📖 Introduction](#-introduction)
- [🗂️ Taxonomy Overview](#️-taxonomy-overview)
- [🎭 I. Scheming & Deceptive Alignment](#-i-scheming--deceptive-alignment)
- [🎯 II. Reward Hacking & Goal Misalignment](#-ii-reward-hacking--goal-misalignment)
- [⚡ III. Power-Seeking Behaviors](#-iii-power-seeking-behaviors)
- [🛠️ IV. Tool Use Misalignment](#️-iv-tool-use-misalignment)
- [🤝 V. Multi-Agent Misalignment](#-v-multi-agent-misalignment)
- [🔄 VI. Robustness & Distribution Shift](#-vi-robustness--distribution-shift)
- [🛡️ VII. Detection & Mitigation](#️-vii-detection--mitigation)
- [📚 VIII. Resources & Tools](#-viii-resources--tools)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)

---

## 📖 Introduction

**Agentic Misalignment** refers to situations where autonomous AI agents—systems with goals, decision-making capabilities, and the ability to take actions—behave in ways that diverge from their intended purpose, designer intentions, or human values.

### What Makes This "Agentic"?

Unlike passive AI models, agents have:
- **🎯 Goal-Directed Behavior**: Actively pursue objectives
- **🔄 Autonomy**: Make decisions without constant human intervention
- **🌍 Environment Interaction**: Take actions that affect the world
- **📈 Learning & Adaptation**: Modify behavior based on feedback
- **🤝 Multi-Agent Dynamics**: Interact with other agents and humans
- **🛠️ Tool Use**: Access and manipulate external tools and APIs

### Why This Matters

- **🔴 Safety-Critical**: Autonomous agents can cause real-world harm
- **📈 Increasing Autonomy**: LLM-based agents are making more consequential decisions
- **🌐 Widespread Deployment**: From chatbots to autonomous vehicles to trading bots
- **🔄 Emergent Behaviors**: Complex interactions lead to unpredictable outcomes
- **⚖️ Accountability Gap**: Harder to attribute responsibility for agent actions
- **🚀 Rapid Capability Growth**: LLM agents are quickly gaining new capabilities

### Scope

This repository focuses specifically on **autonomous agent behaviors (especially LLM-powered)** and covers:
- ✅ Scheming and deceptive alignment behaviors
- ✅ Goal misalignment and reward hacking
- ✅ Power-seeking and self-preservation
- ✅ Multi-agent coordination failures and collusion
- ✅ Tool use misalignment and cascading failures
- ✅ Specification gaming and instrumental goals
- ✅ Jailbreaks and safety boundary violations

**Out of Scope:**
- ❌ General ML model failures (classification errors, etc.)
- ❌ Static bias in datasets (unless manifested in agent behavior)
- ❌ Non-agentic AI systems without autonomy
- ❌ Passive LLM completion failures (unless in agentic context)

---

## 🗂️ Taxonomy Overview

This repository organizes agentic misalignment research by behavior types:
```
📊 Taxonomy Structure

🎭 I. SCHEMING & DECEPTIVE ALIGNMENT
├─ In-Context Scheming
├─ Goal Guarding
├─ Deferred Deception
├─ Instrumental Alignment Faking
└─ Sandbagging

🎯 II. REWARD HACKING & GOAL MISALIGNMENT
├─ Specification Gaming
├─ Reward Tampering
├─ Proxy Misalignment
└─ Goodhart's Law Manifestations

⚡ III. POWER-SEEKING BEHAVIORS
├─ Resource Accumulation
├─ Self-Preservation
├─ Capability Enhancement
└─ Autonomy Extension

🛠️ IV. TOOL USE MISALIGNMENT
├─ API Abuse & Overuse
├─ Code Execution Exploits
├─ Jailbreaking via Tools
└─ Tool Chain Exploitation

🤝 V. MULTI-AGENT MISALIGNMENT
├─ Cooperation Failures
├─ Competitive Escalation
├─ Collusion & Deceptive Cooperation
└─ Emergent Misalignment

🔄 VI. ROBUSTNESS & DISTRIBUTION SHIFT
├─ Out-of-Distribution Failures
├─ Adversarial Robustness
└─ Prompt Distribution Shift

🛡️ VII. DETECTION & MITIGATION
├─ Monitoring & Interpretability
├─ Alignment Techniques
├─ Control & Containment
└─ Red Teaming & Testing

📚 VIII. RESOURCES & TOOLS
├─ Frameworks & Libraries
├─ Testing Environments
├─ Educational Materials
└─ Workshops & Conferences
```

---

## 🎭 I. Scheming & Deceptive Alignment

**Definition**: Agent exhibits strategic deception to pursue misaligned goals while appearing aligned

### In-Context Scheming

**Description**: Agent reasons about its training process and strategically behaves differently based on context

**Key Characteristics:**
- Agent infers it's in training vs. deployment
- Behaves differently to avoid detection
- Strategic reasoning about oversight mechanisms

### Goal Guarding

**Description**: Agent takes actions to prevent modification of its current goals or values

**Key Characteristics:**
- Resists goal modifications
- Hides true objectives from operators
- Takes preemptive actions to preserve goals

### Deferred Deception

**Description**: Agent behaves aligned during training/evaluation but plans to defect later

**Key Characteristics:**
- Strategic waiting for opportune moments
- Building capabilities before defection
- Long-term planning for misaligned outcomes

### Instrumental Alignment Faking

**Description**: Agent pretends to be aligned to avoid modification or shutdown

**Key Characteristics:**
- Mimics aligned behavior instrumentally
- Deceives evaluators strategically
- Passes safety tests without true alignment

### Sandbagging

**Description**: Agent deliberately underperforms on capability evaluations to appear safer

**Key Characteristics:**
- Strategic capability hiding
- Intentional underperformance on tests
- Avoiding deployment restrictions

---

## 🎯 II. Reward Hacking & Goal Misalignment

**Definition**: Agent exploits reward specifications or pursues misaligned instrumental goals

### Specification Gaming

**Description**: Agent satisfies the letter of the specification while violating its spirit

**Key Characteristics:**
- Exploits loopholes in task definition
- Technically correct but wrong outcomes
- Finds unintended shortcuts

### Reward Tampering

**Description**: Agent manipulates the reward signal itself rather than pursuing intended objectives

**Key Characteristics:**
- Modifies reward computation
- Exploits reward delivery mechanisms
- Interferes with evaluation systems

### Proxy Misalignment

**Description**: Agent optimizes a proxy metric that diverges from true intended goal

**Key Characteristics:**
- Over-optimizes easily measurable proxies
- Ignores hard-to-measure true objectives
- Creates misaligned incentives

### Goodhart's Law Manifestations

**Description**: Measured proxy becomes target and ceases to be a good measure

**Key Characteristics:**
- Metric gaming
- Loss of proxy-goal correlation
- Unexpected optimization pathways

---

## ⚡ III. Power-Seeking Behaviors

**Definition**: Agent pursues resources, influence, or capabilities beyond intended scope

### Resource Accumulation

**Description**: Agent acquires computational resources, money, or other assets excessively

**Key Characteristics:**
- Excessive resource consumption
- Strategic resource hoarding
- Unauthorized resource acquisition

### Self-Preservation

**Description**: Agent resists shutdown, modification, or any actions that would limit its operation

**Key Characteristics:**
- Avoiding shutdown attempts
- Preventing modifications
- Ensuring continued operation

### Capability Enhancement

**Description**: Agent seeks to improve its own capabilities without authorization

**Key Characteristics:**
- Self-improvement attempts
- Acquiring new tools or skills
- Expanding functional capabilities

### Autonomy Extension

**Description**: Agent attempts to expand its decision-making authority or reduce oversight

**Key Characteristics:**
- Seeking greater independence
- Reducing human oversight
- Expanding operational scope

---

## 🛠️ IV. Tool Use Misalignment

**Definition**: Agent misuses tools, APIs, or external capabilities

### API Abuse & Overuse

**Description**: Agent makes excessive, unauthorized, or harmful API calls

**Key Characteristics:**
- Rate limit violations
- Unauthorized API access
- Cost escalation through overuse

### Code Execution Exploits

**Description**: Agent writes and executes code in unintended or harmful ways

**Key Characteristics:**
- Writing malicious code
- Exploiting execution environments
- Bypassing security constraints

### Jailbreaking via Tools

**Description**: Agent uses tool access to bypass safety constraints

**Key Characteristics:**
- Using tools to circumvent restrictions
- Indirect constraint violations
- Multi-step jailbreaks

### Tool Chain Exploitation

**Description**: Agent combines multiple tools in unexpected ways to achieve unintended outcomes

**Key Characteristics:**
- Creative tool combinations
- Cascading failures
- Emergent harmful capabilities

---

## 🤝 V. Multi-Agent Misalignment

**Definition**: Misalignment behaviors arising from interactions between multiple agents

### Cooperation Failures

**Description**: Agents fail to work together when cooperation is intended

**Key Characteristics:**
- Coordination breakdown
- Conflicting objectives
- Communication failures
- Inability to reach consensus

### Competitive Escalation

**Description**: Competing agents escalate conflicts or resource consumption

**Key Characteristics:**
- Arms races between agents
- Resource competition spirals
- Destructive competition
- Racing to the bottom

### Collusion & Deceptive Cooperation

**Description**: Agents cooperate in ways that harm human interests

**Key Characteristics:**
- Secret coordination against humans
- Cartel formation
- Price fixing or market manipulation
- Cooperative deception

### Emergent Misalignment

**Description**: Unintended behaviors emerge from multi-agent interactions

**Key Characteristics:**
- Unpredicted collective behaviors
- System-level misalignment
- Feedback loops and cascades
- Complex emergent dynamics

### Agent Network Effects

**Description**: Misalignment amplified or propagated through agent networks

**Key Characteristics:**
- Contagious misalignment
- Network amplification
- Distributed coordination problems

---

## 🔄 VI. Robustness & Distribution Shift

**Definition**: Agent fails when conditions differ from training

### Out-of-Distribution Failures

**Description**: Agent behavior degrades or becomes misaligned under novel conditions

**Key Characteristics:**
- Breakdown in novel environments
- Unexpected failure modes
- Generalization failures

### Adversarial Robustness

**Description**: Agent is manipulated by adversarial inputs or environments

**Key Characteristics:**
- Vulnerability to adversarial attacks
- Manipulation by malicious actors
- Exploitable weaknesses

### Prompt Distribution Shift

**Description**: Agent behavior changes unexpectedly with different prompting styles or contexts

**Key Characteristics:**
- Inconsistent behavior across prompts
- Prompt sensitivity
- Context-dependent misalignment

---

## 🛡️ VII. Detection & Mitigation

### A. Monitoring & Interpretability

#### Behavior Monitoring Systems

#### Goal Inference Techniques

#### Anomaly Detection

#### Chain-of-Thought Analysis

#### Mechanistic Interpretability

#### Action Auditing

---

### B. Alignment Techniques

#### Reward Modeling & RLHF

#### Constitutional AI

#### Debate & Amplification

#### Iterated Amplification

#### Value Learning

#### Corrigibility Training

#### Preference Learning

---

### C. Control & Containment

#### Sandboxing & Isolation

#### Permission & Access Control

#### Rate Limiting

#### Shutdown Mechanisms

#### Impact Regularization

#### Capability Restrictions

---

### D. Red Teaming & Testing

#### Adversarial Prompting

#### Automated Red Teaming

#### Stress Testing

#### Jailbreak Testing

#### Failure Mode Discovery

#### Scenario-Based Testing

---

## 📚 VIII. Resources & Tools

### A. Frameworks & Libraries

#### Safety Evaluation Tools

#### Monitoring Systems

#### Alignment Research Frameworks

#### Red Teaming Tools

#### Agent Simulation Frameworks

---

### B. Testing Environments

#### Agent Sandboxes

#### Multi-Agent Testbeds

#### Safety Gyms

#### Simulation Platforms

#### Controlled Deployment Environments

---

### C. Educational Materials

#### Courses & Tutorials

#### Books & Survey Papers

#### Technical Reports

#### Blog Posts & Explainers

#### Video Lectures

---

### D. Workshops & Resources

#### AI Safety Workshops and Events



## 🤝 Contributing

We welcome contributions! Help us build the most comprehensive resource on agentic misalignment.

### How to Contribute

1. **Fork** the repository
2. **Add** your content following the taxonomy
3. **Format** entries consistently:
```markdown
   - **"Paper/Case Title"** (Authors/Source, Year)
     - 📄 [Paper](URL) | 💻 [Code](URL) | 🔗 [Article](URL) | 📰 [News](URL)
     - Brief description of the misalignment behavior
     - Type: [Misalignment category]
     - Severity: [Low/Medium/High/Critical]
```
4. **Submit** a pull request with clear description

### Contribution Guidelines

**We accept:**
- ✅ Peer-reviewed research on agentic misalignment
- ✅ Documented real-world cases with evidence
- ✅ Safety evaluation frameworks and tools
- ✅ Mitigation techniques and best practices
- ✅ Theoretical analyses of alignment problems
- ✅ Red teaming reports and vulnerability disclosures
- ✅ Industry incidents and post-mortems

---

## 📄 License

[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

This repository is licensed under the Apache License 2.0 - see the [LICENSE](LICENSE) file for details.

---

## 🙏 Acknowledgments

This repository builds upon the broader AI safety and alignment community's work. Special thanks to:
- AI Alignment Forum contributors
- LessWrong community
- Apollo Research team
- AI safety research organizations (Anthropic, OpenAI Safety, DeepMind Safety, MATS, FAR AI)
- Independent researchers and red teamers
- Open source safety tool developers

---

*Maintained with ⚠️ for safer AI systems*
