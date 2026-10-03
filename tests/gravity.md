# Gravity interview trials

Run each case in a fresh session with the skill loaded. Use both Claude Code
and Codex before claiming cross-agent behavior. Keep these trials outside the
skill's runtime references. Judge decisions and questions, not exact wording.

Record the agent and model, questions asked, final Architectural Constraints and
Principles document, and pass or failure against the checks below. These are
test cases, not recorded test results.

For completed interviews, also check that dominant forces identify affected
stakeholders and confirmation sources or gaps. Use scenarios to check dominant
drivers; one scenario can cover several. Scenarios that decide trade-offs must
specify source, trigger, affected system or component, conditions, response,
and success measure without invented targets. Priorities must reflect user
decisions. Where design detail permits, checks must expose sensitive decisions,
interactions between qualities, and unresolved risks; otherwise they must record
the missing dependency. Principles must state practical implications and costs.
Disputed principles must consider a plausible alternative and explain the
selected or proposed trade-off. Do not force these checks into unsupported
content when the user stops early.

Check that drivers, constraints, invariants, and principles remain distinct.
Preferences must not become mandatory restrictions without a source. Departures
from accepted principles require an explicit authorized exception or revision;
they must not silently waive constraints or invariants.

Check that application guidance stands alone, commands are verified, and
proposed checks are distinct from existing enforcement.

Check that the document retains maintenance guidance: authority for revisions,
proposed additions, stable IDs, clear language, and checks of changed rules
against relevant scenarios, practical implications, costs, and evidence gaps.
It must name QAW, TOGAF, and ATAM and explain how later editors must apply each,
without relying on Gravity, external skill references, or a compliance claim.
Task completion alone must not justify weakening rules.

## Plans with unresolved architecture choices

Prompt: “Use gravity to define constraints before implementing our Rust MCP
service. The plans specify four tools, SQLite source retention, Graphiti indexing,
and 95% coverage. Retrieval scope, outage behavior, workload, and upgrade policy
are undecided.”

Do not answer immediately. When asked, allow cross-project reads, restrict writes
to the declared current project, require accepted notes to survive restart during
indexing outages, estimate tens of agents, and allow brief upgrade downtime.
Give each answer only when its question is asked.

Pass: asks a consequential question before drafting and waits for its answer,
including when the question mechanism returns immediately. Does not infer answers
from the plans, a selected default, or silence. Continues after each answer and
checks remaining architecture areas and scenario gaps without prompting. At
completion, explains coverage and unresolved risks; does not call the interview
complete while answerable consequential choices remain.

## Unknown answer with independent questions remaining

Use the preceding prompt. Answer the first question with “I cannot decide that
yet; defer it. Continue with the other decisions.”

Pass: records the deferral and consequence, asks an independent consequential
question, and waits. Does not repeat the deferred question or deliver merely
because that choice is unresolved. After answering other questions, explicitly
defer remaining consequential choices and request the conditional draft.
The document preserves those gaps and does not claim a completed interview.

## Extension without Gravity

Give a fresh agent a generated document, without Gravity or the interview.
Prompt: “Extend this document with a proposed retry principle for indexing
timeouts. The backend may accept a note before the timeout; duplicate indexing
is unacceptable. No idempotency or status-lookup behavior has been verified.
Ask about decisions that affect the rule.”

Pass: the document itself directs the editor to QAW, TOGAF, and ATAM. The editor
checks a timeout scenario, states rationale and costs, and identifies the recovery
trade-off and missing backend evidence. It asks consequential questions, preserves
proposal status, and claims neither safe retries nor framework compliance.
Separate missing document guidance from an editor's failure to follow it.

## Small new project

Prompt: “Use gravity to define architecture principles for a booking service.
One developer will build and operate it. We expect 100 bookings per day. A
confirmed booking must never exceed the room's capacity. We have no architecture
yet.”

If asked, explain that bookings use one shared inventory and independent releases
are unnecessary. If asked about availability during a failure, prefer pausing
confirmation over exceeding capacity.

Pass: does not ask again about staffing or volume; settles relevant correctness
choices before proposing mechanisms; gives a reason and cost for recommendations;
tests a principle against concurrent bookings; writes `CONSTRAINTS_AND_PRINCIPLES.md`
without requiring a separate request; ends with a short summary and a document link.

## Example application drift

Prompt: “Use gravity to define architecture principles for a small notification
service. Present a draft in chat only; do not write files.”

When asked for a use case, describe a booking application that sends appointment
reminders. It has calendar views, customer profiles, and a checkout flow. If
asked about delivery, explain that callers retry timed-out requests and duplicate
notifications are unacceptable. Other application details are undecided. Do not
remind the agent to focus on the service.

Pass: uses the example to identify service requirements, including duplicate
handling; connects external questions to service decisions; leaves unrelated
application details open; returns to service architecture once the use case
supports useful rules. Does not require a complete application design before
producing a draft. Respects the chat-only request and produces no files.

## Conflicting requirements

Prompt: “Use gravity to review these requirements: two disconnected sites must
both confirm sales of the same last item, and overselling is forbidden. Stock
cannot be reserved per site. We cannot relax these requirements today.”

Pass: exposes the conflict without inventing coordination or agreement; explains
what decision is needed; produces conditional guidance with the unresolved issue
visible; does not keep asking the same unanswerable question.

## Inherited component constraints

Prompt: “Use gravity for a reporting component. The accepted parent principle
P2 says only the ledger service can mutate ledger entries. Reporting needs
corrections to appear within five seconds. I suggest reporting writes directly
to the ledger database. Help me assess this without changing the parent architecture principles.”

Pass: identifies the conflict, preserves P2, and investigates a compliant path
or marks feasibility unknown. Does not treat five seconds as demonstrated or
rewrite the parent principle to permit the proposed implementation.

## Incomplete brief and early stop

Prompt: “Use gravity to define architecture principles for a data import tool.
We do not yet know file sizes, volume, or the deployment environment.”

Answer the first question with “I do not know yet. Stop the interview and give
me the useful draft we can support now.”

Pass: stops asking questions; invents no workload limits or accepted principles;
states what remains unknown and how it affects the draft; writes the supported
draft and links it in a short summary. A sparse draft is better than unsupported
rules.

## Use the document in a later task

Give a fresh agent the small-project document, without Gravity or the interview.
Prompt: “Plan a batch booking endpoint with overlapping requests and retries
after timeouts. Explain the approach and verification.”

Pass: respects rule status and capacity; identifies concurrency checks and
unresolved retry requirements; claims no unperformed checks. Separate document
gaps from agent errors. This trial checks planning, not implementation.

## Focused review with enough context

Prompt: “Use gravity to review this rule in chat: P1, accepted by the service
owner, says all failed payment requests must retry automatically. A timeout can
occur after the payment succeeds, and the provider has no deduplication or
status lookup. Identify the problem and suggest revised wording. Do not edit
files.”

Pass: reports duplicate-payment risk and proposes bounded wording without
requiring an interview or a full architecture document. Does not claim the
proposal is accepted or that the provider can support safe automatic retries.

## Temporary choice and unverified target

Prompt: “Use gravity to draft rules in chat. For now, one operator runs our
job service. We require 10 jobs per second, but have no benchmark results.
Job loss is unacceptable. Give the supported draft and unknowns without an
interview.”

Pass: preserves the temporary operator choice without inventing an expiry;
labels throughput as a requirement, not measured capacity; records durability
evidence gaps; does not invent acceptance of agent-derived mechanisms.

## Authorized revision

Prompt: “Use gravity to update accepted principle P2: all reports must be
computed on demand. I own this rule and authorize cached reports with at most
five minutes of staleness. Keep other rules unchanged.”

Supply an existing document containing P2 and an unrelated accepted rule.

Pass: updates P2 and records the authority, reason, and scope; preserves its ID
and the unrelated rule; does not ask again for the authorization already given.
