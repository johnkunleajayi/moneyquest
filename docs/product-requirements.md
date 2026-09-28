# Product requirements

## Project context

MoneyQuest is the capstone project for the **Andela × MIVA × OpenAI Hack-a-thon**, in the **Engagement & Staying in the Learning Journey** track, with **Finance** as the impact theme.

## Product concept

MoneyQuest is a financial decision-learning platform. It helps people practice realistic financial decisions, learn from consequences and mistakes, and develop stronger financial decision-making skills through an adaptive, gamified learning journey.

The product is for people navigating important financial decisions; it is not restricted to young people.

## Initial learning journey

The first journey is **Financial Resilience**. The MVP should use realistic Nigerian financial contexts while keeping the architecture suitable for future localization.

## Core learning loop

**Scenario → Decision → Consequence → Explanation → Reflection → Retry/Next Challenge → Progress**

## Major product components

- Scenario Engine
- Learning Engine
- Mistake Bank
- Gamification
- AI Coach

The Scenario Engine is the deterministic authority for scenario evaluation. The AI Coach may explain, teach, personalize, and provide additional practice, but must not determine the correct financial outcome or override deterministic business rules.

## Planned technical stack

- React, TypeScript, and Vite
- Tailwind CSS
- Python and FastAPI
- PostgreSQL
- OpenAI API for the AI Coach

## Confirmed hackathon judging criteria

1. **Depth of Codex Integration:** Codex should be visible across planning, building, reviewing, and documenting. `AGENTS.md`, Plan Mode, MCPs, and reusable skills can strengthen the submission.
2. **Real-world Impact:** Explain the concrete problem, who benefits, and how it connects to Finance.
3. **Reusability & Adoption Potential:** Make the project understandable and usable by contributors beyond its creator, with clean structure, documentation, and a credible path from prototype to production.
4. **Demo & Pitch Quality:** Prepare a 3–5 minute walkthrough of the problem, solution, Codex’s role, and what another month could enable.

## MVP scope

The smallest credible MVP is one complete Financial Resilience learning journey with a small set of connected scenarios sufficient to demonstrate a decision, deterministic consequence, explanation, reflection, retry or next challenge, and progress. It includes mistake capture, a few explicit gamification rules, and an optional bounded AI Coach explanation or practice prompt. Use fictional learner details and illustrative amounts.

This is a prototype for decision learning. It should not present itself as individualized financial advice or recommend real financial products.

## Explicitly outside the initial MVP

- A large scenario library or multiple complete learning journeys
- Personalized financial advice, product comparisons, or transaction recommendations
- AI-generated scoring, consequence calculation, or unrestricted scenario generation
- Real financial account connections, payments, or unnecessary sensitive financial data collection
- Social feeds, leaderboards, peer messaging, or complex competition mechanics
- Advanced adaptive learning models before there is evidence and data to justify them
- Microservices, event streaming, elaborate plugin systems, or multi-tenant administration
- Full localization beyond keeping context and presentation suitable for future localization
- Claims that a prototype demo establishes long-term financial outcomes

## Open product details

The confirmed brief does not specify detailed scenario content, the precise intended learner segments, assessment measures, persistence and retention policy, authentication, deployment, or production operations. Do not invent these as settled requirements; resolve them when needed and document decisions.
