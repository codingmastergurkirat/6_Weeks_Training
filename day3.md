Day 3 - LangChain Fundamentals & LCEL

Date: 26 June 2026

Overview

The third day introduced the LangChain framework, focusing on its modular components, unified provider abstractions, and the LangChain Expression Language (LCEL). We transitioned from raw API scripts to structured, composable AI pipelines.

Topics Covered

LangChain Architecture

Why use an orchestration framework?
Core abstractions: Prompts, Models, Output Parsers, and Runnables
Unified chat model interfaces across Google Gemini, Anthropic Claude, and OpenAI
LangChain Expression Language (LCEL)

The declarative philosophy of LCEL
The pipe operator (`|`) for chaining runnables seamlessly
Batching, streaming, and asynchronous execution out-of-the-box
Inspectability and fallbacks using `with_fallbacks()`
Output Parsers

`StrOutputParser` for clean string responses
`JsonOutputParser` and `PydanticOutputParser` for strict typed objects
Automated format instructions injection
Complex Chain Composition

Sequential chains passing data from one model invocation to the next
Parallel branches using `RunnableParallel` to execute concurrent tasks
Conditional routing using `RunnableBranch`
Practical Work

Installed and configured `langchain`, `langchain-core`, and provider packages.
Built an LCEL chain combining `PromptTemplate | ChatModel | StrOutputParser`.
Implemented a multi-step pipeline: Input Analysis -> Content Generation -> Structured Output Parsing.
Integrated parallel execution to evaluate a code snippet with two different model personas concurrently.
Key Takeaways

LCEL provides a clean, declarative syntax that handles streaming, batching, and async seamlessly.
LangChain abstracts away provider-specific API nuances, enabling easy model swapping.
Output parsers provide the bridge between unstructured language and typed backend application code.
Next Steps

Explore LLM state and memory systems.
Learn how to maintain multi-turn conversational context.
Implement persistent chat history mechanisms.
