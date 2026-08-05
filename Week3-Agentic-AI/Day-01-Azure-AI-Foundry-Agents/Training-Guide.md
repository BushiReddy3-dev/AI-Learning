# Week 3 Day 1
# Azure AI Foundry Agents

## Objective

Learn:

- Azure AI Foundry Agent Service
- Agent Architecture
- Agent Lifecycle
- Agent Instructions
- Agent Threads
- Tool Integration
- Knowledge Integration
- Enterprise Agent Design

---

# Learning Outcomes

After completing this training you should be able to:

✅ Explain Azure AI Foundry Agent Service

✅ Design Agent Architecture

✅ Understand Threads and Memory

✅ Configure Agent Instructions

✅ Design Knowledge-Based Agents

✅ Design Enterprise AI Solutions

✅ Prepare for Semantic Kernel

✅ Prepare for Microsoft Agent Framework

---

# Topic 1 - What is Azure AI Foundry?

Azure AI Foundry is Microsoft's unified AI platform.

Provides:

- Models
- Agents
- Prompt Flow
- Evaluations
- Monitoring
- Safety Controls

Architecture:

Application
↓
Azure AI Foundry
↓
Models + Agents
↓
Enterprise Systems

---

# Topic 2 - What is an Agent?

Traditional Chatbot:

User
↓
GPT
↓
Answer

Agent:

User
↓
Reasoning
↓
Planning
↓
Tool Calling
↓
Execution
↓
Response

Agent =

LLM
+
Instructions
+
Tools
+
Knowledge
+
Memory

---

# Topic 3 - Azure AI Foundry Agent Components

1. Agent

Behavior definition.

2. Model

Examples:

- GPT-4o
- GPT-4.1
- GPT-4o Mini

3. Instructions

System behavior.

4. Tools

External capabilities.

5. Knowledge

Enterprise documents.

6. Threads

Conversation memory.

---

# Topic 4 - Agent Instructions

Example:

You are an Employee Exit Assistant.

Responsibilities:

- Search exit policy
- Generate handover checklist
- Generate email drafts

Always provide professional responses.

Use enterprise documents when available.

---

# Topic 5 - Agent Threads

Threads store:

- Conversation history
- Context
- User intent

Example:

User:
What is my leave balance?

User:
Apply one day leave.

User:
Notify my manager.

The thread preserves context.

---

# Topic 6 - Agent Lifecycle

Create Agent
↓
Configure Instructions
↓
Add Knowledge
↓
Add Tools
↓
Deploy Agent
↓
Monitor Usage
↓
Improve Agent

---

# Topic 7 - Built-In Tools

Common Tools:

### File Search

Search enterprise documents.

### Knowledge Search

Search indexed knowledge.

### Code