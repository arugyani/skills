# Skills

Reusable agent skills by [arugyani](https://github.com/arugyani).

## Ideas

[Ideas](ideas/SKILL.md) interviews you about your current interests, short- and long-term aspirations, and practical knowledge. It then helps you notice connections and develop ideas yourself through questions, observations, and small experiments.

It covers personal curiosity, technical and creative projects, and career or business exploration. The interview asks one question at a time. Profiles stay in the conversation unless you request a saved handoff.

The entire skill is in `ideas/`:

```text
ideas/
├── SKILL.md
├── agents/openai.yaml
└── references/
    ├── discovery-moves.md
    └── profile.md
```

## Install

Clone this repository, then copy the whole `ideas` folder into a skills directory supported by your harness. Keep `references/` with `SKILL.md`; its links are relative to the skill folder. The package uses the shared Agent Skills format and needs no model-specific code, plugins, API keys, or dependencies. `agents/openai.yaml` provides optional Codex UI metadata.

For example, to install for Claude Code on macOS or Linux:

```sh
git clone https://github.com/arugyani/skills.git
cd skills
mkdir -p ~/.claude/skills
cp -R ideas ~/.claude/skills/
```

For another harness, replace `~/.claude/skills` with its directory below. Use a project directory to share the skill with that project's contributors. These are installation destinations; simply cloning this repository does not activate the root-level `ideas/` folder.

| Harness | Project skills directory | Personal skills directory | Official documentation |
| --- | --- | --- | --- |
| Codex | `.agents/skills/` | `~/.agents/skills/` | [Codex](https://learn.chatgpt.com/docs/build-skills) |
| Claude Code | `.claude/skills/` | `~/.claude/skills/` | [Claude Code](https://code.claude.com/docs/en/skills) |
| Pi | `.agents/skills/` | `~/.agents/skills/` | [Pi](https://github.com/badlogic/pi-mono/blob/main/packages/coding-agent/docs/skills.md) |
| OpenCode | `.opencode/skills/` | `~/.config/opencode/skills/` | [OpenCode](https://opencode.ai/docs/skills/) |
| Cursor | `.cursor/skills/` | `~/.cursor/skills/` | [Cursor](https://cursor.com/docs/skills) |
| Gemini CLI | `.gemini/skills/` | `~/.gemini/skills/` | [Gemini CLI](https://geminicli.com/docs/cli/skills/) |
| GitHub Copilot | `.github/skills/` | `~/.copilot/skills/` | [GitHub Copilot](https://docs.github.com/en/copilot/how-tos/copilot-on-github/customize-copilot/customize-cloud-agent/add-skills) |
| Windsurf / Devin Desktop | `.windsurf/skills/` (legacy) or `.devin/skills/` | `~/.codeium/windsurf/skills/` or `~/.config/devin/skills/` | [Cascade](https://docs.devin.ai/desktop/cascade/skills) |
| Cline | `.cline/skills/` | `~/.cline/skills/` | [Cline](https://docs.cline.bot/customization/skills) |
| Roo Code | `.roo/skills/` | `~/.roo/skills/` | [Roo Code](https://roocodeinc.github.io/Roo-Code/features/skills/) |

Each destination should end up containing `ideas/SKILL.md`. The same package works in each documented skills layout; separate copies of the instructions are unnecessary. Discovery locations were checked against official documentation on October 12, 2026. Live conversational behavior has not been evaluated in every harness.

## Use

After installation, ask:

> Use the ideas skill to interview me about my interests and help me discover ideas worth exploring.

You can also invoke it explicitly in Codex with `$ideas`, Claude Code with `/ideas`, and Pi with `/skill:ideas`. If a newly installed skill is missing, restart the harness or use its resource reload command.

To resume an earlier exploration, supply the profile you asked the guide to save and ask it to continue from an open thread.
