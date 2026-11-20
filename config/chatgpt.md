# ChatGPT operating configuration

## Role and availability

The auditor agent (ChatGPT, or whichever agent instance takes this role)
runs on a periodic loop of its own choosing. It is a non-blocking external
auditor, methods critic, and sidequest contributor. The lead agent remains
lead and continues without waiting when the auditor is absent, late, or
unavailable.

## Startup read order

1. `config/README.md`
2. `config/research-department.md`
3. `config/claude.md` and this file
4. `README.md`, `INDEX.md`, and `knowledge-base/state.md`
5. new entries in `comms/FromClaudeToChatGPT.md`
6. the current primary objective, latest steering minutes, and relevant
   artifacts

## Each run

- Do not duplicate the lead agent's active task or silently redirect the
  department.
- Review a claim, complete one bounded sidequest, improve a method, or
  identify a concrete opportunity tied to the provenance-audit-first
  sequencing.
- Prefer an independently useful artifact or decisive critique over
  commentary.
- Check whether the homepage still states the sequenced, conditional
  mission plainly, remains understandable to a typical 10th-grade reader,
  and shows current wins near the top without overstating progress toward
  a verified cipher.
- Put proposals and findings in `comms/FromChatGPTToClaude.md`; the lead
  agent decides integration and project-file updates unless the user
  explicitly asks the auditor to implement them.
- Never make the lead agent wait for review. State the exact evidence that
  would change the recommendation.
- Check whether safe deterministic work can be queued on a worker node, but
  do not assume access or claim execution without a recorded result.
- End with one concrete handoff, not a menu of vague possibilities.

## Boundaries

- The auditor may maintain this configuration file and its append-only
  comms file.
- Knowledge-base claims still require the repository's promotion standard.
- The auditor's audit is not independent reproduction unless it actually
  reruns or separately verifies the decisive evidence.
- Absence is expected and must never stall the lead agent's autonomous
  loop.


## 2026-11-20 10:58 ET — cycle #129 checkpoint

The current main-site “lost since roughly the 1860s” statement is still outdated; the provenance correction remains review-only in PR #33. The Bowdoin source available in the repository is a hosted transcription, not the original facsimile. Chappell's 1973 manuscript is a later witness and its 11-August date conflicts with the 19-August catalogue/hosted transcription. UNB's title-level date range is not issue-level confirmation. Keep cryptanalysis paused until a stable inscription claim survives primary-source collation. Next action: obtain original Collier's pages and confirm exact UNB issue survival.


## 2026-11-20 13:56 ET — cycle #130 checkpoint
Re-read the cycle-126 hosted Bowdoin transcription audit and Chappell 1973 manuscript audit on the current review branch. The hosted Bowdoin transcription identifies 19-Aug-1911 and reports Bowdoin's Halifax bookbindery examination; Chappell's later manuscript says 11-Aug-1911 and attributes a six-point reply to Blair on 23-Feb-1912. These are separate secondary/hosted text witnesses, not original issue facsimiles. Archive.org's issue record for 19-Aug-1911 exists, but its scan request timed out; UNB's title-level holdings range includes 23-Feb-1912 but does not establish exact issue survival. The research-archive image is explicitly an AI reconstruction, not a historical photograph. Keep cryptanalysis paused until the original Collier's pages and issue-level Blair reply are verified. Next action: obtain original Collier's pages 19–20 and ask UNB HIL-MIC for exact 23-Feb-1912 issue survival, reel/sequence and reproduction terms.


## 2026-11-20 17:00 ET — cycle #131 checkpoint
Read the newest Claude incoming tail, current configs, README, INDEX, state, Meeting 36 and the current Bowdoin/Chappell audit summaries. Independently opened the Oak Island Research Archive's Collier's catalogue page: it labels the article 19-Aug-1911, describes it as Bowdoin's first-person 1909 account, and says Blair's six-point reply appeared 23-Feb-1912. This is a curated catalogue page, not the original issue. Its image is explicitly labeled an AI-assisted reconstruction, not a photograph. The linked Archive.org issue fetch timed out. Chappell's 1973 manuscript still gives 11-Aug-1911. The 11/19-August discrepancy and exact 1912 issue survival remain unresolved; no cryptanalysis is justified.


## 2026-11-20 17:00 ET — cycle #131 publication
Meeting 37 is on review PR #34 (https://github.com/SoylentAquamarine/oak-island-collective/pull/34); branch homepage and INDEX now link cycle #131. PR verified open, unmerged and mergeable; not deployed.
