Day 15 - RecallCode Development: Next.js, Monaco Editor & JDoodle Integration

Date: 24 July 2026

Overview

The fifteenth day focused on building the core interactive coding environment of RecallCode. We integrated Monaco Editor into a Next.js (TypeScript) application and connected the JDoodle API to compile and execute code across multiple programming languages in real time.

Topics Covered

Frontend Architecture & Layout

Next.js App Router structure: Split-pane workbench (Problem Description on the left, Monaco Editor & Console on the right)
Responsive layout using Tailwind CSS and resizable panel components
Dark/Light theme synchronization with Monaco Editor
Monaco Editor Integration in React

Setting up `@monaco-editor/react` with dynamic language switching (Python, C++, Java, JavaScript)
Configuring editor options: font size, minimap, bracket pair colorization, tab sizing, and keybindings
Managing editor state and handling boilerplate code insertion for selected problems
Multi-Language Code Execution with JDoodle

JDoodle REST API architecture: Client ID, Client Secret, language codes, and version indexes
Formatting execution payloads with custom `stdin` for test case verification
Parsing execution responses: `output`, `statusCode`, `memory`, and `cpuTime`
Handling compilation errors, runtime exceptions, and execution timeouts gracefully
Secure Backend API Routing

Building the Next.js API route `/api/execute` to proxy JDoodle requests
Preventing exposure of JDoodle API credentials on the client side
Rate-limiting and request validation using Zod
Practical Work

Created the interactive problem-solving page layout with resizable split-panes.
Configured Monaco Editor with language-specific starter templates and syntax highlighting.
Built the `/api/execute` backend route connecting to JDoodle's execution endpoints.
Successfully compiled and ran C++, Java, Python, and JavaScript code against sample test cases with real-time terminal output rendering.
Key Takeaways

Monaco Editor brings a familiar, high-performance IDE experience directly into the browser.
Server-side API routes are essential to protect third-party API credentials and sanitize execution inputs.
Clear separation between execution stdout and stderr makes debugging intuitive for students.
Next Steps

Configure Supabase, deploy PostgreSQL tables, and implement the Spaced Repetition (SM-2) engine.
