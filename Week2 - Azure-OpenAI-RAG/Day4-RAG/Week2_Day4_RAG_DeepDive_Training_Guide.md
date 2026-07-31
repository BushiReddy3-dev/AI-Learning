# Week 2 - Day 4 Training Guide

# RAG Deep Dive (Retrieval Augmented Generation)

## The Most Important Topic for an AI Solution Architect

If someone asks:

> What is the most important concept in Enterprise Generative AI?

The answer is:

```text
RAG (Retrieval Augmented Generation)
```

Most enterprise AI solutions today are built using:

- Enterprise Search
- Knowledge Assistants
- Employee Assistants
- Support Bots
- AI Copilots
- AI Agents

All of these depend on RAG.

---

# Duration

```text
2 Hours
```

---

# Learning Objectives

By the end of Day 4, you should understand:

- RAG
- Why RAG exists
- RAG architecture
- Chunking
- Embeddings
- Retrieval
- Context injection
- Grounding
- Hallucinations
- Enterprise RAG architecture
- Security considerations
- Cost optimization
- End-to-end RAG flow

---

# Why RAG Exists

Imagine a user asks:

```text
What is the IDD Tech PR approval process?
```

GPT cannot answer accurately by itself.

Why?

Because GPT was not trained on:

```text
IDD Tech Documents
Project Runbooks
Support Guides
Architecture Documents
Internal Policies
```

---

# Traditional GPT Problem

```text
User Question
       ↓
GPT
       ↓
Answer
```

Problems:

- No company knowledge
- No access to documents
- Hallucinations
- Outdated answers

---

# Solution

Retrieve company information before asking GPT.

```text
Retrieval
Augmented
Generation
```

---

# What is RAG?

RAG has three parts.

---

## Retrieval

Find relevant information.

Example:

```text
Search Project Documentation
```

---

## Augmentation

Attach documents to the prompt.

Example:

```text
User Question
      +
Relevant Documents
```

---

## Generation

Generate the final answer.

GPT now uses:

```text
User Question
+
Retrieved Content
```

---

# Simple RAG Architecture

```text
User Question
      ↓
Search Documents
      ↓
Relevant Content
      ↓
GPT
      ↓
Answer
```

---

# Traditional GPT vs RAG

## Traditional GPT

```text
Question
     ↓
GPT
     ↓
Answer
```

Problem:

```text
No Internal Knowledge
```

---

## RAG

```text
Question
      ↓
Document Search
      ↓
Context Retrieval
      ↓
GPT
      ↓
Answer
```

Benefits:

- Company knowledge
- Better accuracy
- Current information
- Reduced hallucinations

---

# Complete Enterprise RAG Architecture

```text
Documents
      ↓

Chunking
      ↓

Embeddings
      ↓

Azure AI Search
      ↓

User Question
      ↓

Question Embedding
      ↓

Vector Search
      ↓

Relevant Chunks
      ↓

Azure OpenAI
      ↓

Answer
```

---

# Topic 1 - Chunking

One of the most important concepts.

---

## Problem

Document:

```text
Employee Handbook

500 Pages
```

Cannot send entire document.

---

## Solution

Split document.

```text
Chunk 1

Chunk 2

Chunk 3

Chunk 4
```

---

# Example

Document:

```text
Travel Policy
```

becomes:

```text
Chunk 1
Introduction

Chunk 2
Travel Requests

Chunk 3
Approvals

Chunk 4
Reimbursements
```

---

# Why Chunking?

Benefits:

- Faster
- Lower cost
- Better retrieval
- Better answers
- Better search accuracy

---

# Topic 2 - Embedding Pipeline

Documents become vectors.

```text
Document
      ↓
Chunking
      ↓
Embedding Model
      ↓
Vector
      ↓
Vector Index
```

---

# Example

```text
Project Document
      ↓
Chunking
      ↓
Azure OpenAI Embeddings
      ↓
Vectors
      ↓
Azure AI Search
```

---

# Topic 3 - Retrieval

User asks:

```text
How does leave approval work?
```

System performs:

```text
Question
      ↓
Embedding
      ↓
Vector Search
      ↓
Relevant Chunks
```

Output:

```text
Leave Policy Section
```

---

# Topic 4 - Context Injection

Retrieved content is injected into GPT.

Example:

```text
Context:

Leave approval requires manager approval.

Question:

How does leave approval work?
```

GPT answer:

```text
Based on retrieved content,
manager approval is required.
```

---

# Topic 5 - Grounding

Grounding means:

```text
Only answer from retrieved content.
```

Without grounding:

```text
GPT guesses.
```

With grounding:

```text
GPT uses actual documents.
```

Benefits:

- Accuracy
- Reliability
- Trust

---

# Topic 6 - Hallucinations

Hallucination means:

```text
AI confidently generates
incorrect information.
```

---

# Example

Question:

```text
What is our reimbursement policy?
```

Without RAG:

```text
GPT may invent an answer.
```

With RAG:

```text
GPT reads company policy.
```

Result:

- More accurate
- Less hallucination

---

# Topic 7 - Enterprise RAG Architecture

```text
SharePoint
Blob Storage
SQL
PDF Files
Word Documents
      ↓

Document Processing
      ↓

Chunking
      ↓

Azure OpenAI Embeddings
      ↓

Azure AI Search
      ↓

Retriever API (.NET)
      ↓

Azure OpenAI GPT
      ↓

Application
```

---

# Architect View

A developer asks:

```text
What is RAG?
```

A Solution Architect asks:

```text
Where does data come from?

How will documents be chunked?

Where will embeddings be stored?

How will access be controlled?

How is monitoring implemented?

How is cost optimized?

How is security enforced?
```

---

# Security Architecture

Always include security in enterprise RAG design.

---

## Authentication

```text
Microsoft Entra ID
```

---

## Authorization

```text
Azure RBAC
```

---

## Secrets

```text
Azure Key Vault
```

---

## Monitoring

```text
Azure Monitor

Application Insights
```

---

## Network Security

```text
Private Endpoint
```

---

# Cost Optimization

Avoid:

```text
Sending entire 100-page documents
to GPT
```

Use:

```text
Chunking
```

Benefits:

- Lower token usage
- Faster responses
- Lower cost
- Better accuracy

---

# RAG vs Fine Tuning

## RAG

Uses:

```text
External Data
```

Best for:

- Document Search
- Knowledge Assistants
- Internal Policies
- Enterprise Search

---

## Fine Tuning

Changes:

```text
Model Behavior
```

Best for:

- Specialized output style
- Domain-specific writing style

---

# Enterprise Recommendation

Most customers should start with:

```text
RAG
```

before considering:

```text
Fine Tuning
```

---

# Mini Hands-On Activity

Create this architecture in Draw.io:

```text
Documents
      ↓
Chunking
      ↓
Azure OpenAI Embeddings
      ↓
Azure AI Search
      ↓
Retriever API (.NET)
      ↓
Azure OpenAI GPT
      ↓
Response
```

Save editable diagram as:

```text
Diagrams/RAG.drawio
```

Export image as:

```text
Diagrams/RAG.png
```

---

# Mini Lab

Scenario:

```text
IDD Tech Knowledge Assistant
```

Data sources:

- Project Documentation
- Support Guides
- Architecture Documents
- Runbooks
- FAQs

Design layers:

```text
Storage Layer

Search Layer

AI Layer

Application Layer
```

---

# Assignment

Answer the following questions in your own words.

## Q1

What is RAG?

## Q2

Why is RAG needed?

## Q3

What is Chunking?

## Q4

What is Grounding?

## Q5

What is Context Injection?

## Q6

How does RAG reduce hallucinations?

## Q7

Why is Azure AI Search used?

## Q8

Why is chunking important?

---

# Architect Exercise

Design:

```text
IDD Tech Knowledge Assistant v3
```

Architecture:

```text
Blob Storage
      ↓
Chunking
      ↓
Embeddings
      ↓
Azure AI Search
      ↓
Retriever API
      ↓
Azure OpenAI
      ↓
Web Application
```

Identify:

- Security controls
- Cost optimization
- Monitoring
- Retrieval strategy
- Metadata strategy

---

# Learning Outcome

After Day 4, you should confidently explain:

- RAG
- Chunking
- Embeddings
- Retrieval
- Context injection
- Grounding
- Hallucinations
- Enterprise RAG architecture
- Security considerations
- Cost optimization
- End-to-end knowledge assistant design

---

# Week 2 Day 5 Preview

Day 5 will cover:

- AI Agents and Agentic Architecture
- Agent vs RAG
- Tool Calling
- Agent Memory
- Agent Planning
- Multi-Agent Systems
- Azure AI Foundry Agents
- Copilot Studio Agents
- Enterprise Agent Architecture

This completes the core foundation required for an AI Solution Architect before moving into Copilot Studio, Semantic Kernel, AI Foundry, and Enterprise AI Projects.
