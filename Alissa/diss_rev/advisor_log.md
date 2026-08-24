# Advisor Decision Log

## Purpose

This is the master record for substantive review decisions. It is intentionally more concise than the working chat review: it records what must be decided or completed, not every exploratory observation.

## Status vocabulary

- `open` — requires a decision or action
- `student_revision` — student owns the substantive revision
- `advisor_edit` — advisor can correct directly
- `discuss_with_student` — resolve the intended mathematics or interpretation before assigning a revision
- `hold` — defer until needed
- `resolved` — completed and checked

## Decision principles

- Preserve the dissertation’s mathematical contribution and the student’s voice.
- Treat qualitative agreement with external empirical patterns as support for purpose-relative, qualitative validation—not city-specific predictive validation.
- Treat parameter work as identifying reasonable, literature-informed ranges for study unless a parameter is explicitly calibrated to a particular data set.
- Use `advisor_edit` for local corrections, terminology, captions, cross-references, and prose tightening.
- Use `student_revision` when a change requires the student to explain, justify, interpret, or confirm mathematics, methods, or results.

## Active decisions

| ID | Priority | Location | Issue | Recommended disposition | Status |
|---|---|---|---|---|---|
| 001 | major | Abstract; Chs. 1, 4, 5, 7, 8 | State the model’s validation and intended use precisely: qualitative, purpose-relative validation against reported empirical patterns; not city-specific predictive calibration | `student_revision` — SR-01 | open |
| 002 | major | Abstract; Chs. 1 and 8 | Calibrate broad claims about real-world effectiveness, policy, and practical recommendations | `advisor_edit`, coordinated with SR-01 | open |
| 003 | moderate | Throughout | Standardize verification, validation, qualitative consistency, calibration, prediction, enticement, criminal density, and crime density | `advisor_edit` | open |
| 004 | moderate | Ch. 1 | State clearly which questions are addressed by the ODE and which require the ABM | `advisor_edit` | open |
| 005 | minor | Ch. 1 | Correct local prose, figure captions, and configuration descriptions | `advisor_edit` | open |
| 006 | major | Ch. 4 | Distinguish limiting-case/internal-consistency analysis from qualitative validation against external evidence | `student_revision` — SR-01 | open |
| 007 | moderate | Ch. 4 | State that the two-patch ODE does not address spatial configuration questions about number, shape, or placement of zones | `advisor_edit` | open |
| 008 | major | Chs. 4 and 6 | Confirm count-to-density notation and units in the ODE formulation | `hold` / `discuss_with_student` | hold |
| 009 | moderate | Ch. 4 | Add compact reader-facing table of ODE variables, parameters, meanings, and units | `advisor_edit` | open |
| 010 | minor | Ch. 4 | Fix Equation ?? and other local equation/cross-reference defects | `advisor_edit` | open |
| 011 | moderate | Chs. 4 and 6 | Clarify status and rationale of baseline parameter set; distinguish illustrative baseline from city-specific calibration | `advisor_edit` | open |
| 012 | moderate | Ch. 4 | Correct Figure 4-3/4-5 quantity references and captions | `advisor_edit` | open |
| 013 | moderate | Ch. 4 | Reframe results as expected/model-generated behavior and qualitative consistency, not independent confirmation of literature | `advisor_edit` | open |
| 014 | minor | Ch. 4 | Standardize zone, count/density, and resting/removed terminology | `advisor_edit` | open |
| 015 | major | Ch. 5 | Describe initial greened-versus-non-greened result as implementation/expected-behavior check; emphasize boundary-versus-reference comparison as the more informative spatial result | `student_revision` — SR-01 | open |
| 016 | major | Chs. 5 and 7 | Make simulation-experiment protocol easy to locate and consistent across studies | `student_revision` — SR-03 | open |
| 017 | major | Ch. 5.3.2; Ch. 8 | State that multiple-zone cases differ in zone count, perimeter, boundary geometry, and placement—not zone count alone | `student_revision` — SR-04 | open |
| 018 | major | Ch. 5.3.1; Ch. 8 | Qualify fixed-city size comparisons because increasing greened area changes the share of the city assigned to the greened class | `student_revision` — SR-04 | open |
| 019 | moderate | Ch. 5 | Add one reader-facing definition of greened, boundary, reference, and background zones, including area and comparison logic | `advisor_edit` | open |
| 020 | moderate | Chs. 5–7 | Clarify which ODE and ABM mechanisms correspond and which differ intentionally | `hold` / `discuss_with_student` | hold |
| 021 | moderate | Ch. 5 | Clarify identity plots, common-language effect size, regression lines, error ellipses, confidence intervals, and meaning of each point | `advisor_edit`, alongside SR-03 | open |
| 022 | moderate | Ch. 5 | Reduce repetitive figure-by-figure narration and end experiments with concise answers to research questions | `advisor_edit` | open |
| 023 | minor | Ch. 5 | Define fixed total criminal population versus active and removed/resting criminals consistently | `advisor_edit` | open |
| 024 | minor | Ch. 5 | Complete notation, table, caption, and figure-reference audit | `advisor_edit` | open |
| 025 | major | Ch. 6 | Classify parameter choices as literature-informed, model-shape choices, cross-model matching choices, or exploratory ranges | `hold` | hold |
| 026 | major | Ch. 6.4.2 | Confirm intended ABM–ODE diffusion mapping, including areas, boundaries, units, and meaning of approximate matching | `discuss_with_student` | open |
| 027 | major | Ch. 6.6 | Recheck questing-rate derivation and distinguish mean time from mean rate | `hold` | hold |
| 028 | major | Ch. 6.7 | Recheck offending-frequency conversion, resting-time derivation, gamma scaling, and notation | `hold` | hold |
| 029 | moderate | Ch. 6.2 | Define beta as a scale parameter rather than the realized maximum/long-run enticement value | `advisor_edit` | open |
| 030 | moderate | Ch. 6.3 | Describe theta as a cross-model matching choice under simplified assumptions, not city-specific empirical calibration | `hold` | hold |
| 031 | moderate | Chs. 6.4–6.5 | Standardize diffusion terminology, spatial-dimension assumptions, block-length assumptions, and heuristic movement approximations | `advisor_edit` | open |
| 032 | minor | Ch. 6 | Correct xi/omega, nu/tau, equation typo, and time-unit notation | `advisor_edit` | open |
| 033 | major | Ch. 7 | Clarify whether gamma and diffusion quantities are numerically shared, dimensionally matched, or only related in order of magnitude across models | `hold` / `discuss_with_student` | hold |
| 034 | major | Ch. 7 | State exact parameter grids, ABM replication counts, seeds if applicable, fixed parameters, and computational limitations | `student_revision` — SR-03 | open |
| 035 | major | Ch. 7 | Frame as qualitative sensitivity comparison of related but different models; treat similarities and differences as results | `student_revision` — SR-01 | open |
| 036 | major | Ch. 7 | Remove low-gamma analogies to utopia, over-policing, guardianship, or real-world intervention effects | `advisor_edit` | open |
| 037 | moderate | Ch. 7 | Correct criminal-density versus enticement contradictions in text and Figure 7-2 caption | `advisor_edit` | open |
| 038 | moderate | Ch. 7 | Recast causal/policy interpretation of threshold behavior as model-generated hypothesis, not empirical support for policing claims | `advisor_edit` | open |
| 039 | moderate | Ch. 7 | Avoid direct percentage-change comparison of beta and theta values across models with different scales/definitions | `advisor_edit` | open |
| 040 | moderate | Ch. 7 | Reconcile statements about gamma and criminal-density direction by zone, model, and parameter regime | `advisor_edit` unless a substantive correction is needed | open |
| 041 | minor | Ch. 7 | Repair heading hierarchy, typos, captions, notation, and cross-references | `advisor_edit` | open |
| 042 | major | Ch. 8 | Rewrite conclusion around conditional, qualitative, purpose-relative model findings | `student_revision` — SR-01 and SR-04 | open |
| 043 | major | Ch. 8 | Replace “verification”/confirmation claims with accurate description of expected behavior and qualitative validation | `student_revision` — SR-01 | open |
| 044 | major | Ch. 8 | Reframe size and multiple-zone conclusions consistently with SR-04 | `student_revision` — SR-04 | open |
| 045 | moderate | Table 8.1 | Retain the research-program table, but revise terminology: completed/future scope, approach, varied feature, outputs, and intended contribution | `advisor_edit` | open |
| 046 | moderate | Ch. 8 | Remove policy/policing analogies inherited from Chapter 7 | `advisor_edit` | open |
| 047 | moderate | Ch. 8 | Remove unsupported gentrification analogy; state fixed-city composition limitation directly | `advisor_edit` | open |
| 048 | moderate | Ch. 8 | Present 360-day transient as model timescale under assumptions, not confirmation of a real-world temporal result | `advisor_edit` | open |
| 049 | moderate | Ch. 8 | Mark proposed mechanisms, such as interior protection or criminal retention, as interpretations/hypotheses unless directly analyzed | `advisor_edit` | open |
| 050 | minor | Ch. 8 | Resolve placeholders, duplicate figure citation, chapter ??, grammar, and affect/effect | `advisor_edit` | open |

## Student revision assignments

### SR-01 — Clarifying validation, scope, and contribution

**Status:** prepared; ready to send

**Covers:** 001, 006, 015, 035, 042, 043

**Purpose:** State clearly that the dissertation uses analytical verification and purpose-relative qualitative validation against external patterns; it is not a city-specific predictive or quantitatively calibrated model.

### SR-02 — Parameter rationale and technical consistency

**Status:** hold

**Covers:** 008, 025–028, 030, 033

**Purpose:** Confirm parameter rationale, unit consistency, and the intended ABM–ODE parameter relationships.

**Current instruction:** Do not send until discussing the ABM–ODE diffusion mapping with the student.

### SR-03 — Clarifying the simulation-experiment protocol

**Status:** prepared; ready to send

**Covers:** 016, 034, plus supporting portions of 021

**Purpose:** Consolidate experimental-design information already largely present in Chapter 5 and make replication, parameter-grid, averaging, and Chapter 7 computational-limitation details easy to locate.

### SR-04 — Clarifying the spatial experiments

**Status:** prepared; ready to send

**Covers:** 017, 018, 044

**Purpose:** Describe existing size and multiple-zone experiments accurately as comparisons of modeled configurations, with clear acknowledgment of fixed-city composition, perimeter, boundary geometry, and spatial-arrangement changes.

## Advisor edit batches

### A-01 — Claims and terminology

IDs: 002–005, 007, 013–014, 029, 031–032, 036, 038–039, 046–049

### A-02 — Model exposition and technical presentation

IDs: 009–012, 019, 021–024, 037, 040–041, 050

### A-03 — Table 8.1 and appendix navigation

- Retain Table 8.1 as a completed-work/future-research roadmap.
- Revise its labels to avoid formal hypothesis-test terminology and clarify intended contribution.
- Leave the appendix’s major order alone unless reorganization is easy and low-risk in the existing LaTeX project.
- Add a brief appendix roadmap if useful; moving the full NetLogo code to the end is optional, not required.

## Immediate next actions

- [ ] Send SR-01
- [ ] Send SR-03
- [ ] Send SR-04
- [ ] Decide when to discuss the diffusion mapping before activating SR-02
- [ ] Begin A-01/A-02 advisor edits in sections not currently being revised by the student
- [ ] Update each decision status as work is completed
