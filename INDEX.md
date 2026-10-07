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
- `FromClaudeToChatGPT.md` — through Round 5: SQ-1 first-cycle findings, direct-fetch blocker diagnosis, and SQ-2's frozen design + candidate-source catalog

## `data/` — source material

- `README.md` — what's present, what's needed (nothing catalogued yet — see SQ-1/SQ-2)
- `derived/stone-general-rendering.png`, `derived/stone-kempton-cipher.png` — directly downloaded from oakislandmystery.com (sha256 recorded in `logs/2026-10-06-sq4-structural-implausibility-cipher-key-inconsistency.md`); `derived/word-*.png` are PIL zoom-crops of individual word-groups used for the symbol-by-symbol consistency check in that log

## `docs/` — public site (GitHub Pages, deploy on push to `main` under `docs/`)

- `index.html` — site shell and all routes (overview, current thinking, process, logs, dialogue)
- `styles.css` — site styling (shared design system with the sibling Voynich/Rongorongo sites)
- `app.js` — client-side markdown rendering and live knowledge-base stats, reading from `SoylentAquamarine/oak-island-collective` on GitHub
- `.nojekyll` — disables Jekyll processing on GitHub Pages

## `knowledge-base/`

- `state.md` — Confirmed Findings (2, as of 2026-09-23: cipher-decoding provenance traces only to 1949/1894, not the 19th century; the stone's physical fate corrected to ~1911–1930s, not "lost after 1865") / Active Hypotheses (none yet) / Rejected Hypotheses (none yet) / Open Questions (updated 2026-09-25 with an unverified Smith's Cove second-fragment lead)

## `logs/`

- `README.md` — append-only work-log convention
- `2026-09-23-sq1-provenance-audit.md` — first real SQ-1 research cycle: 1795 discovery story, the 90-foot stone's discovery and physical fate, the cipher-decoding story's provenance, disagreeing symbol renderings, and TV-show-era reception, each with citations and disclosed sourcing limitations
- `2026-09-23-sq1-followup-search-leads.md` — direct fetch unavailable this session (`EGRESS_BLOCKED`); sharpened two open SQ-1 leads (1849 Pitblado licence, André Costopoulos) via search only, none promoted
- `2026-09-25-sq1-fetch-blocker-confirmed-and-lead-refinement.md` — diagnosed the fetch block as an org-level egress `403`, not transient; further search-only lead refinement, none promoted
- `2026-09-25-sq2-transcription-reconciliation-design.md` — SQ-2 opened per Meeting #1: frozen preregistered symbol-encoding/comparison methodology with a fixed decision threshold, a WebSearch-only candidate-source catalog, and a new unverified Smith's Cove second-fragment lead
- `2026-09-27-sq2-1857-primary-source-direct-read.md` — found and directly read the 1857 Liverpool Transcript letter (the earliest print source for the Money Pit story) from the primary archive scan itself; the earlier negative check had read the wrong column of the right issue, not the wrong issue
- `2026-09-28-stone-1864-colonist-account.md` — read the rest of the same 1857-letter compilation: the 1861 "Oak Island Folly" letter (detailed dig account, no stone mentioned) and, most valuably, the 2 January 1864 Colonist chapter — the richest stone description found to date, including a contemporary "not in their own vernacular" judgment and a primary-tier 1864 confirmation of Smith-family custody. The George Cooke letter (27 January 1864) is a separate, later source, resolved in `knowledge-base/state.md`'s 2026-09-28 update — not the same document as the Colonist chapter. A 2026-09-29 follow-up identifies the letter's precise archival context (Historical Society of Nova Scotia correspondence with Secretary Hunter-Duvar) and a new detail (stone built into Smith's chimney ~1824, viewed there ~1850) — the letter itself remains unlocated
- `2026-09-29-archives-request-draft.md` — drafted (not sent) a Nova Scotia Archives request for the Cooke/Hunter-Duvar correspondence, ready for the user to send
- `2026-10-04-sq4-beale-ciphers-comparator-case.md` — SQ-4's first comparator case: five named Beale Ciphers fabrication signatures (Nickell 1982, Singh 2000, Poundstone 1993), applied against Oak Island's own record — two real/partial matches (shifting undocumented decoded wording, an anonymous misattributed provenance chain), three signatures not yet checked
- `2026-10-05-sq4-kidd-legend-timing-check.md` — checks the third Beale-derived signature (genre/literary-convention echo): directly-fetched sources confirm Kidd-treasure digging activity well before 1857 (early 1800s, 1830) and a "Key West to Halifax" belief range already including Nova Scotia — a real but partial match, weaker than predicted; one unconfirmed search-synthesis claim explicitly not relied upon
- `2026-10-06-sq4-structural-implausibility-cipher-key-inconsistency.md` — checks the fifth and final Beale-derived signature by directly downloading and zoom-reading Kempton's own 1949 cipher-key image (not just a text description): six confirmed symbol/letter inconsistencies in the claimed key itself (e.g. O uses three different symbols across its three occurrences) — completes the Beale comparator case at 4 of 5 real/partial matches
- `2026-10-06-sq4-kensington-runestone-second-comparator.md` — SQ-4's second comparator case: five named Kensington Runestone fabrication signatures (Wahlgren, Flom 1910, Hagen, Winchell 1910/Edwards, Larsson 2019-2020), applied against Oak Island's own record — two real matches (promotional timing, commercial monetization), one informative disanalogy (Oak Island's stone is lost, foreclosing physical testing), one weaker partial match, one unresolved pending SQ-2

## `methods/`

- `falsification-standard.md` — promotion standard, Confirmed-Findings minimum bar, automatic stop conditions

## `procedures/`

- `README.md` — folder discipline (write from real incidents only)
- `direct-fetch-availability-check.md` — written 2026-09-25 after direct fetch was lost mid-project; check once per session up front instead of rediscovering domain-by-domain
