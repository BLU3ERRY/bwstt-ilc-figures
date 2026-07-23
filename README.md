# BWSTT Control — Report and Lab-Meeting Figures

Figures for the cable-driven BWSTT controller, including phase-indexed ILC and R-GED.
They are hosted here so report and presentation Markdown can render commit-pinned raw URLs.
No subject-identifying information is included (cohort means + anonymous individual points only).

| File | Section | Content |
|------|---------|---------|
| `s17_force_rmse_4cond_4subj_multispeed.png` | Results I | Force RMSE (4 conditions x 3 speeds) |
| `s24a_phase_fidelity_front.png` | Results I | Phase-shape fidelity (Pearson r) |
| `s26c_ilc_efficiency.png` | Results I | Actuator-effort efficiency |
| `s24_t1_cohort_4subj_multispeed.png` | Results II | IC-locked peak interaction force |
| `s17b_per_harmonic_4cond_4subj_vert.png` | Results III | Per-harmonic force-error amplitude |
| `s22b_proto_second_share.png` | Results III | Harmonic error-energy share (H=4 cutoff) |
| `s22d_p_stability_gate.png` | Results III | Stability gate (spectral radius) |
| `s14i_ilc_ff_convergence.png` | Results III | ILC feedforward convergence |
| `s14f_convergence_spiral_statespace.png` | Results III | 2-state convergence spiral (eigenvalue) |

## 2026-07-24 lab meeting

Slide-ready opaque PNGs are listed below. Most also have a
`_transparent.png` sibling; method diagrams include editable SVG where noted.

| File | Slide | Evidence scope |
|------|-------|----------------|
| `20260724_s03_two_failures.png` | S3 | Conceptual split between force-profile representation and gait-event observation at the shared contact boundary |
| `20260724_s05_ap_handover_step_cause.png` | S4 | One pre-fix run: 35.0-N representative handover and the same run's event distribution |
| `20260724_s05_contact_endpoint_pairing.png` | S5 | Actual logged AP table values and equal-order offline fits showing ±8.28-N Fourier endpoint mismatch and exact contact matching |
| `20260724_s07_learning_amplification_coevolution.png` | S6 | Actual pre-change logs: delivery gap, table magnitude, and residual co-evolution |
| `20260724_bspline_profile_construction.png` | S7 | Actual completed-step error projected through fixed local cubic bases into a same-side profile correction |
| `20260724_bspline_model_dimension.png` | Legacy / unused | Nominal coefficient-space accounting; retained for backup but not used in the main deck |
| `20260724_bspline_smoothness_selection.png` | S9 | One-trial, n=84 offline fit-rate trade-off used to choose lambda_rel=3 |
| `20260724_s07_profile_formation.png` | Appendix A7 | N=1 offline profile fit |
| `20260724_s09_two_chart_seam_fit.png` | Legacy / unused | N=1 offline representation fit |
| `20260724_s10_seam_rate_constrained_fit.png` | Legacy / unused | N=1 offline constrained fit |
| `20260724_ilc_profile_generation_pipeline.png` | Appendix A8 | Current-code ILC learning and 500-Hz application paths |
| `20260724_s12_n4_paired_seam.png` | S10 | Online N=4 × 6 trials; same-session shadow comparison |
| `20260724_s14_early_transition_tail.png` | Legacy / unused | Conceptual mechanism schematic annotated with an N=1 logged-data summary; removed from the main deck because the curves are not an actual-data trace |
| `20260724_s15_same_interface_different_failure.png` | S12 | Physical distinction between an early observed IC, a missed IC with cadence fallback, and offline timing displacement |
| `20260724_final_live_rged_algorithm_flowchart.png` | Appendix / legacy | Dense integrated R-GED audit figure; superseded in the main deck because it mixes active and unused paths |
| `20260724_rged_baseline_to_extended_active.png` | S13/S15 | Main-deck comparison of the healthy low-speed baseline and the actually active gait-relative extension; unused candidates omitted |
| `20260724_s24_timeout_waveform.png` | S20 | Anonymized logged timeout; contact attribution unresolved |
| `20260724_s27_independent_checks.png` | S23 | Independent count and post-hoc containment checks |
| `20260724_s28_guard_relativization.png` | S24 | Guard-design context; event-level correctness not established |
| `20260724_s32_three_mechanisms_compared.png` | S28 | Conceptual comparison; unconfirmed |

For the timeout/independent-check figures and the legacy integrated flowchart, `alpha=0.65` is a
post-hoc crossing-containment candidate with zero live trials. The new
baseline-to-active comparison intentionally omits exact tuning values.
Observer presses are count-only and are not contact-timing or event-level
ground truth.

Method and concept diagrams generally include editable SVG versions.
