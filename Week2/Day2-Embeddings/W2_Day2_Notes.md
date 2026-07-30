# Day 2 Notes - Embeddings and Vector Search

## What are Embeddings?

Embeddings are numerical representations of text or other content.

They convert meaning into numbers.

Example:

```text
Azure OpenAI → [0.12, -0.23, 0.89, ...]
```

---

## Why Embeddings are Important

Embeddings help machines understand semantic meaning.

They are used for:

- Similarity search
- Semantic search
- RAG
- Recommendations
- Classification
- Clustering

---

## What is a Vector?

A vector is a list of numbers that represents data.

In AI, vectors represent meaning.

Example:

```text
Azure Service Bus → [0.18, 0.77, -0.21, ...]
```

---

## What is Similarity Search?

Similarity search finds items with similar meaning.

Example:

```text
Question: How to configure Azure Service Bus?
Similar Document: Azure Service Bus setup guide
```

---

## What is Vector Search?

Vector search retrieves documents by comparing embeddings.

Flow:

```text
User Query
 ↓
Embedding Model
 ↓
Query Vector
 ↓
Vector Index
 ↓
Similar Documents
```

---

## What is Azure OpenAI Embeddings?

Azure OpenAI embedding models convert text into vectors.

These vectors can be stored and searched using Azure AI Search.

---

## What is Azure AI Search Vector Search?

Azure AI Search can store and query vectors.

It supports vector search and hybrid search scenarios.

---

## Search Types

| Search Type | Meaning |
|---|---|
| Keyword Search | Matches exact words |
| Semantic Search | Understands meaning |
| Vector Search | Finds similar vectors |
| Hybrid Search | Combines keyword and vector search |

---

## How Embeddings Help RAG

RAG uses embeddings to retrieve relevant documents before asking the GPT model to answer.

Flow:

```text
User Question
 ↓
Embedding
 ↓
Vector Search
 ↓
Relevant Context
 ↓
GPT Model
 ↓
Answer
```

---

## Key Learnings

- Embeddings convert meaning into numbers.
- Vectors represent semantic meaning.
- Vector search finds similar content.
- Azure AI Search can be used as the vector search layer.
- Embeddings are foundational for RAG architecture.
