# Day 5 Notes - Prompt Engineering Masterclass

## What is Prompt Engineering?

Prompt Engineering is the process of writing effective instructions to get high-quality responses from AI models such as ChatGPT, Copilot, Gemini, and Claude.

The quality of the response depends greatly on the quality of the prompt.

---

## Prompt Formula

A good prompt usually contains:

```text
Role + Task + Context + Output Format
```

### Example

Role:
Azure Solution Architect

Task:
Explain Azure Service Bus

Context:
Audience has 12 years of .NET experience

Output Format:
Markdown with examples

---

## Types of Prompting

### Zero-Shot Prompting

No examples are provided.

Example:

Translate:

Hello World

---

### One-Shot Prompting

One example is provided.

Example:

Input: Good Morning
Output: Bonjour

Translate:

Input: Thank You

---

### Few-Shot Prompting

Multiple examples are provided.

Example:

Input: Good Morning
Output: Bonjour

Input: Thank You
Output: Merci

Input: How Are You

---

### Role-Based Prompting

Assign a role to AI.

Examples:

- Azure Solution Architect
- Security Consultant
- Project Manager
- Technical Interviewer

Example:

Act as an Azure Architect and explain Azure Event Grid.

---

### Chain of Thought Prompting

Ask AI to think step by step.

Example:

Think step by step and design a secure Azure OpenAI solution.

---

### Structured Output Prompting

Ask AI to respond in a specific structure.

Example:

Provide:

1. Summary
2. Architecture
3. Risks
4. Recommendations

---

## Prompt Optimization Techniques

### Be Specific

Bad Prompt:

Explain Azure.

Good Prompt:

Explain Azure Service Bus including architecture, security, and cost.

### Add Context

Mention audience and business scenario.

### Request Format

Specify Markdown, table, bullet points, etc.

### Ask for Examples

Include real-world or enterprise examples.

---

## Temperature

Temperature controls creativity.

### Low Temperature

0.1 - 0.3

Best for:

- Documentation
- Technical Content
- Reports

### High Temperature

0.7 - 1.0

Best for:

- Creative Writing
- Brainstorming
- Idea Generation

---

## Key Learnings

- Prompt quality impacts response quality.
- Better prompts generate better results.
- Few-shot prompting improves consistency.
- Role-based prompting improves context awareness.
- Prompt Engineering is critical for AI Architects.