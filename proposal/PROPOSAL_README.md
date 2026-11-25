# PhD Proposal: "Weaves, Knits, and Chainmail: Design Frameworks for Fibrillar Structures and Their Physical Realization"

This folder holds the proposal, built on the TAMU thesis template
(`../template`). The narrative is organized around one idea: every
construction in the dissertation is a scaffold, a small set of local
labels, and a replacement rule, and hypergraph rotation systems (H-GRS)
unify the cycle-based constructions with a single twist operator. The
proposed work is manufacturing volumetric weaves and a mechanical
exploration of cP-weave plate lattices against TPMS baselines.

## Compiling

XeLaTeX + BibTeX (`compile.bat` runs the sequence):

```
xelatex Proposal_TolgaYildiz.tex
bibtex Proposal_TolgaYildiz
xelatex Proposal_TolgaYildiz.tex
xelatex Proposal_TolgaYildiz.tex
```

With all figures as placeholders the build is 56 pages with no
undefined references. Real images will change the page count somewhat.

## Figures

Figures are placeholders until their image is saved in `graphic/` under
the filename in its `\includegraphics`. Each caption ends with a red
`\figtodo{...}` note naming the source; `FIGURE_SOURCES.md` has the same
list as a checklist (21 figures). Images stay local and are not
committed to this repository.

## Structure

| File | Content | Source |
|---|---|---|
| `data/abstract.tex` | Abstract | |
| `data/section1.tex` | Ch. 1, Introduction and Background: motivation, background, thesis statement, scheme table (Table 1.1), contributions C1 to C7 | |
| `data/section2.tex` | Ch. 2, Modularity and Symmetry in Planar Weaves | SMI 2023 |
| `data/section3.tex` | Ch. 3, Volumetric Bravais Weaves | PNAS Nexus 2025, enumeration manuscript |
| `data/section4.tex` | Ch. 4, An Algebra for Populating Labeled Lattices | SMI 2024 |
| `data/section5.tex` | Ch. 5, Linked and Catenated Structures | SMI 2025, SMI 2026 |
| `data/section6.tex` | Ch. 6, Hypergraph Rotation Systems, with the synthesis table (Table 6.1) | ACM TOG / SIGGRAPH Asia 2026 |
| `data/section7.tex` | Ch. 7, Proposed Work I: Manufacturing Volumetric Weaves | SCF 2025, unpublished methods |
| `data/section8.tex` | Ch. 8, Proposed Work II: Mechanical Exploration of cP-Weave Plate Lattices | in progress |
| `data/section9.tex` | Ch. 9, Summary, Contributions, and Timeline | |
| `data/appendix2.tex` | Appendix A, Publications and manuscripts | |

`data/dedication.tex`, `data/acknowledgements.tex`, and
`data/appendix1.tex` (GF(2) operators) are kept but not included; restore
their `\include`/`\input` lines to bring them back.

## Remaining TODOs

1. `data/section9.tex`: timeline dates.
2. `data/myReference.bib`: volume and pages for the SMI 2024 nonwoven
   paper and the SMI 2026 polycatenane paper once assigned.
3. Figures: add images using `FIGURE_SOURCES.md`.
