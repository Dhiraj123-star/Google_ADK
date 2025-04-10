

# 🧠 Agent Development Kit (ADK)

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](LICENSE)

The **Agent Development Kit (ADK)** empowers developers to build sophisticated AI agents with full control over logic, behavior, and deployment. Designed for deep integration with Google Cloud services, ADK is a code-first framework that prioritizes modularity, extensibility, and local development.

Whether you're crafting simple assistants or complex multi-agent workflows, ADK gives you the tools to build, debug, test, and deploy with confidence—from your laptop to production-grade environments.

---

## ✨ Highlights

- **Code-Driven Agent Design:** Define agent logic, orchestration, tools, and workflows directly in Python for full visibility, testability, and version control.
- **Multi-Agent Support:** Compose specialized agents to work collaboratively, enabling modular, scalable systems.
- **Extensive Tooling Ecosystem:** Use pre-built tools, custom Python functions, or external APIs to extend agent capabilities.
- **Flexible Orchestration:** Combine deterministic workflows with dynamic, LLM-based routing for adaptive agent behavior.
- **Streamlined Developer Experience:** Develop and debug locally with a CLI and integrated web UI.
- **Built-In Evaluation:** Measure agent performance, analyze execution traces, and iterate efficiently.
- **Deployment Flexibility:** Seamlessly containerize and run agents on Vertex AI, Cloud Run, Docker, or any custom environment.
- **Real-Time Interaction:** Native support for streaming inputs and outputs, including text and audio.
- **Memory, State & Artifacts:** Manage short-term memory, long-term state, and file artifacts with ease.
- **Highly Extensible:** Hook into agent behavior with callbacks or integrate third-party services as needed.

---

## 🚀 Installation

Install ADK via pip:

```bash
pip install google-adk
```

---

## 🛠️ Quick Start

Start by creating your agent in `my_agent/agent.py`:

```python
# my_agent/agent.py
from google.adk.agents import Agent
from google.adk.tools import google_search

root_agent = Agent(
    name="search_assistant",
    model="gemini-2.0-flash-exp",  # Replace with your preferred model
    instruction="You are a helpful assistant. Answer user questions using Google Search when needed.",
    description="An assistant capable of searching the web.",
    tools=[google_search]
)
```

Then, initialize the module:

```python
# my_agent/__init__.py
from . import agent
```

To run the agent from the folder **containing** `my_agent`, use:

```bash
adk run my_agent
```

Or launch the visual interface with:

```bash
adk web
```

Explore more in the [Quickstart Guide](https://google.github.io/adk-docs/get-started/quickstart/) or try out some [Sample Agents](https://github.com/google/adk-samples).

---

## 📚 Learn More

- 📖 **[Getting Started](https://google.github.io/adk-docs/get-started/)**
- 🧪 **[Agent Evaluation](https://google.github.io/adk-docs/evaluate/)**
- 🚢 **[Deployment Options](https://google.github.io/adk-docs/deploy/)**
- 🛠️ **[API Reference](https://google.github.io/adk-docs/api-reference/)**
- 💡 **[Example Agents](https://github.com/google/adk-samples)**

---

## 🤝 Contribute

We're always open to community contributions! Check out our [Contributing Guidelines](./CONTRIBUTING.md) for how to get involved—whether it's a bug fix, new feature, or documentation improvement.

---

## 📄 License

Licensed under the [Apache 2.0 License](LICENSE).

---

*Build smarter agents, faster.*

---