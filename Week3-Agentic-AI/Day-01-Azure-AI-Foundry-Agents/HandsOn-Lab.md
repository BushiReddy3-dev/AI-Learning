# Week 3 Day 1 Hands-On Lab

# Scenario

Design Employee Exit Assistant

Goal:

Use Azure AI Foundry Agent Architecture.

---

# Business Requirements

The assistant should:

1. Search policies

2. Search employee documents

3. Generate exit checklist

4. Create service request

5. Generate email template

---

# Architecture Components

Frontend

- Teams
- Web Application

Agent Layer

- Employee Exit Agent

AI Layer

- Azure OpenAI

Knowledge Layer

- Azure AI Search

Documents

- SharePoint

Operations

- Service Desk
- HRMS

---

# Security Requirements

- Entra ID
- Managed Identity
- RBAC
- Key Vault

---

# Monitoring

- Azure Monitor
- Application Insights

---

# Deliverable

Create Draw.io Architecture

Show:

Employee
↓
Teams
↓
Foundry Agent
↓
Azure OpenAI
↓
Azure AI Search
↓
SharePoint

and

Foundry Agent
↓
HRMS

Foundry Agent
↓
Ticketing System

Include Security Layer.
``