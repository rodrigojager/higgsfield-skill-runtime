# Changes from upstream v3.40.0

## 3.40.0-rodrigo.1

Keep the 36 English skill identities and their creative/service capabilities. Retain 120 runtime files and remove 106 development, maintenance, redundant-output, and platform-specific files.

| Removed group | Files | Reason |
| --- | ---: | --- |
| `tests/` | 27 | Tests of the library and its tooling, including fixtures |
| `evals/` | 19 | Tests of skill coverage and documentation claims |
| `.claude/`, `.github/` | 11 | Claude-specific configuration and repository CI |
| `assets/` | 5 | Fonts used to generate the library's PDF manual |
| Extra `docs/` files | 5 | Maintenance history, audit archives, PDF manifest, and upstream experiment backlog |
| Extra `scripts/` files | 10 | Library validation, index/spec maintenance, PDF generation, and their helpers |
| Extra `specs/` files | 11 | Older catalog snapshots and the maintenance cross-check allowlist |
| `workspace/` scaffolding | 7 | Empty-folder instructions and placeholders; project workspaces are created on demand |
| Extra root files | 9 | Original README, contributor/Claude instructions, changelog, generated index, development configuration and PDF dependencies |
| Extra `db/` files | 2 | Test-only demo ledger and a redundant generated memory summary |

Operational changes:

- Keep the production linter and request preflight. Embed the unchanged media-role predicate directly in `preflight.py`, removing its dependency on the larger `refresh_specs.py` maintenance CLI.
- Keep the routing-memory roster; update its description to its runtime purpose, removing references to PDF tooling.
- Remove dead links, maintenance commands, and generated-index validation claims from retained resources. Production helpers direct stale/missing-schema issues to current platform discovery rather than missing maintenance programs.
- Retain current video/image/audio/3D JSON/YAML/Markdown specs, their 2026-09-26 source snapshots, CLI baseline constraints, and runtime retired-ID metadata used by historical job records.
- Keep operational memory databases, the ledger format, and the generated cross-project ledger used by the memory helper. Memory summaries can be generated on demand.
- Clarify that working folders belong to the current delivery project, outside the globally installed library.
- Correct the 3D skill's obsolete statement that no generated 3D spec exists; point to the retained cached 3D constraints and live schema verification.

One-time delivery checks after reduction: an ordinary Seedance 2.5 text-to-video request passed cached platform preflight; an omni-reference request without references was rejected; prompt lint and memory queries ran; memory health reported no database issues. Pi resolved all 36 skills for the main profile and delegated child. No skill-development test suite is included, and no paid generation was performed.
