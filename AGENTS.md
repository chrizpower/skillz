# Working on skills

## Communication and scope

- Use ASD-STE100 Simplified Technical English, adapted to software terminology. Preserve technical precision. Use expressive marketing copy when requested.
- Keep explanations and instructions concise. Remove repetition and obvious advice without losing decision boundaries. Challenge changes that broaden a skill beyond its purpose.
- Reviews and proposals do not authorize edits. Preserve unrelated work. Commit and push only when requested; stage explicit reviewed paths.

## Repository and portability

- Follow the repository's source layout and packaging conventions. Maintain one canonical source per skill; avoid divergent copies for different environments.
- Keep distributed packages self-contained. Update relevant manifests and catalogs when packaging changes.
- Keep shared instructions tool-neutral. Separate environment-specific metadata and setup from the skill's workflow. Do not assume tools or paths exist in every environment.
- Keep activation descriptions precise; put marketing copy in repository or package descriptions.

## Skill design

- Define one clear purpose per skill. Prefer narrow corrections supported by observed failures. Consolidate overlap before adding instructions; use references for substantial detail needed only in specific cases.
- Before and after substantive edits, compare word counts for `SKILL.md` and changed references separately. Explain growth; prefer replacing or consolidating instructions over adding them. Fewer words alone do not prove better results.
- When shortening instructions, preserve scope, authority, stopping conditions, and evidence distinctions. Check revised guidance against existing behavioral scenarios.
- Use examples within scope. Stop exploring related systems when further detail cannot change the result.
- Distinguish observed behavior, proposals, accepted requirements, and measured evidence. Existing authorization remains valid; do not create redundant approval steps.
- Make generated artifacts usable without the original conversation. Include application guidance, checks, gaps, and maintenance instructions where relevant. Documentation alone does not enforce behavior.
- Respect requested output format, destination, and revision scope. After writing an artifact, give a short summary and link.
- Scale methods and validation to the task. Do not impose full frameworks when selected practices are sufficient.

## Validation and releases

- Run available validators and check the diff for whitespace errors. Verify changed links and package references.
- Keep behavioral trials outside runtime instructions. Distinguish static validation from observed agent behavior; report unrun trials. Test each target environment before claiming compatibility.
- Update versions according to the release process. Verify the intended installed version; account for caches and duplicate discovery sources where applicable.
