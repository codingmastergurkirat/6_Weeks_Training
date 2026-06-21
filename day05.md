Day 5 - Transformers, Embeddings & Semantic Search

Date: 1 July 2026

Overview

The fifth day provided a technical foundation in Transformer architectures and vector embeddings. We explored how text is transformed into dense mathematical vectors that capture semantic meaning, enabling semantic search and similarity matching beyond keyword matching.

Topics Covered

Transformer Architecture Essentials

The evolution from RNNs/LSTMs to Transformers
The Self-Attention mechanism: Query (Q), Key (K), and Value (V) calculations
Encoder-only (BERT), Decoder-only (GPT), and Encoder-Decoder (T5) architectures
Tokenization, subwords (Byte-Pair Encoding), and positional encodings
Vector Embeddings

What is a dense embedding vector?
How semantic relationships are represented in high-dimensional vector spaces
Comparing sparse embeddings (TF-IDF, BM25) vs dense embeddings (Sentence Transformers)
Popular embedding models: OpenAI `text-embedding-3`, HuggingFace `all-MiniLM-L6-v2`, Google `text-embedding-004`
Vector Distance & Similarity Metrics

Cosine Similarity (measuring angle between vectors)
Euclidean Distance ($L2$ norm)
Dot Product (inner product for normalized vectors)
When to use each similarity metric depending on vector normalization
Semantic Search Principles

Why keyword search fails on synonyms, context, and paraphrasing
The semantic search workflow: Query embedding -> Distance computation -> Top-K ranking
Practical Work

Generated dense vector embeddings for sample texts and coding problem descriptions.
Calculated cosine similarity matrices between related and unrelated technical concepts.
Built a simple nearest-neighbor semantic search script in Python using NumPy.
Visualized 2D projections of multi-dimensional embeddings using PCA and t-SNE.
Key Takeaways

Embeddings translate semantic language meaning into geometry in high-dimensional space.
Cosine similarity is the primary metric for comparing normalized text vectors.
Semantic search matches concepts and intent rather than exact surface keywords.
Next Steps

Study dedicated Vector Databases (ChromaDB, FAISS).
Learn vector indexing algorithms like HNSW.
Implement metadata filtering for technical datasets.
