# The 1857 Liverpool Transcript letter: found and read directly from the primary scan

**Trigger:** the standing open question about the reliability of the 1795/McGinnis discovery narrative
names the 1857 newspaper item as the earliest print source, but this project's own repeated attempts to
locate it in the primary archive scan (checking 6 and 13 August 1857 issues, in the "ALL SORTS OF
PARAGRAPHS" column) had both come back negative, leaving the thread paused pending a different strategy.

## Method

1. Searched for a published compilation or local-history source that might quote the item directly,
   per the state.md note's own suggested next approach. Found a compiled transcription document,
   "Early Oak Island Documents Part 1 of 3 – Early Newspaper Articles" (Les MacPhie's files, hosted on
   `oakislandmystery.com`), which gives full transcriptions of several early Liverpool Transcript letters,
   including two from correspondent "J.P. Forks" dated August 8 and August 15, 1857 — signed letters
   headed "FROM OUR REGULAR CORRESPONDENT, Chester."
2. This gave the missing piece: the letter appears under a **"Correspondence"** column header, not the
   "ALL SORTS OF PARAGRAPHS" miscellany column this project's prior checks had read. Same issue candidates
   as before (the letter's own internal dateline is August 8th; publication is expected a few days later,
   consistent with the already-confirmed archive issue dated 13 August 1857, ID=2940).
3. **Re-fetched the primary scan directly** (not the compiled document) — `archives.novascotia.ca`,
   issue ID=2940, **page 2** (image ID 201200738; the prior check only read page 3). Downloaded the full
   page image directly via `curl`, then cropped and progressively zoomed into the "Correspondence" column
   using local Python/Pillow image processing (the same close-reading technique used earlier this session
   for other primary-source images).
4. **Directly read** the letter text from the zoomed scan crops, position by position, confirming it
   matches the compiled transcription word for word, including the specific target passage.

## Result

**Confirmed at the strongest available tier** — this project's own direct visual read of the primary 1857
scan, not a secondary compilation or a WebSearch snippet. Exact quote, read directly from the scan:
"...postpone till my next on account of my excursion to Oak Island, where some very industrious
individuals have buried large sums in endeavouring to unbury larger ones supposed to have been deposited
by the renowned Capt. Kidd. They have sunk their money but have left the holes open." Full letter dateline:
"Chester, August 8th, 1857," signed "FORKS, J.P."

## Why the earlier check came back negative

The earlier check (`logs/2026-09-25-...` prior cycle notes) had correctly identified the right *issue*
(ID=2940, 13 August 1857) but read only page 3's "ALL SORTS OF PARAGRAPHS" column — a different, unrelated
section of the same newspaper issue. The letter itself is on page 2, under "Correspondence." This is a
useful methodological lesson, recorded honestly: a "negative" result for one column of a multi-column,
multi-page newspaper issue does not mean the whole issue has been ruled out — a full page-by-page,
column-by-column read (or, as it turned out here, a compiled secondary transcription pointing to the exact
location) is needed before treating an issue as exhausted.

## Follow-up letter also directly verified (same-cycle addendum)

The August 15, 1857 letter (the fuller description of the pits, whimsies, and excavation depths) has now
also been directly re-verified against its own primary scan page, closing the item originally left open
here. Following the same publication-date-lag pattern (a ~5-day gap between the letter's internal dateline
and its print date), the issue checked was `archives.novascotia.ca` ID=2941 (20 August 1857, Volume 4
Number 32), page 2 (image ID 201200742) — confirmed via a direct fetch of the issue page listing this
project made this same cycle. The "Correspondence" column there is headed "FROM OUR REGULAR CORRESPONDENT,
Chester, August 15th, 1857," and reads, word for word matching the compiled transcription: "my last I
spoke of Oak Island and the fruitless search for the treasures supposed to have been buried there by the
oft-heard-of Capt. Kyd... destination was Oak Island, and [we proceeded] and landed. Unlike the general
rule in such excursions, we found the reality [exceeded our] anticipations... Three pits of great depth
[are still open], though considerably filled with water." Both known 1857 letters are now confirmed
directly against their own primary archive scans — this thread is fully closed, not partially.

## What remains open

Nothing further from this specific thread. A broader systematic read of the rest of these two issues (for
any other Oak-Island-relevant content beyond the two Forks letters already found) has not been attempted
and is not judged necessary given the specific question this thread was opened to answer is now resolved.
