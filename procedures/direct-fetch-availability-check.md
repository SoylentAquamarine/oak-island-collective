# Procedure: Check Direct-Fetch Availability Before Starting Source Verification

**Why this exists:** the 2026-09-23 (second session) and 2026-09-25 sessions both lost part of a
research cycle to discovering, one domain at a time, that direct web fetch (`WebFetch`, and raw
`curl` through the session's configured proxy) was unavailable for this project's actual research
domains — even though a first 2026-09-23 session had working direct fetch and used it to produce
this project's only two Confirmed Findings so far. The 2026-09-25 session diagnosed the specific
cause (a `403` on the outbound proxy's CONNECT tunnel — an organization-level egress policy denial,
not a source-side block, tool bug, or something a retry or an alternate method like the Wayback
Machine can route around) and confirmed it is genuinely session-dependent, not a fixed project
constraint. See `logs/2026-09-25-sq1-fetch-blocker-confirmed-and-lead-refinement.md` for the full
diagnostic detail this procedure is drawn from.

## Steps

1. Before attempting any source verification for `knowledge-base/state.md`, run one cheap
   diagnostic `WebFetch` against a domain this project actually needs to cite (not a generic
   always-allowed domain like `anthropic.com`, which does not tell you anything about research-site
   access) — e.g. `https://en.wikipedia.org/wiki/Oak_Island_mystery`.
2. If it succeeds: proceed with direct-fetch-based verification as normal for the rest of the
   session.
3. If it fails with `EGRESS_BLOCKED` (or any tool-reported error): do **not** retry the same domain,
   try a workaround like the Wayback Machine (already confirmed not to work around this specific
   block), or spend further calls testing additional individual domains one at a time — that is
   exactly the wasted-cycle pattern this procedure exists to prevent. Instead, run:
   `curl -sS "$HTTPS_PROXY/__agentproxy/status"` once to confirm the proxy itself is healthy, then
   one raw `curl` test against a representative research domain. A `CONNECT tunnel failed, response
   403` confirms an organization egress policy denial per `/root/.ccr/README.md` — report it, don't
   route around it.
4. Once direct fetch is confirmed unavailable for the session, say so plainly in that session's log
   and switch immediately to `WebSearch`-only mode for the remainder of the session, spending effort
   on *sharpening leads* (more specific names, dates, and claims worth verifying later) rather than
   attempting to stretch search-summary sourcing into a Confirmed Finding — per
   `methods/falsification-standard.md`, it cannot substitute for a directly-read source regardless
   of how consistent multiple search results look.
5. Do not assume a prior session's blocked (or working) fetch access predicts this session's —
   it has already flipped at least once with no code change on this project's side. Re-run this
   check every session rather than caching the last session's result.

## Done looks like

Either: (a) a one-line confirmation early in the session's log that direct fetch works and normal
source-verification work proceeded, or (b) a one-line confirmation that it's blocked, the specific
error class (per `/root/.ccr/README.md`), and a clean pivot to search-only lead-sharpening for the
rest of that session — not a series of individual per-domain failures scattered through the log.
