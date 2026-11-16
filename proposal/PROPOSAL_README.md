# PhD Proposal — "Volumetric Weaves: Design, Manufacturing, and Application"

This folder is a filled-in copy of `../template` (the TAMU Thesis/Dissertation
LaTeX template) containing a full draft of Tolga Yildiz's PhD proposal,
built from:

- `../template/data/abstract.tex` (the existing abstract, carried over verbatim)
- `../presentation/Prelim_v2` (the preliminary-exam slide deck)
- `../papers/*` (the attached manuscripts)

## Compiling

The template is designed for XeLaTeX + BibTeX:

```
xelatex Proposal_TolgaYildiz.tex
bibtex Proposal_TolgaYildiz
xelatex Proposal_TolgaYildiz.tex
xelatex Proposal_TolgaYildiz.tex
```

This was verified to compile cleanly (no errors, no undefined references) in
this environment (TeX Live 2023) and produces a 67-page PDF.

## Figure placeholders

Every chapter (and Appendix A) now has `\includegraphics` calls with
descriptive filenames and full captions — 29 figures in total — but **none
of the underlying image files exist yet**. To let the document still
compile cleanly, `graphicx` is loaded with the `demo` option (see the
comment at the top of `Proposal_TolgaYildiz.tex`), which draws a plain
black box of the requested size instead of erroring on a missing file.
This means:

- Every figure's position, size, and caption are already correct and will
  show up properly in the Table of Contents / List of Figures.
- The box itself is just a placeholder — nothing to read into its
  appearance.
- **As you get real images**, drop each one into `graphic/` under the
  exact filename already used in its `\includegraphics` call (e.g.,
  `ch04_fig02_cp_eight_local_configurations.png`) — no `.tex` edits
  needed. They just won't render yet: `demo` mode draws a placeholder box
  for *every* figure regardless of whether the file exists, so nothing
  will look different until you take the next step.
- **Once every figure has a real file**, remove (or comment out) the line
  `\PassOptionsToPackage{demo}{graphicx}` near the top of
  `Proposal_TolgaYildiz.tex` and recompile — all 29 figures will render
  for real at once. (Removing it earlier, while some files are still
  missing, will bring back "File not found" errors for those figures.)

## Structure

- `Proposal_TolgaYildiz.tex` — main file (title, degree, committee variables; chapter includes)
- `data/titlepage.tex` — edited to show **co-chairs** (Akleman + Krishnamurthy)
- `data/abstract.tex` — your existing abstract, lightly cleaned (removed commented-out drafts, straightened smart quotes/dashes that XeLaTeX + the `times` package can't render)
- `data/dedication.tex`, `data/acknowledgements.tex` — optional front matter, drafted but easy to delete
- `data/contributors.tex` — Contributors & Funding Sources (required by the template); filled with real funding info found in the papers (NSF #2048182, DFG SFB/TRR280) and per-chapter authorship attribution
- `data/nomenclature.tex` — abbreviations used across the chapters (cP/hP/cF/oF/cI, H-GRS, FDM, TPU, PLA, DIC, ...)
- `data/section1.tex` – Ch. I: Introduction and Literature Review
- `data/section2.tex` – Ch. II: Conceptual Preliminaries (topological labeling, cell-induced elements)
- `data/section3.tex` – Ch. III: Completed Research I — modular planar bi-axial weaves (SMI 2023 paper)
- `data/section4.tex` – Ch. IV: Completed Research II — volumetric Bravais weaves / cP-weave enumeration (PNAS Nexus paper + arXiv enumeration paper)
- `data/section5.tex` – Ch. V: Completed Research III — algebraic nonwoven framework + $2^K$/$8^K$-adic periodic design (SMI 2024 paper)
- `data/section6.tex` – Ch. VI: Completed Research IV — Hypergraph Rotation Systems + Primal-Dual Polycatenanes (SIGGRAPH Asia 2026 submission + SMI 2026 draft)
- `data/section7.tex` – Ch. VII: Proposed Research — manufacturing strategies + auxetic-foam mechanical characterization plan
- `data/section8.tex` – Ch. VIII: Summary, Anticipated Contributions, Timeline
- `data/appendix1.tex` – Appendix A: GF(2) / symmetry-operator representation used for cP-weave enumeration (from the PNAS Nexus supplementary document)
- `data/appendix2.tex` – Appendix B: table of manuscripts/status
- `data/myReference.bib` — merged bibliography (see below)

## The `SCF25_Optics` paper

This manuscript ("Fabricating Interactions through Optical Pathways") isn't
part of the volumetric-weaves narrative in your abstract or prelim slides,
so — pending your confirmation — it's currently given only a brief mention
as ancillary/related work in Chapter I and the Contributors section, plus a
line in the Appendix B publication table. If you'd rather it get its own
chapter, or be dropped entirely, say so and I'll adjust.

## TODOs before this is submission-ready

Search the `.tex` files for `TODO` — every one marks something only you (or
your committee) can supply:

1. **Title page** (`Proposal_TolgaYildiz.tex`): 2nd–4th committee members,
   department head, target month/year.
2. **`data/contributors.tex`**: names/departments of the additional
   committee members; any personal fellowship/assistantship funding.
3. **`data/myReference.bib`**: five citations named only by author/year on
   the prelim slides (Liu 2018, Andriamanalina et al. 2025, Liu et al. 2021,
   Abtew et al. 2020, Li 2021) — I could not find these in any attached
   manuscript's `.bib` file, so I left clearly-marked placeholder entries
   rather than invent volume/page/DOI details. Also: fill in exact
   volume/page/DOI for the two SMI (Computers & Graphics) papers and the
   PNAS Nexus paper once those are finalized, and the arXiv ID for the
   enumeration preprint once posted.
4. **`data/section8.tex`**: the proposed timeline table is entirely
   placeholder dates — replace with your actual plan.
5. **Figures**: all 29 figure placements, filenames, and captions are now
   in place (see "Figure placeholders" above) — the presentation and
   papers were provided/created without their image files, so these are
   all placeholders. Populate `graphic/` with real images (or renders
   regenerated from the papers' source figures) under the filenames
   already referenced, then remove the `demo` option once all of them
   exist.
6. **Dedication/Acknowledgements**: optional pages, currently drafted —
   edit, or delete the corresponding `\include{...}` line in the main file.
