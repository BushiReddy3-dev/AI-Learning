# Architect Notes

## Enterprise RAG Architecture

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
Response

---

## Azure Services Mapping

| Capability | Azure Service |
|------------|---------------|
| Embeddings | Azure OpenAI |
| Retrieval | Azure AI Search |
| LLM | Azure OpenAI GPT |
| Authentication | Entra ID |
| Monitoring | Azure Monitor |
| Secrets | Azure Key Vault |
| API Layer | ASP.NET Core API |

---

## Security Considerations

### Authentication

Microsoft Entra ID

### Authorization

Azure RBAC

### Secrets

Azure Key Vault

### Monitoring

Azure Monitor
Application Insights

### Networking

Private Endpoint

---

## Metadata Recommendations

Store:

- Document Name
- Project
- Department
- Author
- Created Date
- Classification

---

## Cost Optimization

- Chunk documents
- Cache responses
- Limit token usage
- Use Hybrid Search
- Monitor search operations

---

## Enterprise Use Cases

- HR Assistants
- Project Assistants
- Knowledge Search
- Support Assistants
- Internal Copilots

## Architect Learning

RAG is the foundation of most enterprise AI applications.