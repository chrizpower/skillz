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

## Interview before delivery

For creation or broad revision, interview by default. Plans supply facts, not
answers to unresolved choices. Before drafting, ask the highest-impact open
question whose prerequisites are known and wait for the user's answer. Sending
a question is not receiving an answer; do not deliver while it is pending.
Skip the interview only for an explicit draft-only request or when context
settles all consequential choices; explain the latter. Focused reviews and
specific authorized revisions need only questions that affect their result.

Reuse known answers and priorities. Ask one question at a time unless requested
otherwise. Track coverage of purpose, correctness, ownership, dependencies,
performance, operations, and evolution; distinguish settled, deferred, blocked,
and irrelevant areas with reasons. Avoid a fixed questionnaire.

Use concrete boundary use cases. Explore external details only when they affect
requirements or trade-offs; explain the connection.

Support recommendations with evidence, reason, and main cost. Allow alternatives
and unknown answers; defaults and silence are not decisions. Record unknowns,
their consequences, and resolution paths.

After each answer, state what changed, reassess coverage and scenario gaps, and
ask the next answerable question that could materially change the rules. Continue
independent questions when a choice is blocked or deferred; do not repeat deferred
questions or require exhaustive implementation detail. Finish when none remain
or the user stops. Summarize coverage and residual risks; deliver a conditional
draft if consequential choices remain unresolved.

## Establish domain language

Read the existing glossary and apply the [glossary template's](references/glossary-template.md)
DDD and maintenance guidance during the interview. For document creation, create
or maintain `GLOSSARY.md` beside `GRAVITY.md`; preserve existing entries and add
settled terms. For revisions, update affected entries only. Retain standalone
guidance and explicit gaps, even if no terms are settled; completeness is not a
delivery condition. Include the architecture template's domain language rule
and relative glossary link in `GRAVITY.md`.

## Check the rules

Scale these selected practices to the decision; they are not full framework
compliance. A focused review needs only affected rules and scenarios.

- **QAW:** Check dominant drivers with scenarios; one can cover several. Ask about priorities only when they affect the outcome. For scenarios that decide trade-offs, state source, trigger, component, conditions, response, and success measure. Preserve workload and numerical limits; mark unknown targets.
- **TOGAF:** State each principle's rule, rationale, permitted or rejected choices, and practical costs or restrictions. Compare disputed principles with a plausible alternative.
- **ATAM:** Apply rules to priority scenarios. Identify sensitive decisions or assumptions, quality interactions, risks, and missing design detail. Scenario reasoning does not prove implementation behavior.

Consult [foundations](references/foundations.md) when sources or method details
are needed.

## Deliver and maintain

For documents, read and adapt the [template](references/architecture-principles-and-constraints-template.md).
Retain standalone use, maintenance, and QAW/TOGAF/ATAM instructions for later
editors without the skill. Omit other unused sections and generic goals; combine
fields where useful. Rules must stand alone and leave compliant implementation
choices open. Verify referenced tools and commands. State where and when rules
that conflict with current behavior apply.

For creation, write `GRAVITY.md` or use the existing equivalent.
For revision, update within the requested scope. Reviews do not authorize edits.
Respect chat-only requests; clarify an unclear destination or update scope early.
After writing, if the project has an `AGENTS.md` file, add or update a relative
Markdown link to the document and instruct agents to read it for architecture
decisions and follow accepted rules within scope. Preserve unrelated instructions
and avoid duplicate links. Do not create `AGENTS.md` if it is absent.
Summarize key rules and unknowns and link the document.

Agent-derived rules are proposed and do not govern work until accepted. Follow
accepted rules within scope. For conflicts, use any already-authorized specific
revision or exception; otherwise propose a compliant path or request the needed
decision. Continue unaffected work. Principle exceptions do not waive constraints
or invariants. Preserve rule IDs and source authority; record reasons for changes
and retirements. Never weaken rules merely to justify existing code.
