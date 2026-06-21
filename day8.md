Day 8 - Advanced RAG Patterns & Hybrid Search

Date: 8 July 2026

Overview

The eighth day focused on overcoming the limitations of naive RAG pipelines by implementing Advanced RAG architectures. We integrated hybrid search combining lexical and semantic retrieval, reciprocal rank fusion, query transformation, and cross-encoder re-ranking.

Topics Covered

Limitations of Naive RAG

The "Lost in the Middle" phenomenon in long context windows
Semantic blindness to specific IDs, error codes, and technical jargon
False positive retrievals and semantic drift
Hybrid Search (Lexical + Semantic)

Combining BM25 (sparse keyword search) with dense vector retrieval
Why hybrid search provides superior coverage across technical and conversational queries
Reciprocal Rank Fusion (RRF) algorithm for merging disparate ranked lists
Query Transformation & Expansion

Multi-Query Generation: Using an LLM to generate multiple query perspectives
Hypothetical Document Embeddings (HyDE): Generating a hypothetical answer before embedding
Step-Back Prompting and Query Rewriting for conversational follow-ups
Re-Ranking with Cross-Encoders

Bi-Encoders (fast vector search) vs Cross-Encoders (deep query-document attention)
Using re-rankers (e.g., Cohere ReRank, BGE-Reranker) on initial Top-20 candidates
Narrowing down to the Top-3 to 5 highest-quality passages for prompt injection
Practical Work

Implemented a BM25 retriever alongside a ChromaDB vector retriever.
Combined both retrieval outputs using a custom Reciprocal Rank Fusion function.
Integrated a cross-encoder re-ranking model to filter and re-order retrieved passages.
Evaluated retrieval precision before and after re-ranking on domain-specific test questions.
Key Takeaways

Hybrid search resolves the blind spots of pure semantic search, particularly for technical terminology and syntax.
Re-ranking dramatically cleans the context fed into the LLM, reducing prompt token costs and hallucination risks.
Query transformation bridges user phrasing with the terminology in stored documentation.
Next Steps

Learn about LLM Tool Calling and Function Calling.
Enable models to query external systems and execute structured actions.
