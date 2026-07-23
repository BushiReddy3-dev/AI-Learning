# Week 1 - Day 3 Training Guide

# Deep Learning & Neural Networks

## Duration

2 Hours

---

# Goal

By the end of Day 3, you should understand:

- What is Deep Learning
- What is a Neural Network
- How Neural Networks work
- CNN (Convolutional Neural Networks)
- RNN (Recurrent Neural Networks)
- Transformers
- Why Transformers power ChatGPT
- Deep Learning use cases
- Deep Learning lifecycle

---

# Learning Resources

## Microsoft AI for Beginners

https://microsoft.github.io/AI-For-Beginners/

## Azure AI Fundamentals

https://learn.microsoft.com/training/paths/get-started-with-artificial-intelligence-on-azure/

## Hugging Face Transformers

https://huggingface.co/docs/transformers/index

## TensorFlow Playground

https://playground.tensorflow.org

---

# Day 3 Agenda

| Activity | Duration |
|-----------|-----------|
| Theory | 60 Minutes |
| Hands-on | 45 Minutes |
| Assignment | 15 Minutes |

---

# Topic 1: What is Deep Learning?

Deep Learning is a subset of Machine Learning that uses artificial neural networks with multiple hidden layers.

## Hierarchy

```text
AI
│
└── Machine Learning
      │
      └── Deep Learning
```

## Examples

- ChatGPT
- Microsoft Copilot
- GitHub Copilot
- Face Recognition
- Self Driving Cars

---

# Topic 2: What is a Neural Network?

A Neural Network is inspired by the human brain.

It consists of:

```text
Input Layer
      ↓
Hidden Layers
      ↓
Output Layer
```

## Example

```text
Employee Age
Experience
Salary
      ↓
Neural Network
      ↓
Will Employee Leave?
```

---

# Topic 3: Neural Network Components

## Input Layer

Receives data.

## Hidden Layer

Processes information.

## Output Layer

Produces prediction.

## Weights

Importance assigned to inputs.

## Bias

Adjusts predictions.

## Activation Function

Decides whether a neuron activates.

Examples:

- ReLU
- Sigmoid
- Softmax

---

# Topic 4: CNN (Convolutional Neural Networks)

CNN is mainly used for image processing.

## Use Cases

- Face Recognition
- Medical Imaging
- Security Cameras
- Object Detection

## Architecture

```text
Image
  ↓
Convolution Layer
  ↓
Pooling Layer
  ↓
Fully Connected Layer
  ↓
Prediction
```

---

# Topic 5: RNN (Recurrent Neural Networks)

RNN is designed for sequence-based data.

## Use Cases

- Language Translation
- Speech Recognition
- Text Prediction
- Time Series Forecasting

## Architecture

```text
Word1
  ↓
Word2
  ↓
Word3
  ↓
Prediction
```

---

# Topic 6: Transformers

Transformers are the foundation of modern Generative AI.

Used by:

- GPT
- ChatGPT
- Copilot
- Gemini
- Claude
- Llama

## Why Transformers?

### RNN Problems

- Slow Training
- Long Context Issues

### Transformer Advantages

- Faster Training
- Better Accuracy
- Long Context Understanding
- Parallel Processing

---

# Transformer Architecture

```text
Input Text
     ↓
Tokenizer
     ↓
Embeddings
     ↓
Transformer Layers
     ↓
Output
```

---

# Topic 7: How ChatGPT Works

```text
User Prompt
      ↓
Tokenizer
      ↓
Embeddings
      ↓
Transformer Model
      ↓
Generated Response
```

---

# Topic 8: Deep Learning Use Cases

## Vision

- Face Recognition
- OCR
- Image Classification

## Speech

- Speech Recognition
- Voice Assistants

## NLP

- ChatGPT
- Copilot
- Translation

## Autonomous Systems

- Robotics
- Self Driving Cars

---

# Hands-On Activity

## Create Folder Structure

```text
Week1
│
├── Day1
├── Day2
│
└── Day3
     │
     ├── Notes.md
     ├── DL-Diagrams.md
     ├── Assignment.md
     ├── Architect-Notes.md
     ├── DeepLearning.drawio
     └── DeepLearning.png
```

---

# Notes.md

```markdown
# Deep Learning Fundamentals

## What is Deep Learning?

Deep Learning is a subset of Machine Learning that uses Neural Networks.

## Neural Network Components

- Input Layer
- Hidden Layer
- Output Layer
- Weights
- Bias
- Activation Functions

## CNN

Used for image processing.

Examples:
- Face Recognition
- Medical Imaging

## RNN

Used for sequential data.

Examples:
- Language Translation
- Speech Recognition

## Transformers

Used by modern AI systems.

Examples:
- GPT
- ChatGPT
- Copilot
- Claude
- Gemini

## Key Learning

Transformers are the foundation of modern Generative AI systems.
```

---

# Draw.io Diagram

Create the below architecture:

```text
Deep Learning
│
├── Neural Networks
│   ├── Input Layer
│   ├── Hidden Layer
│   └── Output Layer
│
├── CNN
│   ├── Image Recognition
│   └── Object Detection
│
├── RNN
│   ├── Translation
│   └── Speech Recognition
│
└── Transformers
    ├── GPT
    ├── Claude
    ├── Gemini
    └── Copilot
```

Export:

```text
DeepLearning.png
```

Save:

```text
DeepLearning.drawio
```

---

# DL-Diagrams.md

```markdown
# Deep Learning Diagrams

![Deep Learning](DeepLearning.png)

## Neural Networks

Foundation of Deep Learning.

## CNN

Used for image processing.

## RNN

Used for sequence-based tasks.

## Transformers

Used in modern AI systems.

Examples:

- ChatGPT
- Copilot
- Gemini
- Claude

## Learning Outcome

Transformers revolutionized modern AI and enabled Large Language Models.
```

---

# Assignment.md

```markdown
# Day 3 Assignment

## Compare CNN, RNN and Transformers

| Model | Best For |
|---------|---------|
| CNN | Images |
| RNN | Sequential Data |
| Transformers | Language Models |

## CNN Examples

1. Face Recognition
2. Medical Imaging
3. Security Cameras

## RNN Examples

1. Language Translation
2. Speech Recognition
3. Time-Series Forecasting

## Transformer Examples

1. ChatGPT
2. Microsoft Copilot
3. GitHub Copilot
4. Gemini
5. Claude

## My Learning

Transformers are the foundation of modern Generative AI.
```

---

# Architect-Notes.md

```markdown
# Deep Learning and Azure Services

| Concept | Azure Service |
|----------|--------------|
| Deep Learning | Azure Machine Learning |
| GPU Compute | Azure AI Compute |
| LLM | Azure OpenAI |
| Transformers | GPT Models |
| Speech AI | Azure Speech Services |
| Vision AI | Azure AI Vision |
| OCR | Azure Document Intelligence |

## Enterprise Use Cases

- Chatbots
- AI Copilots
- Invoice Processing
- OCR
- Document Intelligence
- Image Classification

## Architect Learning

Understand how Deep Learning powers enterprise AI solutions on Azure.
```

---

# Day 3 Completion Checklist

- [ ] Created Day3 folder
- [ ] Completed Notes.md
- [ ] Completed DL-Diagrams.md
- [ ] Completed Assignment.md
- [ ] Completed Architect-Notes.md
- [ ] Created DeepLearning.drawio
- [ ] Exported DeepLearning.png
- [ ] Committed code to GitHub

---

# Day 3 Outcome

You should now understand:

- Deep Learning
- Neural Networks
- CNN
- RNN
- Transformers
- ChatGPT Architecture
- Azure OpenAI Foundations
- Enterprise Deep Learning Use Cases
