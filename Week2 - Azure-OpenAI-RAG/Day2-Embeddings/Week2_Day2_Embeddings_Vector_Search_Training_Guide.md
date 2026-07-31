# Week 2 - Day 2 Training Guide

# Embeddings, Vectors, Similarity Search & Vector Search Foundations

This guide is designed for your AI Solution Architect learning path. It connects your existing experience in .NET, Azure Services, Terraform, Azure DevOps, GitHub Actions, CI/CD, and SQL Server with the foundation required for RAG, Azure AI Search, enterprise knowledge assistants, and AI Agents.

---

# Duration

2 Hours

---

# Learning Objective

By the end of Week 2 Day 2, you should understand:

- What embeddings are
- What vectors are
- Why embeddings are important in Generative AI
- How semantic similarity works
- What vector search is
- Why vector search is important for RAG
- How Azure OpenAI embedding models are used
- How Azure AI Search supports vector search
- Difference between keyword search, semantic search, vector search, and hybrid search
- Basic architecture for embedding-based search
- How to document embedding and vector search architecture in GitHub

---

# Day 2 Agenda

| Section | Duration | Activity |
|---|---:|---|
| Theory | 60 min | Learn embeddings, vectors, similarity search, vector search, semantic search, and hybrid search |
| Hands-On | 45 min | Create GitHub folder structure, notes, diagram, and mini lab documentation |
| Assignment | 15 min | Compare search approaches and design a small semantic search concept |
| Optional Architect Thinking | 30 min | Extend IDD Tech Knowledge Assistant with embeddings and vector search |

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
    ├── Day1-AzureOpenAI
    │
    └── Day2-Embeddings
         │
         ├── README.md
         ├── Notes.md
         ├── Assignment.md
         ├── Architect-Notes.md
         ├── Embeddings-Diagrams.md
         ├── Resources.md
         │
         ├── Diagrams
         │    ├── Embeddings.drawio
         │    └── Embeddings.png
         │
         ├── HandsOn
         │    └── Mini-Lab.md
         │
         └── Screenshots
```

---

# Part 1: Theory

## 1. What are Embeddings?

Embeddings are numerical representations of content such as text, documents, images, or audio.

In simple words:

```text
Text → Numbers
```

Example:

```text
Azure OpenAI
```

can be represented as:

```text
[0.12, -0.23, 0.89, 0.44, ...]
```

These numbers capture meaning. Similar text will have similar vectors.

---

## 2. Why Embeddings are Important

Traditional systems search using exact words.

Example:

```text
Search query: "car"
```

A keyword search may not match:

```text
automobile
vehicle
transport
```

Embeddings help search by meaning, not only by exact keywords.

Example:

```text
car ≈ automobile ≈ vehicle
```

This is why embeddings are important for:

- Semantic search
- RAG systems
- Recommendation systems
- Classification
- Clustering
- Enterprise knowledge assistants

---

## 3. What is a Vector?

A vector is a list of numbers.

In AI systems, a vector represents the meaning of a piece of data.

Example:

```text
"Azure Service Bus" → [0.18, 0.77, -0.21, 0.56, ...]
```

The number of values in a vector is called dimensions.

Example:

```text
1536 dimensions
3072 dimensions
```

More dimensions can capture more semantic meaning, but may increase storage and compute cost.

---

## 4. What is Similarity Search?

Similarity search is the process of finding items whose vectors are close to each other.

Example:

```text
Question:
How do I configure Azure Service Bus?

Similar document:
Steps to create and configure Azure Service Bus namespace
```

The words are not exactly the same, but the meaning is similar.

---

## 5. Common Similarity Measures

### Cosine Similarity

Measures the angle between two vectors.

Used often for text similarity.

### Euclidean Distance

Measures straight-line distance between two vectors.

### Dot Product

Measures vector alignment and magnitude.

For solution architecture, you do not need to implement the math deeply on Day 2. You mainly need to understand that these techniques help find similar meaning.

---

## 6. What is Vector Search?

Vector search retrieves content based on vector similarity.

Simple flow:

```text
User Query
    ↓
Embedding Model
    ↓
Query Vector
    ↓
Vector Database / Vector Index
    ↓
Similar Documents
```

---

## 7. What is Azure OpenAI Embeddings?

Azure OpenAI embedding models convert text into embedding vectors.

Example:

```text
Input Text
    ↓
Azure OpenAI Embedding Model
    ↓
Vector
```

These vectors can then be stored in a vector database or Azure AI Search index.

---

## 8. What is Azure AI Search Vector Search?

Azure AI Search supports vector search by indexing and querying numeric representations of content.

It can be used as the retrieval layer for enterprise AI solutions and RAG applications.

Azure AI Search can support:

- Similarity search
- Vector search
- Hybrid search
- Multilingual search
- Multimodal search
- Filtered vector search

---

## 9. Keyword Search vs Vector Search vs Hybrid Search

| Search Type | How It Works | Best For |
|---|---|---|
| Keyword Search | Matches exact words | Exact term search |
| Semantic Search | Understands meaning using language models | Better ranking and understanding |
| Vector Search | Finds similar vectors | Meaning-based retrieval |
| Hybrid Search | Combines keyword and vector search | Enterprise RAG and knowledge search |

---

## 10. Why Hybrid Search Matters

Enterprise documents often need both:

```text
Exact keyword match
+
Semantic meaning match
```

Example:

A user may search:

```text
How do I approve PR?
```

Relevant documents may contain:

```text
Pull Request approval process
Code review approver workflow
Repository reviewer group
```

Hybrid search improves retrieval by combining keyword and vector-based relevance.

---

## 11. How Embeddings Power RAG

RAG means Retrieval-Augmented Generation.

Embeddings help retrieve relevant company content before sending context to the LLM.

RAG flow:

```text
User Question
      ↓
Convert Question to Embedding
      ↓
Search Similar Chunks
      ↓
Retrieve Relevant Context
      ↓
Send Context + Question to GPT Model
      ↓
Generate Grounded Answer
```

---

## 12. Enterprise Example: IDD Tech Knowledge Assistant

Current simple architecture from Day 1:

```text
User
 ↓
Web App
 ↓
.NET API
 ↓
Azure OpenAI
 ↓
Response
```

Day 2 enhanced architecture:

```text
Project Documents
      ↓
Chunking
      ↓
Azure OpenAI Embeddings
      ↓
Azure AI Search Vector Index
      ↓
.NET API Retrieval
      ↓
Azure OpenAI GPT Model
      ↓
Answer
```

---

# Part 2: Hands-On Activity

## Step 1: Create Day 2 Folder

Create:

```text
Week2/Day2-Embeddings
```

Inside it, create:

```text
README.md
Notes.md
Assignment.md
Architect-Notes.md
Embeddings-Diagrams.md
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
# Week 2 Day 2 - Embeddings and Vector Search

## Topic

Embeddings, Vectors, Similarity Search, and Vector Search Foundations

## Learning Objectives

- Understand embeddings
- Understand vectors
- Understand similarity search
- Understand Azure OpenAI embedding models
- Understand Azure AI Search vector search
- Understand keyword, semantic, vector, and hybrid search
- Understand why embeddings are important for RAG

## Deliverables

- Notes.md
- Assignment.md
- Architect-Notes.md
- Embeddings-Diagrams.md
- Diagrams/Embeddings.drawio
- Diagrams/Embeddings.png
- HandsOn/Mini-Lab.md
- Resources.md

## Outcome

After this day, I should be able to explain how embeddings and vector search help build enterprise RAG systems.
```

---

# Notes.md

Paste the below content into `Notes.md`:

```markdown
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
```

---

# Assignment.md

Paste the below content into `Assignment.md`:

```markdown
# Day 2 Assignment - Embeddings and Vector Search

## 1. Compare Search Types

| Search Type | How It Works | Example | Best For |
|---|---|---|---|
| Keyword Search | Matches exact words | Search "Azure OpenAI" | Exact-match search |
| Semantic Search | Understands meaning | "car" and "automobile" | Meaning-based search |
| Vector Search | Compares embeddings | Similar document retrieval | RAG retrieval |
| Hybrid Search | Combines keyword and vector | Enterprise search | Production RAG systems |

---

## 2. Questions

Answer the below questions in your own words.

### Question 1

What is an embedding?

### Question 2

Why do embeddings help in semantic search?

### Question 3

What is a vector?

### Question 4

What is vector search?

### Question 5

Why is hybrid search useful in enterprise RAG applications?

---

## 3. Practical Scenario

Design a search flow for IDD Tech Knowledge Assistant.

Requirements:

- Users ask project-related questions
- Project documents are stored in a knowledge base
- System should return relevant document chunks
- GPT model should generate final answer

Write the high-level flow below.

```text
User Question
 ↓
Convert Question to Embedding
 ↓
Search Similar Documents
 ↓
Retrieve Context
 ↓
Send Context to GPT
 ↓
Generate Final Answer
```

---

## 4. My Learning

Write your observations here.

Example:

- Embeddings help AI search by meaning.
- Vector search is important for RAG.
- Azure AI Search can act as the vector search layer.
- Hybrid search is better for enterprise search scenarios.
```

---

# Architect-Notes.md

Paste the below content into `Architect-Notes.md`:

```markdown
# Architect Notes - Embeddings and Vector Search

## Enterprise Architecture

```text
Source Documents
 ↓
Chunking
 ↓
Embedding Model
 ↓
Vector Index
 ↓
Retriever API
 ↓
GPT Model
 ↓
Grounded Answer
```

---

## Azure Services Mapping

| Capability | Azure Service |
|---|---|
| Embedding Generation | Azure OpenAI Embedding Models |
| Vector Storage | Azure AI Search |
| Search Retrieval | Azure AI Search |
| Backend API | ASP.NET Core API |
| Secret Management | Azure Key Vault |
| Monitoring | Azure Monitor and Application Insights |
| Authentication | Microsoft Entra ID |

---

## Design Considerations

### Chunking

Large documents should be split into smaller chunks before embedding.

### Metadata

Store metadata such as:

- File name
- Document type
- Project name
- Created date
- Access classification

### Security

Ensure users only retrieve documents they are allowed to access.

### Cost

Embedding generation, storage, and search queries all need cost monitoring.

### Performance

Use appropriate index design and retrieval filters.

---

## Enterprise Use Cases

- Project documentation search
- IT support knowledge base
- HR policy assistant
- Developer documentation assistant
- Incident knowledge assistant

---

## Architect Learning

Embeddings and vector search are the retrieval foundation of enterprise RAG systems.
```

---

# Embeddings-Diagrams.md

Paste the below content into `Embeddings-Diagrams.md`:

```markdown
# Embeddings and Vector Search Diagrams

## Embedding and Vector Search Flow

![Embeddings Architecture](Diagrams/Embeddings.png)

---

## Flow

```text
Document
 ↓
Chunking
 ↓
Embedding Model
 ↓
Vector Index
 ↓
User Query
 ↓
Query Embedding
 ↓
Similarity Search
 ↓
Relevant Results
```

---

## RAG Connection

```text
Relevant Results
 ↓
Context
 ↓
GPT Model
 ↓
Grounded Answer
```

---

## Learning Outcome

This diagram shows how embeddings convert text into vectors and how vector search retrieves similar content for RAG systems.
```

---

# Draw.io Diagram Guidance

Create this architecture in Draw.io:

```text
Documents
 │
 ▼
Chunking
 │
 ▼
Azure OpenAI Embedding Model
 │
 ▼
Azure AI Search Vector Index
 │
 ▼
Retriever API (.NET)
 │
 ▼
Azure OpenAI GPT Model
 │
 ▼
Answer
```

Add a second flow on the side:

```text
User Question
 │
 ▼
Query Embedding
 │
 ▼
Similarity Search
```

Save editable file as:

```text
Diagrams/Embeddings.drawio
```

Export image as:

```text
Diagrams/Embeddings.png
```

---

# Resources.md

Paste the below content into `Resources.md`:

```markdown
# Learning Resources

## Microsoft Learn

- Azure OpenAI embeddings documentation
- Azure AI Search vector search documentation
- Azure AI Search documentation

## Topics to Search

- Azure OpenAI embeddings
- Azure AI Search vector search
- Azure AI Search hybrid search
- Azure AI Search semantic search
- Embeddings and vector databases
- Similarity search
- RAG architecture

## Practice Focus

- Understand embeddings
- Understand vectors
- Understand vector search
- Understand how embeddings support RAG
- Understand how Azure AI Search fits into enterprise AI architecture
```

---

# HandsOn/Mini-Lab.md

Paste the below content into `HandsOn/Mini-Lab.md`:

```markdown
# Mini Lab - Embedding Search Design

## Goal

Design an embedding-based search flow for an enterprise knowledge assistant.

---

## Scenario

Build semantic search capability for IDD Tech Knowledge Assistant.

The assistant should help users find relevant information from:

- Project documents
- Technical notes
- Support guides
- Meeting summaries

---

## Proposed Flow

```text
Source Documents
 ↓
Chunk Documents
 ↓
Generate Embeddings
 ↓
Store Vectors in Azure AI Search
 ↓
User Asks Question
 ↓
Generate Query Embedding
 ↓
Find Similar Chunks
 ↓
Return Relevant Context
```

---

## Questions to Answer

### 1. What type of documents will be indexed?

Example:

Technical documents, project notes, deployment guides, and support documentation.

### 2. Why do we need chunking?

Example:

Large documents should be split into smaller sections so retrieval can return only the most relevant parts.

### 3. Where will embeddings be stored?

Example:

Embeddings can be stored in Azure AI Search vector index.

### 4. How will users search?

Example:

Users ask a natural language question and the system converts it into a query embedding.

### 5. Why is this useful for RAG?

Example:

RAG needs relevant context before the GPT model generates the answer.

---

## My Design Notes

Write your own design notes here.
```

---

# Optional Weekend Project Update

Update:

```text
Week2/Weekend-Project/Project-Idea.md
```

Add:

```markdown
# Day 2 Enhancement - Add Embeddings

## New Capability

Add semantic search to IDD Tech Knowledge Assistant.

## Updated Architecture

```text
Documents
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
Answer
```

## Future Enhancement

On Day 4, this will become a complete RAG architecture.
```

---

# GitHub Commit Message

After adding all files, commit using:

```text
Completed Week2 Day2 Embeddings and Vector Search
```

---

# Day 2 Completion Checklist

- [ ] Created Week2/Day2-Embeddings folder
- [ ] Created README.md
- [ ] Created Notes.md
- [ ] Created Assignment.md
- [ ] Created Architect-Notes.md
- [ ] Created Embeddings-Diagrams.md
- [ ] Created Resources.md
- [ ] Created Diagrams folder
- [ ] Created Embeddings.drawio
- [ ] Exported Embeddings.png
- [ ] Created HandsOn/Mini-Lab.md
- [ ] Created Screenshots folder
- [ ] Updated Weekend Project idea if needed
- [ ] Committed changes to GitHub

---

# Day 2 Outcome

After completing Week 2 Day 2, you should be able to explain:

- What embeddings are
- What vectors are
- Why embeddings are important
- What similarity search is
- What vector search is
- What Azure OpenAI embeddings are
- How Azure AI Search supports vector search
- Difference between keyword, semantic, vector, and hybrid search
- How embeddings support RAG architecture

---

# Next Day Preview

Week 2 Day 3 will cover:

- Azure AI Search deep dive
- Search indexes
- Indexers
- Skillsets
- Semantic ranking
- Hybrid search
- Retrieval design for enterprise RAG
