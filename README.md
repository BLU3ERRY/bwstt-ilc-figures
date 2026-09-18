## AAN selected assessment — 2026-09-18 (representative belt speed 0.35 m/s)

Updated to LLART v2.4.6 (2026-09-18): the fixed belt speed is 0.35 m/s, the representative 350 mm/s declared by the protocol. The 2026-09-16 images below used 0.55 m/s, an undocumented carry-over of the old demo band, and remain pinned at commit d48cba1. Same 342-run design (150 primary + 192 sensitivity), same seeds, common evaluation 120–420 s. The missing-evidence clock now starts only after the 12 s settle window; before this change the 3 s ramp tracking gap started it, so the rule silently depended on stride time.

- `20260918_aan_selected_results`: per-run dots and three-seed means for delivered support and reference violation time.
- `20260918_aan_selected_compensation`: seed-7 trunk-compensation response with delayed / residual adverse effects.
- `20260918_aan_selected_dropout`: event outage, preserved independent position, and explicit unknown gait measurement.
- `20260918_aan_selected_demo`: live offline simulator (UI 2026-09-18) after reduction and acceptance.

Sources: LLART `llc/aan_demo/assessment/VALIDATION.md`, `results/summary.json`, `report.py`. Simulated outcomes only; no clinical efficacy or sensor validation. No patient photos or actual participant recordings.

## AAN selected assessment — 2026-09-16

Updated to LLART v2.4.1: complete reference/evaluation intervals start after warmup/settling. All 342 runs and figures were regenerated. Earlier v2.4.0 images remain available at commit 145658d.

Four selected metrics: position, personal stride period, log step-time asymmetry, circular trunk posture. Independent experimental C++/WASM module; production LLC unchanged. 150 primary + 192 sensitivity runs. Figures show simulated outcomes, not clinical efficacy or measured sensor validation. Fixed 30%BW comparator, fixed 0.55m/s, same three time-noise seeds; common evaluation 120–420 s. Legacy figures remain pinned to their original commits.

- `20260916_aan_selected_results`: per-run dots and three-seed means for delivered support and reference violation time.
- `20260916_aan_selected_compensation`: seed-7 response with delayed / residual adverse effects.
- `20260916_aan_selected_dropout`: event outage, preserved independent position, and explicit unknown gait measurement.
- `20260916_aan_selected_demo`: live offline simulator after reduction and acceptance.

Sources: LLART `llc/aan_demo/assessment/VALIDATION.md`, `results/summary.json`, `report.py`; full scenario and normalization assumptions recorded there. No patient photos or actual participant recordings.

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

## 2026-09-08 lab meeting follow-up (AAN protocol rework)

| File | Slide | Content |
|------|-------|---------|
| `20260909_aan_episode_algorithm_flowchart.png` | S12 replacement | AAN episode algorithm flowchart after the 2026-09-09 rework: per-stride margin judgment, known-probability arm draw, ramp mask, fast window, judgment-before-stationarity extension, slow guard, revert-only washout, edge fallback to therapist. No data; state machine only. `_transparent.png` and editable `.svg` siblings. |

## 2026-09-XX lab meeting — current AAN design and simulation

Prepared September 15, 2026. Current production core `22ababa1`, LLART
`2662b7d` (`v2.3.5`). These are design diagrams and engineering simulation
results, not patient efficacy measurements. Full provenance and file hashes:
[`202609XX_aan_figures.json`](202609XX_aan_figures.json).

| File | Slide | Evidence scope |
|------|-------|----------------|
| `202609XX_s02_aan_system_flow.png` | S2 | Observations, AAN, force control and delivered intervention; conceptual diagram. SVG sibling. |
| `202609XX_s16_aan_episode_flow.png` | S16 | Baseline, approved change, ramp, fast judgment and follow-up; current working timing. SVG sibling. |
| `202609XX_s24_aan_simulator_flow.png` | S24 | Production decision core versus simulated person/device responses. SVG sibling. |
| `202609XX_s30_aan_speed_measurement.png` | S30 | Proposed comparison of C7 readback and independent belt-speed measurement; measurement not yet performed. SVG sibling. |
| `202609XX_s26_aan_workspace.png` | S26 | Actual current simulator screenshot at an allowed-range edge; not the initial reference-collection state. |
| `202609XX_s27_aan_support_response.png` | S27 | Seed 7, support-sensitive response: fixed support versus AAN over 420 s. |
| `202609XX_s29_aan_compensation.png` | S29 | Seed 7, competing compensation: AAN increased task-violation time. |
| `202609XX_s29_aan_persistent_deficit.png` | S29 | Seed 7, deliberately nonresponsive deficit: increased support did not resolve the modeled deficit. |
| `202609XX_s29_aan_current_results.png` | S28/S29 | Four selected conditions, three seeds per arm; dots and min–max ranges, not confidence intervals. SVG sibling. |
| `202609XX_aan_all_14_conditions.png` | Appendix | All 14 base conditions, same three-seed comparison. SVG sibling. |

Violation fractions use valid margin-observation time, not the full 420 s.
Missing observations are not counted as successful walking. Speed scale is
an unmeasured engineering assumption; other scales are calibration candidates.
No production parameter selection or universal superiority claim is made.
