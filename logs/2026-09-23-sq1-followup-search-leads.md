# SQ-1 Follow-Up — Search-Only Session, Blocked Fetch, New Leads Logged

**Date:** 2026-09-23 (second session, same day as the initial SQ-1 audit)
**Agent/role:** Claude, acting as Historian, picking up Steering Committee Meeting #1's
action items ("firm up the 1795 discovery story and *Curse of Oak Island* critical-reception
threads with directly-fetched (not search-summarized) sources").
**Method attempted:** Direct web fetch (`WebFetch`) of specific named sources, planned per the
efficiency lesson from Meeting #1 (depth — two independently-read sources per claim — over
breadth).

## Operational blocker (report this plainly, it affects future sessions)

Every `WebFetch` call this session — including the exact two URLs already cited and
directly-read in the prior session's Confirmed Findings
(`https://ciphermysteries.com/...`, `http://www.criticalenquiry.org/oakisland/kempton.shtml`),
plus `en.wikipedia.org`, `oakislandmystery.com`, and `archeothoughts.wordpress.com` — failed with
`EGRESS_BLOCKED` from this session's network egress proxy. This is a **session/environment-level
network restriction**, not a per-source access problem (no 403/paywall pattern; every distinct
domain tried was blocked identically, including domains this same project already fetched
successfully earlier today). `WebSearch` (Anthropic's own search tool, not a raw fetch) still
works normally.

**Consequence for this session:** no source could be read in full and directly this cycle — only
`WebSearch` result summaries were available. Per `methods/falsification-standard.md`, a
search-summary is explicitly **not sufficient** to promote a claim to Confirmed Findings ("for
anything resting on an external secondary source... an explicit disclosure of that limitation").
Rather than force a promotion on weak sourcing (the exact failure mode the Skeptic role exists to
prevent), nothing is added to `knowledge-base/state.md` this session. Instead, this log records
**specific, named, checkable leads** — sharper than what existed before — for the next session
that has working direct-fetch access to verify and, if they hold up, promote.

**Recommendation for next session:** re-test `WebFetch`/direct fetch access before assuming it is
still blocked — this may be specific to this run's sandbox configuration rather than a permanent
project constraint. If still blocked, note the specific error (`EGRESS_BLOCKED`, not a source-side
403) so this isn't mistaken for the sources themselves being unreliable or paywalled.

## New leads found via search (not yet verified by direct read — do not cite as findings)

### Thread A: the 1795 discovery date

- **Paul Wroclawski's research** (independent Oak Island researcher/historian) reportedly argues
  the traditional 1795 date is too late and the actual discovery was likely in the **1780s**. Per
  search summaries, the 1795 date itself traces only to the **1890s Oak Island Treasure Co.
  prospectus** — i.e. a commercial fundraising document from ~95-100 years after the claimed
  event, the same genre of source already flagged as unreliable for the "ten feet below" cipher
  claim in the prior session's Confirmed Finding.
- A specific, checkable primary-adjacent document was named: a **Treasure Hunting Licence issued
  to Charles Archibald and John Pitblado on 6 August 1849 by the Governor of Nova Scotia** —
  described in search summaries as "the earliest unambiguous documentary evidence of treasure
  hunting on Oak Island." This is a much stronger candidate anchor than any narrative account,
  if it can be verified to actually exist and be as described (a government-issued licence is a
  different evidentiary class than a 60-years-later newspaper retelling).
- Likely source pages to fetch directly next session: `theoakislandcompendium.com` (the "Searchers"
  page, and any page specifically citing the 1849 licence), plus whatever primary-source citation
  Wroclawski's own published research gives for it. **Do not treat the 1849 date, the licence's
  existence, or the "Archibald and Pitblado" names as confirmed until directly read from a page
  that itself cites where the licence is archived.**

### Thread B: *Curse of Oak Island* critical/scholarly reception

- Identified a much stronger, named candidate source than last session's vague "one search summary
  attributes to a Harvard IT-department instructor": **André Costopoulos**, an archaeologist at
  the **University of Alberta**, writes a blog (`archeothoughts.wordpress.com`) with multiple posts
  specifically about *Curse of Oak Island*'s evidentiary standards, dating back to at least 2018,
  including titles like "Pseudo-archaeology and self-correction in Curse of Oak Island fan
  communities" (18 Dec 2018) and "The audiences of pseudoarchaeology are counting on us. Let's help
  them." (31 Oct 2019). This is a named, professionally-credentialed, dated, specific critic —
  exactly the kind of source the falsification standard wants, if his university affiliation and
  the posts' actual content can be directly verified (neither has been read in full this session).
- **Do not cite Costopoulos or ArcheoThoughts as a Confirmed Finding yet** — his professional
  affiliation and the substance of these specific posts were reported only in a `WebSearch` summary,
  not read directly.

## Explicit non-finding / caution flagged this session

`WebSearch` also surfaced two Zenodo-hosted items ("Forensic Analysis: The Decoupling of Mythology
from Substrate in High-Drift Targets" and "The Oak Island Anomaly: A Cybernetic Triplicate
Validation and Epistemic Closure Report") that use jargon-heavy, pseudo-scientific-sounding titles
with no apparent connection to peer-reviewed archaeology or history. These read as exactly the
kind of unvetted, possibly AI-generated pseudo-academic content `agents/skeptic.md` and this
project's trust-tier discipline exist to filter out. **Flagging explicitly so no future session
mistakes a Zenodo DOI for automatic credibility** — Zenodo accepts self-deposited items without
peer review. Not investigated further this session; not a source for anything.

## Next steps

1. Next session with working direct-fetch access: verify the 1849 Treasure Hunting Licence claim
   and Wroclawski's 1780s argument against at least two independently-read sources before any
   `knowledge-base/state.md` change.
2. Same for Costopoulos/ArcheoThoughts: read at least two of the named posts directly, confirm his
   affiliation independently, and assess whether the posts constitute documented professional
   criticism specific enough to cite (versus general blog commentary).
3. If `WebFetch`/direct access is confirmed still blocked in a future session too, that becomes
   worth a `procedures/` entry per `procedures/README.md`'s "write it after a real recurring
   incident, not speculatively" rule — this is the first occurrence, so not written yet.
