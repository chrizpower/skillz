# Architectural Constraints and Principles: <system or component>

Scope: <boundary and governed decisions>
Status: <draft, accepted with source, or mixed with entry-level status>
Parent guidance: <link, if applicable>

## Intent

<Properties to preserve and non-goals.>

## Use

Follow accepted rules within scope; proposals do not govern work. Cite relevant rule IDs when explaining a design choice or
conflict. Distinguish planned checks from completed verification.

## Rules

### P1 — <rule name>

- **Type and status:** <principle, constraint, or invariant; proposed or accepted with source; narrower scope if applicable>
- **Rule:** <permitted or rejected choices; required condition for an invariant>
- **Reason and cost:** <driver, stakeholder, source, and trade-off; alternative if disputed>
- **Apply:** <when applicable and required actions>
- **Check:** <method, evidence, and relevant scenarios; distinguish existing enforcement, proposed checks, and gaps>
- **Revisit when:** <changed evidence or conditions; temporary status and known review conditions>

<Repeat or combine fields as needed. Preserve IDs; use P, C, or I for new rules. Mark assumptions and confirmation gaps. List shared drivers separately to avoid repetition.>

## Scenario checks

<Use scenarios to check dominant drivers and record known priorities. For scenarios that decide trade-offs: source, trigger, component, conditions, response, success measure. Record relevant choices, sensitive decisions, quality interactions, risks, and missing evidence. Separate targets, estimates, and measured results. Scenario reasoning is not implementation test evidence.>

## Open questions

<Unknown, affected rule, consequence, and resolution path. Mark conditional guidance.>

<Summarize interview coverage: purpose, correctness, ownership, dependencies,
performance, operations, and evolution. Identify settled, deferred, blocked, or
irrelevant areas with reasons. State whether the interview is complete or stopped
with a conditional draft.>

## Changes and exceptions

For conflicts, use any specific revision or exception already authorized by
the user. Otherwise propose a compliant path or request the needed decision;
accepted rules remain in effect. Continue unaffected work. An exception to a principle does
not waive a constraint or invariant.

For revisions, record the affected IDs, reason, scope, and authority. Preserve
IDs and mark replaced rules as superseded. Do not weaken rules merely to fit
existing code. Reuse rules where possible; mark agent-derived additions as
proposed until accepted. Preserve temporary choices and known review conditions.

For additions and revisions, follow these selected practices, scaled to affected
rules. This is not a claim of full framework compliance; these instructions apply
even when the editor does not have Gravity:

- **QAW (Quality Attribute Workshop):** Check dominant drivers and stakeholder priorities with scenarios. For scenarios that decide trade-offs, record source, trigger, component, conditions, response, and success measure. Preserve known targets; mark unknowns.
- **TOGAF architecture principles:** State the rule, rationale, practical implications, and costs. For disputed principles, compare a plausible alternative.
- **ATAM (Architecture Tradeoff Analysis Method):** Check rules against priority scenarios; record sensitive decisions, quality interactions, risks, and missing design detail. Distinguish scenario reasoning from implementation evidence and required targets from measured results.

Ask about unresolved choices that could change affected rules before completing
an extension; reuse known answers and respect explicit deferrals. Record remaining
unknowns and their consequences. These checks do not grant authority to accept rules.
Use ASD-STE100 Simplified Technical English adapted to software terminology;
preserve technical precision.

<Record changes here. Retain the Use and Changes and exceptions guidance in a
standalone document, including the named method instructions. Omit other unused
sections and all template instructions.>
