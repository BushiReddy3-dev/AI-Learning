# Architect Notes

## Enterprise Search Architecture

Documents
↓
Blob Storage
↓
Indexer
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
| Document Storage | Blob Storage |
| Search Platform | Azure AI Search |
| Embeddings | Azure OpenAI |
| LLM | Azure OpenAI |
| Authentication | Entra ID |
| Secrets | Key Vault |
| Monitoring | Azure Monitor |

---

## Design Considerations

### Index Design

Keep metadata fields.

Examples:

- Project
- Department
- Author
- Classification

---

### Security

Restrict search results.

Users should only retrieve authorized content.

---

### Cost

Monitor:

- Search Queries
- Storage
- Indexer Execution

---

### Performance

Optimize:

- Index Fields
- Filters
- Scoring Profiles

---

## Enterprise Use Cases

- Enterprise Knowledge Search
- HR Assistant
- IT Support Assistant
- Policy Search
- Document Search

## Architect Learning

Azure AI Search is the primary retrieval layer of enterprise RAG solutions.