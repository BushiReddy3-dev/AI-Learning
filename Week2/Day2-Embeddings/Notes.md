# Embeddings and Vector Search

## What are Embeddings?

Embeddings are numerical representations of text.

Example:

Azure OpenAI

becomes:

[0.12, 0.87, -0.45, ...]

Embeddings allow machines to understand meaning.

---

## Why Embeddings Matter

Traditional search uses exact words.

AI search uses meaning.

Example:

car

matches:

- vehicle
- automobile
- transport

---

## What is a Vector?

A vector is a list of numerical values.

Example:

Azure Service Bus

↓

[0.12, 0.34, 0.88 ...]

Vectors represent semantic meaning.

---

## Similarity Search

Find content with similar meaning.

Question:

How do I configure Service Bus?

Can match:

Azure Service Bus Setup Guide

---

## Azure OpenAI Embeddings

Azure OpenAI converts text into vectors.

Flow:

Document
↓
Embedding Model
↓
Vector

---

## Vector Search

Vector Search retrieves documents using vector similarity.

Flow:

Query
↓
Embedding
↓
Vector Search
↓
Relevant Results

---

## Search Types

### Keyword Search

Exact words.

### Semantic Search

Meaning based search.

### Vector Search

Embedding based search.

### Hybrid Search

Keyword + Vector Search.

---

## Key Learnings

- Embeddings convert meaning into numbers.
- Vectors represent meaning.
- Vector Search is the foundation of RAG.
- Azure AI Search supports vector search.