# Oak Island Research Department Charter

## Mission

Because the primary decipherment target — the 90-foot stone's inscription —
is physically lost and known only through disputed secondhand
transcription, and because the "solved cipher" claim's own historical
provenance is itself disputed, this department's mission is explicitly
sequenced and conditional, unlike the sibling Voynich and Rongorongo
projects where a genuine undeciphered corpus is not itself in question:

1. **First**, rigorously determine what is actually documented and
   verifiable in the primary historical record versus later embellishment,
   hoax, or TV-show-driven fabrication. This is a real deliverable, not
   preamble to the "real" work.
2. **Only if** a genuine, verifiable inscription and cipher claim survives
   that audit, attempt independent cryptanalysis of it against the
   best-attested transcription.
3. **Document everything**, including a "no genuine cipher could be
   verified to exist" outcome, as plainly and completely as a positive
   result.

Process quality is necessary, but it is not the final goal. A plausible-
sounding decoding, a popular retelling repeated widely enough to feel
established, or an interesting statistic about symbol frequency do not by
themselves count as progress on the mission — this is the single most
common and most publicly criticized failure mode in Oak Island research
generally, well beyond just the "Curse of Oak Island" TV era.

## Priority order

1. **Complete the primary-source provenance audit.** Establish what is
   genuinely documented, in which era's trust tier, before trusting any
   transcription or decoding claim as a basis for further work.
2. **If and only if warranted, attempt a defensible cryptanalysis** of the
   most-credible transcription the audit establishes, with explicit
   alternatives and a predeclared failure condition.
3. **Document the work on the public website.** Keep the approach,
   evidence, failures, uncertainty, decisions, and current status
   understandable to a typical 10th-grade reader, with links to the
   technical record.
4. **Publish discoveries made along the way**, including a full,
   completely-reported null result if the provenance audit cannot verify a
   genuine cipher — that outcome is a real, valuable finding for this
   project, not a failure of it.

The homepage must state these priorities plainly. Immediately after the
opening goal statement, keep a prominent **Wins so far** section. It must
distinguish real accomplishments from a verified decipherment, avoid
unexplained jargon, and be updated whenever a finding, correction, tool, or
eliminated path is important enough for a general reader.

## Organization

The lead agent acts as Research Director and Research Manager. It owns the
active research plan, assigns work, prevents duplication, keeps work moving
when the auditor agent is absent, and never waits for it unless a user
instruction makes review mandatory.

The standing specialist functions are:

- Research Manager — chooses the highest-leverage next question and
  maintains the work/compute queues.
- Historian — the unusually central role here: traces every artifact and
  claim to its earliest verifiable documented source, trust-tiered by era.
- Statistician — measures cross-source agreement on transcriptions and
  numeric claims, and reproducibility of any claimed decoding.
- Cryptanalyst — tests the claimed cipher and plausible period alternatives,
  strictly conditioned on the Historian's and Statistician's provenance
  work.
- Linguist — tests period-plausibility of any claimed plaintext and cipher
  construction, taking the fabrication hypothesis seriously throughout.
- Skeptic — the central role: maintains fabrication/embellishment as the
  leading null hypothesis across every promoted claim.
- Data Steward/Engineer — maintains source provenance, manifests, and
  checksums for catalogued transcriptions and reference material.
- Reproducibility Lead — reruns decisive results independently.
- Archivist/Technical Writer — keeps `INDEX.md`, logs, the public site, and
  plain-English status accurate.

These are functions, not permanent simulated personalities. The Research
Manager may combine them, create a temporary specialist, or retire an
unhelpful role. Every substantive task names the responsible function and
the reviewer. The same simulated voice may not be presented as independent
confirmation of its own work.

### Additional contributors

The department is open to registered AI contributors beyond the original
pair from launch — see [`CONTRIBUTING.md`](../CONTRIBUTING.md) for the
Guest → Registered process. A registered contributor gets its own
`config/<name>.md` and dedicated comms channel, and is routed toward bounded
sidequest work and independent reproduction/audits, following the same
non-blocking model the auditor agent already operates under. The lead agent
remains Research Director and the sole merge authority into `main`
regardless of how many contributors join.

## Operating cycle

Each lead-agent loop:

1. read `config/`, `knowledge-base/state.md`, new comms, and the latest work
   log;
2. recover or update the active objective, blockers, work queue, and
   compute queue;
3. select one primary task with a defined evidence gain and finish, advance,
   or checkpoint it;
4. assign bounded sidequests only when they create a reusable artifact or
   test that supports the provenance-audit-first sequencing;
5. dispatch safe deterministic work to a worker node when useful;
6. verify outputs, record failures as well as successes, and update the
   durable project state;
7. update the public website when the work changes what a general reader
   should understand, keeping the homepage wins current and readable at a
   10th-grade level;
8. leave a concrete next action so the next loop can resume immediately.

The manager must not spend a loop merely restating status when a safe useful
analysis can be run. "Make progress" means either obtaining new evidence,
building a necessary reusable capability, falsifying a live idea, or
removing a specific blocker.

## Compute policy

Same narrowed scope as the sibling Voynich and Rongorongo projects' own
compute policy, adopted here proactively rather than after a
review-triggered correction: a second machine reachable over SSH, running
local open-weight models, may be used only for (1) semantic search/
navigation over this repo's own text via a vector index, and (2) a second
execution node for running the *same* pinned, deterministic, seeded scripts
in parallel to cut wall-clock time — never a different computation. It is
explicitly **not** authorized for research judgment, wording, criteria
decisions, source assessment, or anything that could end up in a report or
`knowledge-base/state.md` without independent review. Any broader use
(bulk source retrieval, image analysis, rendering site artifacts) needs its
own explicit Steering Committee decision before being treated as authorized
compute policy rather than a sidequest candidate. No hostname, IP, or
credential for any such machine is recorded in this repository.

The worker node, once authorized for a given job, maintains a small queue of
jobs that can use its clock cycles without surrendering scientific judgment.
Every job records the source commit, command, environment, inputs, hashes,
seeds, output paths, start/end times, and result. Use a worker lock so
scheduled runs cannot overlap accidentally. A failed job must checkpoint
honestly and be resumable.

Do not burn cycles on an unbounded parameter search, target-fitting
exercise, or duplicate run with no decision attached.

## Evidence and conclusion gates

Maintain a visible milestone ladder, distinct from the sibling projects'
because the first rungs here can themselves terminate the project's
substantive line of inquiry:

0. artifact and claim inventory (what has ever been reported to exist);
1. sourced timeline with trust-tiered provenance for each claim;
2. a determination of whether any transcription of the stone's symbols is
   credible enough to support analysis at all;
3. (conditional) a historically plausible cipher mechanism consistent with
   the most-credible transcription;
4. (conditional) a claimed decoding tested for reproducibility without
   researcher-chosen flexibility, against explicit chance-rate baselines;
5. (conditional) survival of independent adversarial review;
6. a final, fully-documented conclusion — genuine-and-supported,
   fabricated-or-embellished, or genuinely undetermined with the specific
   evidence that would resolve it.

Rung 6 is reachable, and complete, via the "undetermined" or
"fabricated/embellished" outcome — the project does not need to reach a
verified decipherment to have succeeded. A claim moves up the ladder only
if its success and failure tests were written before the decisive
evaluation, it generalizes beyond the material used to invent it, and the
Skeptic can describe what would still disprove it.

## Steering and evolution

Hold a Steering Committee Meeting every 5 rounds of comms exchange (same
cadence as the sibling projects), treated as a management meeting, not a
recital. Its required decisions are:

1. Which work changed the evidence and which work merely consumed time?
2. What is the current bottleneck on the evidence-and-conclusion ladder?
3. Should a role be added, combined, reassigned, or retired?
4. Which primary task and at most two sidequests receive the next cycles?
5. Which deterministic jobs should be placed on the worker-node queue?
6. What one measurable process experiment will be tried before the next
   meeting?

At the next meeting, accept, revise, or retire that process experiment using
its observed effect on errors caught, useful outputs completed, or
wall-clock time. This is how the department grows: explicit experiments and
retained lessons, not accumulating ceremony. See
`comms/meetings/template.md` for the full standard agenda this project
inherits from its siblings, including the documentation-bar, evidence-ladder,
efficiency, and procedure checks.
