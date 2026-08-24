# Suggested Revision Language

## Purpose

Store text that is ready, or nearly ready, to paste into the dissertation or send to the student.

Use this note for:

- Replacement paragraphs
- Student-facing revision requests
- Exact wording for recurring scope, validation, and interpretation issues
- Brief advisor notes about where wording must be checked before use

Do not use this note for general observations, routine copyedits, or final status decisions. Those belong in `advisor_decision_log`.

## Template

## [ID] — [Short title]

**Location:**  
**Decision:**  
**Purpose:**  

### Proposed dissertation language

> Paste-ready text.

### Student instruction

> Specific requested revision.

### Advisor note

> Anything that must be resolved before this language is used.

---

# Student Revision Requests

## SR-01 — Clarifying Validation, Scope, and Contribution

**Decision:** `student_revision`  
**Purpose:** State the dissertation’s purpose-relative qualitative validation precisely without retreating from the theoretical contribution.

### Student-facing request

The goal of this revision is not to weaken the dissertation’s claims or to suggest that the models have not been validated. Rather, I would like us to state the type of validation being used more precisely and consistently throughout the dissertation.

These models were not intended to predict crime counts for a particular city, nor were they calibrated to a specific neighborhood data set. Their purpose is to provide a theoretical framework for studying how greening, spatial placement, criminal movement, and crime-related enticement can interact. For that purpose, it is appropriate to assess whether the models produce qualitative behavior that is consistent with patterns reported in the empirical literature. The external evidence is limited and often qualitative, but it still provides meaningful support for the models as tools for investigating plausible mechanisms and generating qualitative hypotheses.

The Chapter 6 parameter work should likewise be described as identifying reasonable, literature-informed ranges for study. It is not city-specific parameter calibration for prediction. The parameter choices and parametric study help us examine whether the qualitative findings persist across plausible regimes, and they help clarify which assumptions and mechanisms drive the modeled behavior.

### Required distinctions

Please distinguish consistently among:

1. **Analytical verification or internal consistency:** limiting-case analysis, equilibrium calculations, stability analysis, and checks that the mathematics behaves as intended.
2. **Qualitative validation:** comparison of modeled qualitative patterns with patterns reported in external empirical studies.
3. **Quantitative calibration and prediction:** fitting a model to a particular city or neighborhood to forecast outcomes. This is not the purpose of the present dissertation.

The key message should be that the dissertation provides **qualitative, purpose-relative validation**: the models are supported as useful tools for their intended theoretical purpose because they reproduce relevant qualitative patterns, while they are not presented as calibrated predictive models for particular cities.

### Target sections

- Abstract
- Chapter 1: contribution, scope, and practical implications
- Chapter 4: limiting cases and verification discussion
- Chapter 5: expected-behavior checks and boundary/reference comparison
- Chapter 6: parameter ranges and rationale
- Chapter 7: sensitivity comparison between models
- Chapter 8: final conclusions

### Helpful language

- “The model is qualitatively validated against reported empirical patterns.”
- “The model provides purpose-relative validation for its intended theoretical use.”
- “The selected parameter ranges are literature-informed and are used to explore plausible model regimes.”
- “The results are qualitatively consistent with empirical studies reporting...”
- “The model is not calibrated for prediction in a particular city.”
- “These findings provide theoretical insight and generate hypotheses for further empirical investigation.”

### Proposed abstract language

> Although these models are not calibrated for direct prediction in a particular neighborhood, their qualitative behavior is compared with patterns reported in prior empirical studies of greening and crime. This comparison provides support for their intended use as theoretical tools for examining how the placement and size of greened areas can affect modeled measures of enticement and crime.

### Proposed Chapter 4 language

> We assess internal consistency of the model in two limiting cases. First, when the mechanisms representing broken windows and near-repeat crime are removed and the patches have identical baseline properties, the model admits the expected homogeneous equilibrium. Second, we examine the one-patch reduction to confirm that it admits a stable equilibrium under the stated parameter assumptions. These analyses provide analytical verification of intended limiting behavior; they are distinct from qualitative validation against external empirical patterns.

### Proposed Chapter 5 language

> We first conduct an implementation and expected-behavior check of the ABM. Because greened sites are assigned lower baseline enticement and associated model parameters, we expect them to exhibit lower modeled enticement and related crime measures than comparable non-greened sites. This experiment confirms that the implemented code produces that intended qualitative behavior. The boundary-versus-reference comparison provides a more informative spatial result because those zones are designed to differ principally in their adjacency to the greened area.

### Proposed conclusion

> This dissertation develops and analyzes complementary ODE and agent-based models of a stylized greening intervention. Within the model structures and parameter regimes considered, lower baseline enticement in a greened region produces lower modeled enticement and crime-related outcomes in that region. The agent-based model further produces lower modeled enticement in a boundary region than in a matched reference region, a qualitative spatial pattern consistent with empirical studies reporting benefits near greened sites.
>
> These findings are theoretical and assumption-dependent. The models are not calibrated to a particular city and do not estimate the causal effect of a specific real-world greening program. Instead, they provide a framework for studying how assumptions about spatial structure, movement, enticement dynamics, and greened area may influence modeled crime patterns. Empirical calibration and additional testing would be necessary before drawing implementation-specific recommendations for cities.

---

## SR-03 — Clarifying the Simulation-Experiment Protocol

**Decision:** `student_revision`  
**Purpose:** Make the simulation-design information already present in the dissertation easier to find and apply consistently across Chapters 5 and 7.

### Student-facing request

The ABM itself is carefully documented in Chapter 5, including its state variables, scheduling, parameters, initialization, inputs, and code. This revision is not asking you to repeat that material.

Instead, I would like to make the experimental protocol easier for a reader to locate and apply across the simulation studies in Chapters 5 and 7. In particular, please make clear which summary procedure, number of independent runs, parameter values, and averaging steps apply to each reported set of figures.

### What to add

Please add a short “Simulation Protocol” subsection, or a compact table, that states:

- Number of independent simulation runs for each configuration or parameter combination
- Random-seed handling, if applicable
- Simulation duration
- Transient/burn-in period
- Time window used for reported averages
- Whether outputs are time averages, spatial averages, averages across simulations, or a combination
- What one blue point represents in the identity plots
- How red means, confidence intervals, and error ellipses were calculated
- Which parameter values were varied and which were held fixed in each experiment

### Chapter 5

Please make clear whether the procedure of discarding 4,500 time steps and averaging over the next 2,500 applies throughout the Chapter 5 experiments. State how many independent simulations contribute to each figure.

### Chapter 7

Add a compact parametric-study design table giving exact parameter grids, fixed parameters, number of ABM runs at each grid point, and any computational limitations. Replace “a few simulations” with the actual number. If a pattern is unclear because of limited simulations, it is fine to say so directly.

---

## SR-04 — Clarifying the Spatial Experiments

**Decision:** `student_revision`  
**Purpose:** Interpret the existing size and multiple-zone experiments as carefully defined modeled-configuration comparisons.

### Student-facing request

This revision is about making the interpretation of the spatial experiments as clear and careful as the simulations themselves. The experiments are interesting and worth keeping. I would just like the dissertation to state more precisely what each experiment varies, what the resulting comparisons show, and what conclusions remain outside the scope of the current model.

This is not a request for new simulations. The goal is to clarify the interpretation of the existing results in Chapter 5 and carry that same interpretation through to Chapter 8.

### Greened-zone size experiment

When the greened zone becomes larger, total city size remains fixed. Thus, a larger fraction of the city is assigned to the greened class, which has lower intrinsic enticement and a lower rate of criminal return.

> Within the fixed-city configurations considered here, increasing greened area was associated with lower citywide modeled outcomes. These citywide comparisons should be interpreted together with the boundary-versus-reference comparisons, since the fraction of the city assigned to the greened class also changes as greened area increases.

> The simulations therefore do not identify a universal minimum effective size for real-world greening interventions. Rather, they show how modeled spatial outcomes change as greened area varies under the assumptions of this ABM.

### One large zone versus several smaller zones

The three configurations have equal total greened area, but they differ in more than the number of greened zones. They also differ in perimeter, boundary-zone geometry, and spatial arrangement.

> We compare three modeled configurations with equal total greened area: one large zone, two intermediate zones, and four smaller zones. Because these configurations also differ in perimeter, boundary geometry, and spatial arrangement, the results describe the combined effects of those configurations rather than the isolated effect of zone count.

> Within the modeled cases considered, the results do not strongly favor one of the three configurations. Further experiments would be needed before drawing a general conclusion about the preferred spatial distribution of real-world greening efforts.

### Conclusion wording

> The spatial experiments identify model-dependent patterns that motivate further empirical and modeling work on the size, arrangement, and local effects of greening interventions.

---

# Advisor-Edit Language

## 029 — Meaning of beta in the ABM

**Location:** Chapter 6, Section 6.2  
**Decision:** `advisor_edit`

> In the ABM, \(\beta\) is a scale parameter governing the magnitude of the crime-related enticement term. Because \(F>0\), the value of \(E_{\mathrm{Crime}}(0)\) is \(\beta/(1+F)\), rather than \(\beta\). Moreover, this term decreases toward zero as time since the most recent crime increases. Thus, \(\beta\) should not be interpreted as a long-run enticement level sustained by the city.

**Advisor note:** If the calculation uses \(F\approx 0.07\), state whether \(\beta=0.02\) is a rounded baseline or use the derived value.

## 036 — Interpretation of low gamma

**Location:** Chapter 7, Section 7.3.2.1  
**Decision:** `advisor_edit`

> At the smallest values of \(\gamma\), the modeled return of removed criminals to active behavior is sufficiently low that few crimes occur during the simulated time horizon. Consequently, the dynamic enticement term remains low even as the crime-related enticement parameter increases. This is a property of the modeled recruitment-and-removal mechanism; it should not be interpreted as a direct representation of policing, guardianship, or a crime-free real-world setting.

## 038 — Threshold interpretation

**Location:** Chapter 7  
**Decision:** `advisor_edit`

> This transition is a behavior of the model under the parameter regimes considered. It suggests a possible mechanism that could be investigated further in a model with explicit enforcement or guardianship, rather than providing empirical evidence about the effects of policing small crimes.

## 047 — Fixed-city composition limitation

**Location:** Chapter 8  
**Decision:** `advisor_edit`

> Because the city area is fixed while greened area increases, citywide averages incorporate a growing proportion of sites assigned to the lower-enticement greened class. This compositional feature contributes to the observed changes in whole-city means and should be considered alongside zone-specific comparisons.

---

# Hold Pending Discussion

## 026 — Relating ABM and ODE diffusion

**Location:** Chapter 6, Section 6.4.2  
**Decision:** `discuss_with_student`

### Student instruction when activated

> Please verify the derivation relating the ABM diffusion coefficient \(\zeta\) to the ODE mixing parameter \(\eta\). Explain whether the goal is an exact coefficient match, an order-of-magnitude match, or a reference-geometry match. In particular, address how one shared value of \(\eta\) is used when the greened and non-greened patches have different areas and therefore different factors \(L/A_i\).

## 027 — Questing-time parameter r

**Location:** Chapter 6, Section 6.6  
**Decision:** `hold`

### Potential instruction

> Please revise the derivation of the questing-rate parameter \(r\). The current calculation averages reciprocal times and then interprets the result as an average questing time. Either compute and use a weighted mean completion time, or retain \(r=1\) as a modeling choice and describe the literature as providing an order-of-magnitude justification rather than a direct estimate.

## 028 — Resting-rate parameter gamma

**Location:** Chapter 6, Section 6.7  
**Decision:** `hold`

### Potential instruction

> Please recompute the conversion from 5.5 offenses per active offender per year to a daily rate and revise the resulting resting-time calculation. Also confirm whether gamma is a total return rate, a per-unit-area rate, or a patch-specific rate in each model. Use the same definition and units in Chapters 4–7.

## 030 — ODE parameter theta

**Location:** Chapter 6, Section 6.3  
**Decision:** `hold`

### Potential replacement language

> We select the baseline value of \(\theta\) by matching the ODE’s enticement scale to a simplified ABM benchmark. This procedure is not an empirical calibration to a particular city. It is a cross-model matching choice made under the assumptions of a background-only ABM, a specified criminal population, an approximately one-crime-per-day regime, and the simplified ODE condition \(E_0=0\).
