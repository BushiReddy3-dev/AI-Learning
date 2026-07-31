# Architect Notes

## Architect Perspective

Do not think:

"What is an Agent?"

Think:

"How should enterprise agents be designed?"

---

## Architecture Layers

Presentation Layer

- Teams
- Web App
- Mobile

Agent Layer

- Planner Agent
- Orchestrator Agent
- Domain Agents

Knowledge Layer

- Azure AI Search
- Vector Database
- SharePoint

Business Layer

- ERP
- CRM
- HR Systems

Infrastructure Layer

- Azure OpenAI
- Azure Functions
- Azure Monitor

---

## Security Controls

- Entra ID
- RBAC
- Managed Identity
- Private Endpoints
- Key Vault

---

## Governance

- Prompt Management
- Content Filtering
- Monitoring
- Cost Tracking

---

## Multi-Agent Principle

Enterprise architecture should avoid one giant agent.

Prefer:

Planner Agent
↓
Specialized Agents

Benefits:

- Easier Scaling
- Better Reliability
- Easier Maintenance