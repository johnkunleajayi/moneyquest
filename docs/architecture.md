# Architecture

## Architectural approach

Use a React and TypeScript frontend with a Python and FastAPI backend and PostgreSQL for persistent learner data. Keep the five product engines as clearly separated domain modules within the backend initially; they are conceptual and code ownership boundaries, not separate services. This provides disciplined responsibilities without premature deployment and infrastructure complexity.

Use the OpenAI API only for the bounded AI Coach role. The learner flow and authored explanations must remain useful when the model is unavailable.

## Component responsibilities

### Scenario Engine

- Own scenario definitions and deterministic evaluation rules.
- Accept a scenario version and learner choice and return a structured outcome, including relevant consequences, outcome category, and information needed by other components.
- Be the sole authority for scenario correctness and consequences.
- Do not award rewards, determine learning progression, or use generated AI judgments to evaluate answers.

### Learning Engine

- Own learning objectives, feedback sequencing, reflection prompts, and retry or next-challenge selection.
- Use scenario outcomes and learning signals, including relevant repeated mistakes, to select what to show next.
- Begin with explicit, reviewable rules.
- Do not recalculate scenario outcomes or own rewards.

### Mistake Bank

- Record mistakes and their associated concepts or objectives based on scenario results.
- Provide relevant summaries to the Learning Engine and AI Coach.
- Keep records structured and limited to what supports practice.
- Do not judge a learner’s character, diagnose them, or let generated explanations rewrite outcomes.

### Gamification

- Award points, badges, streaks, or progress markers according to explicit rules.
- Consume completion and learning events; do not decide correctness or independently change the learning path.

### AI Coach

- Explain known outcomes in accessible language, connect them to learning objectives, encourage reflection, or offer additional practice.
- Receive bounded context assembled by the application: scenario facts, deterministic outcome, learning objective, and relevant mistake summary.
- Never evaluate or override outcomes, change consequences, award rewards, or modify learner records.
- Fall back to authored explanations when unavailable or when a response is unsuitable.

## Deterministic responsibilities

Keep scenario evaluation and consequence calculation, answer-to-outcome/objective mapping, mistake recording triggers and classification, retry/next-challenge eligibility, reward rules, progress totals, and persistence of attempts/progress explicit and testable. AI may vary wording, examples, and practice prompts, but must not change an authoritative result for the same scenario version and choice.

## Boundaries and information flow

The Scenario Engine returns the outcome. The Learning Engine uses that outcome and learning signals to choose feedback and the next step. The Mistake Bank records defined learning needs. Gamification responds to defined events. The application may assemble bounded context for the AI Coach, whose response is explanatory or practice content only. These interactions may use explicit interfaces and events; a distributed event architecture is not required for the MVP.

## Planned repository organization

- `frontend/`: React, TypeScript, Vite, and Tailwind application.
- `backend/`: FastAPI application, API layer, domain modules, and infrastructure adapters.
- `backend/.../domain/`: scenario, learning, mistake, gamification, and coaching responsibilities as modules in one backend.
- `content/scenarios/`: version-controlled scenario content, validated by the backend.
- `docs/`: requirements, architecture, authoring, workflow, demo, and decisions.

Scenario content may begin in validated version-controlled files. PostgreSQL is intended for learner progress and records requiring persistence. Whether scenario content itself should be stored in PostgreSQL remains an implementation decision to make when authoring and deployment needs are clearer.

## Data and safety principles

Use fictional people and illustrative amounts in the prototype. Collect only data needed for attempts and progress. Avoid real financial account connections and detailed personal financial profiles. Keep assumptions visible in authored scenarios; do not represent the prototype as individualized financial advice.

## Planned stack

React, TypeScript, Vite, and Tailwind CSS; Python and FastAPI; PostgreSQL; OpenAI API for the AI Coach. These choices do not require a service per engine or an elaborate extensibility framework.

## Production path

Before production, resolve authentication, hosting, data retention, privacy, operational monitoring, and content review requirements. Those details are not specified in the current product brief and should not be guessed in the prototype architecture.
