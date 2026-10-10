# SQ-2 execution: candidate sweep against the frozen design

Executes `logs/2026-09-25-sq2-transcription-reconciliation-design.md`'s §5 next steps, now that direct
fetch has repeatedly proven available (SQ-4's 2026-10-06 Kempton-key check, the 2026-09-27 1857-letter
reads). Checks all 5 originally-catalogued candidate sources (the Zenodo record was already excluded
pre-emptively in the original design and is not re-checked).

## Candidate 1 — oakislandmystery.com/the-mystery/inscribed-stone

Both images on this page (`oak-island-90-foot-inscribed-stone.png`, "general" rendering, and
`oak-island-inscribed-stone-kempton-cipher.png`, captioned as Kempton's translation) were downloaded
directly and viewed at native resolution plus 3-5x crops/zooms (same workaround as SQ-4's prior Kempton-key
read, since WebFetch's text extraction cannot see image content).

**Finding, a disclosed correction to an earlier cycle's claim**: the two images show the **identical
symbol sequence**, position for position. The "Kempton cipher" image is the same glyph sequence as the
"general" image with Kempton's claimed English words ("FORTY FEET BELOW TWO / MILLION POUNDS ARE BURIED")
printed beneath each symbol group — it is not a second, differently-sourced rendering. This corrects
`logs/2026-09-23-sq1-provenance-audit.md` §4, which stated this page "presents at least two distinct
renderings of the symbols" — that earlier claim was based on the page's text/captions (two separately
labeled images exist) via WebFetch, which cannot see image content at all (confirmed again this cycle: a
WebFetch prompt against this same page returned "the text does not describe their symbols... I can't list
shapes, orientation, or positions for either one"). It was never a symbol-level comparison, and its own
disclosure said as much ("only two renderings were directly compared this session, both via one secondary
source's presentation of them side by side"). This cycle's finding is stronger-tier: a direct pixel-level
visual read of both downloaded images, position by position. The two images are not distinct in content —
this page is **one source, not two**, not the two-source situation the 2026-09-25 design session's
candidate catalog assumed when it listed this as "two renderings." Per this project's append-only
discipline, the original 2026-09-23 log is left unedited; this is the disclosed correction.

**Canonical encoding** (two lines, four word-groups each, left to right; `·` = single dot, `··` = the
page's own "two overlapping points" glyph, confirmed as one glyph, not two separate dot positions, by
cross-reference against Candidate 5's independent symbol vocabulary below):

- Line 1, word 1 (6 symbols): triangle-down, triangle-down-crossed (a small downward triangle with a
  vertical stroke through it), X, circle-crossed-diagonally, triangle-up, hook/arrow-down-left
- Line 1, word 2 (3 symbols): triangle-down, two-overlapping-points (``··``), triangle-up
- Line 1, word 3 (5 symbols): cross/dagger (†), two-overlapping-points, bracket/C-shape (open right),
  X, square
- Line 1, word 4 (3 symbols): triangle-up, square, X-with-small-dot
- Line 2, word 1 (7 symbols): double-cross (‡), two-overlapping-points, bracket/C-shape ×2,
  two-overlapping-points, apostrophe/tick, X
- Line 2, word 2 (5 symbols): circle-horizontally-crossed (Θ), tick, cross, X, square
- Line 2, word 3 (3 symbols): single-dot, circle-with-center-dot (ø), two-overlapping-points
- Line 2, word 4 (5 symbols): double-cross, circle-with-center-dot, two-overlapping-points,
  two-overlapping-points, tall-narrow-rectangle

**Source/checksum**: `https://www.oakislandmystery.com/images/content/oak-island-90-foot-inscribed-stone.png`,
retrieved 2026-10-10; page attributes the symbols as drawn "largely from the memory of an earlier viewer,"
with no tracings or rubbings of the original surviving — already SQ-1's own standing provenance caveat,
now directly confirmed from the page's own text rather than recalled from a prior cycle.

**Methodological note for the frozen §2.3 encoding scheme**: the closed primitive vocabulary (triangle,
cross, square, circle, arc, dot, line/dash, zigzag, other) undercounts this specific inscription's real
structure. Several positions are compound glyphs — a base shape plus an attached dot or multi-dot cluster
that functions as part of the glyph itself (confirmed independently by Candidate 5's own vocabulary, which
gives "two overlapping points" and "single dot" as their own named symbol types, and several other base
shapes their own dotted variants, e.g. "square with dots on the edges," "triangle with dots on the edges").
Encoding these as free-standing "dot" positions (as this project's original design implies) would silently
inflate the symbol count and invalidate any position-by-position comparison. This is disclosed here as a
real scoping gap in the frozen design, not corrected unilaterally — the design's own §2.4 threshold stays
exactly as predeclared; this note documents why any future execution needs a revised encoding scheme
(composite base+modifier glyphs, not primitives-only) before the comparison in §2.4 can run meaningfully
even if a second independent rendering is later found.

## Candidate 2 — thecurseofoakisland.com/research/cmhs-inscribed-90-foot-stone

**Excluded from candidacy.** Directly fetched: "CMHS" is the Chester Municipal Heritage Society; the page
names itself a compilation but gives no symbol-by-symbol rendering of its own, no citation for where any
transcription comes from (its own "Copy citation" field has only a title, no source), and states the
Kempton transcription "is itself contested" with "no contemporary verification." Its only image is
explicitly labeled an AI-assisted historical reconstruction, not a photograph or tracing. Per the original
design's own exclusion criterion (`§2.2` fabricated-after-the-fact / no real provenance chain), this source
contributes nothing checkable and is excluded.

## Candidate 3 — theoakislandcompendium.com/post/the-mystery-of-the-90-foot-stone-part-one

**No independent symbol rendering offered.** Directly fetched: this page gives no symbol-by-symbol
transcription of the 90-foot stone at all — only general period descriptions ("rudely cut letters, figures
or characters," Cooke 1864; "several characters," McCully 1862) and reported, non-symbol-level translation
disputes (see "New leads" below). Contributes no comparator encoding to SQ-2's own test.

## Candidate 4 — thecurseofoakisland.com/artifacts/inscribed-stone-90-foot-stone

**No independent symbol rendering offered.** Directly fetched: confirms "no photographs, rubbings, or
tracings of the original inscription survive." Names several alternate interpretive claims (Kempton 1949;
Wilhelm/Ronnstam 1971, a French decipherment of a claimed second hidden message referencing a 522-foot
shaft measurement; Pulitzer's claim the markings are Tifinagh characters; Bowdoin's 1909 account reporting
only the carved initials "L" and "N" as still visible) but shows no symbol sequence for any of them.
Contributes no comparator encoding.

## Candidate 5 — github.com/lucatacconi/oak-island-stone-decryptor

Fetched directly via the GitHub API and the raw source file (`decryptor_v01.php`, MIT-licensed, "PHP code
made for fun"). This is **not a transcription** in the sense SQ-2 needs — it's a brute-force English
dictionary-word solver keyed to inferred word-length groupings, not an ordered glyph-by-glyph rendering of
the stone. It does define its own 20-type symbol vocabulary by shape description in code comments (e.g.
"Triangle pointing down," "Triangle with downward pointing crossed out," "Two overlapping points," "Square
with dots on the edges"). **Cross-check**: this vocabulary's shape descriptions match, symbol-for-symbol,
the first six glyphs this project independently encoded from Candidate 1's image above (triangle-down,
triangle-down-crossed, X, circle-crossed, triangle-up, hook) — a real, if narrow, independent consistency
check that the single circulating rendering is read the same way by two unrelated parties, not evidence of
a second corroborating source (the repo doesn't cite its own upstream source, so this may itself derive
from the same oakislandmystery.com page, per the original design's own single-source-fanout caution).

## Result against the frozen §2.4 comparison

**The predeclared comparison cannot run.** Of the 5 originally-catalogued candidates, only one
(oakislandmystery.com) provides an actual symbol-by-symbol rendering, and its own two displayed images are
now confirmed to be the same single source, not two. The other three checked candidates (CMHS, Compendium,
curseofoakisland/artifacts) provide no rendering at all; the fifth (the GitHub repo) is a solver script
whose symbol vocabulary is consistent with, but not independently sourced from, Candidate 1's.

Per the frozen design's own predeclared rule (§2.4, point 3): **"where fewer than two independently
sourced non-derivative renderings can be identified at all, SQ-2's outcome is 'no reliable ground truth
transcription' — a complete, legitimate SQ-2 completion... not a failure to find one."** That condition is
now met across all originally-identified candidates. This is SQ-2's real, citable, negative-but-complete
result — not a stalled thread awaiting a fetch-capable session, since fetch capability has now been used on
every candidate.

## New leads surfaced, flagged but not pursued this cycle

- **A possibly distinct "Tory Stone"** with disputed markings: a 2018 CX laser scan was analyzed by Doug
  Crowell (compared to Elder Futhark runes) and by Dr. Lila Kopár (Catholic University; said not runic,
  "perhaps Gothic"); some geologists reportedly suspect the markings are natural, not carved. **Not yet
  disambiguated from the 90-foot stone** — may be the same "second Smith's Cove stone" lead already flagged
  in the 2026-09-25 design log's §4, or a third, separate artifact. A dedicated verification pass is needed
  before this is merged into either the Historian's catalog or SQ-2 itself.
- **A reported alternate translation**, per R.V. Harris, attributed to James Liechti (Professor of
  Languages, Dalhousie College): "Ten feet below two million pounds lie buried" — differing from Kempton's
  "forty feet" in the key numeral. This is an interpretation-level dispute (same underlying symbols, if
  any, differently read), relevant to SQ-3 if/when that sidequest proceeds, not a new SQ-2 rendering.
- **Wilhelm/Ronnstam (1971)**: a claimed second hidden message via a 16th-century cryptography manual,
  rendered in French, referencing a 522-foot shaft measurement. **Pulitzer**: claims the markings are
  Tifinagh characters. Neither offers a symbol sequence; both are interpretation-level claims for a future
  SQ-3/SQ-4 pass, not independently verified here.

## Honest sourcing tier

Candidate 1's encoding is a direct visual read of the primary image (strongest tier this project uses for
image content). Candidates 2-4's content is directly-fetched-tier for their own text. Candidate 5's PHP
source was directly read in full. No search-synthesis-only claim is relied upon in this sweep.
