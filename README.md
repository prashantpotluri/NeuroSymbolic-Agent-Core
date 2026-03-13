# 🧠 NeuroSymbolic-Agent-Core

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Python 3.10+](https://img.shields.io/badge/python-3.10+-brightgreen.svg)](https://www.python.org/downloads/)
[![Hybrid AI](https://img.shields.io/badge/AI-Neuro--Symbolic-orange.svg)]()
[![Verifiable Reasoning](https://img.shields.io/badge/Reasoning-Verifiable-red.svg)]()

**NeuroSymbolic-Agent-Core** is a high-performance framework for building hybrid AI agents. It seamlessly integrates the creative perception of Large Language Models (Neural) with the rigorous verification of Knowledge Graphs and Symbolic Logic (Symbolic). This approach ensures that agentic actions are not only intelligent but also verifiable and compliant with predefined logic rules.

---

## 🚀 Key Features

- **🎯 Dual-Layer Reasoning:** Combines LLM-based concept extraction with Knowledge Graph-based verification.
- **🔄 Hallucination Mitigation:** Symbolic guardrails prevent agents from executing actions that lack a logical path in the knowledge base.
- **💾 Dynamic Knowledge Base:** Easily add and manage symbolic rules using a directed graph architecture.
- **🛡️ Verifiable Execution:** High-granularity logging of the verification process for every agent action.
- **⚡ Extensible Orchestration:** Modular design allows for easy integration with different LLM providers and reasoning engines.

---

## 🏗️ Architecture

`mermaid
graph TD
    User([User Query]) --> Perception[Neural Perception Layer]
    Perception --> Concept[Extracted Concept/Symbol]
    Concept --> Verification{Symbolic Verification}
    Verification -- Success --> Action[Verified Agent Action]
    Verification -- Failure --> Risk[Unverified Action / Hallucination Alert]
    Verification <--> KB[(Symbolic Knowledge Base)]
`

---

## 🛠️ Project Structure

`	ext
NeuroSymbolic-Agent-Core/
├── src/
│   ├── orchestrator.py  # Core Neuro-Symbolic logic
│   ├── knowledge/       # Knowledge base and rule management
│   └── utils/           # Shared helper functions
├── examples/            # Jupyter notebooks and usage scripts
├── tests/               # Comprehensive logic test suite
└── requirements.txt     # Project dependencies
`

---

## 📖 Quick Start

`python
from src.orchestrator import NeuroSymbolicOrchestrator, SymbolicRule

# 1. Initialize the Orchestrator
agent = NeuroSymbolicOrchestrator()

# 2. Define symbolic rules (Rigid logic)
agent.add_symbolic_rule(SymbolicRule(premise="access_request", conclusion="trigger_auth"))

# 3. Execute a query (Neural perception + Symbolic verification)
result = agent.execute("I need to request access to the system")

print(result) # Output: Agent Action (Verified): trigger_auth
`

---

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---
<p align="center">Developed with ❤️ by <a href="https://github.com/Beto1806">Prashant Potluri</a></p>