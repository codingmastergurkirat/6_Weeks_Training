Day 9 - Tool Use, Function Calling & Code Execution APIs

Date: 10 July 2026

Overview

The ninth day explored how LLMs interact with external computational environments through tool use and function calling. We learned how models can decide when to invoke external tools, generate structured arguments conforming to JSON schemas, and evaluate code execution results.

Topics Covered

Understanding Tool Use in LLMs

The boundary between pure language generation and environmental action
How LLMs do not execute code directly, but emit structured call intents
The tool execution cycle: Prompt -> Tool Call Generation -> Runtime Execution -> Tool Output Injection -> Final Synthesis
Function Calling Mechanisms

JSON Schema specifications for function signatures (parameters, types, descriptions)
Provider implementations: OpenAI Function Calling, Gemini Function Calling, Anthropic Tool Use
LangChain `@tool` decorator and `bind_tools()` abstraction
Connecting Code Execution Engines

Integrating remote code execution APIs (e.g., JDoodle, Judge0)
Passing language, code payload, stdin, and parsing compilation errors and execution outputs
Security considerations: Timeouts, memory caps, parameter sanitization, and execution sandboxing
Practical Work

Defined custom Python tools for mathematical computation, database lookup, and code execution.
Bound tools to a ChatModel and executed multi-step tool calling flows.
Built a system that queries problem metadata and simulates test case validation based on natural language queries.
Tested tool error recovery when invalid arguments or syntax errors were encountered during execution.
Key Takeaways

Well-crafted docstrings and parameter descriptions in tool definitions are crucial for the model to know when and how to call tools.
Strict parameter validation protects backend systems from malformed agent invocations.
Tool use transforms LLMs from passive text generators into active computational operators.
Next Steps

Transition from scripted tool calling to fully autonomous AI Agents.
Study reasoning loops and the ReAct (Reasoning + Acting) framework.
