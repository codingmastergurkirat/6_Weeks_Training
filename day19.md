Day 19 - System Integration, End-to-End Testing & AI Optimization

Date: 3 August 2026

Overview

The nineteenth day was dedicated to system-wide integration, end-to-end user flow testing, and performance optimization for RecallCode. We benchmarked AI response latencies, implemented streaming feedback via Server-Sent Events, handled execution edge cases, and hardened application reliability.

Topics Covered

End-to-End Integration Testing

Validating the complete user journey:
1. User logs in via Supabase Auth
2. Selects a problem and writes code in Monaco Editor
3. Executes code against test cases using JDoodle API
4. Receives streaming AI feedback on logic, time complexity, and space complexity
5. Automatically receives generated active recall flashcards
6. Flashcard is scheduled into the user's daily SM-2 review queue
AI Latency Optimization & Streaming

Switching from blocking API calls to streaming token responses using Server-Sent Events (SSE)
Reducing perceived user latency: First feedback token renders in under 800ms
Progressive UI rendering of complexity badges and active recall questions
Error Handling & Edge Cases

Handling JDoodle compilation errors, execution timeouts (infinite loops), and rate limits
Sanitizing code inputs to prevent prompt injection inside AI review pipelines
Managing network drops and offline states gracefully in Next.js
Database Optimization

Adding PostgreSQL composite indexes on `(user_id, next_review_date)` and `(user_id, topic)`
Verifying Supabase Row-Level Security policies to prevent unauthorized data access
Practical Work

Configured Server-Sent Events (SSE) on the `/api/ai/feedback` route for real-time streaming feedback.
Executed an automated test suite across 25 diverse DSA problems in Python, C++, and Java.
Tested stress conditions: deliberately submitted infinite loops, invalid syntax, and huge outputs to verify sandbox safety.
Achieved sub-second TTFT (Time to First Token) and verified flawless SM-2 review interval scheduling.
Key Takeaways

Streaming AI responses transforms the user experience from an agonizing wait into an engaging, real-time consultation.
Sandboxed execution APIs must have strict timeouts to isolate malicious or accidental infinite loops.
Rigorous end-to-end testing confirmed that all components (Next.js, Monaco, JDoodle, Supabase, AI) work together harmoniously.
Next Steps

Prepare the presentation slide deck, record demo videos, write project documentation, and rehearse the presentation.
