Day 16 - RecallCode Development: Supabase, PostgreSQL & Spaced Repetition Engine

Date: 27 July 2026

Overview

The sixteenth day focused on implementing database persistence and the spaced repetition scheduling engine for RecallCode. We deployed our relational schema onto Supabase PostgreSQL, configured Row-Level Security (RLS), and programmed the SuperMemo SM-2 algorithm to power algorithmic retention.

Topics Covered

Supabase Backend Architecture

Initializing Supabase client with Next.js (SSR and client-side hooks)
Configuring Supabase Auth for user authentication and session management
Enforcing Row-Level Security (RLS) policies: Users can only read and mutate their own submissions and reviews
Database Schema Implementation in PostgreSQL

Creating tables: `profiles`, `problems`, `submissions`, `flashcards`, and `reviews`
Indexing `user_id` and `next_review_date` for efficient daily review queries
Database triggers to automatically update user streak and solved counts upon submission
The Science of Spaced Repetition & SM-2 Algorithm

The Ebbinghaus Forgetting Curve and spaced review intervals
Understanding the SuperMemo SM-2 algorithm variables:
- Repetition Number ($n$): Consecutive successful recall sessions
- Ease Factor ($EF$): Multiplier reflecting item difficulty (default 2.5, minimum 1.3)
- Interval ($I$): Days until next review ($I(1)=1, I(2)=6, I(n)=I(n-1) \times EF$)
- Quality Score ($q$): User self-assessment from 0 (complete blackout) to 5 (perfect recall)
Algorithm Implementation & Queue Generation

Writing the TypeScript SM-2 utility function
Building the daily review query: Fetching problems and flashcards where `next_review_date <= NOW()`
Updating review states upon user rating after problem practice
Practical Work

Set up the Supabase project and executed SQL migration scripts to build all tables and RLS rules.
Implemented the SM-2 algorithm in TypeScript (`lib/spaced-repetition.ts`).
Built API endpoints to record problem attempts and recalculate the next review timestamp.
Tested the review queue query, confirming that scheduled items appear on their designated due dates.
Key Takeaways

The SM-2 algorithm provides an optimal mathematical schedule to reinforce memory right before forgetting occurs.
Supabase RLS allows confident, secure querying directly from the frontend while enforcing strict authorization.
Automating spaced repetition shifts coding practice from ad-hoc problem cramming into systematic, compounding mastery.
Next Steps

Integrate Generative AI for automated code feedback, complexity analysis, and active recall generation.
