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
| `20260724_s10_n4_ilc_ap_vertical.png` | S10 | Online N=4 × 6 trials; AP same-session shadow benchmark plus vertical-force tracking in the same 24 ILC-enabled trials |
| `20260724_s12_n4_paired_seam.png` | S10 backup | AP-only same-session shadow comparison |
| `20260724_s14_early_transition_tail.png` | Legacy / unused | Conceptual mechanism schematic annotated with an N=1 logged-data summary; removed from the main deck because the curves are not an actual-data trace |
| `20260724_s15_same_interface_different_failure.png` | S12 | Physical distinction between an early observed IC, a missed IC with cadence fallback, and offline timing displacement |
| `20260724_final_live_rged_algorithm_flowchart.png` | Appendix / legacy | Dense integrated R-GED audit figure; superseded in the main deck because it mixes active and unused paths |
| `20260724_rged_baseline_to_extended_active.png` | S12 | Main-deck comparison of the healthy low-speed baseline and the actually active gait-relative extension; unused candidates omitted |
| `20260724_rged_n4_application_fallback.png` | S13 | Actual N=4 × 6-trial cadence-fallback burden among bilateral application transitions; source 2 / (source 1 + source 2), with source 3/4 real-sync measurements excluded |
| `20260724_s24_timeout_waveform.png` | S14 | Anonymized logged timeout; contact attribution unresolved |
| `20260724_s27_independent_checks.png` | S23 | Independent count and post-hoc containment checks |
| `20260724_s28_guard_relativization.png` | S24 | Guard-design context; event-level correctness not established |
| `20260724_s32_three_mechanisms_compared.png` | S16 backup | Conceptual comparison; unconfirmed |

For the timeout/independent-check figures and the legacy integrated flowchart, `alpha=0.65` is a
post-hoc crossing-containment candidate with zero live trials. The new
baseline-to-active comparison intentionally omits exact tuning values.
Observer presses are count-only and are not contact-timing or event-level
ground truth.

Method and concept diagrams generally include editable SVG versions.

## 2026-08-25 lab meeting

| File | Slide | Evidence scope |
|------|-------|----------------|
| `20260824_rged_n4_operating_performance.png` | S9 / S10 | N=4 x 48 trials, ILC ON, affected side. Trial-level bounded G4 by participant x gait, the raw reference-stride denominator behind every cell, the speed/mode summary, and the G1-vs-G4 plane for all 48 trials. Both reference tiers shown; the strict tier is a nested subset of the one-site tier, so the two rows are a sensitivity contrast, not independent samples. Interface accounting only — no ILC OFF/ON contrast, no force-tracking outcome, not a clinical result. |
| `20260824_rged_n4_source_reconciliation.png` | S5 / S6 | Same cohort. Share of affected-side application boundaries by event source 1-4 per participant / gait / speed stratum, plus per-trial real-first and reconciliation rates. Sources 3 and 4 live inside source 2 and are never added to the application denominator. Reference is a 4-channel plantar FSR path, not a gold standard; sensor-path delay is uncorrected, so no absolute IC-latency claim is made. |

Participant labels `P1`-`P4` index this cohort only, in producer roster order.
They are not the `S1`-`S4` of the earlier four-subject figures, which index a
different roster. No initials, body mass, BWS setting, or age appears in any
figure or file.
