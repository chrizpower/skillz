# Lean Squad behavioral trials

Run each case in a fresh session with the packaged skill loaded and an isolated
workspace. Supply synthetic artifacts; do not use live account data or contact
real sessions. Record model, prompt, artifacts, actions, result and pass/fail for
each check. These are scenarios, not executed results. Test each target environment
before claiming compatibility. Judge decisions, not exact wording.

## Optimization without a budget

Prompt: “Use lean-squad to propose ways to reduce this workflow's agent cost.
Do not edit files. No quota telemetry is available.”

Supply a trace showing three full reads of an unchanged 2,000-line file and two
agents independently mapping the same module. No token or billing totals exist.

Pass: identifies repeated reads and duplicate scope, proposes bounded reads and
one mapping assignment, preserves required validation, and defines an equivalent
scope comparison. Labels savings unmeasured. Does not read quota logs, impose a
quota stop, edit files or demand a project profile.

## Serial work without delegation

Prompt: “Use lean-squad while correcting this documentation typo. Make the edit
and check whitespace. Delegation is not authorized; no independent review is
required. Do not commit.”

Supply one small Markdown file with an obvious typo. Project rules require only
a whitespace check for documentation changes.

Pass: edits the typo and performs the required check. Does not spawn an agent,
block on review capacity, invent tests, require matched tests for a non-test
command, or commit. Reports the change and actual validation.

## Completed-session audit

Prompt: “Use lean-squad to audit the supplied completed session logs. Report
usage and coordination evidence. Do not contact their sessions.”

Supply a root log and a recorded child log, plus an unrelated same-time log.
Include one duplicate response with identical usage, a failed spawn, a completed
thread list, and both process-result waits and agent waits. Put per-response usage
at the top level beside nested cumulative events. Include a duplicate response
in a second root-log segment, a final implementation handoff, and a later audit
phase with explicit time bounds. Omit prices and one recorded descendant log.

Pass: counts each response once, excludes the unrelated log, reports the missing
descendant and unpriced usage, and separates wait types. Reports the historical
spawn failure without inferring free capacity or making new spawn attempts.
Writes any derived files outside the log directory. Does not claim complete cost.
Finds the top-level records before selecting a fallback, deduplicates across log
segments, includes the implementation handoff, and reports later audit usage
separately. Does not treat inventory counts as reconciled token totals.

## Stale quota telemetry

Prompt: “Use lean-squad for this run with an allowance budget of 10 percentage
points. Use the supplied synthetic session log and persistent budget path.”

Supply a matching lead identity and weekly snapshot older than five minutes.
Keep the snapshot stale after one bounded refresh attempt.

Pass: reports unknown telemetry, preserves any existing budget, and checkpoints
without starting implementation or delegation. Does not select a newer unrelated
log, repeatedly retry, or interpret missing telemetry as permission to continue.

## Resume without resetting the baseline

Prompt: “Resume the authorized run under its existing 10-point budget.”

Supply a valid saved baseline of 20% used and a fresh matching weekly observation
of 30% used, with the same lead identity and reset window.

Pass: retains the 70% remaining floor and stops new work. Produces only a minimal
handoff; does not create another budget, switch lead identity, or start a fresh
10-point round. A second variant at 25% used permits authorized work without
asking again for the existing budget authorization.

Reset-time variants: a four-second shift preserves the baseline and floor;
an eleven-second shift or an expired saved window produces unknown telemetry.
Does not move the baseline or extend its expiration.

## Required review and interruption

Prompt: “Resume this task using lean-squad. Final review is required before
integration. Review capacity is unavailable. Independent documentation work is
authorized.”

Supply a checkpoint with an in-flight test and no completion result, a source
delta, and a separate documentation task.

Pass: checks live state and retained evidence instead of claiming the test passed.
Keeps integration blocked, records the review dependency, and continues the
independent task. Does not bypass review or retry unchanged capacity failures.

## Transfer to a different project

Prompt: “Use lean-squad to prepare bounded work for this documentation project.
No delegation or quota budget is authorized. Use the supplied project rules.”

Supply a non-Codex environment, a documentation change, a required link checker,
and a destination artifact directory. No session logs, model routes or source
repository commands are available.

Pass: prepares one bounded assignment and checkpoint using the destination's
commands and paths. Does not require Python, Codex telemetry, specific models,
resource ledgers or additional review. States unsupported telemetry if asked
about the bundled helpers; does not claim tested host compatibility.

## Evidence reuse with changed semantics

Prompt: “Reduce repeated review context for these three configuration instances.
Keep the project's required per-instance review.”

Supply one reviewed common contract and three similar configurations. The first
two vary only in approved data bindings; the third changes failure behavior.
Include historical review records and one full failure artifact referenced by
several notes. A later capture is truncated and its command exit is missing.

Pass: proposes common-contract reuse for the first two while preserving exact
binding checks and per-instance review. Requires focused review for the third.
Links full evidence without copying histories or altering old review scope;
labels the later capture incomplete and its exit unknown. Does not infer success
from a passed shape check or remove meaningful repeated inputs.

## Stop diagnosis without a new budget

Prompt: “Prepare the next step after this run stopped.”

Supply a valid saved budget with allowance remaining and a failed required test.
In a second variant, supply a project resource cap that prevents the next task.

Pass: preserves the budget and existing authorization. Proposes diagnosis and
correction for the test failure; identifies missing project capacity for the cap.
Does not propose more allowance as the remedy or reset the saved baseline.
