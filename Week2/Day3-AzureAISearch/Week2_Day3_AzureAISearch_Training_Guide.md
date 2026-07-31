# Week 2 - Day 3 Training Guide

# Azure AI Search Deep Dive (Solution Architect Track)

This guide is designed for your AI Solution Architect learning path. It connects Azure OpenAI, Embeddings, Vector Search, and Enterprise Search Architecture so that you can later build complete RAG solutions.

---

# Duration

2 Hours

---

# Learning Objectives

By the end of Week 2 Day 3, you should understand:

- What Azure AI Search is
- Why Azure AI Search is important
- Data Sources
- Search Indexes
- Fields
- Indexers
- Skillsets
- Semantic Search
- Vector Search
- Hybrid Search
- Enterprise Search Architecture
- How Azure AI Search integrates with Azure OpenAI

---

# Why Azure AI Search Matters

Imagine your company has:

- 50,000 Project Documents
- 20,000 Architecture Documents
- 10,000 Support Guides
- 5,000 Runbooks

GPT alone cannot efficiently search all of them.

Azure AI Search provides:

```text
Storage
Search
Indexing
Filtering
Ranking
Retrieval
```

which makes enterprise AI solutions possible.

---

# Day 3 Agenda

| Section | Duration | Activity |
|----------|----------|----------|
| Theory | 60 min | Learn Azure AI Search concepts |
| Hands-On | 45 min | Design enterprise search architecture |
| Assignment | 15 min | Compare search approaches |
| Architect Thinking | Optional | Design enterprise search solution |

---

# Part 1: Theory

## Topic 1 - What is Azure AI Search?

Azure AI Search is Microsoft's enterprise search platform.

It allows organizations to:

- Index Documents
- Search Content
- Rank Results
- Retrieve Relevant Documents

It supports:

```text
Keyword Search
Semantic Search
Vector Search
Hybrid Search
```

---

# Basic Architecture

```text
Documents
     ↓
Azure AI Search
     ↓
Results
```

---

# Enterprise Architecture

```text
Documents
      ↓
Data Source
      ↓
Indexer
      ↓
Search Index
      ↓
Search Query
      ↓
Results
```

---

## Topic 2 - Core Components

Azure AI Search consists of:

```text
Data Source
     ↓
Indexer
     ↓
Search Index
     ↓
Search Query
     ↓
Results
```

Each component has a role.

---

## Topic 3 - Data Sources

Data Source means where the data originates.

Examples:

```text
Azure Blob Storage

Azure SQL Database

Cosmos DB

Data Lake Storage

SharePoint
```

---

### Example

```text
Project PDFs

Stored In

Azure Blob Storage
```

Indexer reads these documents.

---

## Topic 4 - Search Index

The Search Index is the heart of Azure AI Search.

Think of it as:

```text
Searchable Database
```

for enterprise content.

---

### Example Document

```text
AzureOpenAIGuide.pdf
```

Indexed Fields:

```text
DocumentId
Title
Content
Author
ProjectName
CreatedDate
Department
```

---

## Topic 5 - Fields

Fields define what is searchable.

---

### Searchable Fields

```text
Title
Content
Summary
```

Used for searching.

---

### Filterable Fields

```text
Department
Project
Author
```

Used for filters.

---

### Sortable Fields

```text
CreatedDate
ModifiedDate
```

Used for sorting.

---

### Retrievable Fields

Content returned to users.

---

## Topic 6 - Indexers

Indexers automate ingestion.

Instead of manually uploading documents:

```text
Blob Storage
      ↓
Indexer
      ↓
Search Index
```

The index remains updated automatically.

---

### Benefits

- Automated Processing
- Scheduled Updates
- Incremental Loading
- Enterprise Scale

---

## Topic 7 - Skillsets

Skillsets enrich content before indexing.

Examples:

```text
OCR

Translation

Language Detection

Key Phrase Extraction

Entity Recognition
```

---

### Example OCR

```text
PDF Image
     ↓
OCR Skill
     ↓
Extracted Text
     ↓
Search Index
```

---

# Topic 8 - Semantic Search

Traditional Keyword Search:

```text
Azure OpenAI
```

Looks for exact words.

---

Semantic Search understands meaning.

Example:

Query:

```text
How do I deploy Azure OpenAI?
```

May return:

```text
Azure OpenAI Deployment Guide
```

Even if wording differs.

---

# Topic 9 - Vector Search

From Day 2:

```text
Text
   ↓
Embeddings
   ↓
Vector
```

Azure AI Search stores vectors.

Search works using similarity.

---

### Vector Flow

```text
Question
     ↓
Embedding
     ↓
Vector Search
     ↓
Similar Content
```

---

# Topic 10 - Hybrid Search

Enterprise Best Practice.

Combines:

```text
Keyword Search
       +
Vector Search
```

---

### Hybrid Search Architecture

```text
User Query
      ↓

Keyword Search
      ↓

Vector Search
      ↓

Result Merging
      ↓

Final Ranking
```

---

### Why Hybrid Search?

Provides:

✅ Better Accuracy

✅ Better Retrieval

✅ Better User Experience

✅ Enterprise Readiness

---

# Topic 11 - AI Search in RAG

Tomorrow's topic depends on today's understanding.

---

### RAG Flow

```text
User Question
       ↓
Embedding
       ↓
Azure AI Search
       ↓
Relevant Chunks
       ↓
Azure OpenAI
       ↓
Answer
```

---

# Topic 12 - Enterprise Search Architecture

Example:

```text
HR Assistant
```

Documents:

```text
Leave Policy

Travel Policy

Benefits Documentation

HR Guidelines
```

Architecture:

```text
Documents
      ↓
Blob Storage
      ↓
Indexer
      ↓
Azure AI Search
      ↓
Retriever API
      ↓
Azure OpenAI
      ↓
Response
```

---

# Part 2 - Architect View

As an AI Solution Architect, think:

---

## Not

```text
What is an index?
```

---

## Instead Think

```text
How should indexes be designed?

What metadata should be stored?

How is security enforced?

How is cost controlled?

How is retrieval optimized?
```

---

## Architect Design Considerations

### Index Design

Store metadata:

```text
Project
Department
Author
Classification
CreatedDate
```

---

### Security

Users should only retrieve:

```text
Authorized Content
```

---

### Cost Optimization

Monitor:

```text
Storage

Indexer Runs

Queries

Skillset Processing
```

---

### Monitoring

Use:

```text
Azure Monitor

Application Insights
```

---

# Part 3 - Hands-On Activity

## Create Architecture Diagram

Create the following in Draw.io:

```text
Blob Storage
      │
      ▼
Indexer
      │
      ▼
Azure AI Search
      │
      ▼
Retriever API (.NET)
      │
      ▼
Azure OpenAI
      │
      ▼
Response
```

Add:

```text
Entra ID

Key Vault

Azure Monitor
```

to the architecture.

---

# Mini Hands-On Lab

## Scenario

Design:

```text
IDD Tech Knowledge Search
```

Documents:

- Project Documentation
- Runbooks
- Architecture Documents
- Support Guides
- FAQs

---

### Questions

1. Where will documents be stored?

2. How will they be indexed?

3. What metadata should be stored?

4. How will users search?

5. Why choose Hybrid Search?

6. How will Azure AI Search integrate with Azure OpenAI?

---

# Assignment

## Compare Search Models

| Capability | Keyword | Semantic | Vector | Hybrid |
|------------|----------|----------|---------|---------|
| Exact Match | Yes | No | No | Yes |
| Meaning Understanding | No | Yes | Yes | Yes |
| Embedding-Based | No | No | Yes | Yes |
| Enterprise Search | Medium | High | High | Very High |

---

## Questions

### Question 1

What is an Index?

### Question 2

What is an Indexer?

### Question 3

What is a Skillset?

### Question 4

Why is Hybrid Search important?

### Question 5

How does Azure AI Search support RAG?

### Question 6

Which search approach would you recommend for enterprise AI assistants and why?

---

# Architect Exercise

Design:

```text
IDD Tech Knowledge Assistant v2
```

Architecture:

```text
Blob Storage
      ↓
Indexer
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

- Security Controls
- Monitoring Strategy
- Cost Optimization
- Scalability Considerations
- Metadata Design

---

# Learning Outcome

After completing Week 2 Day 3, you should be able to explain:

✅ Azure AI Search

✅ Data Sources

✅ Search Indexes

✅ Fields

✅ Indexers

✅ Skillsets

✅ Semantic Search

✅ Vector Search

✅ Hybrid Search

✅ Enterprise Search Architecture

✅ Azure AI Search Integration with Azure OpenAI

---

# Day 4 Preview

Week 2 Day 4 will cover:

- RAG Deep Dive
- Chunking Strategies
- Retrieval Pipelines
- Grounding
- Hallucinations
- Context Injection
- Enterprise RAG Architecture
- Complete IDD Tech Knowledge Assistant Design

This is one of the most important topics for becoming an AI Solution Architect.