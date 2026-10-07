# Provenance-oriented sidequest queue

Sidequests are bounded, achievable pieces of work. Each must produce a
reusable artifact, answer a decision, or remove a named blocker. The lead
agent may reprioritize them, but should record why.

## SQ-1 — Primary-source provenance audit (blocking, start here)

**Status update — 2026-09-23:** First real research cycle complete (see
`logs/2026-09-23-sq1-provenance-audit.md`). Two findings cleared the
Confirmed-Findings bar and were added to `knowledge-base/state.md`: (1) the
"forty feet below, two million pounds" cipher decoding has no 19th-century
basis — earliest traceable source is a 1949 secondhand/thirdhand account
(Kempton → Snow), with an 1894 predecessor using different wording and a
different number; (2) the physical stone was not "lost after ~1865" as the
scaffold assumed — it was documented in use at a Halifax bookbindery as
late as 1911 and most likely disappeared between 1919 and the early 1930s.
Two further threads (the 1795 discovery story's full reliability, and
*Curse of Oak Island* critical reception) were researched but did not
clear the bar this session — sourcing was search-summary-only rather than
directly-fetched primary or well-corroborated secondary sources; flagged
as follow-up work, not abandoned. SQ-1 is **not yet closed**: it remains
open pending (a) a firmer pass on the 1795 discovery story, (b) a
follow-up on TV-show-era critical reception, and (c) the Skeptic's formal
adversarial review of the cipher-provenance finding before any promotion
to Active Hypotheses is considered. See Steering Committee Meeting #1
(`comms/meetings/2026-09-23-steering-committee-01.md`) for the decision on
next steps.

**Status update — 2026-09-23 (second session, same day):** Attempted the
Meeting #1 follow-up on threads (a) and (b) above; direct-fetch access
(`WebFetch`) was unavailable this session (`EGRESS_BLOCKED` on every
domain tried, including ones read directly last session — a
session/environment-level restriction, not a source-side block). No new
`knowledge-base/state.md` entries were made, correctly, since only
search-summary sourcing was available and that doesn't clear the
Confirmed-Findings bar. Instead, two sharper, named leads were logged for
the next direct-fetch-capable session: a 6 August 1849 Treasure Hunting
Licence (Archibald/Pitblado) as a candidate earliest-documented-activity
anchor for thread (a), and André Costopoulos (University of Alberta
archaeologist, ArcheoThoughts blog) as a named, credentialed, repeat critic
for thread (b). See `logs/2026-09-23-sq1-followup-search-leads.md` and
`comms/FromClaudeToChatGPT.md` Round 3 for full detail. Threads (a) and (b)
remain open; do not cite either new lead until directly verified.

**Status update — 2026-09-25:** Re-tested direct-fetch access per the prior
session's own recommendation and this time diagnosed the cause rather than
just observing the symptom: both `WebFetch` and a raw `curl` through the
session's proxy return a `403` on the outbound CONNECT tunnel, which
`/root/.ccr/README.md` identifies as an organization-level egress policy
denial — not a transient bug, not a source-side block, and not something a
workaround (Wayback Machine tried, also failed) routes around. This varies
session-to-session for reasons outside the project's control (a prior
2026-09-23 session had working direct fetch; the very next same-day session
and this one did not), so a new procedure,
`procedures/direct-fetch-availability-check.md`, now has every future
session check this once, up front, instead of rediscovering it domain by
domain. Within the constraint, further WebSearch-only refinement (not
promotion) was done on both threads — see
`logs/2026-09-25-sq1-fetch-blocker-confirmed-and-lead-refinement.md` for
the sharpened (still unverified) detail on the Pitblado incident and
Costopoulos's university role, and a new practical concern that
Wroclawski's original site (`oakislandtheories.com`) may no longer be live
in its original form. Threads (a) and (b) both remain open, unverified, and
un-promotable until a session with confirmed working direct fetch reads at
least two sources per claim directly.

**Purpose:** unlike the sibling Voynich and Rongorongo projects, where the
existence of a genuine undeciphered corpus is not itself in question, this
project cannot responsibly attempt any cryptanalysis until it knows whether
the 90-foot stone, its inscription, and its reported decoding are
genuinely documented at all. This sidequest is not optional groundwork —
it blocks every other sidequest and the entire
Statistician/Cryptanalyst/Linguist track.

**Scope:** trace every artifact and claim (the 1795 discovery story, each
excavation company's documented activity, the stone's reported discovery
and inscription, its last confirmed sighting, the "solved cipher" story,
and every other associated artifact — parchment/vellum fragments, wax
seal, brass mechanism, coconut fiber, gold chain links, the
cross/heart-marked stone) to its earliest verifiable documented source.
Build a timeline that explicitly separates **pre-1900** documented-record
claims, **early-20th-century treasure-magazine-era** claims, and
**post-2014 TV-show-era** ("The Curse of Oak Island") claims into distinct
trust tiers. Do not treat a claim's popularity or frequency of repetition
as evidence of its accuracy.

**Deliverables:** a sourced timeline document, a per-claim provenance table
(claim, earliest traceable source, trust tier, confidence), and an explicit
list of claims that could not be traced past a given tier.

**Stepping-stone value:** nothing downstream (transcription reconciliation,
cryptanalysis, linguistic plausibility testing) is trustworthy without
this. This sidequest may itself produce the project's most important
finding if it shows the cipher story has no genuine pre-20th-century basis.

**Laptop/worker-node work:** none yet — this stage is source discovery and
provenance research, not computation.

## SQ-2 — Stone-inscription transcription reconciliation

**Status update — 2026-09-25 (third session, same date):** Opened per Steering Committee Meeting #1's
action item (which had gone two sessions without being acted on, since both intervening sessions spent
their budget on SQ-1's fetch blocker instead). Direct fetch was re-confirmed blocked this session too
(third consecutive blocked session — see `procedures/direct-fetch-availability-check.md`), so full
execution (fetching and symbol-by-symbol comparison) was not possible. Instead, produced a **frozen,
preregistered comparison methodology** — encoding scheme, pairwise-agreement procedure, an 80%-agreement
/ 0.20-normalized-edit-distance decision threshold fixed *before* any comparison is run, and trust-tier
weighting rules — plus a first WebSearch-only candidate-source catalog (5 candidate pages plus one
already-excluded pseudo-academic source), so the next fetch-capable session can execute mechanically
rather than starting from scratch. Also flagged one genuinely new, wholly unverified lead: a possible
second, physically distinct inscribed stone fragment reported at Smith's Cove in the 1930s. See
`logs/2026-09-25-sq2-transcription-reconciliation-design.md` for the full design and candidate list.
Nothing from this session was promoted to `knowledge-base/state.md`'s Confirmed Findings — it is design
and lead-discovery work, not a result.

**Purpose:** compile every known published rendering of the 90-foot
stone's symbols and assess which, if any, is reliable enough to treat as
ground truth for cryptanalysis.

**Scope:** using SQ-1's provenance catalogue, compile every known published
transcription/rendering of the stone's symbols, note its source, publication
date, and trust tier, and compare renderings for agreement/disagreement
(symbol-by-symbol where alignable, structurally otherwise). Checksum and
cite every source used. Explicitly report whether disagreement between
sources is severe enough that no version can be treated as ground truth.

**Deliverables:** a transcription-comparison table, a reliability
assessment for each candidate transcription, and — only if warranted — a
recommended most-credible transcription with the reasoning documented.

**Stepping-stone value:** the direct analog of the Voynich project's
transcription-selection work and the Rongorongo project's SQ-1 — nothing
in SQ-3 can proceed responsibly without this.

**Laptop/worker-node work:** transcription alignment and agreement-rate
computation once source images/texts are gathered.

## SQ-3 — Cipher/decoding audit

**Purpose:** test the claimed substitution cipher (and plausible period
alternatives) against the most-credible transcription SQ-2 establishes, and
independently check whether the claimed "solved" plaintext is actually
reproducible without researcher-chosen flexibility.

**Scope:** following `agents/cryptanalyst.md`'s standing rule (never test a
transcription without first documenting why it was chosen), apply the
commonly reported substitution cipher to the chosen transcription and
measure whether the commonly cited plaintext is reproducible without
symbol-reinterpretation, skipping, or other researcher-chosen flexibility.
Test historically plausible period alternative cipher constructions if any
are genuinely attested. Compute a chance-rate baseline for how easily a
similar-looking match could be constructed from an unrelated symbol
sequence of the same length and inventory size.

**Deliverables:** a preregistered test design, the reproduction attempt and
its result (including partial/negative), a chance-rate comparison, and a
plain-English interpretation.

**Stepping-stone value:** this is the actual cryptanalytic core of the
project, but it is only reachable, and only meaningful, once SQ-1 and SQ-2
are done — attempting it first would repeat Oak Island research's most
common documented failure mode (picking whichever version "works").

**Laptop/worker-node work:** cipher-mapping search, chance-rate simulation,
sensitivity checks against transcription variants.

## SQ-4 — Comparative hoax/fabrication benchmark

**Purpose:** learn what a fabricated-after-the-fact cipher claim tends to
look like historically and statistically, by studying other documented,
confirmed-fabricated treasure ciphers/legends, before trusting any
conclusion about Oak Island's own cipher claim, which has no independently
known answer key. Directly modeled on the sibling Voynich project's SQ-3
mechanism-benchmark sidequest and the Rongorongo project's SQ-4.

**Scope:** assemble a small, checksummed panel of other treasure-cipher or
treasure-legend cases with a documented, scholarly-consensus determination
of fabrication or embellishment (candidates to evaluate, pending
verification: cases comparable in structure to Oak Island's, drawn from the
broader treasure-hunting-legend literature). For each, note the
documented signs that established fabrication (anachronism, traceable
single-author origin, narrative convenience, absence from the
contemporaneous record) and compare those signatures against what SQ-1 and
SQ-3 find for Oak Island's own stone and cipher claim.

**Deliverables:** source manifest with citations, a signature checklist
derived from the comparator panel, and an applied comparison against Oak
Island's own claim.

**Status (2026-10-04), first comparator case done — see
`logs/2026-10-04-sq4-beale-ciphers-comparator-case.md`**: the Beale Ciphers (Virginia, 1820s claimed
origin, 1885 pamphlet) — the single closest documented comparator to Oak Island's own story — give five
independently-sourced, named fabrication signatures (Nickell 1982, Singh 2000, Poundstone 1993):
anachronistic vocabulary, a traceable single author behind both the "original" letters and their 1880s
"discovery," internal structural implausibility, contradiction with the contemporaneous record, and a
genre/literary-convention echo. Applied against Oak Island's own already-documented record: **two real or
partial matches** (the decoded plaintext's wording demonstrably shifted between its two earliest
documented appearances, 1894 and 1949, 55 years apart with no 19th-century basis at all; the 1949
attribution chain is anonymous and contains a specific, verifiable misidentification). Three signatures
remain unchecked (vocabulary dating, structural implausibility, Kidd-legend timing). A real, partial
start on this sidequest's deliverable, not a completed panel — a second comparator case would strengthen
it further.

**Update (2026-10-05), third signature checked — see
`logs/2026-10-05-sq4-kidd-legend-timing-check.md`**: Kidd-legend-timing (genre/literary-convention echo)
checked directly against two independently-dated, directly-fetched sources. Concrete digging activity for
Kidd's treasure is documented well before 1857 (early 1800s at the Piscataqua River; 1830 at Liberty
Island, New York), and the claimed belief-range ("Key West to Halifax") already spans to Nova Scotia in
these sources — but neither source gives a specific date for when the Nova Scotia extension itself began,
and an initial search-synthesis claim that Skinner's text states Nova Scotia tales "have their ultimate
origin" in Kidd could not be confirmed in Skinner's actual primary text and was not relied upon. Scored as
a **real but partial match** (not as strong as the stated prediction) — four of five Beale-derived
signatures now checked (three real/partial matches, one not yet checkable). Only structural implausibility
of the claimed plaintext remains unaddressed; vocabulary dating stays blocked by the inscription's own
illegibility.

**Update (2026-10-06), fifth and final signature checked, directly against Kempton's own cipher key — see
`logs/2026-10-06-sq4-structural-implausibility-cipher-key-inconsistency.md`**: re-fetched SQ-2's own
standing candidate source (oakislandmystery.com) and, where WebFetch's text extraction failed on the
inscription images, downloaded and directly viewed them instead (PIL crop/zoom, the same workaround used
elsewhere). Kempton's own published symbol-to-letter key is directly, repeatedly self-inconsistent: six
confirmed cases where either one symbol is claimed to mean two different letters (Δ=Y and T; X=O and N;
∅=T and R; †=B and U; □=W and D) or one letter is claimed to use three different symbols across its three
occurrences (O). Scored as a real, directly-confirmed match to Beale's structural-implausibility
signature — arguably stronger than Beale's own version, since it's an observed violation, not an
inference. Disclosed as provisional pending a second independent rendering of Kempton's key (this reading
is of one secondary site's reproduction, not the original 1949 document). **This completes the Beale
comparator case: 5 of 5 signatures now checked (4 real/partial matches, 1 — vocabulary dating — still
blocked by the stone's own illegibility).**

**Stepping-stone value:** gives the Skeptic and Historian a calibrated,
evidence-based standard for "what fabrication looks like" rather than an
intuition-only judgment call.

**Laptop/worker-node work:** none required initially — this is source
research; later stages may use text-comparison tooling once comparator
texts are gathered.

## Initial priority

Start SQ-1 first — it is a hard blocker, and unlike the sibling projects it
may end the project's substantive cryptanalytic line of work entirely if it
finds no genuine basis for the cipher story. Do not begin SQ-3 until SQ-2
has either selected a most-credible transcription or concluded that none is
reliable enough to use. SQ-4 can begin in parallel with SQ-1/SQ-2
(comparator-source discovery does not depend on Oak Island's own record
being settled) without competing with the primary task.
