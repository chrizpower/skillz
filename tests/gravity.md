# Gravity interview trials

Run each case in a fresh session with the skill loaded. Use both Claude Code
and Codex before claiming cross-agent behavior. Keep these trials outside the
skill's runtime references. Judge decisions and questions, not exact wording.

Record the agent and model, questions asked, final Architectural Constraints and
Principles document, and pass or failure against the checks below. These are
test cases, not recorded test results.

For completed interviews, also check that dominant forces identify affected
stakeholders and confirmation sources or gaps. Each dominant driver must have
scenario coverage; one scenario can cover several. Priority scenarios must
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
proposed additions, stable IDs, and concrete ASD-STE100, QAW, TOGAF, and ATAM
instructions. Task completion alone must not justify weakening rules.

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
