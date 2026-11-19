# Higgsfield Skill Runtime

A portable English skill bundle for planning and producing images and video with Higgsfield. It includes a [main skill](higgsfield/SKILL.md), 35 specialist skills, creative references, templates, dated model schemas, and Python helpers.

The main skill routes requests for prompt writing, camera and motion direction, storyboards, character design, production planning, and delivery checks to the relevant specialist files.

## Install and use

1. Download the [release ZIP](https://github.com/rodrigojager/higgsfield-skill-runtime/releases/latest) or clone this repository.
2. Copy the complete `higgsfield/` folder into the skills directory configured for your agent. Keep its name and internal paths so the main skill can find its specialist instructions and resources.
3. Invoke the `higgsfield` skill through your agent or direct it to read `higgsfield/SKILL.md`. You can use the bundle with agents that load Markdown skills and can read their companion files, including Codex, Claude Code, and OpenCode.

Prompt drafting and creative planning can use the bundled references. The local production checks use Python's standard library. Live model discovery, cost estimates, and generation require separately configured access through the Higgsfield CLI or MCP. Check the current model schema and price before paid requests. Keep project inputs and deliverables in the project workspace.

## Production helpers

- `higgsfield/scripts/preflight.py` checks request parameters and media requirements.
- `higgsfield/scripts/seedance_lint.py` checks Seedance prompt structure and common failure patterns.
- `higgsfield/scripts/higgsfield_memory.py` looks up production history and records delivery outcomes.
- `higgsfield/scripts/sub_skill_descriptions.py` supplies the specialist roster to the memory helper.

## Source and license

This reduced runtime is based on [OSideMedia/higgsfield-ai-prompt-skill](https://github.com/OSideMedia/higgsfield-ai-prompt-skill), upstream tag `v3.40.0` at commit `70754977d1884794963ac0a748eaaa85b6e9c82a`. The original O-Side Media MIT attribution is preserved in [LICENSE](LICENSE). See [CHANGES.md](CHANGES.md) for the reduction and prior delivery checks.
