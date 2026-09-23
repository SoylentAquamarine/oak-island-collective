# Falsification and Promotion Standard

This is the minimum bar for moving an interpretation into **Active
Hypotheses**. It is deliberately stricter than the bar for recording a
measurement in **Confirmed Findings**. A measurement can be reliable while
supporting several incompatible explanations.

## Minimum bar for Confirmed Findings

Confirmed Findings is a much lower bar than Active Hypotheses — a
measurement or result, not an interpretation, and it doesn't need
alternatives explicitly ruled out. But every entry should still be well
documented and reproducible, not left to habit. Before a PR adds a bullet
to `knowledge-base/state.md`'s Confirmed Findings, it should have:

- a script, a manifest, or a directly-read and cited document/image/text
  source that produced the number or claim — not a description of a
  result alone, with nothing behind it a reader could rerun or re-check;
- the actual output (a summary, a report, or both) committed to the repo,
  not only quoted or paraphrased inline in the bullet;
- enough provenance (source citation, publication date, retrieval method,
  checksum where applicable) that a third party could rerun or re-verify
  it and reasonably expect the same result;
- for anything resting on an external secondary source (a search-engine
  summary, a popular book or TV episode not read/watched directly, a
  paper not read directly), an explicit disclosure of that limitation in
  the same entry — never presented as if it were independently verified
  when it wasn't. This applies with particular force here: the vast
  majority of what is "commonly cited" about Oak Island in casual
  secondary sources is itself contested, imprecise, or of TV-show-era
  origin, so a claim's provenance chain and trust tier (per
  `agents/historian.md`) matter more than usual, and a claim's mere
  popularity is never evidence of its accuracy.

This does not require independent adversarial review the way Active
Hypotheses does — that remains the harder bar. It requires that a
Confirmed Finding always be *checkable*, even when no one has checked it
yet.

## Required hypothesis card

Before running its decisive test, the proponent must record:

1. **Claim** — one operational statement narrow enough to fail.
2. **Alternatives** — at least the strongest genuine-and-undocumented,
   embellished-in-retelling, and fabricated-after-the-fact explanations
   that fit the same observation, or a reason one family is inapplicable.
3. **Discriminating prediction** — an outcome expected under the claim and
   not equally expected under the named alternatives.
4. **Failure condition** — a specific provenance gap, transcription
   mismatch, or reproducibility failure that would count against the
   claim. This may not be invented after seeing the result.
5. **Units and controls** — the sources, transcriptions, eras/trust tiers,
   comparison baselines, exclusions, and randomization unit (where
   applicable).
6. **Dependencies** — transcription selection, era/trust-tier assignment,
   and any translation/interpretation assumptions that could manufacture
   the result.

## Evidence required for promotion

A candidate can enter **Active Hypotheses** only when all of the following
are present:

- a reproducible script or a cited, inspectable document/source protocol;
- an effect size and uncertainty or an equally explicit qualitative
  decision rule, not only an impression of plausibility;
- a negative or chance-rate control appropriate to the claim (particularly
  for any cryptanalytic result — see `agents/cryptanalyst.md`);
- sensitivity to at least the material transcription-selection and
  trust-tier confounds identified in the hypothesis card;
- a check against the comparative fabrication-benchmark panel (SQ-4) when
  the claim concerns genuineness vs. fabrication;
- independent adversarial review by the other collaborator, including
  reproduction of the headline result or a documented reason reproduction
  is impossible;
- a statement of what the result does **not** distinguish.

Promotion means "worth sustained scrutiny," not "probably true."
Confirmation requires surviving the Skeptic's targeted test and explaining
evidence that the strongest alternative does not explain equally well.

## Automatic stop conditions

Do not promote when any of these applies:

- the observation was selected after inspecting the same test set and has
  no holdout, or a transcription/symbol reading was chosen because it
  produced a more satisfying result;
- the effect disappears under one reasonable alternative transcription or
  source selection;
- the comparison changes source, era/trust tier, or claim scope at the
  same time as the claimed variable;
- the proposed cipher mechanism has enough unconstrained choices to fit
  arbitrary symbol sequences;
- the result only restates a claim's popularity or frequency of repetition
  without a genuine primary-source basis;
- an upstream correction has not been propagated through the full dependent
  analysis chain;
- the claim rests on a TV-show-era (2014–present) source being treated as
  equivalent in trust to a pre-1900 or early-20th-century documented
  source, without disclosing the tier difference — the specific,
  well-documented failure mode of casual Oak Island treatments.

## Current consequence

At launch, the repository has no Confirmed Findings and no Active
Hypotheses — this is a genuine bootstrap state, not a placeholder awaiting
cleanup. The first substantive work is the primary-source provenance audit
(`config/sidequests.md`, SQ-1), which is itself infrastructure, not a
finding, and which may itself produce this project's single most important
result: a documented answer to whether there is anything genuine left to
decipher at all.
