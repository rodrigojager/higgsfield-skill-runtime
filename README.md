# Higgsfield skill runtime

Rodrigo's reduced English library for the `higgsfield-specialist` Pi agent. The [higgsfield](higgsfield/SKILL.md) folder contains 36 skills and the production resources they use: creative references, templates, cached platform schemas, job memory, and delivery preflight helpers.

Reduced from 226 files to 120, from 6,669,808 bytes to approximately 2.62 MB. See [CHANGES.md](CHANGES.md) for the removed material and operational adaptations. This repository starts with the reduced bundle; the complete upstream package and its skill-development tests are not included.

## Source and attribution

Derived from [OSideMedia/higgsfield-ai-prompt-skill](https://github.com/OSideMedia/higgsfield-ai-prompt-skill), upstream tag `v3.40.0`, commit `70754977d1884794963ac0a748eaaa85b6e9c82a`. The original O-Side Media MIT attribution is preserved in [LICENSE](LICENSE) and the installed skill bundle. Local runtime version: `3.40.0-rodrigo.1`.

## Use with Pi

The installed library belongs at `~/.agents/skills/higgsfield`, shared globally. Pi discovers the root skill automatically; add `~/.agents/skills/higgsfield/skills` to the `skills` array in `~/.pi/agent/settings.json` to expose the 35 nested skills.

The English [higgsfield-specialist profile and native MCP configuration](https://github.com/rodrigojager/pi-home-kit/tree/main/profiles/higgsfield-specialist) are published separately. The profile defaults to `openai-codex/gpt-6.1-sol`, high thinking, with the model and thinking selectable in Pi.

Release ZIPs contain only the `higgsfield/` runtime folder. They contain no credentials. The local MCP sign-in remains `/mcp login higgsfield`; configuring a profile does not authenticate a service account.

## Production helpers

- `scripts/preflight.py`: checks request parameters, media roles, and cached platform constraints before execution.
- `scripts/seedance_lint.py`: checks production prompt structure and known failure patterns.
- `scripts/higgsfield_memory.py`: reads and records delivery outcomes, recalls known issues, and reports credit history and routing.
- `scripts/sub_skill_descriptions.py`: the domain-skill roster required by routing memory.

These helpers use Python's standard library. Cached schemas retain their dated platform provenance; verify live MCP schemas and costs before paid requests, especially when cached data is old or a model is unknown. The helpers do not submit paid generations.

Delivery inputs and outputs belong in the current project's workspace; create the folders on demand. The shared installation contains skill resources rather than project deliverables.
