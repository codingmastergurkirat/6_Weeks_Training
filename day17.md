Day 17 - RecallCode Development: AI Code Feedback & Active Recall Generation

Date: 29 July 2026

Overview

The seventeenth day focused on developing the AI intelligence layer of RecallCode. We engineered structured LLM pipelines that evaluate user code submissions, explain logical mistakes, calculate asymptotic time and space complexity, and generate active recall flashcards to reinforce core intuition.

Topics Covered

Pedagogical AI Prompt Engineering

The difference between giving away solutions vs Socratic coaching
Designing system instructions that guide students toward self-correction
Structuring the AI prompt with problem description, user code, programming language, and test outputs
Multi-Dimensional Code Analysis

Approach Evaluation: Recognizing standard patterns (Two Pointers, Sliding Window, Dynamic Programming, BFS/DFS)
Bug & Mistake Diagnosis: Identifying off-by-one errors, unhandled edge cases, and redundant state
Asymptotic Complexity Deduction:
- Rigorous Big-O Time Complexity analysis with reasoning
- Auxiliary Space Complexity calculation
- Pinpointing bottlenecks that prevent scaling from $O(N^2)$ to $O(N \log N)$
Active Recall Question & Flashcard Generation

Extracting the core algorithmic invariant into conceptual questions
Example: Instead of memorizing code, asking "Why must the input array be sorted before applying two pointers?"
Structuring generated flashcards with Front (Prompt), Back (Intuition & Explanation), and Pattern Tag
Structured JSON Outputs & Validation

Using Pydantic schemas and JSON Mode to guarantee predictable response formats
Parsing structured feedback directly into React UI components (Complexity Badges, Mistake Callouts, Hint Drawers)
Practical Work

Implemented the `/api/ai/feedback` route using generative LLM API calls with JSON Schema enforcement.
Built prompt templates for code review, Big-O complexity explanation, and active recall flashcard creation.
Tested the feedback pipeline against various student submissions (optimal, sub-optimal, and syntax-broken).
Verified that the model accurately identified $O(N^2)$ vs $O(N)$ solutions on classic problems (e.g., Two Sum, 3Sum, Valid Anagram).
Saved generated active recall flashcards directly into the Supabase `flashcards` table upon successful code submission.
Key Takeaways

Socratic, structured AI feedback is vastly more educational than raw code completions or unguided chat.
Strict JSON schema enforcement ensures AI evaluations reliably render into UI cards, badges, and review tabs.
Automated flashcard generation converts every solved coding problem into permanent revision material.
Next Steps

Build the interactive Flashcard Review UI, Mastery Tracking, and Progress Analytics dashboards.
