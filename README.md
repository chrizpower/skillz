# skillz

Personal skills for Claude Code and Codex. Keep one source copy of each skill
in `skills/<skill-name>/SKILL.md`.

## Structure

```text
skills/                    Shared skill sources
templates/skill/SKILL.md    Starter template; not an active skill
.agents/skills/<name>       Codex link to ../../skills/<name>
.claude/skills/<name>       Claude Code link to ../../skills/<name>
```

No build step or package manager is required.

## Available skills

| Skill | Purpose | Codex | Claude Code |
| --- | --- | --- | --- |
| [gravity](skills/gravity/SKILL.md) | Identify architectural drivers and create or revise architecture principles and constraints. | `$gravity` | `/gravity` |

Use the [Gravity interview trials](tests/gravity.md) to check question quality,
handling of conflicts, and the usefulness of the rules in both agents.

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

## Use a skill in other repos

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
- [Claude Code skill format and discovery](https://code.claude.com/docs/en/skills)
