# Architect Notes

## Enterprise Retrieval Architecture

Documents
↓
Chunking
↓
Embeddings
↓
Azure AI Search
↓
Retriever
↓
GPT Model
↓
Response

---

## Azure Service Mapping

| Capability | Azure Service |
|------------|---------------|
| Embeddings | Azure OpenAI |
| Vector Store | Azure AI Search |
| LLM | Azure OpenAI GPT |
| Authentication | Entra ID |
| Monitoring | Azure Monitor |
| Secrets | Key Vault |

---

## Design Considerations

### Chunking

Split large documents into smaller chunks.

### Metadata

Store:

- Project
- Author
- Document Type
- Created Date

### Security

User should only access authorized content.

### Cost

Monitor:

- Embedding Generation
- Storage
- Search Queries

### Performance

Optimize chunk size.

---

## Enterprise Use Cases

- Knowledge Assistant
- Support Assistant
- HR Assistant
- Documentation Search
- Incident Resolution Assistant

## Architect Learning

Embeddings are the retrieval foundation of all RAG architectures.