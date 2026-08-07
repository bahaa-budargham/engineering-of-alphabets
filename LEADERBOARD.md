# EOA-43 Open Problems — Leaderboard

This is the running list of submissions to the three open questions in the EOA-43 program. The questions and the evaluation framework are defined in the companion paper (EOA-Recurrence, Section 6). The operator that generates the basis sequences is **not** required to be reproduced; the closed-form explanation, the cross-encoding mapping, and the inverse-design method are all candidates for submission.

**How to submit:** Open a GitHub issue with the tag `[EOA-43-open]`, or email `bdarghamneurolabs@gmail.com` with subject `[EOA-43] <question-id>: <short title>`. Submissions are reviewed under the collaboration framework described in EOA-43, Section 2, and are evaluated by the author or an independent reviewer agreed by both parties.

**How "correct, reproducible" is judged:**
- The answer must be **self-contained** — a paper, a preprint, a code repository, or a self-contained proof document.
- It must **reproduce the published empirical result** it claims to explain (the 43-term sequences, the 5 measured LCRs, or the consistency requirement), using only the public basis vectors and the operator's public outputs.
- It must be **public** (arXiv, journal, or open repository). Private disclosures do not qualify.
- A reasonable replication attempt by a third party must reach the same conclusion within 90 days of submission. Disputes are mediated by an independent reviewer agreed by both parties.

---

## Question 1 — Stability within a fixed encoding

**Statement.** Why does the ratio of consecutive terms in the 43-term sequences stabilize to a single value (≈ 3.17 for English IPA) within a fixed encoding, across all 26 letter names, all words, all control inputs (random symbols, number words), and all subsequences after term 30?

**Status:** open. No submission to date.

| # | Date | Author | Link | Status |
|---|---|---|---|---|
| — | — | — | — | open |

---

## Question 2 — Cross-encoding mapping

**Statement.** The LCR varies from 2.710 (Hebrew IPA) to 4.128 (Greek IPA) — a 1.5× spread — depending only on the encoding of letter names. What *property* of an encoding determines its LCR? Seven candidate hypotheses (H1–H7) are listed in the companion paper (Section 5); none is currently excluded by data.

**Status:** open. The empirical mapping is public. The functional form is not.

| # | Date | Author | Link | Status |
|---|---|---|---|---|
| — | — | — | — | open |

---

## Question 3 — Inverse design

**Statement.** Given a target LCR λ*, can one construct an encoding (a mapping letter → name string) that achieves it? The forward direction is empirical; the inverse is an open problem.

**Status:** open. Construction algorithms, impossibility proofs, and constructive counterexamples are all accepted submissions.

| # | Date | Author | Link | Status |
|---|---|---|---|---|
| — | — | — | — | open |

---

## Status codes

- **open** — no submission yet, or all submissions so far have been withdrawn / not reproducible.
- **under review** — submission received, awaiting reproducibility check (max 90 days).
- **accepted** — reproducibility confirmed by independent reviewer; the result is integrated into the EOA framework.
- **withdrawn** — author withdrew the submission.
- **superseded** — replaced by a later submission by the same author.

---

## Notes

- This leaderboard is intentionally empty. The empty state is the invitation.
- The author does not submit to these questions. The author provides the public data and the empirical input-output mapping; the community provides the explanation.
- Submissions are evaluated on **reproducibility and explanatory power**, not on mathematical style. An empirical model that fits all 5 measured LCRs is treated equivalently to a closed-form derivation, as long as it generalizes to a held-out 6th encoding.
- For held-out testing, the author maintains a private 6th encoding (not in the public 5). The first accepted submission is tested against it under the collaboration framework described in EOA-43, Section 2.
- **Authorship:** The first correct, reproducible answer to any question will be offered co-authorship on a joint paper. Alternatively, a solver who prefers to publish independently may do so with acknowledgement, under an agreement permitting independent publication. Priority is adjudicated by timestamped email or public submission, with confirmation posted publicly.
