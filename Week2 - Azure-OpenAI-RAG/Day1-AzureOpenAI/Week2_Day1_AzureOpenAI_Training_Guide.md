# Week 2 - Day 1 Training Guide

# Azure OpenAI Service & GPT Models

This guide is designed for your AI Solution Architect learning path. It connects your existing experience in .NET, Azure Services, Terraform, Azure DevOps, GitHub Actions, CI/CD, and SQL Server with enterprise Generative AI architecture.

---

# Duration

2 Hours

---

# Learning Objective

By the end of Week 2 Day 1, you should understand:

- What Azure OpenAI Service is
- Why enterprises use Azure OpenAI instead of direct OpenAI APIs
- What GPT models are
- What model deployments are in Azure OpenAI
- What Azure AI Foundry is
- Basic enterprise Azure OpenAI architecture
- Security considerations for Azure OpenAI
- Cost considerations for GPT-based applications
- How to document Azure OpenAI architecture in GitHub

---

# Day 1 Agenda

| Section | Duration | Activity |
|---|---:|---|
| Theory | 60 min | Learn Azure OpenAI, GPT models, deployments, AI Foundry, security, and cost basics |
| Hands-On | 45 min | Create GitHub folder structure, notes, diagrams, and mini lab documentation |
| Assignment | 15 min | Compare OpenAI and Azure OpenAI, answer architect-level questions |
| Optional Architect Thinking | 30 min | Design an IDD Tech Knowledge Assistant concept |

---

# GitHub Folder Structure

Create the following structure in your `AI-Learning` repository:

```text
AI-Learning
│
├── Week1
│
└── Week2
    │
    └── Day1-AzureOpenAI
         │
         ├── README.md
         ├── Notes.md
         ├── Assignment.md
         ├── Architect-Notes.md
         ├── AzureOpenAI-Diagrams.md
         ├── Resources.md
         │
         ├── Diagrams
         │    ├── AzureOpenAI.drawio
         │    └── AzureOpenAI.png
         │
         ├── HandsOn
         │    └── Mini-Lab.md
         │
         └── Screenshots
```

---

# Part 1: Theory

## 1. What is Azure OpenAI?

Azure OpenAI Service provides access to OpenAI models through Microsoft Azure.

Instead of using OpenAI directly:

```text
Application
     ↓
OpenAI API
```

Enterprise applications commonly use Azure OpenAI:

```text
Application
     ↓
Azure OpenAI Service
```

Azure OpenAI allows organizations to use powerful GPT models while integrating with Azure security, monitoring, governance, networking, and enterprise controls.

---

## 2. Why Enterprises Use Azure OpenAI

Enterprise systems usually need more than just a model API. They need security, compliance, governance, and operational control.

Azure OpenAI is useful for enterprises because it can be integrated with:

- Microsoft Entra ID
- Azure RBAC
- Managed Identity
- Azure Monitor
- Private Endpoints
- Azure Key Vault
- Azure networking
- Azure governance policies

---

## 3. Azure OpenAI vs OpenAI

| Capability | OpenAI | Azure OpenAI |
|---|---|---|
| GPT Models | Available | Available through Azure |
| Azure RBAC | Not Azure-native | Supported through Azure roles |
| Managed Identity | Not Azure-native | Common enterprise pattern |
| Private Endpoint | Not Azure-native | Supported in Azure architecture |
| Azure Monitor Integration | Not Azure-native | Can be integrated through Azure monitoring |
| Enterprise Governance | Limited Azure governance | Azure governance friendly |
| Azure Networking | Not Azure-native | Works with Azure network controls |
| Enterprise Architecture Fit | Good for standalone apps | Better for Azure enterprise apps |

---

## 4. What are GPT Models?

GPT stands for:

```text
Generative Pre-trained Transformer
```

GPT models are Large Language Models that can understand and generate text, code, summaries, explanations, and structured responses.

Common model capabilities include:

- Question answering
- Summarization
- Code generation
- Document drafting
- Reasoning
- Chat experiences
- Content transformation

---

## 5. Common GPT Models

### GPT-3.5

Useful for simple, lower-cost text tasks.

Typical use cases:

- Basic Q&A
- Simple summarization
- Basic chatbot responses

---

### GPT-4

Useful for stronger reasoning and higher-quality responses.

Typical use cases:

- Architecture explanation
- Complex reasoning
- Detailed analysis

---

### GPT-4o

Useful for fast, multimodal scenarios.

Typical use cases:

- Enterprise assistants
- Chat applications
- Text and image understanding scenarios
- Low-latency interactions

---

### GPT-4.1

Useful for coding, reasoning, and larger context scenarios.

Typical use cases:

- Code assistance
- Architecture design
- Complex document analysis
- Enterprise solution planning

---

## 6. Model vs Deployment

This is a very important Azure OpenAI concept.

```text
Model is not the same as Deployment
```

### Model

The actual GPT model selected from Azure OpenAI.

Example:

```text
gpt-4o
```

### Deployment

A named deployment of the model inside your Azure OpenAI resource.

Example:

```text
gpt4o-dev
```

or

```text
gpt4o-prod
```

Applications usually call the deployment name, not the raw model name.

Example:

```text
Application → gpt4o-prod deployment → GPT-4o model
```

---

## 7. What is Azure AI Foundry?

Azure AI Foundry is Microsoft's AI engineering platform for building, testing, evaluating, deploying, and managing AI solutions.

It is commonly used for:

- Model access
- Azure OpenAI development
- Prompt engineering
- Prompt flow
- Model evaluation
- AI safety
- Agent development
- Monitoring AI applications

Architect view:

```text
Azure Portal = Infrastructure Management
Azure AI Foundry = AI Development and Engineering
```

---

## 8. Basic Azure OpenAI Architecture

Simple architecture:

```text
User
 │
 ▼
Web Application
 │
 ▼
.NET API
 │
 ▼
Azure OpenAI
 │
 ▼
GPT Deployment
 │
 ▼
Response
```

---

## 9. Enterprise Azure OpenAI Architecture

Enterprise architecture should include security, monitoring, and governance.

```text
User
 │
 ▼
Web Application
 │
 ▼
.NET API
 │
 ▼
Managed Identity
 │
 ▼
Azure OpenAI
 │
 ▼
GPT Deployment
 │
 ▼
Response
```

Supporting services:

```text
Azure Key Vault
Azure Monitor
Application Insights
Microsoft Entra ID
Private Endpoint
Azure RBAC
```

---

## 10. Security Considerations

For enterprise AI solutions, security is very important.

### Authentication

Preferred enterprise pattern:

```text
Managed Identity
```

Avoid hardcoding:

```text
API Keys
```

---

### Authorization

Use:

```text
Azure RBAC
```

---

### Secrets

Store secrets in:

```text
Azure Key Vault
```

---

### Networking

Use private access where required:

```text
Private Endpoint
```

---

### Monitoring

Use:

```text
Azure Monitor
Application Insights
```

---

## 11. Cost Considerations

Azure OpenAI cost is usually related to token usage.

Important concepts:

- Input tokens
- Output tokens
- Model selection
- Prompt size
- Response size
- Number of requests

Cost optimization practices:

- Use the correct model for the task
- Avoid unnecessary long prompts
- Limit output size when possible
- Cache repeated responses when suitable
- Monitor token usage
- Separate development and production deployments

---

## 12. Enterprise Use Cases

### HR Assistant

Answers employee policy questions.

### IT Support Assistant

Answers support and troubleshooting questions.

### Project Copilot

Summarizes project documents, meeting notes, risks, and updates.

### Developer Assistant

Helps with code review, documentation, and technical explanation.

### Knowledge Assistant

Answers questions from company documents using future RAG architecture.

---

# Part 2: Hands-On Activity

## Step 1: Create GitHub Folder

Create:

```text
Week2/Day1-AzureOpenAI
```

Inside it, create:

```text
README.md
Notes.md
Assignment.md
Architect-Notes.md
AzureOpenAI-Diagrams.md
Resources.md
```

Also create folders:

```text
Diagrams
HandsOn
Screenshots
```

---

# README.md

Paste the below content into `README.md`:

```markdown
# Week 2 Day 1 - Azure OpenAI Service and GPT Models

## Topic

Azure OpenAI Service and GPT Models

## Learning Objectives

- Understand Azure OpenAI
- Understand GPT Models
- Understand Model Deployments
- Understand Azure AI Foundry
- Understand Enterprise Azure OpenAI Architecture
- Understand Security and Cost Considerations

## Deliverables

- Notes.md
- Assignment.md
- Architect-Notes.md
- AzureOpenAI-Diagrams.md
- Diagrams/AzureOpenAI.drawio
- Diagrams/AzureOpenAI.png
- HandsOn/Mini-Lab.md
- Resources.md

## Outcome

After this day, I should be able to explain Azure OpenAI and design a basic enterprise AI assistant architecture.
```

---

# Notes.md

Paste the below content into `Notes.md`:

```markdown
# Azure OpenAI Fundamentals

## What is Azure OpenAI?

Azure OpenAI provides OpenAI models through Microsoft Azure.

Organizations use Azure OpenAI to build secure and enterprise-ready AI solutions.

---

## Why Azure OpenAI?

Enterprise requirements include:

- Security
- Compliance
- Governance
- Monitoring
- Private Networking
- RBAC
- Managed Identity

---

## Common GPT Models

### GPT-3.5

Fast and cost-effective for basic tasks.

### GPT-4

Better reasoning and accuracy.

### GPT-4o

Supports multimodal scenarios such as text, image, and audio.

### GPT-4.1

Strong for coding, reasoning, and enterprise architecture scenarios.

---

## Model Deployment

A model is not the same as a deployment.

Example:

Model:
GPT-4o

Deployment:
gpt4o-prod

Applications call the deployment name.

---

## Azure AI Foundry

Azure AI Foundry is used for:

- Models
- Agents
- Prompt Flow
- Evaluations
- Monitoring
- Safety

---

## Key Learnings

- Azure OpenAI is enterprise-ready OpenAI on Azure.
- GPT models are accessed through Azure deployments.
- AI Foundry is used for AI engineering activities.
- Enterprise AI design must include security, monitoring, and cost controls.
```

---

# Assignment.md

Paste the below content into `Assignment.md`:

```markdown
# Day 1 Assignment - Azure OpenAI

## 1. Compare OpenAI and Azure OpenAI

| Feature | OpenAI | Azure OpenAI |
|---|---|---|
| GPT Models | Available | Available through Azure |
| Azure RBAC | Not Azure-native | Supported |
| Managed Identity | Not Azure-native | Common enterprise pattern |
| Private Endpoint | Not Azure-native | Supported in Azure architecture |
| Monitoring | Basic platform monitoring | Azure monitoring compatible |
| Governance | Limited Azure governance | Azure governance friendly |

---

## 2. Questions

Answer the below questions in your own words.

### Question 1

Why do enterprises choose Azure OpenAI?

### Question 2

What is a deployment in Azure OpenAI?

### Question 3

What is the role of Azure AI Foundry?

### Question 4

What security features should be considered for Azure OpenAI?

### Question 5

Which GPT model would you recommend for an enterprise assistant and why?

---

## 3. My Learning

Write your observations here.

Example:

- Azure OpenAI is useful for enterprise AI applications.
- Deployments are important because applications call deployment names.
- Security should include Managed Identity, RBAC, Key Vault, and monitoring.
```

---

# Architect-Notes.md

Paste the below content into `Architect-Notes.md`:

```markdown
# Azure OpenAI Architecture Notes

## Basic Enterprise Architecture

```text
User
 ↓
Web Application
 ↓
.NET API
 ↓
Azure OpenAI
 ↓
GPT Deployment
 ↓
Response
```

---

## Recommended Security Controls

- Microsoft Entra ID for user authentication
- Managed Identity for service-to-service authentication
- Azure RBAC for authorization
- Azure Key Vault for secrets
- Private Endpoint for network isolation
- Azure Monitor and Application Insights for observability

---

## Cost Optimization

- Choose the right model for the scenario
- Reduce unnecessary tokens
- Limit response size
- Cache repeated answers where possible
- Monitor request volume
- Separate dev and prod deployments

---

## Enterprise Use Cases

### HR Assistant

Answers employee policy questions.

### IT Support Assistant

Answers internal support and troubleshooting questions.

### Project Copilot

Summarizes project updates, risks, and documentation.

### Developer Assistant

Assists with code explanation, code review, and documentation.
```

---

# AzureOpenAI-Diagrams.md

Paste the below content into `AzureOpenAI-Diagrams.md`:

```markdown
# Azure OpenAI Architecture Diagrams

## Azure OpenAI Basic Architecture

![Azure OpenAI Architecture](Diagrams/AzureOpenAI.png)

---

## Flow

```text
User
 ↓
Web Application
 ↓
.NET API
 ↓
Azure OpenAI
 ↓
GPT Deployment
 ↓
Response
```

---

## Security Layer

The architecture should include:

- Microsoft Entra ID
- Managed Identity
- Azure RBAC
- Azure Key Vault
- Azure Monitor
- Private Endpoint where required

---

## Learning Outcome

This architecture shows how an enterprise application can connect securely to Azure OpenAI through a backend API layer.
```

---

# Draw.io Diagram Guidance

Create this architecture in Draw.io:

```text
User
 │
 ▼
Web Application
 │
 ▼
.NET API
 │
 ▼
Azure OpenAI
 │
 ▼
GPT-4o Deployment
 │
 ▼
Response
```

Add side security boxes:

```text
Microsoft Entra ID
Managed Identity
Azure Key Vault
Azure Monitor
Private Endpoint
Azure RBAC
```

Save editable file as:

```text
Diagrams/AzureOpenAI.drawio
```

Export image as:

```text
Diagrams/AzureOpenAI.png
```

---

# Resources.md

Paste the below content into `Resources.md`:

```markdown
# Learning Resources

## Microsoft Learn

- Azure OpenAI Service documentation
- Azure AI Foundry documentation
- Azure OpenAI models documentation
- Azure AI architecture guidance

## Topics to Search

- Azure OpenAI overview
- Azure OpenAI models
- Azure OpenAI deployments
- Azure AI Foundry
- Azure OpenAI security
- Azure OpenAI private endpoint
- Azure OpenAI managed identity

## Practice Focus

- Understand model vs deployment
- Understand how .NET applications call Azure OpenAI
- Understand security and cost considerations
```

---

# HandsOn/Mini-Lab.md

Paste the below content into `HandsOn/Mini-Lab.md`:

```markdown
# Mini Lab - Azure OpenAI Assistant Architecture

## Goal

Design a simple AI assistant architecture using Azure OpenAI.

---

## Scenario

Build an AI assistant for IDD Tech.

The assistant should help users with:

- Project questions
- Technical explanations
- Summaries
- Developer assistance

---

## Proposed Architecture

```text
User
 ↓
Web Application
 ↓
.NET API
 ↓
Azure OpenAI
 ↓
GPT Deployment
 ↓
Response
```

---

## Architecture Components

### Web Application

Frontend used by users to ask questions.

### .NET API

Backend service responsible for calling Azure OpenAI.

### Azure OpenAI

Provides GPT model capability.

### GPT Deployment

Named deployment used by the application.

---

## Questions to Answer

### 1. How will users authenticate?

Example answer:

Users can authenticate using Microsoft Entra ID.

### 2. How will the .NET API connect to Azure OpenAI?

Example answer:

The .NET API can use Managed Identity or securely stored credentials.

### 3. Where will secrets be stored?

Example answer:

Secrets should be stored in Azure Key Vault.

### 4. How will usage be monitored?

Example answer:

Application logs and metrics can be monitored using Azure Monitor and Application Insights.

### 5. What model would be selected?

Example answer:

GPT-4o can be considered for enterprise assistant scenarios because it provides strong general-purpose capabilities.

---

## My Design Notes

Write your own design notes here.
```

---

# Optional Weekend Project Preparation

Create:

```text
Week2/Weekend-Project/Project-Idea.md
```

Paste:

```markdown
# Weekend Project Idea - IDD Tech Knowledge Assistant

## Goal

Build a simple AI assistant concept using Azure OpenAI and .NET.

---

## Initial Scope

- User asks a question
- .NET API sends prompt to Azure OpenAI
- Azure OpenAI returns response
- Response is displayed to user

---

## Future Enhancements

- Add Azure AI Search
- Add document ingestion
- Add embeddings
- Add RAG
- Add authentication
- Add monitoring
- Add CI/CD
- Add Terraform deployment

---

## Target Architecture

```text
User
 ↓
React Web App
 ↓
ASP.NET Core API
 ↓
Azure OpenAI
 ↓
Response
```

---

## Why This Project Helps

This project connects AI concepts with your existing skills in .NET, Azure, DevOps, Terraform, and SQL Server.
```

---

# GitHub Commit Message

After adding all files, commit using:

```text
Completed Week2 Day1 Azure OpenAI Fundamentals
```

---

# Day 1 Completion Checklist

- [ ] Created Week2/Day1-AzureOpenAI folder
- [ ] Created README.md
- [ ] Created Notes.md
- [ ] Created Assignment.md
- [ ] Created Architect-Notes.md
- [ ] Created AzureOpenAI-Diagrams.md
- [ ] Created Resources.md
- [ ] Created Diagrams folder
- [ ] Created AzureOpenAI.drawio
- [ ] Exported AzureOpenAI.png
- [ ] Created HandsOn/Mini-Lab.md
- [ ] Created Screenshots folder
- [ ] Committed changes to GitHub

---

# Day 1 Outcome

After completing Week 2 Day 1, you should be able to explain:

- What Azure OpenAI is
- Why enterprises use Azure OpenAI
- Difference between OpenAI and Azure OpenAI
- GPT models
- Model deployments
- Azure AI Foundry
- Basic enterprise architecture
- Security considerations
- Cost considerations
- How to start designing an Azure OpenAI based assistant

---

# Next Day Preview

Week 2 Day 2 will cover:

- Embeddings
- Vectors
- Similarity Search
- Semantic Search
- Vector Databases
- Why embeddings are important for RAG
