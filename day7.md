Day 7 - Retrieval-Augmented Generation (RAG) Fundamentals

Date: 6 July 2026

Overview

The seventh day marked the implementation of our first end-to-end Retrieval-Augmented Generation (RAG) system. We addressed the hallucination problem in LLMs by grounding their generative capabilities in external, authoritative knowledge bases.

Topics Covered

The Need for RAG

Why LLM pre-training knowledge is static, cutoff-bound, and prone to hallucinations
Fine-tuning vs RAG: When to use which approach
The RAG tri-part framework: Ingestion, Retrieval, and Generation
Document Ingestion & Chunking

Document Loaders for unstructured data: PDFs, Markdown files, HTML, and text files
Chunking strategies: Fixed-size chunking vs Semantic chunking
`RecursiveCharacterTextSplitter`: Chunk size and chunk overlap dynamics
The impact of chunk boundary truncation on semantic coherence
The Retrieval Pipeline

Embedding chunks and indexing them in ChromaDB
Formulating the retrieval query from user input
Retrieving the Top-K most relevant chunks
Prompt Augmentation & Generation

Injecting retrieved context into structured system prompts
Strict grounding instructions: "Answer based only on the provided context"
Citations and source attribution in model answers
Practical Work

Loaded external algorithm guides and technical documentation.
Split long documents using `RecursiveCharacterTextSplitter(chunk_size=500, chunk_overlap=50)`.
Indexed chunks into ChromaDB and wired a LangChain LCEL RAG chain.
Tested the system with targeted questions, validating that answers accurately cited retrieved chunks without hallucinations.
Key Takeaways

RAG bridges the gap between private enterprise/technical data and general-purpose LLM reasoning.
Chunking strategy is one of the most critical hyperparameters determining retrieval success.
Clear prompt constraints prevent the model from guessing when context is insufficient.
Next Steps

Explore Advanced RAG architectures.
Learn about Hybrid Search (BM25 + Dense Vectors) and Cross-Encoder Re-ranking.
Implement query expansion and rewrite strategies.
