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
| `20260724_s05_ap_handover_step_cause.png` | S5 | Representative N=1 mimic observation |
| `20260724_s07_profile_formation.png` | S7 | N=1 offline profile fit |
| `20260724_s09_two_chart_seam_fit.png` | S9 | N=1 offline representation fit |
| `20260724_s10_seam_rate_constrained_fit.png` | S10 | N=1 offline constrained fit |
| `20260724_ilc_profile_generation_pipeline.png` | S11 | Current-code ILC learning and 500-Hz application paths |
| `20260724_s12_n4_paired_seam.png` | S12 | Online N=4 × 6 trials; same-session shadow comparison |
| `20260724_s14_early_transition_tail.png` | S14 | N=1 mechanism view: an early real contact leaves the outgoing profile endpoint unreached |
| `20260724_s15_same_interface_different_failure.png` | S15 | Physical distinction between an early observed IC, a missed IC with cadence fallback, and offline timing displacement |
| `20260724_final_live_rged_algorithm_flowchart.png` | S16 | Current integrated R-GED, cadence fallback, and event-source handling; mixed validation status shown in figure |
| `20260724_rged_baseline_to_extended_active.png` | S16/S17b | Main-deck comparison of the healthy low-speed baseline and the actually active gait-relative extension; unused candidates omitted |
| `20260724_s24_timeout_waveform.png` | S24 | Anonymized logged timeout; contact attribution unresolved |
| `20260724_s27_independent_checks.png` | S27 | Independent count and post-hoc containment checks |
| `20260724_s28_guard_relativization.png` | S28 | Guard-design context; event-level correctness not established |
| `20260724_s32_three_mechanisms_compared.png` | S32 | Conceptual comparison; unconfirmed |

For S24/S27 and the legacy integrated S16 flowchart, `alpha=0.65` is a
post-hoc crossing-containment candidate with zero live trials. The new
baseline-to-active comparison intentionally omits exact tuning values.
Observer presses are count-only and are not contact-timing or event-level
ground truth.

The S11, S14, S15, and S16/S17b method/concept diagrams also include editable SVG versions.
