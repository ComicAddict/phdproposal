# Figure sources

Every figure in the proposal ends its caption with a red
`\figtodo{...}` note listing the images the figure needs and where each
one comes from. This file is the same information as a checklist.

- Hide all notes at once: set `\showfigtodosfalse` near the top of
  `Proposal_TolgaYildiz.tex`.
- Drop finished images into `graphic/` under the filename already used
  in each `\includegraphics`, then remove the
  `\PassOptionsToPackage{demo}{graphicx}` line once every file exists
  (see `PROPOSAL_README.md`).

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

Figure numbers are as in the current build; filenames are the `\includegraphics` names (`.png`).

### A. Reuse directly from a paper figure

| Fig. | Proposal file | Take from |
|---|---|---|
| 2.1 | `ch02_fig01_2way2fold_local_states` | PNAS supplementary, `2dweaveunits` |
| 3.1 | `ch03_fig01_yinyang_congruent_tiles` | SMI 2023, `fig:2Dweave` + `fig:parametric/flat` |
| 3.2 | `ch03_fig02_tile_unfolding_laser_cut` | SMI 2023, `fig:folding1` (+ `fig:folding0`) |
| 3.3 | `ch03_fig03_assembled_pattern_examples` | SMI 2023, `fig:planarslabs` (+ `fig:photos`) |
| 4.1 | `ch04_fig01_wigner_seitz_cell_types` | PNAS `fig_teaser` (a), or SMI 2026 `fig_teaser` top row |
| 4.2 | `ch04_fig02_cp_eight_local_configurations` | Enumeration `fig:8conf`, or PNAS `cpconfs` |
| 4.3 | `ch04_fig03_symmetry_operations_on_domain` | PNAS `fig:rot_isotopy` + Enumeration `fig:actiononweaves3d` |
| 5.1 | `ch05_fig01_woven_vs_nonwoven_connectivity` | SMI 2024, `fig_woven_vs_nonwoven` |
| 5.2 | `ch05_fig02_octal_tensor_representation` | SMI 2024, `fig_matrix_woven_vs_nonwoven4` + `fig_tensor` |
| 5.3 | `ch05_fig03_padic_cyclic_addition_example` | SMI 2024, `fix_8adic_shifting` (**see note**) |
| 6.1 | `ch06_fig01_hgrs_edge_face_incidence` | SIGGRAPH supp. `fig:supp_chirality` + main `fig:teaser` |
| 6.2 | `ch06_fig02_twist_operator_examples` | SIGGRAPH `fig:3_mantwist` (exact match) |
| 6.3 | `ch06_fig03_primal_dual_polycatenane` | SMI 2026, `fig1_4` + `fig_teaser` cI row + `fig:3dprinting` (**see note**) |
| A.1 | `appA_fig01_translation_rotation_mirror_operators` | Enumeration `fig:actiononweaves` / `fig:actiononweaves3d` |

### B. Reuse from the prelim slides

| Fig. | Proposal file | Slides |
|---|---|---|
| 1.1 | `ch01_fig01_motivation_montage` | 5 (+ chainmail from SIGGRAPH `fig:tetra_link`) — **third-party photos: add credits** |
| 2.2 | `ch02_fig02_cell_induced_elements` | 15 |
| 4.4 | `ch04_fig04_plain_cp_weave_orbits` | 30 (4×4×4); top row from PNAS `fig_plain_weave` |
| 7.1 | `ch07_fig01_chiral_guide_pair` | 56 |
| 7.2 | `ch07_fig02_manufacturing_strategy_comparison` | 53–54, 56–57, 58–60, 61 |
| 7.9 | `ch07_fig09_compression_test_setup` | 71–72 |
| 7.10 | `ch07_fig10_printed_foam_specimens_pla_tpu` | 73 (+ 65) |
| 7.11 | `ch07_fig11_preliminary_force_displacement_curves` | 75–77 |

### C. Compose or redraw (sources exist, layout is new)

| Fig. | Proposal file | Built from |
|---|---|---|
| 1.2 | `ch01_fig02_knowledge_gap_schematic` | slides 8–9 thumbnails, new 3-column layout |
| 8.1 | `ch08_fig01_dissertation_overview_diagram` | slides 3, 18–19 overview + one thumbnail per chapter |

### D. New renders, photos, or plots (no existing image)

| Fig. | Proposal file | What to make |
|---|---|---|
| 7.3a | `ch07_fig03a_wo_wd_geometry_diagram` | annotated render of one 4 mm plain `1_1_1_1` cell (wo, wd, r) |
| 7.3b | `ch07_fig03b_radius_vs_volume_fraction_curve` | vf(r) plot from the bisection-search data in the printed-weave notes |
| 7.4 | `ch07_fig04_printed_abcd_specimens` | photos of the four printed `a_b_c_d` specimens |
| 7.5a | `ch07_fig05a_min_interstrand_clearance` | render of one strand with closest-point segments |
| 7.5b | `ch07_fig05b_64_plain_pattern_shapes` | 8×8 grid of the 64 plain codes `000`–`333` |
| 7.6 | `ch07_fig06_woven_vs_tpms_specimen_sets` | woven-foam renders + one render per TPMS family |
| 7.7 | `ch07_fig07_class_stress_strain_envelopes` | comp-anal `class_envelopes.png`; synthetic demo or schematic until results are reported |
| 7.8 | `ch07_fig08_tpms_scale_matching` | comp-anal `scale_match/scale_trends.png`; same rule |

## Caption mismatches to resolve

- **Fig. 5.3**: the caption describes *cyclic addition*, but the SMI 2024
  8-adic figure shows *shift by multiplication*. Either redraw the 3×7
  cyclic-addition matrix from that paper's §"Design with 2^K-adic
  Symmetry Operations", or reword the caption.
- **Fig. 6.3**: the caption says the right panel is a printed cI-links
  prototype, but the SMI 2026 print photo (`fig:3dprinting`) is the
  tetrahedral–octahedral honeycomb. Reword the caption or photograph a
  cI print.
