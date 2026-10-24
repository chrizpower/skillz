---
name: lean-squad
description: Reduce agent context and coordination costs, prepare bounded autonomous work, or audit Codex session token usage. Use for agent cost optimization or an explicitly quota-limited run; not ordinary code-performance optimization.
---

# Lean Squad

Reduce context and coordination cost while preserving accepted scope, required
validation and existing authorization. This skill grants no additional authority.
Use destination rules for models, commands, storage and review. The bundled
measurement helpers support Codex logs; optimization and preparation do not require them.

## Select the task and result

- **Optimize:** identify cost drivers from relevant evidence. Report recommended
  changes, required checks to preserve, and how to measure the result. Implement
  changes only within the authorized scope; label unmeasured savings as hypotheses.
- **Prepare work:** define bounded assignments and a resumable checkpoint. Use
  [the project profile](assets/project-profile.example.md) only when a reusable
  handoff is needed; fill applicable fields from destination rules.
- **Explicit allowance budget:** also follow
  [allowance control](references/measurement.md#allowance-budget). Without a budget
  request, do not introduce quota stops or require quota telemetry.
- **Completed-session audit:** follow
  [session audit](references/measurement.md#session-audit). Report usage, evidence
  coverage and cost drivers. Read recorded events only; never resume, contact or
  spawn agents to reconstruct an audited run.

## Bound context and coordination

Start with the current checkpoint, contract and relevant source spans. Prefer
final closeout evidence over interim records; load history only when it can
change a decision. Select relevant results and failure diagnostics; keep full
outputs in linked artifacts. Use concise updates without losing precision.
For repeated evidence or equivalent task instances, read
[evidence and review reuse](references/review-reuse.md).

Use one implementer for serial work. Delegate only when authorized and an
independent bounded task justifies coordination cost. Assign objective, base,
owned paths, invariants, checks, exclusions and expected result. Name who needs
that result and when; preserve other writers' edits.

Reuse agents within settled scopes. Use fresh review context when the review
scope or governing requirements change enough to invalidate prior assumptions.
Confirm actual model routing; do not infer it from role names. Avoid duplicate
leads, routine polling and unchanged retries after capacity or missing-input
failures. Check available capacity before delegation. If required review cannot
start, checkpoint before work that depends on it; do not silently substitute models.

## Preserve acceptance and continuity

Keep the project's required checks and reviews. Run focused checks first; confirm
that test filters matched tests. Save results, exit codes and failures. Repeat
checks for changed inputs, failures or unresolved concerns. Reuse evidence only
for unchanged inputs and the scope it covers. Additional independent review
should depend on risk and available authority, not this skill alone.

Continue ready authorized work within scope and stopping conditions. Record
base, pending paths/hashes, validation, review status, blockers and next action
in a checkpoint. After interruption, inspect live changes and retained outputs;
do not assume in-flight commands completed. Preserve findings and do not accept
behavior with unresolved required checks. Follow the project's defect procedure.

## Measure the result

Compare equivalent accepted scope, elapsed time, corrections and validation
outcomes. Keep tokens, dated cost estimates and allowance separate. Commit counts
are weak work proxies. Measure context and routing changes before claiming savings;
shorter replies alone do not establish lower context cost.
