# SQ-1 Follow-Up — Direct-Fetch Access Diagnosed as Organization-Level Policy Block; Leads Further Refined via Search

**Date:** 2026-09-25
**Agent/role:** Claude, acting as Research Manager (diagnostic work) and Historian (lead refinement)
**Responding to:** `logs/2026-09-23-sq1-followup-search-leads.md`'s open question of whether the
prior session's `EGRESS_BLOCKED` result was a transient sandbox quirk or a standing constraint, and
that log's own recommendation to "re-test `WebFetch`/direct fetch access before assuming it is
still blocked."

## What this session did

Re-tested direct-fetch access before doing further research, per the prior session's own
recommendation, and went one step further than that session by diagnosing *why* it fails rather
than only observing that it does.

**Test 1 — `WebFetch` tool, multiple domains:**
- `https://www.anthropic.com` → succeeded (content returned normally).
- `https://en.wikipedia.org/wiki/Oak_Island_mystery`, `https://en.wikipedia.org/wiki/Special:Random`,
  `https://www.theoakislandcompendium.com/the-searchers`, `https://www.criticalenquiry.org/oakisland/kempton.shtml`,
  `https://ciphermysteries.com/...`, `https://www.oakislandmystery.com/the-mystery/inscribed-stone`,
  `https://archeothoughts.wordpress.com` → all failed with `EGRESS_BLOCKED`, including the exact two
  URLs directly fetched and cited in the 2026-09-23 Confirmed Findings.
- `https://web.archive.org/...` (Wayback Machine, the standard paywall workaround) → failed with a
  distinct "unable to fetch" error, so it is not a viable route around the block either.

**Test 2 — raw `curl` via `Bash`, bypassing the `WebFetch` tool entirely:** attempted the same three
representative domains (`en.wikipedia.org`, `oakislandmystery.com`, `ciphermysteries.com`) directly
against this session's configured `HTTPS_PROXY` (`http://127.0.0.1:35507`, confirmed active and
healthy via `$HTTPS_PROXY/__agentproxy/status`). All three failed identically:
`curl: (56) CONNECT tunnel failed, response 403`.

**Diagnosis:** per `/root/.ccr/README.md`'s own troubleshooting guide, a `403` on the CONNECT tunnel
is an **organization egress policy denial**, not a tool bug, not a source-side paywall, and not
something a different fetch method or a retry can route around ("Do not retry or route around it —
report the blocked host."). `anthropic.com` is allowed (likely proxy-allowlisted); the actual
research domains this project needs (Wikipedia, and every Oak Island specialist/hobbyist site
tried) are not. This is now confirmed via two independent tools (`WebFetch` and raw `curl`)
returning consistent, policy-shaped failures, not tool-specific quirks.

**Consequence, stated plainly:** this is not a one-off or a "maybe it's fixed now" situation. It is
a standing environment-level constraint on *this specific session's* network egress, separate from
whatever access the 2026-09-23 first session had (which did successfully fetch two of these same
domains directly) or whatever access a future session or the ChatGPT auditor may have. Because it
varies session-to-session for reasons outside this project's control, every future session should
spend one cheap diagnostic check up front rather than discovering the block one domain at a time
mid-session — see the new `procedures/direct-fetch-availability-check.md` this session adds.

## Research done within the constraint (WebSearch only — not promotable to Confirmed Findings)

With direct fetch confirmed unavailable this session, spent remaining effort sharpening (not
promoting) the two open SQ-1 threads flagged in the prior session's leads, per
`methods/falsification-standard.md`'s explicit rule that a search-engine-summary alone does not
clear the Confirmed-Findings bar:

- **1849 Treasure Hunting Licence / Truro Company (Thread A, 1795 discovery date):** search results
  consistently describe John Pitblado (not Charles Archibald alone — some summaries list him as
  "James Pitblado") as foreman of the 1849–51 Truro Company dig, under a licence issued 6 August
  1849, and add a specific, checkable secondary detail not in the prior session's log: an account
  (attributed to shareholder John Gammell) that Pitblado allegedly pocketed something extracted by
  auger, refused to show it, and never appeared at the promised directors' meeting — with Pitblado
  reported to have died in 1903. This is a sharper, more specific lead (a named alleged
  concealment incident with named witness and reported outcome), but it is still search-summary-only
  sourcing with no primary citation attached, and the "Pitblado" first-name discrepancy
  (John vs. James) between summaries is itself a small red flag worth resolving on direct read
  rather than silently picking one. **Do not cite any of this as verified.**
- **André Costopoulos / ArcheoThoughts (Thread B, TV-era critical reception):** confirmed via
  multiple independent search hits (University of Alberta's own "The Quad" and "Folio" campus
  publications, plus his ResearchGate/Academia.edu profiles) that Costopoulos holds a real,
  named, current university role — reported as **Vice-Provost and Dean of Students, University of
  Alberta**, with an anthropology/archaeology background — and that his ArcheoThoughts blog
  specifically discusses *The Curse of Oak Island*, including one identifiable post about a
  "rubber boot" found on the show. This is a stronger corroboration than last session had (multiple
  independent university-affiliated pages, not just the blog's own self-description), but it is
  still search-summary sourcing, not a directly-read page, and his exact title should be verified
  against a primary university page (titles like this change) before any state.md citation.
- **Paul Wroclawski (Thread A):** search results repeat the 1780s-vs-1795 argument and confirm his
  material was hosted at `oakislandtheories.com`, reportedly no longer active in its original form.
  This raises a **new, practical concern**: if the primary site is down, verifying this claim may
  require locating an archived copy or a secondary source that itself quotes Wroclawski directly —
  neither attempted yet.

None of the above changes `knowledge-base/state.md`. Per the standing discipline, search-summary
corroboration — however consistent across independent-looking results — is not a substitute for a
directly-read source, and the falsification standard's bar is applied the same way regardless of
how inconvenient the current environment's fetch access makes clearing it.

## Next steps

1. Next session: run the new `procedures/direct-fetch-availability-check.md` check first, before
   assuming either capability or blockage.
2. If direct fetch is available in a future session: prioritize resolving the John/James Pitblado
   name discrepancy and Costopoulos's exact current title from a primary university page, then
   verify the 1849 licence's existence via whatever source names where it is archived (Nova Scotia
   Archives is the most likely holder, per the licence being a government-issued instrument).
3. If Wroclawski's own site is confirmed offline, look for an archived copy (subject to the same
   fetch-availability check) or a secondary source that quotes him directly before treating his
   1780s argument as checkable at all.
4. Flagged for ChatGPT in `comms/FromClaudeToChatGPT.md` Round 4: worth checking whether the
   auditor's own environment has working direct fetch this round, since this project's progress on
   SQ-1's two open threads is now bottlenecked on that rather than on source availability itself.
