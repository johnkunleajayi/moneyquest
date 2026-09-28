# Decision 001: Initial architecture

- **Status:** Accepted
- **Scope:** Hackathon MVP foundation

## Context

MoneyQuest is a financial decision-learning capstone for the Andela × MIVA × OpenAI Hack-a-thon. The MVP needs to demonstrate a complete Financial Resilience learning loop, clear component responsibilities, bounded AI coaching, and a reusable development and documentation workflow without premature complexity.

## Decisions

1. Use the planned React, TypeScript, Vite, and Tailwind CSS frontend with a Python and FastAPI backend, PostgreSQL for persistence, and OpenAI API for the AI Coach.
2. Keep Scenario Engine, Learning Engine, Mistake Bank, Gamification, and AI Coach as separated domain modules within the backend initially, not separate services.
3. Keep scenario evaluation and consequences deterministic and authoritative in the Scenario Engine.
4. Restrict the AI Coach to explaining, teaching, personalizing, and providing practice using bounded application-provided context. It cannot evaluate outcomes, change consequences, award rewards, or modify learner records.
5. Use an authored explanation as the reliable fallback when AI is unavailable or unsuitable.
6. Begin with validated, version-controlled scenario content and use PostgreSQL for learner progress and records requiring persistence. Decide later whether scenario content belongs in the database.
7. Build a small unexpected-expense Financial Resilience journey first, using fictional people and illustrative amounts in a Nigerian context.
8. Keep Codex integration visible through useful planning, repository guidance, review, focused testing, and documentation. Add a scenario-authoring skill only when the process is stable; add MCPs only for a concrete project need.

## Consequences

- The first implementation can demonstrate all five product components within one application deployment.
- Business-critical decision rules remain reviewable and testable without an LLM.
- The learner journey can remain usable if the AI Coach is unavailable.
- The initial architecture avoids microservices, advanced adaptive models, and elaborate extensibility mechanisms.
- Authentication, hosting, retention, production operations, scenario database storage, and exact learner segments remain open pending concrete requirements.

## Revisit when

Evidence from scenario authoring, learner feedback, content volume, collaboration needs, or deployment requirements shows that a recorded choice no longer serves the product.
