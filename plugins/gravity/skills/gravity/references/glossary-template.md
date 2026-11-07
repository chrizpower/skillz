# Glossary: <project or system>

Scope: <domain and known bounded contexts; mark uncertain boundaries>

## Use and maintain

This document records the project's ubiquitous language: domain terms shared by
domain experts and developers and used consistently in discussion, documentation,
code, and tests. A bounded context is the boundary within which a domain model
and its terms have consistent meanings. Different contexts can use the same word
with different meanings; state the context rather than forcing one definition.
Determine boundaries from domain meaning, not repository or deployment structure.

During each task that uses domain concepts:

- Read relevant entries and use accepted terms. Avoid listed alternatives within
  that context; preserve external interface names and explain mappings when needed.
- When a new concept, ambiguous use, changed meaning, or obsolete term appears,
  ask the user to define, adjust, or delete the affected entry. Propose precise
  wording and explain the consequence with a concrete example. Use a structured
  question tool when available; otherwise ask a separate question.
- Reuse known answers and existing authorization. Wait for required answers before
  dependent work; silence is not acceptance. Continue independent work and record
  deferred meanings and their consequences without repeatedly asking.
- Check definitions and relationships against normal and boundary scenarios.
  Compare stated meaning with code and surface disagreements. Code shows current
  usage; it does not decide domain meaning. Identify missing domain expertise.
- Record resolved changes during the task. Keep unconfirmed definitions proposed.
  For changes or deletions, check affected terms and references, record the reason,
  and identify remaining naming differences. Do not rename unrelated code or change
  public interfaces without task authorization. If file edits are outside scope,
  present the proposed glossary change instead.

Keep definitions concise but include behavior, lifecycle, or examples when needed
to distinguish concepts. Record domain relationships, not implementation plans.
Include technical terms only when they have a domain-specific meaning. Extend the
glossary as understanding develops; no task must complete the whole glossary.
These practices do not require aggregates, repositories, events, or other DDD
patterns unless the design needs them.

## Terms

### <Context>: <preferred term>

- **Definition:** <meaning and relevant boundary or example>
- **Status and source:** <accepted with source, or proposed with confirmation gap>
- **Avoid:** <confusing alternatives within this context; omit if unnecessary>
- **Relationships:** <related concepts and distinctions; omit if unnecessary>

## Open meanings

<Unresolved term or context, question, consequence, and resolution path.>

## Changes

<Changed or deleted term, context, reason, and authority; note affected references
or remaining naming differences.>

## DDD sources

- [Eric Evans, Domain-Driven Design Reference](https://www.domainlanguage.com/ddd/): core definitions and patterns.
- [Martin Fowler, Ubiquitous Language](https://martinfowler.com/bliki/UbiquitousLanguage.html): shared language tested in conversation and refined with understanding.
- [Vaughn Vernon, Domain-Driven Design Distilled](https://www.informit.com/store/domain-driven-design-distilled-9780134434421): developing language within bounded contexts and checking scenarios.

<Retain Use and maintain and DDD sources so later agents can apply this guidance
without Gravity. Preserve existing content. Omit unused optional fields and these
template instructions; keep unresolved meanings explicit.>
