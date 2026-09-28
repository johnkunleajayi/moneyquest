# MoneyQuest contributor guidance

Before changing product behaviour or architecture, read `docs/product-requirements.md` and `docs/architecture.md`. Treat them as the approved product and architecture baseline; raise unresolved conflicts instead of inventing requirements.

- Keep the Scenario Engine the deterministic authority for scenario evaluation and consequences.
- Keep the AI Coach bounded to explanation, teaching, personalization, and additional practice. It must not determine outcomes, override business rules, or award rewards.
- Test business-critical deterministic rules, including evaluation and any progression or reward rules that are implemented.
- Prefer the smallest clear design that meets approved requirements. Avoid premature services, abstractions, and infrastructure.
- Update relevant documentation when product behaviour, architecture, scenario authoring, or contributor workflow changes.
- Do not add product requirements, integrations, or dependencies without approval.
