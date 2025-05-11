Here is **Week 2** of your advanced AWS Bedrock agent course—**focused on Knowledge Bases, Retrieval-Augmented Generation (RAG), and architecture tuning**—written in **Markdown format** for direct copy-paste or use in docs, Notion, or Obsidian.

---

```markdown
# Week 2: Knowledge Bases and Retrieval-Augmented Agents

## Overview
This week focuses on enabling agents to reason over structured knowledge sources. You will build and test a full RAG pipeline using Amazon Bedrock’s native knowledge base integration and tune for relevance, chunking, and retrieval quality.

---

## Day 1: Knowledge Base Concepts and Setup

### Objectives
- Understand the structure of RAG.
- Create and link a Bedrock knowledge base to your agent.

### Tasks
- 🔗 Read: [Bedrock Knowledge Bases](https://docs.aws.amazon.com/bedrock/latest/userguide/knowledge-base.html)
- 📄 Prepare a dataset (e.g., product catalog, support policies)
- 🗂️ Upload documents to an S3 bucket with proper prefixes
- 📐 Create a knowledge base with:
  - Titan Embeddings
  - Chunk size: 200–300 tokens
- 🔗 Link it to your existing agent

---

## Day 2: DeepLearning.AI Application – Document QA Agent

### Objectives
- Learn how to use KBs in practical applications.
- Apply to real-world support use cases.

### Tasks
- 📺 Watch: DeepLearning.AI Modules 7–8 (Knowledge base walkthrough)
- 🧪 Query your agent with factual questions:
  - "What is the return policy?"
  - "How long does delivery take?"
- ✅ Log:
  - KB hit vs. LLM hallucination
  - Precision of responses
- 🔍 Experiment: What happens when info isn’t in the KB?

---

## Day 3: Chunking Strategy and Relevance Optimization

### Objectives
- Tune chunk sizes and metadata to improve retrieval quality.

### Tasks
- 🧠 Study chunking:
  - Static (by tokens)
  - Semantic (by headings or structure)
- 🛠️ Rechunk documents using custom logic (e.g., Markdown headers)
- 🔁 Re-index your KB with new chunks
- 📊 Evaluate:
  - Short vs. long chunk retrieval accuracy
  - Multi-turn KB memory: ask follow-ups based on prior answer

---

## Day 4: Combining KB + Tool Flows

### Objectives
- Chain retrieval with action group execution in a single agentic flow.

### Tasks
- 🧪 Query design:
  - “What does the warranty say?” (→ KB)
  - “Can you log a warranty claim?” (→ Lambda)
- 🧩 Create a flow that:
  1. Uses KB for retrieval
  2. Validates confidence
  3. Invokes tool if action is required
- ✅ Validate: Does the agent gracefully switch from KB to tool use?

---

## Day 5: Evaluation, Cost Profiling, and Deployment Review

### Objectives
- Measure RAG performance and optimize costs and latency.

### Tasks
- 💸 Log:
  - Latency (p95)
  - Model usage vs retrieval cost
- 📉 Compare Titan vs Cohere embeddings (if possible)
- 🧾 Track usage: 20 retrievals, 10 tool flows
- 📝 Reflection:
  - How well does RAG handle ambiguous queries?
  - What metadata should be added to documents for better precision?

---

## Deliverables for Week 2

- ✅ Agent with linked knowledge base and successful query resolution
- ✅ KB re-indexed with custom chunking strategy
- ✅ Flow that mixes KB retrieval and tool invocation
- ✅ Evaluation log of response quality and architecture diagram
```

