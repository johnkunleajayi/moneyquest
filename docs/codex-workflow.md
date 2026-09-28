# Codex development workflow

Codex should be visible in project work across planning, building, reviewing, and documenting. Use it to make work clearer and more reusable, not as decoration.

## Working sequence

1. **Plan:** Use Plan Mode for cross-cutting work such as selecting the vertical slice or changing engine boundaries. Keep accepted plans and material trade-offs reviewable in the decision log.
2. **Build:** Ask Codex to make bounded changes against the requirements and architecture. Review the resulting diff.
3. **Test:** Add and run focused tests for deterministic business rules: scenario evaluation, mistake mapping, progression, and rewards as implemented. Check that AI responses cannot change those results.
4. **Review:** Ask Codex to review the diff against requirements, architecture, and deterministic boundaries. Verify findings and record their resolution; a review suggestion alone is not evidence of a fix.
5. **Document:** Update setup, architecture, scenario authoring, and demo documentation when implementation changes make it relevant.

## Repository guidance

Read root `AGENTS.md` for the concise contributor rules. Before changing product behaviour or architecture, consult `docs/product-requirements.md` and `docs/architecture.md`. Requirements and decisions remain reviewable repository documents.

## Plan Mode

Use Plan Mode where work crosses components, changes architecture, or has meaningful alternatives. For small isolated work, a short task scope and reviewable diff may be sufficient. Record significant accepted trade-offs in `docs/decisions/`.

## Reusable skills

A project-specific scenario-authoring skill may be useful after the content format and review checklist stabilize. It should help contributors create scenarios consistent with the learning objective, explicit choices, deterministic rules, explanation, and validation approach. Do not create it before there is a stable repeatable process or solely to claim Codex usage.

## MCPs

Use an MCP only if it connects Codex to a genuine project source of truth or collaboration workflow. No external MCP integration is currently required by the approved brief. Keep the repository documentation authoritative unless a concrete team need justifies another source.

## Evidence for the hackathon pitch

Show a compact, truthful trail: an accepted plan, a meaningful implementation diff, focused deterministic test evidence, the Codex review and verified resolution, and updated project documentation. The demo should make clear which work Codex assisted with and which behavior is enforced by application rules.
