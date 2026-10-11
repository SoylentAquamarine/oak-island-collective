# SQ-4: the Kempton spelling-consistency check — found infeasible, not abandoned without reason

## Precommitment self-review (written before concluding, after exploratory sourcing)

**Known:** the Dare Stones comparator (2026-10-10) surfaced a concrete, not-yet-attempted idea:
an "unnaturally consistent spelling" test on Kempton's own 1949 cipher key text, modeled on
Sparkes's 1941 method of catching the Dare Stones forger by spotting spelling/style that was
too modern and too internally consistent for a genuine period document. This lead has sat open
in `config/sidequests.md` and `comms/FromClaudeToChatGPT.md` since that cycle.

**Not done yet:** nobody had checked whether the source material this test needs actually
exists in a usable (text, not image) form, or whether it's long enough for the test to mean
anything.

**Design and why it's non-circular:** before running any comparison, first verify the two
preconditions the test depends on — (a) a machine-readable text of the key/translation exists,
and (b) that text is long enough for a spelling-pattern analysis to be statistically meaningful
at all (the Dare Stones case had full multi-sentence forged inscriptions; a single short
sentence would not support the same kind of analysis). This is scoping work, not the test
itself — reporting "infeasible, here's why" honestly is a legitimate outcome per this project's
own standing policy on disclosed, genuine no-ops.

**Honesty precommitment:** report the actual outcome (feasible / infeasible / partially
feasible) without forcing a conclusion either way about Kempton's own reliability.

## Findings

**Precondition (a) — fails.** Directly fetched `criticalenquiry.org/oakisland/kempton.shtml`,
the most specific source on Kempton found in this project's prior research. It embeds Kempton's
rendering of the cipher symbols only as an image (`images/kempton.jpg`); the page's own text
never transcribes the symbol-to-letter key. No machine-readable version of the key itself was
located this pass.

**Precondition (b) — fails independently, even granting a transcription.** The claimed
*decoded* plaintext — the actual target a "spelling consistency" check would examine — is a
single short sentence. Multiple sources give **two different, competing readings**: the
commonly repeated modern version, "forty feet below two million pounds are buried" (first
appearing in print in Snow's 1949 book, sourced to Kempton), versus the earlier historical
readings — an 1862 letter by treasure hunter Jotham McCully ("ten feet below are two million
pounds buried") and a 1909 newspaper account ("ten feet below, 2,000,000 pounds lie buried").
Every version is 7-9 words. This is categorically different from the Dare Stones case, where
Sparkes had full, multi-sentence forged inscriptions to analyze for internal spelling patterns.
A 7-9 word sample does not support any meaningful spelling-consistency analysis regardless of
transcription access.

## Outcome

**This specific test is infeasible, for two independent reasons, and is closed out as such
rather than left open indefinitely.** This is a real, substantive finding — not a non-result —
because it (1) explains concretely why this comparator-derived lead cannot be completed the way
it was originally envisioned, and (2) surfaces a new, previously undocumented fact in this
project's own record: **the "forty feet" reading is not the only historical version** — the two
earliest documented readings (1862, 1909) both say "ten feet," not "forty feet," which is itself
a relevant data point about the claim's instability over time, independent of the Kempton/Snow
1949 episode already documented.

## Limitation disclosed

This pass did not attempt to locate the Kempton typescript's full text (beyond the symbol
image) through an archival request — Nova Scotia Archives item numbers for Kempton/Blair
correspondence were already recorded in a prior cycle's log and remain a possible future lead
if the user wants to pursue archival access, which is outside this project's research-only
scope to initiate unilaterally.
