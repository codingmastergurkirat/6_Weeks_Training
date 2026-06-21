Day 21 - Final Capstone Project Presentation: RecallCode at Alert

Date: 6 August 2026

Overview

The final day of the summer internship and training program was dedicated to delivering the formal capstone project presentation on **RecallCode** at Alert / AlertEnterprise. The presentation covered the core educational problem, technical architecture, live interactive demonstration of multi-language coding, AI feedback, and spaced repetition, followed by a rigorous technical defense and Q&A session with the evaluation panel and mentors.

Topics Covered

Final Project Presentation & Defense at Alert

Delivered the capstone presentation before the evaluation panel, technical mentors, and fellow interns:
Project Title: RecallCode - AI-Powered DSA Learning & Retention Platform
Presenter: Gurkirat Singh
Organization / Venue: Alert / AlertEnterprise (Summer Internship Final Project Evaluation)
Key Presentation Sections

1. Problem Statement & Motivation
   - The "Forgetting Curve" in algorithmic problem-solving: students practice hundreds of questions on LeetCode/HackerRank, but quickly lose intuition and pattern recognition after a few weeks.
   - Traditional platforms focus solely on binary test-case validation (Pass/Fail) without explaining *why* an approach was chosen, why an approach is sub-optimal, or how to retain the concept long-term.
   - The need for an active recall and spaced repetition system combined directly with an in-browser code editor and pedagogical AI mentor.

2. Platform Architecture & Engineering Stack
   - Frontend: Next.js (App Router), React, TypeScript, and Tailwind CSS delivering a responsive, split-pane coding workbench.
   - In-Browser IDE: Monaco Editor offering syntax highlighting, autocompletion, and multi-language support.
   - Remote Code Execution: JDoodle API integration proxying compilation and execution for C++, Python, Java, and JavaScript inside a secure sandbox.
   - Backend & Database: Supabase PostgreSQL with Row-Level Security (RLS) policies, session management, and relational schema.
   - AI Intelligence Layer: Prompt-engineered Generative AI pipelines delivering streaming pedagogical feedback, Big-O time and space complexity proofs, and automated active recall flashcard generation.
   - Retention Engine: SuperMemo SM-2 Spaced Repetition algorithm calculating optimal review intervals based on user recall difficulty.

3. Live Software Demonstration
   - Demo 1 (Interactive Coding & JDoodle Execution): Solved an algorithmic problem in Monaco Editor in Python. Executed code against sample test cases via JDoodle with real-time console streaming.
   - Demo 2 (Streaming AI Feedback & Complexity Analysis): Submitted a sub-optimal solution. Showcased streaming AI feedback that diagnosed the inefficiency, deduced $O(N^2)$ time complexity, and offered Socratic hints toward an $O(N)$ approach without spoiling the solution.
   - Demo 3 (Active Recall & Flashcard Generation): Displayed the automated creation of conceptual flashcards capturing the core problem invariant.
   - Demo 4 (Spaced Repetition & Mastery Dashboard): Completed a daily flashcard review drill using the 3D flip card interface, rated recall difficulty, verified SM-2 interval updates in Supabase, and inspected the dynamic progress analytics and topic mastery charts.

4. Technical Defense & Q&A
   - Addressed panel questions regarding code execution sandboxing, timeout enforcement, and security isolation.
   - Defended the choice of the SM-2 algorithm over simple fixed-interval scheduling for retention optimization.
   - Explained the prompt engineering strategies and JSON schema validations used to eliminate LLM hallucinations during complexity analysis.
   - Discussed scalability considerations: caching frequent AI evaluations, database indexing on review queues, and potential migration to self-hosted Dockerized execution runners.

Practical Work

Delivered the full 20-minute presentation and 10-minute live demonstration without technical hitches.
Successfully defended the architecture, data models, and algorithmic designs during the mentor Q&A.
Completed final repository handover, including comprehensive documentation, setup guides, and database migration scripts.
Received formal project evaluation, positive feedback from mentors at Alert, and successfully concluded the internship program.

Key Takeaways

Successfully conceptualized, built, and defended RecallCode as the capstone project at Alert.
Mastered end-to-end full-stack AI development: bridging modern web frameworks (Next.js, React, TypeScript), database engineering (Supabase, PostgreSQL), developer tooling (Monaco Editor, JDoodle API), and Generative AI.
Validated the power of combining cognitive learning science (Active Recall & Spaced Repetition) with generative AI to solve real learning problems.
Concluded the internship training program with exemplary marks and commendations from the review panel at Alert.

Next Steps

Deploy RecallCode to production on Vercel and Supabase Cloud for public student access.
Expand the problem catalog with community-contributed questions and automated test case generators.
Continue advancing expertise in AI system engineering, multi-agent workflows, and high-performance software design.
