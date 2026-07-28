# Week 1 - Day 5 Training Guide

# Prompt Engineering Masterclass (Solution Architect Track)

Prompt Engineering is one of the most important skills in your AI learning journey because it is the foundation for ChatGPT, Microsoft Copilot, GitHub Copilot, Copilot Studio, Azure OpenAI, AI Agents, and RAG-based enterprise solutions.

---

# Duration

2 Hours

---

# Learning Objectives

By the end of Day 5, you will understand:

- What is Prompt Engineering
- Why Prompt Engineering matters
- Zero-Shot Prompting
- One-Shot Prompting
- Few-Shot Prompting
- Chain of Thought Prompting
- Role-Based Prompting
- Structured Output Prompting
- Prompt Optimization Techniques
- Azure OpenAI Playground basics
- Enterprise Prompt Patterns
- Architect-level Prompt Design

---

# Day 5 Agenda

| Section | Duration | Activity |
|---|---:|---|
| Theory | 60 min | Learn prompt engineering concepts |
| Hands-on | 45 min | Practice different prompt patterns |
| Assignment | 15 min | Create enterprise prompts |

---

# Part 1: Theory

## 1. What is Prompt Engineering?

Prompt Engineering is the process of writing clear and effective instructions to get better responses from AI models.

A prompt is the input that we give to an AI model.

The quality of the prompt directly impacts the quality of the output.

---

## 2. Why Prompt Engineering Matters

The same AI model can produce different quality outputs depending on the prompt.

### Poor Prompt

```text
Explain Azure.
```

This may produce a generic answer.

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

Provide the response in Markdown format.
```

This produces a more detailed and architect-level response.

---

# 3. Prompt Formula

A good prompt usually follows this formula:

```text
Role + Task + Context + Output Format
```

## Explanation

### Role

Tell the AI what role to act as.

Example:

```text
Act as an Azure Solution Architect.
```

### Task

Tell the AI what it needs to do.

Example:

```text
Design a secure document processing solution.
```

### Context

Give background information.

Example:

```text
The audience has 10 years of .NET and Azure experience.
```

### Output Format

Tell the AI how to structure the response.

Example:

```text
Provide output as a Markdown table with recommendations.
```

---

# 4. Zero-Shot Prompting

Zero-shot prompting means asking the AI to perform a task without giving any example.

## Example

```text
Translate the following sentence into French:

Hello, how are you?
```

## When to Use

Use zero-shot prompting for:

- Simple questions
- General explanations
- Quick translations
- Basic summarization

---

# 5. One-Shot Prompting

One-shot prompting means giving one example before asking the AI to complete the task.

## Example

```text
Example:

Input:
Good Morning

Output:
Bonjour

Now translate:

Input:
How are you?

Output:
```

## Benefit

One example helps the AI understand the expected pattern.

---

# 6. Few-Shot Prompting

Few-shot prompting means giving multiple examples before asking the AI to perform the task.

## Example

```text
Input:
Good Morning

Output:
Bonjour

Input:
Thank You

Output:
Merci

Input:
How Are You

Output:
```

## Benefits

Few-shot prompting improves:

- Accuracy
- Consistency
- Formatting
- Pattern understanding

---

# 7. Role-Based Prompting

Role-based prompting means asking the AI to respond from a specific role or perspective.

## Example Roles

```text
Act as an Azure Solution Architect.
```

```text
Act as a Senior .NET Architect.
```

```text
Act as a Project Manager.
```

```text
Act as a Technical Interviewer.
```

```text
Act as a Security Consultant.
```

## Example Prompt

```text
Act as an Azure Solution Architect.

Explain Azure Service Bus for enterprise integration.

Include:

- Architecture
- Use cases
- Security
- Cost considerations
- Alternatives
```

---

# 8. Chain of Thought Prompting

Chain of Thought prompting asks the AI to solve or explain something step by step.

## Example

```text
Think step by step.

Design a secure Azure OpenAI architecture for an enterprise application.
```

## Benefits

This improves:

- Reasoning
- Clarity
- Analysis
- Accuracy
- Decision-making

---

# 9. Structured Output Prompting

Structured output prompting tells the AI exactly how the response should be organized.

## Example

```text
Provide the response in the below format:

1. Summary
2. Architecture
3. Risks
4. Recommendations
5. Action Items
```

## Useful For

- Meeting summaries
- Architecture reviews
- Status reports
- Project plans
- Risk assessments
- Technical documentation

---

# 10. Enterprise Prompt Patterns

As an Azure AI Solution Architect, you should practice enterprise-level prompts.

---

## 10.1 Architecture Design Prompt

```text
Act as an Azure Solution Architect.

Design an enterprise document processing solution using:

- Azure OpenAI
- Azure AI Search
- Azure Blob Storage
- Azure Functions

Include:

1. Architecture
2. Data Flow
3. Security
4. Monitoring
5. Cost Considerations
6. Alternatives

Provide the response in Markdown format.
```

---

## 10.2 Code Review Prompt

```text
Act as a Senior .NET Architect.

Review the below API code.

Identify:

1. Security issues
2. Performance issues
3. Code smells
4. Best practices
5. Suggested improvements

Provide the response in table format.
```

---

## 10.3 Meeting Summary Prompt

```text
Summarize the meeting notes.

Provide:

1. Key Discussions
2. Decisions Taken
3. Risks
4. Open Questions
5. Action Items with Owner and Due Date
```

---

## 10.4 Project Plan Prompt

```text
Act as a Project Manager.

Create a project plan for implementing Azure OpenAI in an enterprise application.

Include:

1. Phases
2. Tasks
3. Dependencies
4. Risks
5. Deliverables
6. Timeline format
```

---

## 10.5 Risk Assessment Prompt

```text
Act as an AI Governance Consultant.

Identify risks in a Generative AI solution.

Include:

1. Security risks
2. Privacy risks
3. Hallucination risks
4. Compliance risks
5. Mitigation strategy
```

---

# 11. Prompt Optimization Techniques

## Technique 1: Be Specific

Instead of:

```text
Explain cloud.
```

Use:

```text
Explain Azure Service Bus for enterprise application integration.
```

---

## Technique 2: Use a Role

```text
Act as an Azure Solution Architect.
```

---

## Technique 3: Add Context

```text
The audience has 12 years of .NET and Azure experience.
```

---

## Technique 4: Define Output Format

```text
Provide the response as a Markdown table.
```

---

## Technique 5: Ask for Examples

```text
Include real-world enterprise examples.
```

---

## Technique 6: Ask for Pros and Cons

```text
Include benefits, limitations, and alternatives.
```

---

## Technique 7: Ask for Step-by-Step Explanation

```text
Explain the solution step by step.
```

---

# 12. Azure OpenAI Playground Basics

Azure OpenAI Playground is used to test prompts and evaluate model responses.

## Playground Workflow

```text
Prompt
  ↓
AI Model
  ↓
Response
  ↓
Improve Prompt
  ↓
Better Response
```

## What You Can Practice

- Test different prompts
- Compare model responses
- Adjust temperature
- Improve output format
- Test enterprise scenarios

---

# 13. Temperature in Prompting

Temperature controls creativity.

## Low Temperature

```text
0.1 to 0.3
```

Best for:

- Accurate answers
- Technical documentation
- Code review
- Business summaries

## High Temperature

```text
0.7 to 1.0
```

Best for:

- Creative writing
- Brainstorming
- Idea generation

---

# Part 2: Hands-On Activity

## Step 1: Create Day 5 Folder Structure

Create this folder structure in your GitHub repository:

```text
AI-Learning
│
└── Week1
    ├── Day1
    ├── Day2
    ├── Day3
    ├── Day4
    └── Day5
        ├── Notes.md
        ├── Prompt-Diagrams.md
        ├── Assignment.md
        ├── Architect-Notes.md
        ├── PromptEngineering.drawio
        └── PromptEngineering.png
```

---

# Content for Notes.md

Paste the below content into `Week1/Day5/Notes.md`:

```markdown
# Day 5 Notes - Prompt Engineering

## What is Prompt Engineering?

Prompt Engineering is the process of writing effective instructions to get better responses from AI models.

## Prompt Formula

Role + Task + Context + Output Format

## Prompting Techniques

### Zero-Shot Prompting

No example is provided.

### One-Shot Prompting

One example is provided.

### Few-Shot Prompting

Multiple examples are provided.

### Role-Based Prompting

The AI is asked to act as a specific role.

Examples:

- Azure Architect
- Project Manager
- Security Consultant
- Technical Interviewer

### Chain of Thought Prompting

The AI is asked to solve or explain step by step.

### Structured Output Prompting

The AI is asked to provide output in a specific format.

## Key Learnings

- Prompt quality impacts AI response quality.
- Role-based prompts improve context.
- Few-shot prompts improve consistency.
- Structured prompts improve readability.
- Prompt Engineering is important for Azure OpenAI, Copilot Studio, and AI Agents.
```

---

# Draw.io Diagram Guidance

Create the following prompt engineering diagram in Draw.io:

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

Save the editable diagram as:

```text
PromptEngineering.drawio
```

Export the image as:

```text
PromptEngineering.png
```

---

# Content for Prompt-Diagrams.md

Paste the below content into `Week1/Day5/Prompt-Diagrams.md`:

```markdown
# Prompt Engineering Diagrams

## Prompt Engineering Flow

![Prompt Engineering](PromptEngineering.png)

## Components

### Role

Defines who the model should act as.

### Task

Defines what the model should do.

### Context

Provides background information.

### Output Format

Defines how the response should be structured.

### LLM

Processes the prompt and generates a response.

## Learning Outcome

A well-structured prompt improves response quality, consistency, and usefulness.
```

---

# Content for Assignment.md

Paste the below content into `Week1/Day5/Assignment.md`:

```markdown
# Day 5 Assignment

## Create Prompts for the Following Scenarios

### 1. Azure Architecture Design

Create a prompt to design a secure Azure AI solution.

### 2. Code Review

Create a prompt to review a .NET API for security and performance.

### 3. Meeting Summary

Create a prompt to summarize a project status meeting.

### 4. Project Plan

Create a prompt to prepare an Azure OpenAI implementation project plan.

### 5. Risk Assessment

Create a prompt to identify risks in a Generative AI solution.

---

## Sample Answers

### Azure Architecture Design Prompt

```text
Act as an Azure Solution Architect.

Design a secure Azure AI solution using Azure OpenAI, Azure AI Search, and Azure Blob Storage.

Include architecture, data flow, security, monitoring, cost considerations, and risks.

Provide the response in Markdown format.
```

### Code Review Prompt

```text
Act as a Senior .NET Architect.

Review the below API code and identify security issues, performance issues, code smells, and best practice improvements.

Provide the output in table format.
```

### Meeting Summary Prompt

```text
Summarize the project meeting notes.

Provide key discussions, decisions, risks, open questions, and action items with owners and due dates.
```

### Project Plan Prompt

```text
Act as a Project Manager.

Create a project plan for implementing Azure OpenAI in an enterprise application.

Include phases, tasks, dependencies, risks, deliverables, and milestones.
```

### Risk Assessment Prompt

```text
Act as an AI Governance Consultant.

Identify risks in a Generative AI solution.

Include security, privacy, data leakage, hallucination, compliance, and mitigation strategy.
```

---

## My Learning

- Prompt quality impacts AI response quality.
- Role-based prompting improves context.
- Few-shot prompting improves consistency.
- Structured output improves readability.
- Prompt Engineering is critical for enterprise AI solutions.
```

---

# Content for Architect-Notes.md

Paste the below content into `Week1/Day5/Architect-Notes.md`:

```markdown
# Prompt Engineering for Solution Architects

## Why Prompt Engineering Matters for Architects

AI Solution Architects use prompts to design, review, document, and validate AI solutions.

## Common Architect Prompts

### Architecture Review Prompt

```text
Act as an Azure Solution Architect.

Review the architecture and identify security risks, scalability issues, performance bottlenecks, and cost optimization opportunities.
```

### RAG Solution Prompt

```text
Act as a Senior AI Architect.

Design a RAG solution using Azure OpenAI, Azure AI Search, and Azure Blob Storage.

Include architecture, data flow, chunking strategy, embeddings, security, monitoring, and cost optimization.
```

### Copilot Studio Prompt

```text
Act as a Copilot Studio Architect.

Design an enterprise Copilot agent for employee exit management.

Include topics, actions, Power Automate flows, authentication, security, and escalation process.
```

## Enterprise Use Cases

- Copilot Development
- AI Agents
- RAG Applications
- Document Processing
- Knowledge Management
- Chatbots
- Code Review
- Meeting Summaries
- Risk Analysis

## Architect Learning

Prompt Engineering helps Solution Architects communicate clearly with AI models and produce better technical designs, documentation, and implementation plans.
```

---

# GitHub Push Steps Using github.dev

1. Open your GitHub repository.
2. Press `.` to open github.dev.
3. Create `Week1/Day5` folder.
4. Add the Day 5 markdown files.
5. Upload Draw.io file and PNG image.
6. Open Source Control from the left side.
7. Enter commit message:

```text
Completed Week1 Day5 Prompt Engineering Masterclass
```

8. Click Commit.
9. Click Sync Changes or Push.

---

# Day 5 Completion Checklist

- [ ] Created Week1/Day5 folder
- [ ] Created Notes.md
- [ ] Created Prompt-Diagrams.md
- [ ] Created Assignment.md
- [ ] Created Architect-Notes.md
- [ ] Created PromptEngineering.drawio
- [ ] Exported PromptEngineering.png
- [ ] Committed and pushed changes to GitHub

---

# Day 5 Outcome

After Day 5, you should be able to explain and use:

- Prompt Engineering
- Zero-Shot Prompting
- One-Shot Prompting
- Few-Shot Prompting
- Chain of Thought Prompting
- Role-Based Prompting
- Structured Output Prompting
- Enterprise Prompt Design
- Azure OpenAI Playground Basics
- Prompt Optimization Techniques

---

# Week 1 Completion Summary

By the end of Week 1, you completed:

- Day 1: AI Fundamentals
- Day 2: Machine Learning Fundamentals
- Day 3: Deep Learning and Neural Networks
- Day 4: Generative AI, LLMs, Tokens and Embeddings
- Day 5: Prompt Engineering Masterclass

---

# Week 2 Preview

Week 2 will focus on:

- Azure OpenAI Service
- GPT Models
- Embeddings
- Azure AI Search
- RAG Implementation
- Azure AI Foundry
- AI Agents
- Copilot Studio
- Enterprise AI Architecture
