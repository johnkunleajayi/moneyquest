# MoneyQuest

MoneyQuest is a financial decision-learning platform for people navigating important financial decisions. It helps learners practice realistic decisions, learn from consequences and mistakes, and strengthen financial decision-making through an adaptive, gamified learning journey. The initial learning journey is **Financial Resilience**, using realistic Nigerian financial contexts and an architecture suitable for future localization.

The core learning loop is:

**Scenario → Decision → Consequence → Explanation → Reflection → Retry/Next Challenge → Progress**

## Project status

This repository currently contains the project governance and planning foundation only. The application, database models, API endpoints, scenario engine implementation, frontend UI, and AI integration have not been built.

## Project documents

- [Product requirements](docs/product-requirements.md)
- [Architecture](docs/architecture.md)
- [Scenario authoring](docs/scenario-authoring.md)
- [Codex workflow](docs/codex-workflow.md)
- [Demo script](docs/demo-script.md)
- [Initial architecture decision](docs/decisions/001-initial-architecture.md)
- [Contributor guidance](AGENTS.md)

## Planned technology

- React, TypeScript, Vite, and Tailwind CSS for the frontend
- Python and FastAPI for the backend
- PostgreSQL for persistent learner data
- OpenAI API for the bounded AI Coach

These are planned technologies; dependencies and application code have not yet been added.

## Planned first vertical slice

An unexpected-expense Financial Resilience journey in a fictional Nigerian context: a learner makes a choice, receives a deterministic consequence and authored explanation, reflects, retries or advances, and sees progress. An optional AI Coach may explain or offer practice using the established outcome without changing it. See [the demo script](docs/demo-script.md) and [architecture](docs/architecture.md).
