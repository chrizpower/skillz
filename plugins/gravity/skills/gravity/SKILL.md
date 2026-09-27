---
name: gravity
description: Define or challenge software architecture principles and constraints from the forces that shape a system. Use to resolve design priorities or revise rules when conditions change.
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

Identify whether the user wants new rules, a review, or a revision. Establish the system or component in scope, intended outcome, and decisions the user controls. Treat example applications as context unless the user expands scope. Read relevant requirements and existing rules. For components, identify inherited rules and local freedom. Inspect code for facts; ask about intent.

For existing systems, distinguish observed patterns from accepted rules. If a proposed rule conflicts with current behavior, state where and when it applies.

Keep a short record of drivers, sources, decisions, and unknowns. For each dominant driver, identify the affected stakeholder and requirement source, or record the gap. Reuse known answers.

## Interview

Ask only when missing information could change the result. Choose the highest-impact question whose prerequisites are known. In an interview, ask one question at a time unless the user requests another format. If the supplied context is sufficient, proceed to the result.

Use concrete use cases to expose requirements at the system boundary. Explore external details only when they could change those requirements or a design trade-off; state the connection. Stop refining a use case when further detail would not change the architectural rules.

When evidence supports a design recommendation, state its reason and main cost. Allow alternatives. Label recommendations as proposals. Suggested options must allow a different answer or an unknown; do not treat a default or silence as a decision.

After each answer, state only what changed. Continue only if another question could change the result. For unknowns, record the consequence and how to resolve them; continue with independent questions.

Check gaps in purpose, correctness, ownership, dependencies, performance, operations, and evolution. Preserve temporary choices and their scope; do not invent an expiry. Separate required targets, estimates, and measured results. Avoid a fixed questionnaire.

## Apply engineering practices

- **QAW:** Use concrete scenarios to check dominant drivers; reuse scenarios that cover several. Reuse known priorities, or ask when priority changes the outcome. For scenarios that decide a trade-off, state source, trigger, affected component, conditions, response, and success measure. Preserve relevant workload and numerical limits; mark unknown targets.
- **TOGAF:** Each principle needs a clear rule, rationale, and practical implications. State which choices it permits or rejects and what work or restriction it introduces. Compare disputed principles with a plausible alternative.
- **ATAM:** Apply draft rules to priority scenarios. Identify decisions or assumptions that control results, interactions between qualities, and unresolved risks. Record missing design detail instead of inventing it. Scenario reasoning does not prove implementation behavior.

Scale the detail to the decision. A focused review needs only the affected rules and scenarios. These are selected practices, not full framework compliance. Consult [foundations](references/foundations.md) for sources or method details.

## Deliver and maintain

For a new or revised document, adapt the [template](references/architecture-principles-and-constraints-template.md) so rules are usable without the interview. Omit unused sections and combine fields when this improves clarity. Mark agent-derived rules as proposed until accepted. Preserve source authority; do not reconfirm settled decisions. Omit generic goals that cannot guide a concrete choice. Reference only verified tools and commands; leave implementation choices open within the rules.

Finish a review when the relevant findings and proposed corrections are clear. Finish rule creation or revision when the rules guide decisions and no known unresolved issue would materially change them. If an issue cannot be resolved now, give a conditional draft. If the user stops, deliver the supported draft and unknowns.

For rule creation, write `CONSTRAINTS_AND_PRINCIPLES.md` or use the existing equivalent by default. For a review, report findings without editing unless revision is requested. For a revision, update the existing document within the requested scope. Respect explicit chat-only requests. Ask early if the destination or scope of an update is unclear. After writing, give a short summary of the rules and key unknowns, with a link to the document. Add a project instruction link only when integration is requested.

Proposed rules do not govern work until accepted. Follow accepted rules within scope. When a task conflicts with them, identify the conflict and check whether the user has already authorized the specific revision or exception. Otherwise propose a compliant path or ask for the needed decision; continue unaffected work. An exception to a principle does not waive a constraint or invariant. Preserve established rules and IDs; explain changes and retirements. Never weaken a rule merely to justify existing code.
