# Architectural Constraints and Principles: <system or component>

Scope: <boundary and governed decisions>
Status: <draft, accepted with source, or mixed with entry-level status>
Parent guidance: <link, if applicable>

## Intent

<Properties to preserve and non-goals.>

## Use

Apply accepted rules within their scope. Proposed rules do not govern work
until accepted. Cite relevant rule IDs when explaining a design choice or
conflict. Distinguish planned checks from completed verification.

## Rules

### P1 — <rule name>

- **Type and status:** <principle, constraint, or invariant; proposed or accepted with source; scope if narrower than the document>
- **Rule:** <permitted or rejected choices; required condition for an invariant>
- **Reason and cost:** <driver, stakeholder, source, and trade-off; alternative if disputed>
- **Apply:** <when relevant and required actions or decision steps>
- **Check:** <method, evidence, and relevant scenarios; distinguish existing enforcement, proposed checks, and gaps>
- **Revisit when:** <relevant changed evidence or conditions; preserve temporary status and known review conditions>

<Repeat as needed; combine fields where useful. Preserve existing IDs; use P, C, or I for new rules. Mark assumptions and confirmation gaps. List shared drivers separately only to avoid repetition.>

## Scenario checks

<Use scenarios to check dominant drivers and record known priorities. For scenarios that decide trade-offs: source, trigger, component, conditions, response, success measure. Record relevant choices, sensitive decisions, quality interactions, risks, and missing evidence. Separate targets, estimates, and measured results. Scenario reasoning is not implementation test evidence.>

## Open questions

<Unknown, affected rule, consequence, and resolution path. Mark conditional guidance.>

## Changes and exceptions

Accepted rules remain in effect until an authorized revision or exception.
When a task conflicts with them, identify the conflict and any specific change
already authorized by the user. Otherwise propose a compliant path or request
the needed decision. Continue unaffected work. An exception to a principle does
not waive a constraint or invariant.

For revisions, record the affected IDs, reason, scope, and authority. Preserve
IDs and mark replaced rules as superseded. Do not weaken rules merely to fit
existing code. Reuse rules where possible; mark agent-derived additions as
proposed until accepted. Preserve temporary choices and known review conditions.

Check changed rules against relevant scenarios. State their rationale and
practical implications, including costs, quality trade-offs, and evidence gaps.
Use ASD-STE100 Simplified Technical English adapted to software terminology;
preserve technical precision.

<Record changes here. Retain the Use and Changes and exceptions guidance in a
standalone document. Omit other unused sections and all template instructions.>
