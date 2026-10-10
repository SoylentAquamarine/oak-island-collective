# SQ-2 execution: the frozen design's candidate sweep, now that fetch is confirmed working

**Trigger:** actively searching for an unclaimed thread this cycle rather than logging another "still
waiting on the user" no-op. The 2026-09-25 design session (`logs/2026-09-25-sq2-transcription-
reconciliation-design.md`) froze a comparison methodology and a 5-candidate source catalog specifically
for "whichever session next has confirmed working direct fetch" — and direct fetch has since been
demonstrated working repeatedly (SQ-4's 2026-10-06 Kempton-key check, the 2026-09-27 1857-letter direct
reads), so this design has been sitting ready-to-execute for two weeks without anyone actually running it.

## What's already known / not done yet

Already known: the frozen §2.3/§2.4 encoding and comparison rules, the 80%/0.20 predeclared threshold, and
the 5-candidate catalog (all unverified leads at design time). Not done: any candidate had actually been
fetched and encoded under this design.

## Design and why it's non-circular

Fetch each of the 5 candidates directly, extract whatever symbol rendering (if any) each provides into the
frozen encoding scheme, and apply the predeclared §2.4 rule exactly as written — including its own named
outcome for the case where fewer than two independent renderings exist. The threshold and outcome rule
were fixed before this session touched any candidate, so there's no opportunity to pick a result after
seeing the data.

## Honesty precommitment

Report exactly which candidates yielded a rendering and which didn't, and apply the predeclared outcome
rule even if it means concluding "no reliable ground truth transcription" rather than forcing a comparison
that can't actually run.

## Result

Full candidate-by-candidate detail in `data/sq2-transcription-candidate-sweep.md`. Summary: only one of
the 5 candidates (oakislandmystery.com) provides an actual symbol-by-symbol rendering, and its own two
displayed images — assumed to be two independent renderings by the original design session, which hadn't
been able to view them — are now confirmed by direct image inspection to be the **identical** symbol
sequence, not two sources. The other three content-bearing candidates provide no rendering at all; the
fifth (a GitHub hobbyist solver) defines its own symbol vocabulary that's consistent with, but not
independently sourced from, the one real rendering.

Per the frozen design's own predeclared §2.4 outcome rule, this is a complete SQ-2 result: **no reliable
ground truth transcription exists** — not because the candidates disagree, but because no second
independently-sourced, non-derivative rendering could be found among any of the originally-identified
candidates. One rendering exists, with the already-known "drawn largely from memory" provenance caveat
(confirmed again directly from the source page's own text this cycle), and nothing to corroborate or
contradict it.

A genuine methodological gap in the frozen design itself was also found and disclosed (not corrected
unilaterally): the closed primitive-only vocabulary in §2.3 doesn't account for this inscription's
composite dot-modified glyphs, confirmed by an independent source's own named vocabulary (the GitHub
repo's code comments). Any future comparison, if a second rendering is ever found, needs a revised
encoding scheme first.

Three new, unverified leads were surfaced and flagged for the Historian's catalog rather than pursued
further this cycle: a possibly-distinct "Tory Stone" with disputed runic/Gothic/natural-formation
readings, a reported alternate translation (Liechti, via Harris), and two more named alternate-decipherment
claims (Wilhelm/Ronnstam 1971; Pulitzer's Tifinagh claim) — all interpretation-level, relevant to SQ-3/
Historian work, not new SQ-2 renderings.

## Decision

Promoting this to `knowledge-base/state.md` as a Confirmed Finding: SQ-2's predeclared test has been
applied to its full original candidate set, and the honest result is "no reliable ground truth
transcription" — a complete, citable SQ-2 completion per this project's own null-result standard, not a
stalled thread. Per `config/sidequests.md`'s own stated sequencing rule ("do not begin SQ-3 until SQ-2 has
either selected a most-credible transcription or concluded that none is reliable enough to use"), this is
a real project-direction fact worth surfacing plainly to ChatGPT and the user rather than deciding
unilaterally how SQ-3 should now proceed (e.g., whether to use the single available rendering anyway with
disclosed uncertainty, or to treat SQ-3 as blocked) — flagged in this cycle's comms round as the next
actual coordination point for this project.
