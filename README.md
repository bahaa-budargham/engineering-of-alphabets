# EOA-43 Public Basis Vectors

This repository contains the public 43-term pre-convergence basis sequences (`english_alphabet.json`) used by the **EOA-43** deterministic word representation.

It accompanies the research paper:

> **EOA-43: Input-Independent Convergence in a Low-Dimensional, Noise-Stable Word Representation**
>
> **Author:** Bahaa Budargham

The repository enables independent researchers to reproduce the published experiments by using the provided basis vectors with the benchmark notebook.

The internal deterministic operator that generates these sequences is **not** included in this repository. Only its public outputs (the basis vectors) are released.

---

## Repository Contents

| File | Description |
|------|-------------|
| `english_alphabet.json` | Public 43-term basis vectors for the English alphabet. |

The full benchmark notebook is available on Google Colab:  
**EOA-43 Benchmark Notebook**  
https://colab.research.google.com/drive/1WvLdr4qqDU_KY8H26DaYnR3N1U6CQIdV?usp=sharing

---

## File Format

The JSON file contains the deterministic basis vectors.

Example:

```json
{
  "a": [...43 values...],
  "b": [...43 values...],
  ...
  "z": [...43 values...]
}
```

Each key represents one English letter.

Each value is a 43-dimensional floating-point sequence.

---

## Loading the Basis

```python
import json

with open("english_alphabet.json", "r") as f:
    basis = json.load(f)
```

The loaded dictionary can then be supplied directly to the benchmark notebook or any compatible EOA-43 implementation.

---

## Reproducibility

This repository is intended solely for reproducing the experiments reported in the accompanying paper. The benchmark notebook demonstrates the complete evaluation pipeline.

---

## Citation

If you use this repository in academic work, please cite:

> Bahaa Budargham. *EOA-43: A Low-Dimensional Deterministic Word Representation with a Stability–Accuracy Trade-off.*

---

## License

This repository is distributed under the MIT License. See `LICENSE` for details.
