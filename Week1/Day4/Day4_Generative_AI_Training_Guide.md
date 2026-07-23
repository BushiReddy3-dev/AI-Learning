# Week 1 - Day 4 Training Guide

# Generative AI, LLMs, Tokens, Embeddings & Prompt Engineering

## Duration

2 Hours

---

# Learning Goals

By the end of Day 4, you should understand:

- What is Generative AI
- What is an LLM
- What are Tokens
- What are Embeddings
- What is Prompt Engineering
- What is a Context Window
- What is Temperature
- How ChatGPT Generates Responses
- What is RAG
- What are AI Agents

---

# Learning Resources

## Microsoft Generative AI for Beginners

[ttps://microsoft.github.io/generative-ai-for-beginners/

## Microsoft Learn

[Explore Generative AI](https://learn.microsoft.com/trainingive-ai/

## Prompt Engineering Guide

[Prompt Engineering Guide](https# Azure OpenAI Documentation

[Azure OpenAI.microsoft.com/azure/ai-services/openai/

---

# Day 4 Agenda

| Activity | Duration |
|----------|----------|
| Theory | 60 Minutes |
| Hands-On | 45 Minutes |
| Assignment | 15 Minutes |

---

# Topic 1: What is Generative AI?

Generative AI is a type of Artificial Intelligence that creates new content.

Examples:

- Text
- Images
- Audio
- Video
- Code

## Traditional AI

```text
Input
  ↓
Prediction
```

Example:

```text
Spam Detection
```

## Generative AI

```text
Prompt
   ↓
Generate Content
```

Example:

```text
Write a leave application
```

---

# Topic 2: What is an LLM?

LLM stands for:

```text
Large Language Model
```

An LLM is a Deep Learning model trained on massive amounts of text data.

Examples:

- GPT
- Gemini
- Claude
- Llama
- Mistral

## What Can LLMs Do?

- Answer Questions
- Generate Code
- Draft Emails
- Summarize Documents
- Translate Languages
- Create Content

---

# LLM Architecture

```text
Text Data
      ↓
Training
      ↓
Transformer Model
      ↓
LLM
```

---

# Topic 3: What are Tokens?

Large Language Models do not directly understand words.

They process:

```text
Tokens
```

## Example

Sentence:

```text
I love Azure OpenAI
```

Might become:

```text
I
love
Azure
OpenAI
```

or

```text
I
love
Azure
Open
AI
```

depending on the tokenizer.

## Why Tokens Matter?

Tokens determine:

- Cost
- Input Length
- Output Length
- Context Size

---

# Topic 4: Context Window

A context window is the amount of information the model can remember in one conversation.

Example:

```text
User:
My name is Bushi.

User:
What is my name?
```

The model can answer because it remembers the context.

## Why Context Window Matters

A larger context window allows:

- Longer conversations
- Document analysis
- Better reasoning
- More accurate responses

---

# Topic 5: What are Embeddings?

Embeddings convert text into numerical vectors.

Example:

```text
Azure OpenAI
```

becomes:

```text
[0.12, 0.45, 0.96, 0.88...]
```

## Why Embeddings?

Embeddings help AI measure similarity.

Example:

```text
How to configure Azure Service Bus?
```

```text
How do I create Service Bus?
```

These have similar meanings and therefore similar embeddings.

---

# Embedding Architecture

```text
Text
 ↓
Embedding Model
 ↓
Vector
 ↓
Vector Database
```

---

# Topic 6: Vector Databases

Vector Databases store embeddings.

Examples:

- Azure AI Search
- Pinecone
- Weaviate
- ChromaDB

## Why Vector Databases?

They help find similar information.

Example:

```text
User Question
       ↓
Vector Search
       ↓
Related Documents
       ↓
Response
```

---

# Topic 7: Prompt Engineering

Prompt Engineering is the process of creating effective prompts.

## Weak Prompt

```text
Explain Azure.
```

## Better Prompt

```text
Explain Azure Service Bus for a Solution Architect.

Include:
- Architecture
- Benefits
- Drawbacks
- Cost
- Alternatives

Format the answer as Markdown.
```

---

# Prompt Formula

```text
Role
+
Task
+
Context
+
Output Format
```

Example:

```text
Act as an Azure Solution Architect.

Explain Azure Event Grid.

Include:
1. Architecture
2. Benefits
3. Limitations
4. Use Cases

Provide response in markdown format.
```

---

# Topic 8: Temperature

Temperature controls creativity.

## Low Temperature

```text
0.1
```

Output:

```text
More Accurate
Less Creative
```

## High Temperature

```text
1.0
```

Output:

```text
More Creative
More Diverse
Less Predictable
```

---

# Topic 9: How ChatGPT Generates Responses

```text
User Prompt
      ↓
Tokenizer
      ↓
Embeddings
      ↓
Transformer
      ↓
Token Prediction
      ↓
Generated Response
```

---

# Topic 10: What is RAG?

RAG stands for:

```text
Retrieval Augmented Generation
```

## Problem

LLMs do not automatically know company-specific documents.

## Solution

```text
User Question
        ↓
Vector Search
        ↓
Relevant Documents
        ↓
LLM
        ↓
Answer
```

---

# Topic 11: What are AI Agents?

AI Agents are intelligent systems that:

- Reason
- Plan
- Execute Tasks
- Use Tools
- Automate Actions

Examples:

- Microsoft Copilot Agents
- Azure AI Foundry Agents
- Copilot Studio Agents

---

# Hands-On Activity

## Create Folder Structure

```text
Week1
│
├── Day1
├── Day2
├── Day3
│
└── Day4
     │
     ├── Notes.md
     ├── GenAI-Diagrams.md
     ├── Assignment.md
     ├── Architect-Notes.md
     ├── GenAI.drawio
     └── GenAI.png
```

---

# Notes.md

```markdown
# Day 4 Notes - Generative AI

## What is Generative AI?

Generative AI creates new content such as text, code, images and audio.

## What is an LLM?

Large Language Model trained on huge text datasets.

Examples:

- GPT
- Gemini
- Claude
- Llama

## What are Tokens?

Small units of text processed by LLMs.

## What are Embeddings?

Numerical representations of text used for similarity search.

## What is Prompt Engineering?

The process of writing effective prompts to get better results.

## What is RAG?

Retrieval Augmented Generation combines search and generation.

## What are AI Agents?

Systems that reason and perform actions using tools.

## Key Learnings

- Generative AI creates content.
- LLMs power modern AI assistants.
- Embeddings enable vector search.
- Prompt engineering improves response quality.
```

---

# Draw.io Diagram

Create the following diagrams:

## Diagram 1: Generative AI Architecture

```text
User Prompt
      │
      ▼
Tokenizer
      │
      ▼
Embeddings
      │
      ▼
LLM
      │
      ▼
Generated Response
```

## Diagram 2: RAG Architecture

```text
User Question
       │
       ▼
Vector Search
       │
       ▼
Relevant Documents
       │
       ▼
LLM
       │
       ▼
Response
```

Save as:

```text
GenAI.drawio
```

Export as:

```text
GenAI.png
```

---

# GenAI-Diagrams.md

```markdown
# Generative AI Diagrams

GenAI.png

## Components

### Prompt

User instruction.

### Tokenizer

Converts text into tokens.

### Embeddings

Converts text into vectors.

### LLM

Processes tokens and predicts output.

### RAG

Combines search with generation.

### AI Agents

Uses LLMs together with tools and actions.

## Learning Outcome

Understanding how ChatGPT, Copilot, Azure OpenAI and RAG-based systems work.
```

---

# Assignment.md

```markdown
# Day 4 Assignment

## Compare Traditional AI and Generative AI

| Feature | Traditional AI | Generative AI |
|----------|---------------|---------------|
| Purpose | Predict | Create |
| Output | Classification | Content Generation |
| Example | Spam Detection | ChatGPT |

## Examples of Generative AI

1. ChatGPT
2. Microsoft Copilot
3. GitHub Copilot
4. Gemini
5. Claude
6. Midjourney
7. DALL-E
8. Azure OpenAI

## My Learning

- LLMs power Generative AI.
- Tokens impact cost and context.
- Embeddings enable vector search.
- Prompt engineering improves responses.
- RAG enables enterprise knowledge retrieval.
```

---

# Architect-Notes.md

```markdown
# Generative AI on Azure

| Concept | Azure Service |
|----------|--------------|
| LLM | Azure OpenAI |
| Embeddings | Azure OpenAI Embedding Models |
| Vector Search | Azure AI Search |
| RAG | Azure AI Search + Azure OpenAI |
| AI Agents | Azure AI Foundry Agents |
| Prompt Management | Azure AI Foundry |
| Content Safety | Azure AI Content Safety |

## Enterprise Use Cases

- Employee Exit Assistant
- HR Chatbot
- IT Support Assistant
- Knowledge Search
- Customer Service Bot
- Document Q&A Assistant

## Architect Learning

RAG + Azure AI Search + Azure OpenAI is the foundation of most enterprise AI solutions.
```

---

# Git Commit

```bash
git add .
git commit -m "Completed Week1 Day4 Generative AI Fundamentals"
git push origin main
```

---

# Day 4 Completion Checklist

- [ ] Created Day4 Folder
- [ ] Completed Notes.md
- [ ] Completed GenAI-Diagrams.md
- [ ] Completed Assignment.md
- [ ] Completed Architect-Notes.md
- [ ] Created GenAI.drawio
- [ ] Exported GenAI.png
- [ ] Committed Code to GitHub

---

# Day 4 Outcome

You should now understand:

- Generative AI
- LLMs
- Tokens
- Embeddings
- Context Window
- Prompt Engineering
- Temperature
- Vector Databases
- RAG
- AI Agents
- Azure OpenAI Architecture