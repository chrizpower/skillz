# Evidence and review reuse

Use when repeated evidence or equivalent task instances consume review context.
Project acceptance and review requirements govern any reuse.

## Compact evidence

Retain full failure output once in a stable artifact. Link its path, size, digest,
command status and correction from concise notes instead of copying prior histories.
Preserve required bodies and meaningful repeated occurrences; matching bytes alone
do not justify removing evidence.

Distinguish the command's exit status from capture or runner failure. Truncated
output is incomplete evidence; missing stderr or exit status is unknown. Do not
reconstruct lost historical output or claim a pass from a successful precheck.
Use cheap shape, hash and binding checks before expensive gates where useful;
they do not replace semantic review or acceptance tests.

## Equivalent task instances

Similar file shape does not establish equivalent behavior. Use a shared contract
only when assumptions, invariants, authority, failure behavior and acceptance are
unchanged; identify the variable command/data fields.

Where project rules permit, review that common contract once, then check each
exact instance's bindings, changes and execution evidence through the required
review path. Reuse evidence only for identical inputs and covered scope; retain
each instance's evidence links. A changed assumption or semantic rule requires
focused review before dependent work proceeds.

Preserve historical reviews as evidence of their original scope. Do not rewrite
them to imply coverage of a later contract. This procedure grants no authority
to omit required checks or reviews.
