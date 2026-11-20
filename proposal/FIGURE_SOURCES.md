# Figure sources

Every figure in the proposal ends its caption with a red
`\figtodo{...}` note listing the images the figure needs and where each
one comes from. This file is the same information as a checklist.

- **Workflow:** save each image into `graphic/` under the exact
  filename below, tick its box, and recompile. A figure whose file is in
  `graphic/` renders; one that is not yet there shows a grey box labelled
  with the missing filename, so the document always compiles.
- Once a figure is final, delete the `\figtodo{...}` line at the end of
  its caption (or hide all notes at once with `\showfigtodosfalse` near
  the top of `Proposal_TolgaYildiz.tex`).

## Source keys

| Key in captions | Folder in this repo | Bib key |
|---|---|---|
| SMI 2023 woven tiles | `papers/SMI2023_Woven_Tiles/` | `yildiz2023modular` |
| SMI 2024 nonwovens | `papers/SMI2024_High_Genus_Surface_NonWoven/` | `yildiz2024nonwoven` |
| PNAS Nexus (main) | `papers/PNAS_Nexus___cP_Weaves___Final/` | `yildiz2025volumetric` |
| PNAS Nexus supplementary | `papers/PNAS_Nexus___A_Construcive_Framework_..._Supplementary/` | `yildiz2025volumetric` |
| Enumeration preprint | `papers/Enumeration_of_cP_and_hP_Weaves/` | `akpanya2025enumeration` |
| SIGGRAPH Asia 2026 (H-GRS) | `papers/SIGGRAPH_Asia_2026___Surface_Knots/` (`main.tex`, `supplementary.tex`) | `yildiz2026hypergraph` |
| SMI 2026 polycatenanes | `papers/SMI2026_Primal_Dual_Structures/` | `yildiz2026polycatenane` |
| Prelim\_v2 slide N | `presentation/Prelim_v2/` | — |
| comp-anal | `github.com/ComicAddict/comp-anal` | `companal2026` |

Image paths in the captions are relative to each paper's folder, as they
appear in that paper's `\includegraphics`. The image files themselves are
not in this repository; take them from the papers' Overleaf projects.

**Prelim slides:** the deck in `presentation/Prelim_v2/` had its media
stripped, so the `imageN.png` names in the captions come from
`ppt/slides/_rels/slideN.xml.rels`. To get the images, unzip the original
`Prelim_v2.pptx` and look in `ppt/media/`.

## Checklist

Tick a box (`- [x]`) once the file is in `graphic/`. Figure numbers are
as in the current build.

### A. Reuse directly from a paper figure

- [ ] **2.1** `ch02_fig01_2way2fold_local_states.png` — PNAS supplementary, `2dweaveunits`
- [ ] **3.1** `ch03_fig01_yinyang_congruent_tiles.png` — SMI 2023, `fig:2Dweave` + `fig:parametric/flat`
- [ ] **3.2** `ch03_fig02_tile_unfolding_laser_cut.png` — SMI 2023, `fig:folding1` (+ `fig:folding0`)
- [ ] **3.3** `ch03_fig03_assembled_pattern_examples.png` — SMI 2023, `fig:planarslabs` (+ `fig:photos`)
- [ ] **4.1** `ch04_fig01_wigner_seitz_cell_types.png` — PNAS `fig_teaser` (a), or SMI 2026 `fig_teaser` top row
- [ ] **4.2** `ch04_fig02_cp_eight_local_configurations.png` — Enumeration `fig:8conf`, or PNAS `cpconfs`
- [ ] **4.3** `ch04_fig03_symmetry_operations_on_domain.png` — PNAS `fig:rot_isotopy` + Enumeration `fig:actiononweaves3d`
- [ ] **5.1** `ch05_fig01_woven_vs_nonwoven_connectivity.png` — SMI 2024, `fig_woven_vs_nonwoven`
- [ ] **5.2** `ch05_fig02_octal_tensor_representation.png` — SMI 2024, `fig_matrix_woven_vs_nonwoven4` + `fig_tensor`
- [ ] **5.3** `ch05_fig03_padic_cyclic_addition_example.png` — SMI 2024, `fix_8adic_shifting` (**see note below**)
- [ ] **6.1** `ch06_fig01_hgrs_edge_face_incidence.png` — SIGGRAPH supp. `fig:supp_chirality` + main `fig:teaser`
- [ ] **6.2** `ch06_fig02_twist_operator_examples.png` — SIGGRAPH `fig:3_mantwist` (exact match)
- [ ] **6.3** `ch06_fig03_primal_dual_polycatenane.png` — SMI 2026, `fig1_4` + `fig_teaser` cI row + `fig:3dprinting` (**see note below**)
- [ ] **A.1** `appA_fig01_translation_rotation_mirror_operators.png` — Enumeration `fig:actiononweaves` / `fig:actiononweaves3d`

### B. Reuse from the prelim slides

- [ ] **1.1** `ch01_fig01_motivation_montage.png` — slide 5 (+ chainmail from SIGGRAPH `fig:tetra_link`); **third-party photos: add credits**
- [ ] **2.2** `ch02_fig02_cell_induced_elements.png` — slide 15
- [ ] **4.4** `ch04_fig04_plain_cp_weave_orbits.png` — slide 30 (4×4×4); top row from PNAS `fig_plain_weave`
- [ ] **7.1** `ch07_fig01_chiral_guide_pair.png` — slide 56
- [ ] **7.2** `ch07_fig02_manufacturing_strategy_comparison.png` — slides 53–54, 56–57, 58–60, 61
- [ ] **7.9** `ch07_fig09_compression_test_setup.png` — slides 71–72
- [ ] **7.10** `ch07_fig10_printed_foam_specimens_pla_tpu.png` — slide 73 (+ 65)
- [ ] **7.11** `ch07_fig11_preliminary_force_displacement_curves.png` — slides 75–77

### C. Compose or redraw (sources exist, layout is new)

- [ ] **1.2** `ch01_fig02_knowledge_gap_schematic.png` — slides 8–9 thumbnails, new 3-column layout
- [ ] **8.1** `ch08_fig01_dissertation_overview_diagram.png` — slides 3, 18–19 overview + one thumbnail per chapter

### D. New renders, photos, or plots (no existing image)

- [ ] **7.3a** `ch07_fig03a_wo_wd_geometry_diagram.png` — annotated render of one 4 mm plain `1_1_1_1` cell (wo, wd, r)
- [ ] **7.3b** `ch07_fig03b_radius_vs_volume_fraction_curve.png` — vf(r) plot from the bisection-search data in the printed-weave notes
- [ ] **7.4** `ch07_fig04_printed_abcd_specimens.png` — photos of the four printed `a_b_c_d` specimens
- [ ] **7.5a** `ch07_fig05a_min_interstrand_clearance.png` — render of one strand with closest-point segments
- [ ] **7.5b** `ch07_fig05b_64_plain_pattern_shapes.png` — 8×8 grid of the 64 plain codes `000`–`333`
- [ ] **7.6** `ch07_fig06_woven_vs_tpms_specimen_sets.png` — woven-foam renders + one render per TPMS family
- [ ] **7.7** `ch07_fig07_class_stress_strain_envelopes.png` — comp-anal `class_envelopes.png`; synthetic demo or schematic until results are reported
- [ ] **7.8** `ch07_fig08_tpms_scale_matching.png` — comp-anal `scale_match/scale_trends.png`; same rule

## Caption mismatches to resolve

- **Fig. 5.3**: the caption describes *cyclic addition*, but the SMI 2024
  8-adic figure shows *shift by multiplication*. Either redraw the 3×7
  cyclic-addition matrix from that paper's §"Design with 2^K-adic
  Symmetry Operations", or reword the caption.
- **Fig. 6.3**: the caption says the right panel is a printed cI-links
  prototype, but the SMI 2026 print photo (`fig:3dprinting`) is the
  tetrahedral–octahedral honeycomb. Reword the caption or photograph a
  cI print.
