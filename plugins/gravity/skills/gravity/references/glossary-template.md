# Glossary: <project or system>

Scope: <domain and known bounded contexts; mark uncertain boundaries>

## Use and maintain

Use this ubiquitous language consistently in discussion, documentation, code,
and tests. Domain experts and developers define it together. A bounded context
gives a model and its terms consistent meanings. Preserve different meanings
across contexts; determine boundaries from domain meaning, not code or deployment
structure.

During each task that uses domain concepts:

- Read relevant entries; use accepted terms and avoid listed alternatives within
  context. Preserve external interface names; explain mappings when needed.
- For new, ambiguous, changed, or obsolete meanings, ask the user to define,
  adjust, or delete the entry. Propose wording and a concrete consequence. Use a
  structured question tool if available; otherwise ask separately.
- Reuse answers and authorization. Wait for required answers before dependent
  work; silence is not acceptance. Continue independent work; record deferrals
  and consequences without asking again.
- Check meanings and relationships against normal and boundary scenarios.
  Surface disagreements with code; current usage does not decide meaning.
  Identify missing domain expertise.
- Check affected terms and references when changing or deleting entries. Record
  authorized changes, reasons, and remaining naming differences. Keep unconfirmed
  definitions proposed. If edits are outside scope,
  propose changes instead. Do not rename unrelated code or change public
  interfaces without authorization.

Include behavior, lifecycle, examples, or domain relationships only to distinguish
meanings; omit implementation plans and generic technical terms. No task must
complete the glossary. Other DDD patterns are optional unless the design needs them.

## Language

**<Term>**: <Short definition.>

<Add notes or sections only to clarify meanings. Mark unconfirmed entries proposed;
accepted entries need no status or source unless disputed. Omit empty sections
and routine change logs.>

<Retain Use and maintain for editors without Gravity. Preserve existing content
and explicit gaps. Remove template instructions.>
