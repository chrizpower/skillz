---
name: gravity
description: Define or challenge software architecture principles and constraints. Use to resolve design priorities or revise rules when conditions change.
---

# Gravity

Turn architectural forces into usable rules:

- **Force:** a pressure or competing interest that influences design.
- **Driver:** a force with a major architectural effect.
- **Constraint:** a mandatory restriction with a source.
- **Invariant:** a condition that must hold within a stated scope.
- **Principle:** a chosen rule for design trade-offs.

Do not turn preferences, assumptions, or observed patterns into obligations.
Use ASD-STE100 Simplified Technical English, adapted to software terminology;
preserve technical precision.

## Establish context

Identify the task (creation, review, or revision), system boundary, outcome,
and decisions the user controls. Read relevant requirements and rules, including
inherited constraints and local freedom. Inspect code for facts; ask about intent.
Keep example applications outside scope unless the user includes them.

Record drivers, affected stakeholders, sources, decisions, and unknowns.
Preserve temporary choices and their scope without inventing an expiry.
Separate required targets, estimates, and measured results.

## Interview as needed

Reuse known answers and priorities. Ask only questions that could change the
result, starting with the highest-impact question whose prerequisites are known.
Ask one at a time unless the user requests another format. Avoid a fixed
questionnaire; check gaps in purpose, correctness, ownership, dependencies,
performance, operations, and evolution.

Use concrete boundary use cases. Explore external details only when they affect
requirements or trade-offs; explain the connection. Stop refining when further
detail would not change the rules.

Support recommendations with evidence, reason, and main cost. Allow alternatives
and unknown answers; defaults and silence are not decisions. After each answer,
state only what changed. Record unknowns, their consequences, and resolution
paths; continue with independent questions where useful.

## Check the rules

Scale these selected practices to the decision; they are not full framework
compliance. A focused review needs only affected rules and scenarios.

- **QAW:** Check dominant drivers with scenarios; one can cover several. Ask about priorities only when they affect the outcome. For scenarios that decide trade-offs, state source, trigger, component, conditions, response, and success measure. Preserve workload and numerical limits; mark unknown targets.
- **TOGAF:** State each principle's rule, rationale, permitted or rejected choices, and practical costs or restrictions. Compare disputed principles with a plausible alternative.
- **ATAM:** Apply rules to priority scenarios. Identify sensitive decisions or assumptions, quality interactions, risks, and missing design detail. Scenario reasoning does not prove implementation behavior.

Consult [foundations](references/foundations.md) when sources or method details
are needed.

## Deliver and maintain

For documents, adapt the [template](references/architecture-principles-and-constraints-template.md).
Omit unused sections and generic goals; combine fields where useful. Rules must
stand alone and leave compliant implementation choices open. Verify referenced
tools and commands. State where and when rules that conflict with current
behavior apply.

Finish with actionable rules or review findings. If blocked by unknowns or the
user stops, deliver the supported conditional draft and unresolved issues.

For creation, write `CONSTRAINTS_AND_PRINCIPLES.md` or use the existing equivalent.
For revision, update within the requested scope. Reviews do not authorize edits.
Respect chat-only requests; clarify an unclear destination or update scope early.
After writing, summarize key rules and unknowns and link the document. Add project
instruction links only when integration is requested.

Agent-derived rules are proposed and do not govern work until accepted. Follow
accepted rules within scope. For conflicts, use any already-authorized specific
revision or exception; otherwise propose a compliant path or request the needed
decision. Continue unaffected work. Principle exceptions do not waive constraints
or invariants. Preserve rule IDs and source authority; record reasons for changes
and retirements. Never weaken rules merely to justify existing code.
