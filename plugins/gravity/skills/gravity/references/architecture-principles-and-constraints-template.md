# Architectural Constraints and Principles: <system or component>

Scope: <boundary and governed decisions>
Status: <draft, accepted with source, or mixed with entry-level status>
Parent guidance: <link, if applicable>

## Intent

<Properties to preserve and non-goals.>

## Use

For each change, identify applicable rule IDs, scope, and status. Explain how
the approach follows them. Claim compliance only with evidence; report gaps.
Proposed rules require acceptance. Resolve conflicts and exceptions below
before affected work proceeds.

## Rules

### P1 — <rule name>

- **Type and status:** <principle, constraint, or invariant; scope or status differences>
- **Rule:** <permitted or rejected choices; required condition for an invariant>
- **Reason and cost:** <driver, stakeholder, source, and trade-off; alternative if disputed>
- **Apply:** <when relevant and required actions or decision steps>
- **Check:** <method, evidence, and relevant scenarios; distinguish existing enforcement, proposed checks, and gaps>
- **Revisit when:** <changed evidence or conditions>

<Repeat as needed. Preserve existing IDs; use P, C, or I for new rules. Mark assumptions and confirmation gaps. List shared drivers separately only to avoid repetition.>

## Scenario checks

<Driver coverage and user priorities. For priority scenarios: source, trigger, component, conditions, response, success measure. Record resulting choices, costs, sensitive decisions, quality interactions, risks, and missing evidence. Do not present reasoning as implementation test results.>

## Open questions

<Unknown, affected rule, consequence, and resolution path. Mark conditional guidance.>

## Changes and exceptions

This document evolves when requirements, constraints, or evidence change. A task
request does not by itself authorize changing its governing rules.

- **Apply:** Follow accepted rules within scope. If a task conflicts with them, report the conflict and propose a compliant alternative or request a specific exception. Continue unaffected work. Exceptions to principles do not waive constraints or invariants.
- **Revise:** Identify the changed force or evidence, affected rule IDs, consequences, and authority for the change. Keep accepted rules in effect until an authorized revision or exception is established. Changes to wording, scope, status, or checks must not silently weaken a rule.
- **Extend:** Reuse an existing rule when it covers the concern. Otherwise add a stable ID using the rule format above. Cite its source; mark agent-derived additions as proposed until accepted. Avoid task-specific implementation detail.
- **Record:** Preserve rule IDs. Record the reason, authority, and scope of revisions or exceptions. Give temporary exceptions an expiry or review condition. Mark replaced rules as superseded rather than silently deleting them.

For additions and revisions, use ASD-STE100 Simplified Technical English, adapted
to software terminology without losing precision. Preserve these selected
practices: **QAW**—cover changed drivers with prioritized scenarios that state
source, trigger, component, conditions, response, and success measure;
**TOGAF**—state each principle's rationale and practical implications;
**ATAM**—check affected rules against scenarios and record sensitive decisions,
quality trade-offs, and risks. Reuse existing evidence and record gaps. These are
selected practices, not full framework compliance.

<Record changes here. Retain the Use and maintenance guidance in the output;
omit other unused sections and template instructions.>
