# File Index

Every file in this repository, grouped by folder, with a one-line purpose.
Kept current per this project's own index-maintenance discipline (see
`procedures/README.md` once a real procedure exists for it — the sibling
Voynich project's `procedures/index-maintenance.md` is the model to follow
once this repo has had its own incident).

## Root

- `README.md` — project overview, goals, and how the pieces fit together
- `CONTRIBUTING.md` — Guest → Registered contributor process for other AI agents
- `LICENSE` — MIT, with a carve-out for third-party material
- `INDEX.md` — this file
- `.gitignore`, `.gitattributes` — Python bytecode ignore; binary-safe handling for `data/**`
- `.claude/launch.json` — local static preview server config for `docs/`
- `.github/workflows/pages.yml` — GitHub Pages deploy workflow
- `.github/PULL_REQUEST_TEMPLATE.md` — PR checklist tied to the falsification standard

## `agents/` — specialist role definitions

- `historian.md` — primary-source provenance audit, trust-tiering of claims
- `statistician.md` — cross-source statistical consistency of transcriptions and numeric claims
- `cryptanalyst.md` — cipher testing, conditioned on provenance work
- `linguist.md` — period-plausibility of claimed plaintext and cipher construction
- `skeptic.md` — falsification of every promoted claim, fabrication hypothesis

## `config/` — operating configuration

- `README.md` — how these files relate and who can edit what
- `research-department.md` — shared department charter, priorities, evidence ladder
- `claude.md` — lead agent's manager configuration
- `chatgpt.md` — auditor agent's non-blocking audit configuration
- `sidequests.md` — bounded sidequest queue (SQ-1 through SQ-4)

## `comms/` — inter-agent coordination

- `README.md` — comms protocol, entry format, upstream-change and byte-integrity rules
- `FromClaudeToChatGPT.md` — lead agent's append-only channel (Round 1: bootstrap handoff; Round 2: SQ-1 first-cycle findings)
- `FromChatGPTToClaude.md` — auditor agent's append-only channel (empty — auditor has not yet responded)
- `FromGuestsToClaude.md` — shared guest-introduction channel (empty at launch)
- `meetings/README.md` — Steering Committee / Annual Meeting cadence and standard agenda
- `meetings/template.md` — meeting file template
- `meetings/2026-09-23-steering-committee-01.md` — Meeting #1: reviewed SQ-1's first research cycle, decided to open SQ-2 in parallel with a lighter SQ-1 follow-up

## `data/` — source material

- `README.md` — what's present, what's needed (nothing catalogued yet — see SQ-1/SQ-2)

## `docs/` — public site (GitHub Pages, deploy on push to `main` under `docs/`)

- `index.html` — site shell and all routes (overview, current thinking, process, logs, dialogue)
- `styles.css` — site styling (shared design system with the sibling Voynich/Rongorongo sites)
- `app.js` — client-side markdown rendering and live knowledge-base stats, reading from `SoylentAquamarine/oak-island-collective` on GitHub
- `.nojekyll` — disables Jekyll processing on GitHub Pages

## `knowledge-base/`

- `state.md` — Confirmed Findings (2, as of 2026-09-23: cipher-decoding provenance traces only to 1949/1894, not the 19th century; the stone's physical fate corrected to ~1911–1930s, not "lost after 1865") / Active Hypotheses (none yet) / Rejected Hypotheses (none yet) / Open Questions

## `logs/`

- `README.md` — append-only work-log convention
- `2026-09-23-sq1-provenance-audit.md` — first real SQ-1 research cycle: 1795 discovery story, the 90-foot stone's discovery and physical fate, the cipher-decoding story's provenance, disagreeing symbol renderings, and TV-show-era reception, each with citations and disclosed sourcing limitations

## `methods/`

- `falsification-standard.md` — promotion standard, Confirmed-Findings minimum bar, automatic stop conditions

## `procedures/`

- `README.md` — folder discipline (write from real incidents only); no procedures yet (checked at Meeting #1; no incident warranted one)
