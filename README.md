# skillz

Personal skills for Claude Code and Codex. Each installable plugin contains its
skill source. `skills/<skill-name>` links to that source for local use.

## Gravity: find the forces that shape your software

A bridge must answer to gravity. An engine must answer to heat. Software gives
us extraordinary freedom to reshape a design, but that freedom can obscure the
forces it still has to answer to: correctness, latency, cost, and the people
who build and operate it.

Gravity brings that engineering mindset to software architecture. Through a
focused interview, it uncovers the forces that matter, challenges trade-offs,
and turns them into explicit principles and constraints. The result is an
`ARCHITECTURE.md` grounded in your system, with rules you can use to design,
review, and evolve it. Real constraints stay distinct from deliberate choices.

## Structure

```text
.agents/plugins/marketplace.json          Codex marketplace catalog
plugins/gravity/.codex-plugin/plugin.json Plugin manifest
plugins/gravity/skills/gravity/           Shared skill source
skills/gravity                           Link to the packaged skill
templates/skill/SKILL.md                  Starter template
.agents/skills/<name>                     Codex local discovery link
.claude/skills/<name>                     Claude Code local discovery link
```

No build step or package manager is required.

## Available skills

| Skill | Purpose | Codex | Claude Code |
| --- | --- | --- | --- |
| [gravity](skills/gravity/SKILL.md) | Find your software's gravity. Turn architectural forces into principles and constraints. | `$gravity` | `/gravity` |

Use the [Gravity interview trials](tests/gravity.md) to check question quality,
handling of conflicts, and the usefulness of the rules in both agents.

## Install in Codex

Run these commands with a Codex CLI that supports `codex plugin`:

```sh
codex plugin marketplace add chrizpower/skillz
codex plugin add gravity@skillz
```

Start a new session in your target project and invoke `$gravity`. You can also
use `/plugins` to browse the `skillz` marketplace and install Gravity.

For later releases, refresh the marketplace and reinstall the plugin:

```sh
codex plugin marketplace upgrade skillz
codex plugin add gravity@skillz
```

Start a new session after an update. Plugins use an installed cache; local edits
do not update that copy. Use either the installed plugin or the local discovery
links in a session to avoid duplicate skills. The links remain useful for
development and Claude Code.

For published releases, update the plugin manifest's version before committing
and pushing.

## Test the local package

Before publishing, add this checkout as a marketplace source:

```sh
codex plugin marketplace add /absolute/path/to/skillz
codex plugin add gravity@skillz
```

Use a separate target project for the interview trials. The local and Git sources
have the same marketplace name; configure one at a time.

## Create a skill

Run these commands from the repo root on macOS or Linux. Replace `my-skill`
with a name that uses lowercase letters, digits, and single hyphens between
words. Keep it under 64 characters. Do not use `synced` or `anthropic-skills`.

```sh
skill_name=my-skill
mkdir "skills/$skill_name"
cp templates/skill/SKILL.md "skills/$skill_name/SKILL.md"
```

Edit the new file. Set `name` to the folder name, replace the description with
the task and when to use it, and replace the body with the actual instructions.
Then enable the skill in this repo:

```sh
mkdir -p .agents/skills .claude/skills
ln -s "../../skills/$skill_name" ".agents/skills/$skill_name"
ln -s "../../skills/$skill_name" ".claude/skills/$skill_name"
```

Commit the source folder and both links together. Start a new session in this
repo. Invoke the skill with `$my-skill` in Codex or `/my-skill` in Claude Code.
Check one request that should use the skill and one that should not.

To publish it as a separate plugin, follow the Gravity layout under
`plugins/<name>/`, add its manifest and catalog entry, and replace
`skills/<name>` with a link to the packaged source. Keep all plugin resources
inside its folder so installation does not depend on external links.

## Keep skills portable

- Use `name` and `description` in the shared YAML frontmatter.
- Write instructions that both tools can follow. Avoid tool-specific variables,
  tool names, and slash commands in the shared workflow.
- Add `scripts/`, `references/`, or `assets/` inside a skill only when needed.
  Link supporting files from `SKILL.md` with paths relative to the skill folder.
- State required tools and dependencies. A shared file format does not make
  external tools available in both agents.
- Add optional Codex metadata in `agents/openai.yaml` only when needed.
  Claude-specific frontmatter and execution features need separate checks.

## Use local links in other repos

To make one completed skill available to your local user in both tools, run
these commands from this repo's root:

```sh
skill_name=my-skill
skills_repo=$(pwd -P)
mkdir -p "$HOME/.agents/skills" "$HOME/.claude/skills"
ln -s "$skills_repo/skills/$skill_name" "$HOME/.agents/skills/$skill_name"
ln -s "$skills_repo/skills/$skill_name" "$HOME/.claude/skills/$skill_name"
```

Keep the repo at that path while the links are in use. The commands do not
replace existing entries. Use either repo-local or user-level links for a skill
to avoid duplicate discovery. On systems without symlink support, copy the
complete skill folder to each discovery folder and keep the copies in sync.

## References

- [Codex skill format and discovery](https://learn.chatgpt.com/docs/build-skills)
- [Codex plugin packaging and marketplaces](https://developers.openai.com/plugins/build/plugins)
- [Claude Code skill format and discovery](https://code.claude.com/docs/en/skills)
