[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.21842891.svg)](https://doi.org/10.5281/zenodo.21842891)
# EOA-43: A Rank-Collapsed Deterministic Word Representation with a Convergent Recursive Basis
[![License: CC BY-NC 4.0](https://img.shields.io/badge/License-CC%20BY--NC%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by-nc/4.0/)

> A deterministic, training-free word representation with a strange reproducible property: the ratio of consecutive terms in its 43-term basis sequences stabilizes to ≈ 3.17 — for **every** letter name, for **every** word, and across **random symbols** the system was never built for. The number is **not a universal constant**. Across 5 encodings in 4 languages it shifts from **2.710 (Hebrew)** to **4.128 (Greek)** — a 1.5× spread. The empirical mapping is in the paper. The theoretical explanation is **open**.

![EOA-43 — Limiting Convergence Ratio across 5 encodings, 4 languages](figures/lcr_across_encodings.png)
*The English IPA bar coincidentally sits near π; this proximity is not a structural property.*

---

**Papers:** [EOA-43 (paper 1)](#citation) · [EOA-Recurrence (paper 2, cross-encoding)](#citation) · **Benchmark notebook:** [Colab](https://colab.research.google.com/drive/1WvLdr4qqDU_KY8H26DaYnR3N1U6CQIdV?usp=sharing)

---

## What is in this repository

| File | Description |
| :--- | :--- |
| `data/encodings/` | Letter-name input strings for all five encodings reported in the companion paper (English canonical, English alternative, Arabic, Hebrew, Greek). |
| `notebooks/allcolab.ipynb` | Main Colab notebook containing all benchmark experiments for EOA‑43 (uniform noise, Tables 3–4, PCA, rank diagnostics, and reproducibility). |
| `notebooks/ocrs.ipynb` | Colab notebook for the OCR noise experiment (Table 5). |
| `figures/` | Figures from both the EOA‑43 and EOA‑Recurrence papers. |
| `LEADERBOARD.md` | Tracks submissions for the open theoretical questions (see below). |

The internal deterministic operator that generates the basis sequences is **not** in this repository. Only its public outputs are released. See [Disclosure status](#disclosure-status) below.

---

## Open theoretical questions

The companion paper (EOA-Recurrence) formalizes three open questions derived from the public sequences. The questions (stability within a fixed encoding, cross-encoding mapping, and inverse design) are described in detail in EOA-Recurrence, Section 6. A bank of seven candidate hypotheses (H1–H7) is provided in Section 5.

The 43-term sequences are public and fully measurable by anyone. The operator that generated them is the only gated piece. For access under research-protective terms, please refer to the Research Disclosure Program in EOA-43, Section 2 (contact details provided there). Submissions of theoretical explanations are tracked in [`LEADERBOARD.md`](./LEADERBOARD.md).

---

## Disclosure status

**Public (this repository and the linked Colab notebook):**

- The letter-name input strings for the five encodings.
- The benchmark code, baselines, and evaluation pipeline.
- The precomputed noisy-word vectors for the OCR experiment (required because the generator for out-of-alphabet characters is not disclosed).
- The empirical LCR measurements for 5 encodings across 4 languages (paper 2, Section 3).
- The cross-encoding consistency experiment (paper 2, Section 4).
- The hypothesis bank H1–H7 (paper 2, Section 5).

**Not public:**

- The 43‑term basis sequences (`english_alphabet.json`) – access restricted.
- The interactive playground (`eoa43-playground.html`) – access restricted.
- The internal deterministic operator that produces the basis sequences.
- The closed-form mapping from encoding properties to LCR (open question).

A preliminary least-squares test of the natural linear hypothesis (v<sub>n+1</sub> = M · v<sub>n</sub>) yielded large reconstruction errors on the public data; the status of this hypothesis and the need for normalized-error analysis are discussed in EOA-Recurrence, Section 2. The operator is made available to qualified research collaborators under research-protective terms. Contact the author for the agreement. The mathematical properties attributed to the operator in either paper should be read as **empirical observations of its outputs** unless and until a full formal specification is published.

---

## How to Cite

If you use any materials from this repository in your research, please cite the EOA-43 and/or EOA-Recurrence papers as appropriate:

**EOA-43:**
Budargham, B. (2026). EOA-43: A Rank-Collapsed Deterministic Word Representation with a Convergent Recursive Basis. [arXiv:XXXX.XXXXX]

**EOA-Recurrence:**
Budargham, B. (2026). EOA-Recurrence: Cross-Encoding Variation of the Limiting Ratio (LCR). [arXiv:XXXX.XXXXX]

**BibTeX:**
@article{Budargham2026EOA43,
  author = {Bahaa Budargham},
  title = {EOA-43: A Rank-Collapsed Deterministic Word Representation with a Convergent Recursive Basis},
  year = {2026},
  note = {arXiv:XXXX.XXXXX}
}

@article{Budargham2026EOARecurrence,
  author = {Bahaa Budargham},
  title = {EOA-Recurrence: Cross-Encoding Variation of the Limiting Ratio (LCR)},
  year = {2026},
  note = {arXiv:XXXX.XXXXX}
}
