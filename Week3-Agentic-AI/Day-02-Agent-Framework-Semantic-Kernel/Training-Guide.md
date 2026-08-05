# Week 3 Day 2
# Microsoft Agent Framework & Semantic Kernel (.NET Architect Focus)

---

# Learning Objectives

Learn:

- What is Semantic Kernel
- What is Microsoft Agent Framework
- Semantic Kernel Architecture
- Plugins
- Memory
- Function Calling
- AI Services Integration
- Multi-Agent Design
- Enterprise Patterns

---

# Learning Outcomes

After completing this module you should be able to:

✅ Explain Semantic Kernel

✅ Explain Microsoft Agent Framework

✅ Create Plugins

✅ Design AI Applications using SK

✅ Design Multi-Agent Architecture

✅ Build Enterprise AI Solutions in .NET

✅ Prepare for MCP Integration

✅ Prepare for Production Agent Development

---

# Section 1 - Why Semantic Kernel?

Traditional Application:

UI
↓
API
↓
Database

AI Application:

UI
↓
Semantic Kernel
↓
Azure OpenAI
↓
Enterprise Systems

Semantic Kernel acts as the orchestration layer.

---

# Section 2 - What is Semantic Kernel?

Semantic Kernel is Microsoft's open-source SDK for building AI-powered applications.

Supports:

- C#
- Python
- Java

Purpose:

Connect LLMs with:

- Business Logic
- APIs
- Databases
- Enterprise Systems

Architecturally it provides AI orchestration and plugin integration. 【3-50339c】【1-f9a7a6】

---

# Section 3 - Semantic Kernel Architecture

Application
↓
Kernel
↓
AI Services
↓
Plugins
↓
External Systems

Components:

1. Kernel

2. AI Services

3. Plugins

4. Memory

5. Planning

6. Function Calling

---

# Section 4 - Kernel

The central orchestrator.

Responsibilities:

- Manage AI Services
- Manage Plugins
- Handle Prompts
- Execute Functions

Think of it as:

Dependency Injection Container

for AI Applications.

---

# Section 5 - AI Services

Examples:

Azure OpenAI

OpenAI

Anthropic

Future Models

Kernel abstracts model access.

---

# Section 6 - Plugins

Plugins expose business capabilities.

Examples:

EmployeePlugin

LeavePlugin

TicketPlugin

WeatherPlugin

A function may be exposed to the AI model.

Example:

GetEmployeeDetails()

CreateTicket()

CheckLeaveBalance()

Semantic Kernel supports plugin-based orchestration. 【4-e5278e】【5-b15cae】

---

# Section 7 - Function Calling

User:

Create a service ticket.

Process:

LLM
↓
Identify Function
↓
Call Function
↓
Receive Result
↓
Generate Response

This creates Tool-Calling behavior.

---

# Section 8 - Memory

Memory stores:

- Past Conversations
- User Preferences
- Context

Example:

User:
My project is ESG.

Later:

Generate ESG report.

System remembers context.

---

# Section 9 - Semantic Kernel Flow

User
↓
Prompt
↓
Kernel
↓
Model
↓
Plugin Execution
↓
Response

---

# Section 10 - What is Microsoft Agent Framework?

Microsoft Agent Framework is Microsoft's framework for creating AI agents and multi-agent systems. Microsoft documentation describes agent creation, collaboration, orchestration, and workflow capabilities. 【2-7266ce】【1-f9a7a6】

Provides:

- Agent Creation
- Agent Communication
- Multi-Agent Workflows
- Task Orchestration
- Human Interaction

---

# Section 11 - Semantic Kernel vs Agent Framework

Semantic Kernel

Focus:

- AI Orchestration
- Plugins
- Memory
- Prompting

Agent Framework

Focus:

- Agents
- Multi-Agent Systems
- Collaboration
- Workflows

Think:

Semantic Kernel
=
Engine

Agent Framework
=
Agent Ecosystem

This relationship is reflected in Microsoft and community guidance that positions Agent Framework above orchestration and plugin infrastructure. 【5-b15cae】【6-cb8fe3】

---

# Section 12 - Multi-Agent Pattern

User
↓
Orchestrator Agent
↓
├── HR Agent
├── IT Agent
├── ESG Agent
└── Reporting Agent

Benefits:

- Separation of Responsibility
- Scalability
- Better Maintainability
- Reuse

Microsoft training content includes multi-agent solution development scenarios. 【2-7266ce】

---

# Section 13 - Enterprise Pattern

Frontend

- Teams
- Web Portal

Agent Layer

- Orchestrator Agent
- Domain Agents

Knowledge Layer

- Azure AI Search

Business Layer

- HRMS
- ServiceNow
- Azure DevOps

AI Layer

- Azure OpenAI

---

# Section 14 - .NET Architect Example

Employee Exit Assistant

Plugins:

EmployeePlugin

TicketPlugin

NotificationPlugin

Knowledge:

Azure AI Search

Documents:

Exit Policies

Actions:

Create Ticket

Generate Email

Notify Manager

This is where your existing Exit Management POC naturally evolves into an enterprise solution.

---

# Section 15 - Security Architecture

Authentication

Managed Identity

Authorization

RBAC

Secret Management

Key Vault

Networking

Private Endpoints

Monitoring

Application Insights

Azure Monitor

---

# Section 16 - Production Considerations

Monitoring

Audit Logging

Responsible AI

Prompt Governance

Cost Control

Performance Testing

Disaster Recovery

---

# Hands-On Exercise

Design:

Employee Exit Assistant

Requirements:

1. Search Exit Policy

2. Search Handover Checklist

3. Generate Exit Email

4. Create Service Ticket

5. Notify Manager

Create:

- Semantic Kernel Architecture
- Plugin Design
- Agent Architecture

No coding required.

Focus on architecture.

---

# Summary

Semantic Kernel

Provides:

- Plugins
- Memory
- Function Calling
- AI Orchestration

Microsoft Agent Framework

Provides:

- Agents
- Multi-Agent Systems
- Collaboration
- Enterprise Workflows

Together they form the foundation of enterprise AI development in .NET.