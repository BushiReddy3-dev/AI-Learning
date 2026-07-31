# Azure AI Search Fundamentals

## What is Azure AI Search?

Azure AI Search is Microsoft's enterprise search platform.

Provides:

- Keyword Search
- Semantic Search
- Vector Search
- Hybrid Search

---

## Core Components

Data Source
↓
Indexer
↓
Search Index
↓
Search Query
↓
Results

---

## Data Sources

Azure AI Search can read from:

- Azure Blob Storage
- SQL Database
- Cosmos DB
- SharePoint
- ADLS

---

## Search Index

The Search Index is the searchable repository.

Example:

Document

AzureOpenAIGuide.pdf

Fields:

- Title
- Content
- Author
- Project
- CreatedDate

---

## Fields

### Searchable

- Title
- Content

### Filterable

- Department
- Project
- Author

### Sortable

- Created Date

---

## Indexers

Indexers automate data ingestion.

Flow:

Blob Storage
↓
Indexer
↓
Search Index

---

## Skillsets

Skillsets enrich content.

Examples:

- OCR
- Language Detection
- Translation
- Entity Recognition

---

## Semantic Search

Understands meaning.

Question:

How to create Azure OpenAI?

Can match:

Azure OpenAI Deployment Guide

---

## Vector Search

Uses embeddings.

Searches based on meaning.

---

## Hybrid Search

Best practice.

Combines:

Keyword Search
+
Vector Search

---

## Key Learnings

- Azure AI Search is the retrieval layer.
- Indexes store searchable content.
- Indexers automate ingestion.
- Hybrid Search provides best results.