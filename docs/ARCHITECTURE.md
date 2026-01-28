# System Architecture

The EPC Knowledge Assistant uses a Hybrid RAG pipeline:

1. User submits query through chat UI
2. Query is embedded into vector space
3. Hybrid retrieval is performed:
   - Semantic Vector Search (FAISS/Pinecone)
   - Keyword Search (BM25)
4. Retrieved context is injected into the LLM prompt
5. LLM generates citation-backed response
6. Feedback and logs are stored for monitoring
