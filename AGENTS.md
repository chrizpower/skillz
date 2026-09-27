# Working in skillz

## Communication and scope

- Use ASD-STE100 Simplified Technical English, adapted to software terminology. Preserve technical precision. Use expressive marketing copy when requested.
- Keep explanations and instructions concise. Remove repetition and obvious advice without losing decision boundaries. Challenge proposed changes when they would broaden a skill beyond its purpose.
- Reviews and proposals do not authorize edits. Preserve unrelated work. Commit and push only when requested; stage explicit reviewed paths.
- Never read, change, or include any `AI.md` in searches, diffs, formatting, staging, or agent context.
- Prefix shell commands with `rtk`; use `rtk proxy` for commands without a wrapper.

## Repository

- Maintain one shared skill source for Claude Code and Codex. Published sources live in `plugins/<name>/skills/<name>/`; `skills/<name>`, `.agents/skills/<name>`, and `.claude/skills/<name>` provide local links.
- Keep plugins self-contained. Update their `.codex-plugin/plugin.json` and `.agents/plugins/marketplace.json` when packaging changes. See `README.md` for installation and layout.
- Keep shared instructions tool-neutral. Put Codex display metadata in `agents/openai.yaml`. Keep activation descriptions precise; use the README and plugin descriptions for positioning.

## Skill design

- Define one clear purpose per skill. Prefer narrow corrections supported by observed failures. Consolidate overlap before adding instructions; keep detailed templates and methods in references.
- Before and after substantive skill edits, compare word counts for `SKILL.md` and changed references separately. Explain growth; prefer replacing or consolidating instructions over adding them. Fewer words alone do not prove better results.
- When shortening instructions, preserve scope, authority, stopping conditions, and evidence distinctions. Check revised guidance against existing behavioral scenarios.
- Keep Gravity focused on architectural constraints and principles. Broad codebase discovery, implementation plans, and enforcement tooling are separate work.
- Use examples to expose requirements within scope. Stop exploring a consuming application when further detail cannot change the target system's rules.
- Preserve distinctions between observed behavior, proposed rules, accepted obligations, and measured evidence. Existing authorization remains valid; do not create redundant approval steps.
- Artifacts must work without the skill or interview: explain application, checks, gaps, and authorized maintenance. Preserve compliant implementation freedom. Never imply that documentation itself enforces a rule.
- For Gravity rule creation, write `CONSTRAINTS_AND_PRINCIPLES.md` or use the existing equivalent by default. Reviews report findings; revisions update the existing document within scope. Respect chat-only requests. After writing, give a short summary and link.
- Apply selected QAW, TOGAF, and ATAM practices in proportion to the decision. Preserve useful scenario evidence, rationale, implications, and risks without imposing full framework compliance.

## Validation and releases

- Run available skill/plugin validators and check the diff for whitespace errors. Verify changed links and package references.
- Keep behavioral trials in `tests/`, outside runtime instructions. Distinguish static validation from observed agent behavior; report unrun trials. Test both agents before claiming cross-agent behavior.
- Bump the plugin version for published plugin changes. Installed caches do not follow local edits; test the intended version without duplicate discovery sources.
