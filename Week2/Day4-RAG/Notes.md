# RAG Fundamentals

## What is RAG?

RAG stands for:

Retrieval Augmented Generation

RAG retrieves relevant information before generating an answer.

---

## Why RAG Exists

GPT models do not know:

- Company Documents
- Internal Processes
- Runbooks
- Project Documentation

RAG solves this problem.

---

## RAG Flow

User Question
↓
Search Documents
↓
Retrieve Context
↓
GPT
↓
Answer

---

## Components of RAG

### Retrieval

Find relevant documents.

### Augmentation

Attach retrieved content.

### Generation

Generate final answer.

---

## Chunking

Large documents are divided into smaller sections.

Example:

Employee Handbook

↓

Chunk 1
Chunk 2
Chunk 3

Chunking improves:

- Accuracy
- Performance
- Cost

---

## Embeddings

Chunks are converted into vectors.

Document
↓
Embedding Model
↓
Vector

---

## Retrieval

User Question
↓
Query Embedding
↓
Vector Search
↓
Relevant Chunks

---

## Context Injection

Retrieved chunks are sent to GPT.

Context:
Leave approval requires manager approval.

Question:
How does leave approval work?

---

## Grounding

Grounding means GPT answers only from retrieved data.

This reduces hallucinations.

---

## Hallucinations

AI generates incorrect answers.

Without RAG:

GPT guesses.

With RAG:

GPT reads actual documents.

---

## Key Learnings

- RAG improves accuracy.
- Chunking reduces costs.
- Retrieval finds relevant information.
- Grounding reduces hallucinations.
- Azure AI Search is commonly used as the retrieval layer.