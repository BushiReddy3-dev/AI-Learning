# Week 1 - Day 5 Training Guide

# Prompt Engineering Masterclass & Azure OpenAI Playground

## Duration

2 Hours

---

# Learning Goals

By the end of Day 5, you should understand:

- What is Prompt Engineering
- Why Prompt Engineering Matters
- Types of Prompts
- Zero-Shot Prompting
- One-Shot Prompting
- Few-Shot Prompting
- Chain of Thought Prompting
- Role-Based Prompting
- Azure OpenAI Playground Basics
- Enterprise Prompt Design
- Common Prompting Mistakes

---

# Why Day 5 is Important?

Prompt Engineering is the skill that makes Generative AI more effective.

The same model can produce:

- Poor Output
- Good Output
- Excellent Output

depending on the prompt quality.

---

# Learning Resources

## Microsoft Generative AI for Beginners

https://microsoft.github.io/generative-ai-for-beginners/

## Prompt Engineering Guide

https://www.promptingguide.ai/

## Azure OpenAI Documentation

https://learn.microsoft.com/azure/ai-services/openai/

---

# Day 5 Agenda

| Activity | Duration |
|-----------|-----------|
| Theory | 60 Minutes |
| Hands-On | 45 Minutes |
| Assignment | 15 Minutes |

---

# Topic 1: What is Prompt Engineering?

Prompt Engineering is the process of designing effective prompts to obtain better responses from AI models.

---

## Example

### Weak Prompt

```text
Explain Azure.
```

### Better Prompt

```text
Act as an Azure Solution Architect.

Explain Azure Service Bus.

Include:

1. Architecture
2. Benefits
3. Drawbacks
4. Cost Considerations
5. Alternatives

Format response in Markdown.
```

---

# Topic 2: Prompt Structure

Good prompts usually contain:

```text
Role
+
Task
+
Context
+
Output Format
```

---

## Example

```text
Role:
Act as a Senior Azure Architect

Task:
Explain Azure Event Grid

Context:
Audience has 10 years of .NET experience

Output:
Provide architecture diagram and key points
```

---

# Topic 3: Zero-Shot Prompting

No examples are provided.

---

## Example

```text
Translate this sentence to French:

Hello, how are you?
```

The model performs the task without examples.

---

# Topic 4: One-Shot Prompting

One example is provided.

---

## Example

```text
Example:

Input:
Good Morning

Output:
Bonjour

Translate:

Input:
How are you?

Output:
```

---

# Topic 5: Few-Shot Prompting

Multiple examples are provided.

---

## Example

```text
Input: Good Morning
Output: Bonjour

Input: Thank You
Output: Merci

Input: How Are You
Output:
```

This improves accuracy.

---

# Topic 6: Role-Based Prompting

Assign a role to the AI.

---

## Example

```text
Act as a Project Manager.
```

```text
Act as a Solution Architect.
```

```text
Act as a Technical Interviewer.
```

---

## Benefits

- Better responses
- More context-aware answers
- Structured outputs

---

# Topic 7: Chain of Thought Prompting

Ask the model to think step-by-step.

---

## Example

```text
Solve this problem step by step.
```

Benefits:

- Better reasoning
- Reduced mistakes
- Improved explanations

---

# Topic 8: Structured Output Prompting

Force the model to return a structured format.

---

## Example

```text
Provide response in:

1. Summary
2. Risks
3. Recommendations
4. Action Items
```

---

# Topic 9: Enterprise Prompt Patterns

As an Azure Solution Architect, these prompts are useful.

---

## Architecture Prompt

```text
Act as an Azure Solution Architect.

Design a scalable document processing solution using:

- Azure OpenAI
- Azure AI Search
- Azure Storage

Include:

- Architecture
- Data Flow
- Security
- Cost Considerations
```

---

## Code Review Prompt

```text
Act as a Senior .NET Architect.

Review the below code.

Identify:

- Security Issues
- Performance Issues
- Best Practices
- Suggested Improvements
```

---

## Meeting Summary Prompt

```text
Summarize the meeting.

Provide:

- Key Discussions
- Decisions
- Risks
- Action Items
```

---

# Topic 10: Azure OpenAI Playground

The Playground is used to:

- Test prompts
- Evaluate responses
- Compare prompt variations
- Experiment with temperature settings

---

## Playground Workflow

```text
Prompt
   ↓
Model
   ↓
Response
   ↓
Improve Prompt
   ↓
Better Response
```

---

# Topic 11: Common Prompt Mistakes

## Bad Example

```text
Explain cloud.
```

Problem:

- Too vague

---

## Better Example

```text
Explain Azure Service Bus
for a .NET architect.

Include:

- Architecture
- Security
- Pros
- Cons

Provide response as Markdown.
```

---

# Topic 12: Prompt Optimization Tips

### Be Specific

Instead of:

```text
Explain Azure
```

Use:

```text
Explain Azure Service Bus
for enterprise integration.
```

---

### Use Roles

```text
Act as Azure Architect.
```

---

### Use Output Formatting

```text
Provide response in markdown.
```

---

### Include Audience

```text
Audience: .NET Developers
```

---

### Ask for Examples

```text
Include real-world examples.
```

---

# Hands-On Activity

## Create Folder Structure

```text
Week1
│
├── Day1
├── Day2
├── Day3
├── Day4
│
└── Day5
     │
     ├── Notes.md
     ├── Prompt-Diagrams.md
     ├── Assignment.md
     ├── Architect-Notes.md
     ├── PromptEngineering.drawio
     └── PromptEngineering.png
```

---

# Notes.md

```markdown
# Day 5 Notes - Prompt Engineering

## What is Prompt Engineering?

Prompt Engineering is the process of designing prompts to get better AI responses.

## Prompt Formula

Role + Task + Context + Output Format

## Prompting Techniques

### Zero-Shot

No examples provided.

### One-Shot

Single example provided.

### Few-Shot

Multiple examples provided.

### Chain of Thought

Ask the model to think step-by-step.

### Role-Based Prompting

Assign a role such as Architect, Developer or Project Manager.

## Key Learning

Prompt quality directly impacts response quality.
```

---

# Draw.io Diagram

Create the following diagram:

```text
User Prompt
      │
      ▼
Role
      │
      ▼
Task
      │
      ▼
Context
      │
      ▼
Output Format
      │
      ▼
LLM
      │
      ▼
Response
```

Save as:

```text
PromptEngineering.drawio
```

Export as:

```text
PromptEngineering.png
```

---

# Prompt-Diagrams.md

```markdown
# Prompt Engineering Architecture

PromptEngineering.png

## Components

### Role

Defines who the model should act as.

### Task

Specifies what needs to be done.

### Context

Provides background information.

### Output Format

Defines response structure.

### Response

Generated by the LLM.

## Learning Outcome

Better prompts generate better results.
```

---

# Assignment.md

```markdown
# Day 5 Assignment

## Create Prompts for the Following

### 1. Azure Architecture Design

Design a secure Azure document processing solution.

### 2. Code Review

Review a .NET API for security and performance.

### 3. Meeting Summary

Summarize a meeting and generate action items.

### 4. Project Plan

Create a project plan for AI implementation.

### 5. Risk Assessment

Identify risks in an Azure OpenAI solution.

## My Learning

- Prompt quality impacts AI quality.
- Role-based prompting improves responses.
- Few-shot prompting improves consistency.
- Chain of Thought improves reasoning.
```

---

# Architect-Notes.md

```markdown
# Prompt Engineering for Solution Architects

## Common Architect Prompts

### Architecture Review

Act as an Azure Architect.

Review the architecture and identify:

- Security Risks
- Performance Issues
- Cost Optimization Opportunities

### AI Solution Design

Design an enterprise AI solution using:

- Azure OpenAI
- Azure AI Search
- Azure Storage

### Cost Optimization

Recommend Azure cost optimization strategies.

## Enterprise Use Cases

- Copilot Development
- AI Agents
- RAG Applications
- Document Processing
- Knowledge Management
- Chatbots
```

---

# Git Commit

```bash
git add .
git commit -m "Completed Week1 Day5 Prompt Engineering Masterclass"
git push origin main
```

---

# Day 5 Completion Checklist

- [ ] Created Day5 folder
- [ ] Completed Notes.md
- [ ] Completed Prompt-Diagrams.md
- [ ] Completed Assignment.md
- [ ] Completed Architect-Notes.md
- [ ] Created PromptEngineering.drawio
- [ ] Exported PromptEngineering.png
- [ ] Committed Code to GitHub

---

# Day 5 Outcome

You should now understand:

- Prompt Engineering
- Zero-Shot Prompting
- One-Shot Prompting
- Few-Shot Prompting
- Chain of Thought Prompting
- Role-Based Prompting
- Enterprise Prompt Design
- Azure OpenAI Playground Basics
- Prompt Optimization Techniques

## Next Step (Week 2)

- Azure OpenAI Service
- GPT Models
- Azure AI Search
- RAG Implementation
- AI Agents
- Azure AI Foundry
- Copilot Studio
- Enterprise AI Architecture