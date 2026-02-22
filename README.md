# LangGraph Search Agent 🚀

An AI Agent built using **LangGraph MessageGraph** that performs intelligent question answering by dynamically planning, searching, and responding using external tools.

---

## 🧠 Project Overview

This project demonstrates a **multi-node AI Agent workflow** where user queries pass through structured reasoning stages:

Planner → Search → Responder

Each stage is implemented as an independent node and orchestrated using **LangGraph’s MessageGraph**, converting Python functions into executable graph nodes.

---

## 🏗️ Architecture

### 1️⃣ Planner Node

* Receives the user question
* Decides whether online search is required
* Generates an optimized search query

### 2️⃣ Search Node

* Executes the query using **Tavily Search API**
* Retrieves real-time web results

### 3️⃣ Responder Node

* Combines:

  * Original user question
  * Search results
* Produces the final natural language answer

---

## 🔄 Graph Workflow

Entry Point → Planner → Search → Responder → END

The workflow is constructed using **MessageGraph**, enabling message-state transitions across nodes.

---

## 🛠️ Tech Stack

* **LangGraph** — Agent workflow orchestration
* **LangChain** — LLM interaction & tooling
* **MessageGraph** — Function → Node conversion
* **Tavily API** — Real-time web search
* **Python** — Core implementation

---

## ⚙️ Key Implementation Concept

Instead of prebuilt agents, this project uses:

* Custom node functions
* Explicit graph edges
* Controlled execution flow

This demonstrates deeper control compared to traditional ReAct-style agents.

---

## 📌 Example Query

> “Who is the current Deputy Chief Minister of Andhra Pradesh?”

### Execution Flow:

1. Planner analyzes the question
2. Generates search query
3. Tavily fetches results
4. Responder synthesizes final answer

---

## 🚀 How to Run

1️⃣ Install dependencies:

```bash
pip install langchain langgraph tavily-python
```

2️⃣ Set environment variables:

```bash
export TAVILY_API_KEY=your_key
export OPENAI_API_KEY=your_key
```

3️⃣ Run notebook cells sequentially.

---

## 📂 Repository Structure

```
langgraph-search-agent/
│
├── langgraph_search_agent.ipynb
└── README.md
```

---

## 🌟 Learning Outcomes

* Building custom AI agents using LangGraph
* Converting functions into graph nodes
* Designing multi-step reasoning workflows
* Tool integration within agent pipelines
* Message state management using MessageGraph

---

## 🔮 Future Improvements

* Conditional routing (Search optional)
* Multi-tool integration
* Memory nodes
* Streaming responses
* Deployment as API / Web App

---
## Author
Purnima Nallamilli  


