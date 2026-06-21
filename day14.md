Day 14 - Project Inception: RecallCode Architecture & System Design

Date: 22 July 2026

Overview

The fourteenth day marked the official inception and architectural planning of our Capstone Project: **RecallCode**—an AI-powered DSA learning and retention platform. We designed the end-to-end system architecture, selected the modern tech stack, defined PostgreSQL database schemas in Supabase, and formulated the development roadmap leading up to the final presentation at Alert.

Topics Covered

The Core Problem in Technical Interview Preparation

The "Forgetting Curve" in Data Structures & Algorithms (DSA): Students solve hundreds of LeetCode problems but forget core intuition weeks later
Passive learning vs Active Recall: Reading solutions gives an illusion of competence without long-term retention
Lack of personalized pedagogical feedback on time complexity, space complexity, and specific approach mistakes
RecallCode Core Value Proposition

Interactive multi-language coding environment with real-time execution
Automated active recall questions and algorithmic concept flashcards
Spaced repetition scheduling (SuperMemo SM-2 algorithm) to maximize memory consolidation
AI-powered pedagogical feedback, time/space complexity analysis, and mastery analytics
Tech Stack Selection & Architecture

Frontend: Next.js (App Router), React, TypeScript, Tailwind CSS
Code Editor: Monaco Editor (VS Code in-browser editing experience)
Code Execution: JDoodle API (remote sandboxed compilation across C++, Python, Java, JavaScript)
Backend & Database: Supabase (PostgreSQL, Row-Level Security, Authentication, Realtime)
AI Engine: Generative AI (LLMs) with structured outputs for feedback, complexity analysis, and flashcard generation
Database Schema Design (PostgreSQL)

`users`: Profile, streak counter, total solved, mastery level
`problems`: Title, slug, difficulty, topic tags, description, starter templates, test cases
`submissions`: Code payload, language, execution status, runtime, memory, AI feedback report
`flashcards`: Conceptual prompts, algorithmic patterns, code snippets, linked problem ID
`spaced_reviews`: SM-2 parameters (repetition number, ease factor, interval, next review date)
Practical Work

Drafted the complete system architecture diagram and component hierarchy.
Designed the relational PostgreSQL schema with foreign keys and indexes.
Set up the project repository with Next.js, TypeScript, and ESLint configurations.
Pitched the RecallCode project specification to mentors at Alert and received approval for capstone development.
Key Takeaways

Combining spaced repetition with practical code execution bridges the gap between memory retention and implementation skill.
Monaco Editor + JDoodle provides a robust, sandboxed coding workbench without the overhead of building a custom container runner.
Supabase and Next.js offer rapid development velocity with production-grade database security through Row-Level Security (RLS).
Next Steps

Begin Phase 1 of Development: Build the Next.js frontend, embed Monaco Editor, and integrate JDoodle code execution.
