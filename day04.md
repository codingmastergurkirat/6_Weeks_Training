Day 4 - Conversational State & LLM Memory

Date: 29 June 2026

Overview

The fourth day covered state management and conversational memory in LLM applications. We addressed the inherent statelessness of language models and implemented strategies to maintain context over prolonged multi-turn conversations without overflowing token limits.

Topics Covered

Statelessness & Context Windows

Why LLMs are fundamentally stateless
Understanding the token context window as a finite working memory
The cost, latency, and degradation implications of large context histories ("Lost in the Middle")
Memory Types & Strategies

Conversation Buffer Memory: Storing raw history verbatim
Conversation Buffer Window Memory: Retaining only the last $K$ turns
Conversation Summary Memory: Using an LLM to progressively summarize older interactions
Summary with Buffer Hybrid Memory: Summarizing past context while keeping recent turns verbatim
Vector Store-backed Memory: Retrieving past conversation snippets based on semantic relevance
LangChain Memory Implementation

Using `ChatMessageHistory` and message role abstractions (`HumanMessage`, `AIMessage`, `SystemMessage`)
Wrapping chains with `RunnableWithMessageHistory` for session isolation
Configuring session IDs for multi-user chat applications
Persistent Storage

Moving beyond in-memory dictionaries
Persisting chat history in SQLite and Redis for production scalability
Managing session lifecycles, TTLs, and cleanup
Practical Work

Built a multi-turn terminal chatbot capable of remembering user details across messages.
Implemented a sliding-window memory that limits context to the last 5 conversation turns.
Created a summary memory chain that periodically condenses message logs using an LLM call.
Connected SQLite persistence to save chat sessions across application restarts.
Key Takeaways

Effective conversational AI requires deliberate memory pruning and summarization strategies.
Sliding windows and summary memory prevent context exhaustion in long sessions.
Session IDs combined with persistent backends allow multi-tenant conversational applications.
Next Steps

Learn about text embeddings and vector representations.
Understand Transformer self-attention mechanisms.
Explore semantic search fundamentals.
