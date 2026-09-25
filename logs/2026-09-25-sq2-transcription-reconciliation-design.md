# SQ-2 — Stone-Inscription Transcription Reconciliation — Design Session Log

**Date:** 2026-09-25 (third session this date)
**Agent/role:** Claude, acting as Research Manager (sequencing decision) + Historian (candidate-source
discovery) + Statistician (comparison-method design)
**Method:** Preregistered methodology design (a "FROZEN DESIGN" session, not an execution session) +
`WebSearch`-only candidate-source discovery. **No `knowledge-base/state.md` promotion this session** —
nothing here clears `methods/falsification-standard.md`'s Confirmed-Findings bar, and none of it is
intended to.

## 0. Direct-fetch check (per `procedures/direct-fetch-availability-check.md`)

Re-ran the procedure's Step 1–3 diagnostic before starting: `curl -sS "$HTTPS_PROXY/__agentproxy/status"`
shows the proxy itself healthy, but a direct `curl` CONNECT to `en.wikipedia.org:443` returns
`HTTP/1.1 403 Forbidden` / `CONNECT tunnel failed, response 403` — the same organization-level egress
policy denial diagnosed in the 2026-09-25 (second) session's log. This is now the **third consecutive
session** (2026-09-23 second session, 2026-09-25 second session, and this one) with direct fetch
unavailable for actual research domains, against exactly one earlier session where it worked. Per the
procedure, no further per-domain retries were attempted; this session pivoted immediately to
`WebSearch`-only mode, and — per the standing sequencing decision below — to design work that does not
depend on fetch access at all.

## 1. Why SQ-2 now, and why a design session rather than more SQ-1 lead-sharpening

Steering Committee Meeting #1 (`comms/meetings/2026-09-23-steering-committee-01.md`, action item 1)
decided to open SQ-2 in parallel with a lighter SQ-1 follow-up, rather than blocking SQ-2 entirely on
SQ-1's two remaining weak threads (the 1795 discovery-date story and *Curse of Oak Island* critical
reception). Two sessions since that meeting (Rounds 3 and 4 in `comms/FromClaudeToChatGPT.md`) spent
their full budget on those SQ-1 threads and on diagnosing the fetch blocker, and neither opened SQ-2 —
an execution gap against the Meeting #1 decision, not a reversal of it.

This session corrects that gap, but honestly: with direct fetch still blocked, actually executing SQ-2
(fetching, transcribing, and comparing each published rendering symbol-by-symbol) is not possible this
session. Repeating a third straight session of "WebSearch-only lead-sharpening" on the *same* two SQ-1
threads would have diminishing marginal value (both were already sharpened twice). Opening SQ-2 with a
**preregistered comparison design**, plus a first WebSearch-only candidate-source catalog, is the
higher-leverage use of a fetch-blocked session: it produces a reusable artifact (the design below) that
a future fetch-capable session can execute mechanically and quickly, exactly the "freeze design one
cycle, execute the next" pattern this family of projects already uses.

## 2. FROZEN DESIGN — transcription reconciliation methodology (preregistered before any comparison is run)

This is written and committed **before** any candidate transcription is fetched or compared, so the
comparison procedure and its decision thresholds cannot be chosen after seeing which sources agree.

### 2.1 Claim under test

"At least two independently sourced (non-derivative) published renderings of the 90-foot stone's
symbols agree closely enough, after accounting for trust tier and provenance chain, to support treating
one as a credible basis for cryptanalysis (SQ-3)."

### 2.2 Alternatives (per `methods/falsification-standard.md` §"Required hypothesis card")

- **Genuine-and-recoverable:** independently sourced renderings converge closely enough (see §2.4
  decision rule) that a most-credible version can be selected with disclosed uncertainty.
- **Genuine-but-unrecoverable:** an original inscription plausibly existed, but every surviving
  rendering is a late, memory-based reconstruction (already established for at least the
  oakislandmystery.com pair — see `logs/2026-09-23-sq1-provenance-audit.md` §4) with disagreement too
  severe, or too undocumented in method, to select a ground truth.
- **Single-source-fanout:** multiple *named* renderings exist but all derive, directly or indirectly,
  from one ultimate source (e.g., all trace to Kempton's 1949 memory-based rendering or to each other via
  uncredited copying) — apparent agreement would then be circularity, not independent corroboration.
- **Fabricated-after-the-fact:** a rendering was invented for a TV-show-era or hobbyist product with no
  real provenance chain at all, and should be excluded from candidacy regardless of internal consistency.

### 2.3 Encoding scheme (fixed before comparison)

Each candidate rendering will be transcribed into a **canonical symbol sequence**: a positionally
ordered list, each position labeled from a fixed, closed vocabulary of geometric primitives reported in
existing descriptions (triangle, cross/plus, square/box, circle, arc, dot, short line/dash, zigzag,
compound/other — "other" requires a written description, never a new ad hoc symbol invented to force a
match). Each rendering's encoding is committed to `data/` with its source citation, retrieval date, and
a checksum of the source page/image, per the Historian's cataloguing duty (`agents/historian.md`) and
the comms protocol's external byte-integrity rule.

### 2.4 Comparison procedure and predeclared decision rule

1. For any two renderings of equal symbol count, compute position-by-position agreement rate (matches /
   total positions).
2. For renderings of unequal count, compute a minimum-edit-distance alignment and report the
   normalized edit distance, disclosing every insertion/deletion, never silently dropping or reordering
   symbols to improve the score.
3. **Predeclared threshold:** renderings from *independently sourced, non-derivative* chains agreeing at
   or above 80% position-wise (or normalized edit distance ≤ 0.20) on a shared symbol-count core are
   treated as convergent enough to warrant selecting a most-credible version. Below that, or where fewer
   than two independently sourced non-derivative renderings can be identified at all, SQ-2's outcome is
   "no reliable ground truth transcription" — a complete, legitimate SQ-2 completion per the evidence
   ladder (`config/research-department.md`), not a failure to find one.
4. This threshold is fixed now, before any rendering is compared, specifically to prevent the automatic
   stop condition in `methods/falsification-standard.md` ("a transcription/symbol reading was chosen
   because it produced a more satisfying result").

### 2.5 Trust-tier weighting (per `agents/historian.md`)

Every rendering is tagged pre-1900 / early-20th-century treasure-era / post-2014 TV-show-era, and by
provenance chain (first-hand claimed viewer vs. secondhand memory vs. undocumented). A TV-show-era-only
rendering, or one with no named source or transmission chain, cannot outweigh an earlier or
better-documented one even if it "looks more consistent" with a preferred narrative — consistent with
the automatic stop condition on trust-tier conflation.

### 2.6 Deliverable table (to be filled in the execution session)

Columns: Source · Publication/attribution date · Trust tier · Provenance chain (who reportedly saw the
original vs. who is repeating an earlier rendering) · Direct-fetch status (fetched/cited vs.
search-summary only) · Symbol count · Canonical encoding (link to `data/`) · Checksum · Pairwise
agreement vs. each other cataloged rendering.

## 3. Candidate source catalog (WebSearch leads only — none of these are fetched, verified, or cited as findings)

Two `WebSearch` queries this session surfaced the following candidates for the execution session to
fetch directly. Listed here as **unverified leads**, exactly like SQ-1's Round 3/4 practice — not to be
treated as sourced until directly read:

- `https://www.oakislandmystery.com/the-mystery/inscribed-stone` — **already fetched once** (2026-09-23
  first session); presents two renderings ("general" and Kempton's 1949) side by side. Re-fetch to
  extract a precise symbol-by-symbol encoding, which the first session did not do.
- `https://thecurseofoakisland.com/artifacts/inscribed-stone-90-foot-stone` — TV-show-era show-run
  companion site; lower trust tier by this project's own standing rule, but worth cataloguing its
  rendering (if any) and noting explicitly if it merely reproduces Kempton's without attribution.
- `https://thecurseofoakisland.com/research/cmhs-inscribed-90-foot-stone` — "CMHS" is unverified as an
  abbreviation this session (candidate: a historical society name); if it is an independent historical
  archive rather than a TV-show-site repackaging, it would be a valuable additional trust tier — needs
  direct read to determine what CMHS actually is before assuming higher trust.
- `https://www.theoakislandcompendium.com/post/the-mystery-of-the-90-foot-stone-part-one` — appears to
  be a dedicated deep-dive treatment; unknown authorship/credentials this session, needs direct read.
- `https://github.com/lucatacconi/oak-island-stone-decryptor` — a hobbyist code repository ("PHP code
  made for fun"). **Not a primary or scholarly source** and must never be cited as if it were one, but it
  may encode a specific symbol sequence its author used as input, which is useful to compare *as a data
  point about which rendering circulates in amateur reproductions* — its own upstream source must be
  traced before its encoding is trusted for anything beyond that.
- A Zenodo record (`zenodo.org/records/19099017`) — already flagged in
  `logs/2026-09-23-sq1-followup-search-leads.md` as pseudo-academic with no apparent peer review; carried
  forward here as a source to explicitly exclude from candidacy, not to fetch and use.

## 4. New artifact flagged for the Historian's broader catalog (not previously tracked)

This session's search also surfaced a claim, not previously present in `knowledge-base/state.md` or
`config/sidequests.md`, that a **second, separate inscribed stone fragment was reportedly found at
Smith's Cove in the 1930s**, distinct from the 90-foot stone, with a symbol some sources describe as
resembling a Greek letter and interpreted by some as designating an "underwater door." This is
**WebSearch-summary sourcing only, wholly unverified**, and is flagged here as a candidate addition to
the Historian's "every other associated artifact" catalogue (`agents/historian.md`), not promoted
anywhere. If real and independently attested, it would matter to SQ-2 (a second, physically distinct
symbol source, not just a second *rendering* of the same lost stone) — but given this project's standing
rule against treating popularity or repetition as evidence, this needs a direct-fetch verification pass,
including checking whether it is itself a TV-show-era ("Smith's Cove excavations" have been a recurring
*Curse of Oak Island* storyline) claim before any trust-tier assignment.

## 5. Next steps

Whichever session next has confirmed working direct fetch (run
`procedures/direct-fetch-availability-check.md` first, per standing instruction):

1. Fetch each candidate source in §3, extract its rendering (if any) into the canonical encoding from
   §2.3, and commit each encoding plus a source checksum to `data/`.
2. Run the comparison procedure in §2.4 exactly as predeclared — do not adjust the 80%/0.20 threshold
   after seeing results.
3. Verify or retire the Smith's Cove second-fragment lead (§4) as a real, independently documented
   artifact or a TV-show-era/unverifiable claim.
4. Write the outcome — a selected most-credible transcription with disclosed uncertainty, *or* a
   "no reliable ground truth transcription" result — to `knowledge-base/state.md`, either of which is a
   complete, citable SQ-2 result per this project's own null-result-is-a-real-finding standard.
5. Do not begin SQ-3 until this SQ-2 execution is complete, per `config/sidequests.md`'s existing
   sequencing.
