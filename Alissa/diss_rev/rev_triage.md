# Revision Triage

## Purpose

This note converts the full advisor decision log into a short working plan. It separates substantive revisions the student should own from edits the advisor can make directly.

## Current strategy

Work on student revisions one at a time. Use Overleaf for the manuscript revisions and comments. Avoid having advisor and student edit the same passages simultaneously.

### Suggested division of Overleaf work

**Student-owned sections while a student revision is active**

- Abstract and Chapter 1 scope/contribution passages
- Chapter 4 limiting-case and validation discussion
- Chapter 5 interpretation of spatial results
- Chapter 6 parameter discussion when activated
- Chapter 7 interpretation and simulation-protocol material
- Chapter 8 conclusions

**Advisor-owned sections while student revision is active**

- Figure captions
- Cross-references and unresolved placeholders
- Local grammar and style edits
- Terminology standardization
- Tables, formatting, and appendix roadmap
- Sections not implicated by the active student revision

## Student revisions

### SR-01 — Clarifying validation, scope, and contribution

**Status:** ready to send

**Why:** The dissertation should explain accurately that it uses analytical verification and purpose-relative qualitative validation against reported empirical patterns. It is not a city-specific predictive model.

**Primary locations:** Abstract; Chapters 1, 4, 5, 6, 7, and 8.

**Related decision IDs:** 001, 006, 015, 035, 042, 043.

**Next action:**

- [ ] Send student-facing SR-01 request
- [ ] Student revises in Overleaf
- [ ] Advisor reviews scope language across all affected chapters
- [ ] Mark decisions 001, 006, 015, 035, 042, and 043 `resolved` when checked

### SR-02 — Parameter rationale and technical consistency

**Status:** hold

**Why:** This includes a useful technical audit, but the ABM–ODE diffusion mapping should be discussed before any formal request is sent.

**Primary locations:** Chapters 4 and 6.

**Related decision IDs:** 008, 025–028, 030, 033.

**Current instruction:** Do not send. Discuss the intended relationship between ABM diffusion \(\zeta\), ODE mixing \(\eta\), area, boundary length, and units first.

**Next action:**

- [ ] Discuss diffusion mapping with student
- [ ] Decide whether to activate a narrowed SR-02
- [ ] If activated, separate parameter-rationale cleanup from any deeper mathematical derivation

### SR-03 — Clarifying the simulation-experiment protocol

**Status:** ready to send

**Why:** The ABM itself is well documented. This request asks only for the simulation-experiment protocol to be made easy to locate and consistent across Chapters 5 and 7.

**Primary locations:** Chapters 5 and 7.

**Related decision IDs:** 016, 034, and supporting part of 021.

**Next action:**

- [ ] Send student-facing SR-03 request
- [ ] Student adds or consolidates simulation-protocol and parametric-study tables/subsections
- [ ] Advisor verifies number of runs, averaging windows, parameter grids, plotted-point definitions, and stated computational limitations
- [ ] Mark decisions 016 and 034 `resolved` when checked

### SR-04 — Clarifying interpretation of spatial experiments

**Status:** ready to send

**Why:** Existing size and multiple-zone simulations should be described as comparisons of specified modeled configurations. No new simulations are requested.

**Primary locations:** Chapter 5, Sections 5.3.1–5.3.2; Chapter 8.

**Related decision IDs:** 017, 018, 044.

**Next action:**

- [ ] Send student-facing SR-04 request
- [ ] Student revises interpretation of fixed-city size comparisons
- [ ] Student revises interpretation of one-large versus several-small-zone configurations
- [ ] Advisor checks conclusion language against revised Chapter 5 language
- [ ] Mark decisions 017, 018, and 044 `resolved` when checked

## Advisor edit batches

### A-01 — Claims and terminology

**Status:** begin after SR-01 wording is stable

**Decision IDs:** 002–005, 007, 013–014, 029, 031–032, 036, 038–039, 046–049.

Includes:

- Claim calibration and terminology standardization
- Research-question/model alignment
- ODE and ABM scope clarifications
- Parameter wording and notation cleanup
- Removal of unsupported policing and gentrification analogies
- Conclusion polishing after student revisions return

### A-02 — Model exposition and technical presentation

**Status:** can begin now in sections not being revised by student

**Decision IDs:** 009–012, 019, 021–024, 037, 040–041, 050.

Includes:

- Parameter and zone-definition tables
- Figure/caption corrections
- Equation and chapter cross-references
- Terminology and local prose cleanup
- Figure-by-figure narration reduction
- Heading, grammar, and placeholder audit

### A-03 — Table 8.1 and appendix navigation

**Status:** advisor edit

- Retain Table 8.1 as a summary of completed work and future research direction.
- Replace hypothesis-test terminology with language matching the actual approaches.
- Use headings such as `Completed`/`Future work`, `Approach`, `Varied feature`, `Primary outputs`, and `Intended contribution`.
- Keep the appendix’s large-scale order unless reorganization is easy and low-risk in the existing LaTeX project.
- Add a brief appendix roadmap if useful.

## Immediate sequence

1. [ ] Send SR-01
2. [ ] Begin low-risk advisor edits outside student-owned passages
3. [ ] Send SR-03
4. [ ] Send SR-04
5. [ ] Review student revisions by request, rather than waiting for all work at once
6. [ ] Discuss whether to activate SR-02
7. [ ] Complete final global consistency, cross-reference, figure, and copyediting pass

## Final resubmission check

- [ ] All student revisions returned and reviewed
- [ ] Scope/validation wording is consistent in Abstract, Chapters 1, 4–8, and conclusion
- [ ] Parameter terminology and units are consistent
- [ ] Simulation protocol is clearly stated
- [ ] Spatial-experiment claims match the actual designs
- [ ] All placeholders, figure references, equation references, and chapter references resolved
- [ ] Table 8.1 revised and future-work agenda retained
- [ ] Appendix roadmap added if desired
- [ ] Final compile checked for references, citations, figures, tables, and formatting
