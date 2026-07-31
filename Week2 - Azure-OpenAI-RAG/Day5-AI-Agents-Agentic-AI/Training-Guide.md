# Week 2 Day 5
# AI Agents & Agentic AI Fundamentals

## Objective

Learn:

- What is an AI Agent
- Agent vs RAG
- Agent Architecture
- Tool Calling
- Planning & Reasoning
- Multi-Agent Systems
- Azure AI Foundry Agents
- Copilot Studio Agents

---

# Learning Outcomes

After completing this module you should be able to:

✅ Explain AI Agents

✅ Explain Agent vs RAG

✅ Design Enterprise Agent Architecture

✅ Identify Agent Use Cases

✅ Understand Tool Calling

✅ Understand Multi-Agent Systems

✅ Design Azure-based Agent Solutions

---

# Topic 1 - What Is An AI Agent?

Traditional AI:

User
↓
LLM
↓
Answer

Agent:

User
↓
Agent
↓
Reason
↓
Use Tools
↓
Execute Action
↓
Response

An Agent is:

LLM
+
Memory
+
Planning
+
Tool Calling
+
Execution

---

# Topic 2 - Agent vs RAG

RAG:

Retrieve Information
Generate Answer

Agent:

Retrieve Information
Plan
Execute Tasks
Call Tools
Take Actions

Example:

RAG:

"What is leave policy?"

Returns policy.

Agent:

"Apply leave tomorrow"

Checks leave balance.
Creates leave request.
Sends notification.

---

# Topic 3 - Agent Components

1. LLM

Examples:

- GPT-4o
- GPT-4.1

2. Memory

Stores:

- Context
- Preferences
- Chat history

3. Tools

Examples:

- SQL
- SharePoint
- GitHub
- ServiceNow
- Azure APIs

4. Planner

Creates execution plan.

5. Executor

Runs actions.

---

# Topic 4 - Tool Calling

Example:

User:
Show open incidents.

Agent:

Step 1:
Call Incident API

Step 2:
Retrieve Incidents

Step 3:
Summarize Results

---

# Topic 5 - Multi-Agent Systems

Planner Agent

↓

Research Agent

↓

Data Agent

↓

Reporting Agent

Benefits:

- Scalability
- Better Accuracy
- Independent Responsibilities
- Easier Maintenance

---

# Topic 6 - Azure AI Foundry Agents

Concepts:

- Agents
- Agent Service
- Tool Integration
- Model Selection
- Monitoring
- Evaluation

---

# Topic 7 - Copilot Studio Agents

Low Code Agent Platform

Common Scenarios:

- HR Assistant
- IT Support
- Knowledge Assistant
- Employee Exit Assistant

---

# Topic 8 - Enterprise Agent Architecture

Focus Areas:

- Security
- RBAC
- Managed Identity
- Monitoring
- Responsible AI
- Cost Optimization

---

# Architecture Exercise

Design:

Employee Exit Management Agent

Features:

- Exit Policy Search
- Ticket Creation
- Checklist Generation
- Approval Workflow
- Email Drafting