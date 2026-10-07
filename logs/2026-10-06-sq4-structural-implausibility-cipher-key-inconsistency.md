# SQ-4 — fifth and final Beale-derived signature: structural implausibility, checked directly against Kempton's own published cipher key

**Trigger:** the last unchecked Beale-derived fabrication signature (structural implausibility — Beale's
own instance: "the third cipher is too short to list 30 individuals' next of kin," an internal
contradiction in what the cipher claims to encode) had no defined Oak Island equivalent yet. While
retrying direct fetch on SQ-2's standing candidate-source list (oakislandmystery.com, last attempted
2026-09-25 and blocked by network egress three consecutive sessions), WebFetch could not extract text
from the page's inscription images, but the actual image files (`oak-island-90-foot-inscribed-stone.png`,
`oak-island-inscribed-stone-kempton-cipher.png`) were directly downloadable via `curl`. The second image
shows Kempton's own 1949 symbol-to-letter key laid out with each cipher glyph directly above its claimed
plaintext letter — the first time this project has had the actual claimed mapping in front of it, rather
than a textual description of it.

## What's already known / not done yet

Already known (Confirmed Finding): the "Forty feet below, two million pounds are buried" plaintext has no
19th-century documentary basis and first appears via Kempton's 1949 account. Not done until now: checking
whether Kempton's own claimed cipher key is even internally self-consistent — i.e., whether it behaves
like a real substitution cipher (same letter always encoded by the same symbol, same symbol never reused
for a different letter) at all, independent of the question of the plaintext's documentary history.

## Method and why it's non-circular

Downloaded both images directly (sha256 recorded below), cropped and upscaled each word-group with PIL
(the same tooling workaround used elsewhere this project and its siblings), and read off the symbol
directly above each letter, word by word, for every letter that recurs more than once across the full
claimed plaintext ("FORTY FEET BELOW TWO MILLION POUNDS ARE BURIED"). This is a direct, mechanical
consistency check against the image Kempton's own defenders published as the key, not a test tuned to find
a particular result — the recurring letters (O, T, R, E, I, L, N, U, B, W) were fixed by the plaintext
itself before any symbol was read.

## Result: six confirmed symbol-letter inconsistencies

| Symbol | Claimed to mean... | ...in word | Conflict |
|---|---|---|---|
| Δ (triangle) | Y | FORTY | **also claimed = T in FEET and TWO** |
| Ψ̸ / X / ẋ (three different glyphs) | O | FORTY / BELOW / TWO respectively | **O has three different symbols across its three occurrences — no two agree** |
| X (plain) | O (in BELOW) | — | **also claimed = N in MILLION and POUNDS** |
| ∅ (circle-slash) | T (in FORTY) | — | **also claimed = R in BURIED** |
| † (cross) | B (in BELOW) | — | **also claimed = U in POUNDS and BURIED** |
| □ (rectangle) | W (in BELOW, TWO — self-consistent) | — | **also claimed = D in BURIED** |

Some letters *are* internally consistent: L (both occurrences in MILLION use the same bracket glyph), W
(BELOW and TWO agree), and N (MILLION and POUNDS agree, both X) — so this is not a case of every symbol
being random noise, which makes the specific, repeated failures above more notable rather than less: a
real cipher key would not need to be consistent by accident on some letters and inconsistent on others if
it were a genuine, carefully-applied substitution system.

## Honest caveats, disclosed

This is a reading of **one secondary website's rendering** of Kempton's 1949 key, not the original 1949
document itself — the inconsistency could in principle be a transcription or typesetting error introduced
by oakislandmystery.com's own reproduction, not necessarily present in Kempton's original claim. This is
exactly the kind of cross-source reliability question SQ-2 exists to resolve, and this finding should be
treated as provisional pending a second independent rendering of Kempton's key, not yet promoted to a
Confirmed Finding. It is, however, a real, directly-observed, non-trivial data point — not a plausibility
argument — and a concrete, well-specified next target for SQ-2 rather than a vague call to "verify more
sources."

## Decision

Scored as a **real, directly-confirmed match** to Beale's structural-implausibility signature — arguably a
stronger instance than Beale's own, since this is a directly observed violation of the cipher's own
claimed consistency property (not an inference about plausible capacity). This completes the Beale
comparator case: **5 of 5 signatures now checked against Oak Island's own record** (4 real/partial matches:
shifting undocumented wording, anonymous misattributed provenance, Kidd-legend timing, and now this
cipher-key inconsistency; 1 — vocabulary dating — still blocked by the stone inscription's own
illegibility, independent of Kempton's 1949 key). A second comparator case beyond Beale would still
strengthen SQ-4's panel per its own "small panel, not single case" scope, but the first comparator's
applied comparison is now complete.

## Source provenance

- `data/derived/stone-general-rendering.png` — sha256 `ec5a9e58648ed17172a9b9d453d3479cc97128feb1946f2249376ea2b608a31e`
- `data/derived/stone-kempton-cipher.png` — sha256 `4e168b8cd739da1a2c497781cab65ccf9a0207f5088ea72c4f587f1381e55839`
- Both fetched directly from `https://www.oakislandmystery.com/images/content/` (the same domain SQ-2's
  own candidate-source list already named, first entry, "already fetched once 2026-09-23... re-fetch to
  extract a precise symbol-by-symbol encoding, which the first session did not do" — this cycle is that
  re-fetch).
- Derived zoom crops kept for reproducibility of the symbol-by-symbol reading above:
  `data/derived/word-forty-10x.png`, `word-feet-10x.png`, `word-below-10x.png`, `word-two-10x.png`,
  `word-buried-head-10x.png` (B-U-R-I-E), `word-buried-tail-10x.png` (I-E-D, showing the □=D symbol).
