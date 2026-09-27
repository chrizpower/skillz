---
name: gravity
description: Ground software architecture in the forces that shape it, as gravity shapes structural engineering. Use a focused interview to define or challenge architecture principles and constraints, resolve design priorities, or revise rules when conditions change.
---

# Gravity

Produce rules that guide design and review:

- **Force:** a pressure, constraint, or competing interest that influences design.
- **Driver:** a force with a major effect on architecture.
- **Constraint:** a mandatory restriction with a source.
- **Invariant:** a condition that must hold within a stated scope.
- **Principle:** a chosen rule for design trade-offs.

A force describes pressure; it does not by itself impose an obligation. Do not turn preferences or assumptions into obligations.

Use ASD-STE100 Simplified Technical English for all user-facing output, including documents. Adapt it to software engineering terms. Preserve technical precision over strict compliance.

## Establish context

State the system or component in scope, intended outcome, and decisions the user controls. Treat example applications as context unless the user expands scope. Read relevant requirements and existing rules. For components, identify inherited rules and local freedom. Inspect code for facts; ask about intent. Current behavior does not establish desired architecture.

Keep a short record of drivers, sources, decisions, and unknowns. For each dominant driver, identify the affected stakeholder and who can confirm the requirement. Reuse known answers; flag missing input.

## Interview

Ask the unresolved question most likely to change architecture within scope, with prerequisites known. Ask one question, then wait, unless the user requests another format.

Use concrete use cases to expose requirements at the system boundary. Explore external details only when they could change those requirements or a design trade-off; state the connection. Stop refining a use case when further detail would not change the architectural rules.

When evidence supports a design recommendation, state its reason and main cost. Allow alternatives. Do not suggest guessed answers to factual or preference questions.

After each answer, state only what changed and select the next question. For unknowns, record the consequence and how to resolve them; continue with independent questions.

Check gaps in purpose, correctness, ownership, dependencies, performance, operations, and evolution. Keep temporary limits distinct from enduring rules. Avoid a fixed questionnaire.

## Apply engineering practices

- **QAW:** Cover each dominant driver with a scenario; scenarios can cover several drivers. Establish priorities with the user; reuse known priorities. Refine priority scenarios with source, trigger, affected component, conditions, response, and success measure. Preserve relevant workload and numerical limits; mark unknown targets.
- **TOGAF:** Each principle needs a clear rule, rationale, and practical implications. State which choices it permits or rejects and what work or restriction it introduces. Compare disputed principles with a plausible alternative.
- **ATAM:** Apply draft rules to priority scenarios. Identify decisions or assumptions that control results, interactions between qualities, and unresolved risks. Record missing design detail instead of inventing it. Scenario reasoning does not prove implementation behavior.

These are selected practices, not full framework compliance. Consult [foundations](references/foundations.md) for sources or method details.

## Deliver and maintain

Use the [template](references/architecture-principles-and-constraints-template.md). Mark agent-derived rules as proposed until accepted. Preserve source authority; do not reconfirm settled decisions. Omit generic goals that cannot guide a concrete choice.

Finish when the rules guide decisions and no known unresolved issue would materially change them. If an issue cannot be resolved now, give a conditional draft. If the user stops, deliver the supported draft and unknowns.

Write the outcome to `ARCHITECTURE.md` or update the existing equivalent by default. Respect explicit chat-only requests. Ask early if the destination or scope of an update is unclear. After writing, give a short summary of the rules and key unknowns, with a link to the document. Add a project instruction link only when integration is requested.

Follow accepted principles within scope. Before departing, record an authorized exception or revision and its reason. This does not waive constraints or invariants. Preserve established rules and IDs; explain changes and retirements. Never weaken a rule merely to justify existing code.
