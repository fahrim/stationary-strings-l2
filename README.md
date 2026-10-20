# Stationary Strings Letter 2 — No Source, No Agreement

> **Türkçe:** [README_TR.md](./README_TR.md)

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](LICENSE)

**L2: No Source, No Agreement — A Forensic Protocol for Literature Values in Model-Assisted Physics**

Author: Fahri Meral · Date: October 20, 2026 · Version: v1 (L2)

> **Status:** Unpublished preprint (v1). Not peer-reviewed. *[![DOI](https://img.shields.io/badge/DOI-10.5281%2Fzenodo.23517495-blue.svg)](https://doi.org/10.5281/zenodo.23517495)*

## The claim in one paragraph

We report a self-inflicted error in our own preprint series and turn it into a
transferable method. A table of experimental ratios was labelled
*independent literature, outside the model* and compared against two model
outputs; both model outputs landed inside the two quoted intervals. The
intervals existed in no source — four primary papers were downloaded and
scanned in full (PDF text *and* LaTeX source) and the quoted numbers occur
nowhere in them. The claim was withdrawn. Two independent forensic tests are
released as code: **repository archaeology** (did the value carry a source
record *before* the agreement that uses it was asserted?) and
**source-existence scanning** (does the quoted interval exist in the corpus at
all?). The two apparent confirmations were also **algebraically dependent** —
the second ratio is the square of the first divided by a locked constant — so
the apparent two-point agreement rested on a single degree of freedom resting
on a value with no source. Of the six literature quantities used in the two
affected tests, **three could not be traced to any source** and two more were
numerically wrong.

## What is and is not claimed

- **Claimed:** a quoted literature interval that exists in no source can
  masquerade as a confirmation; it is detectable; here is a six-step
  protocol and a tool that implements the two cheapest steps.
- **Claimed:** the specific interval in our own work was phantom, and the
  claim was withdrawn.
- **Not claimed:** that the tool can decide whether a value is *true*. It
  reports repository provenance and corpus existence; the semantic reading of
  the source remains a human act, and the letter says so explicitly.
- **Not claimed:** that we know where the interval came from. The repository
  establishes only that it had no provenance *there*.
- **Independent of the rest of the series:** no model, lock or ansatz of
  Theorems I–X / Stationary Strings XI–XIV enters this letter.

## Contents

| File | Description |
|---|---|
| `paper/stationary_strings_L2_ghost_parameter_forensics_EN.tex` | Letter, English (7 pages, Table 1, Figure 1) |
| `paper/stationary_strings_L2_ghost_parameter_forensics_TR.tex` | Turkish version |
| `figs/fig16_ghost_parameter_forensics{,_en}.{pdf,png}` | Forensic summary figure (2×2) |

The numerical machinery lives in the
[`stationary-strings-v`](https://github.com/fahrim/stationary-strings-v)
repository:

```bash
python -W ignore duran_sicimler_sim/mini_check_l2.py    # 7/7 PASS
python -W ignore duran_sicimler_sim/ghost_audit.py \
    --repo . --values 1.55 1.70 --groups "1.55+1.70" \
    --paths duran_sicimler_sim \
    --sources "G:\my_scientific_work\sources\antimatter"
```

The tool does **not** import the solver and does not depend on the physical
model: it operates on a repository and a source corpus.

## Citation

```bibtex
@misc{meral2026ghost,
  author = {Fahri Meral},
  title  = {No Source, No Agreement: A Forensic Protocol for Literature Values in Model-Assisted Physics},
  year   = {2026},
  url    = {https://github.com/fahrim/stationary-strings-l2},
  doi    = {10.5281/zenodo.23517495},
}
```

See also `CITATION.cff`.

## License

CC BY 4.0 — see `LICENSE`. Content is not peer-reviewed.
