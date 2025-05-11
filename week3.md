Here is **Week 3** of your advanced AWS Bedrock agent course, fully written in **Markdown format**, focusing on **CrewAI orchestration, multi-agent collaboration, and inter-agent workflows**.

---

````markdown
# Week 3: Multi-Agent Orchestration with CrewAI

## Overview
This week introduces CrewAI, an open-source framework for coordinating multiple LLM-powered agents. You’ll design collaborative workflows, assign roles and tools, and use AWS Bedrock as the LLM backend. The focus is on multi-agent flows that combine reasoning, retrieval, and action.

---

## Day 1: Understand CrewAI Concepts and Install Toolkit

### Objectives
- Learn the core abstractions in CrewAI.
- Install and run a minimal CrewAI pipeline.

### Tasks
- 🔗 Read: [CrewAI GitHub](https://github.com/joaomdmoura/crewAI)
- 🔧 Install:
  ```bash
  pip install crewai
````

* 🔎 Study core components:

  * `Agent`: role, goal, tools, memory
  * `Crew`: coordinator that manages agent interaction
  * `Task`: scoped goals and expected outputs
* 🛠️ Run the simple crew example (`crew_simple.py`)
* 📝 Note how task delegation works between agents

---

## Day 2: Define Your Own Agent Crew

### Objectives

* Create a multi-agent system where each agent handles a distinct responsibility.

### Tasks

* 🧠 Define a real-world scenario (e.g., compliance assistant, support triage, document QA).
* 👤 Roles:

  * PlannerAgent (decides flow)
  * RetrieverAgent (queries Bedrock KB or local RAG)
  * ExecutorAgent (calls Bedrock tools or Lambda)
* 🔧 Define each agent with:

  * Goal
  * Allowed tools
  * Bedrock foundation model config (Claude/Titan)
* 📦 Store roles and tools in a `crewai_roles.yaml`

---

## Day 3: Integrate Bedrock with CrewAI via Tool Wrappers

### Objectives

* Wrap Bedrock and AWS SDK functions as callable tools for CrewAI agents.

### Tasks

* 🔌 Create a Python wrapper for:

  * `bedrock-agent` invocation
  * `bedrock-agent start-agent-conversation`
  * S3 retrieval or `boto3` KB query
* ✏️ Register tool in your `tools.py`
* 👁️ Test local tool use by a single agent before multi-agent deployment

---

## Day 4: Build and Execute a Multi-Agent Workflow

### Objectives

* Run a coordinated flow using all three agents.

### Tasks

* 🔄 Create a single task that requires inter-agent collaboration:

  > "Summarize the key points of this compliance document and flag high-risk sections."
* ⚙️ Workflow:

  * Planner assigns subtasks to Retriever and Executor
  * Retriever fetches relevant text from the KB
  * Executor evaluates or annotates it
* 🧪 Run the system end-to-end
* 🧾 Log outputs of each agent’s decisions and result

---

## Day 5: Debugging, Memory, and Flow Robustness

### Objectives

* Ensure stability, clarity, and retry behavior of agent flows.

### Tasks

* 🔄 Test edge cases:

  * Missing KB result
  * Tool failure (simulate Lambda error)
* 💬 Enable memory tracking:

  * Long context window
  * Internal scratchpad logging (CrewAI support)
* 🔍 Add retry logic or fallback planner logic if flow fails
* 📝 Reflect: Where does CrewAI shine? Where does it struggle with Bedrock?

---

## Deliverables for Week 3

* ✅ Working multi-agent CrewAI system integrated with AWS Bedrock
* ✅ Agent definitions + role schema in YAML or Python
* ✅ Tool wrappers for Bedrock and Lambda
* ✅ Logs of at least one real example run with comments

```

