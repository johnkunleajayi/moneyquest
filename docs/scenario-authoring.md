# Scenario authoring

This guide records the intended authoring contract for Financial Resilience scenarios. The scenario format and validator have not yet been implemented.

## Authoring principles

- Use realistic Nigerian financial contexts while keeping locale-specific context in content where practical so future localization remains possible.
- Use fictional people and illustrative amounts.
- State assumptions needed to understand and evaluate the situation.
- Make each scenario serve a clear learning objective and decision-learning purpose.
- Define choices and their outcomes clearly enough for deterministic evaluation.
- Provide an authored explanation that can be shown without the AI Coach.
- Do not frame the scenario as individualized financial advice or a recommendation to use a real financial product.

## Information a scenario should define

As the scenario format is designed, it should represent:

- A stable scenario identifier and version.
- The scenario context and relevant assumptions.
- The learning objective.
- The decision prompt and available choices.
- Explicit deterministic evaluation and consequences for choices.
- Outcome categories and any mistake/concept mapping used by the Mistake Bank.
- An authored explanation and reflection prompt.
- The defined retry or next-challenge relationship, if applicable.

This is a content checklist, not a final schema. Avoid adding fields without a concrete use in the learner journey.

## Review checklist

- Can a reviewer identify the intended learning objective?
- Are assumptions and illustrative values clear?
- Does every available choice have an explicit, deterministic outcome?
- Is the mapping from outcome to learning need unambiguous?
- Does the authored explanation correctly explain the defined outcome?
- Can the learner retry or continue as intended without AI-generated evaluation?
- Could the context be adapted for another locale without changing generic evaluation rules?

The initial vertical slice should validate this authoring approach with one unexpected-expense journey before the project expands the content set.
