# Suggested Revision Language

## 001 — Scope and validation language

**Location:** Abstract; Chapter 1; Chapter 8  
**Decision:** `student_revision`  
**Purpose:** Distinguish analytical verification and qualitative agreement with 
published studies from empirical validation or city-specific prediction.

### Proposed abstract language

> Although these models are not calibrated for direct prediction in a particular
> neighborhood, their qualitative behavior is consistent with patterns reported
> in prior empirical studies of greening and crime. They provide a theoretical
> framework for examining how the placement and size of greened areas can affect
> modeled measures of enticement and crime.

### Student instruction

Revise the Abstract, Introduction, and Conclusions so that they use consistent
language about model scope. Do not claim that the models have been proved valid
through anecdotal evidence. Describe the limiting-case analysis as analytical
verification or internal consistency analysis, and describe agreement with the
literature as qualitative consistency.

---

## 002 — Conditional interpretation of spatial distribution results

**Location:** Chapter 1, Sections 1.3–1.4; Chapter 8  
**Decision:** `advisor_edit`  
**Purpose:** Avoid presenting model output as a general recommendation to cities.

### Proposed replacement for the end of Section 1.3

> Within the modeled configurations and parameter values considered here, the
> simulations did not strongly favor a single large greened zone over several
> smaller zones with the same total area. This result motivates further empirical
> investigation of how spatial distribution affects greening outcomes in real
> cities.

### Proposed replacement for Section 1.4

> The model reproduces qualitative patterns consistent with studies reporting
> reduced crime near greened areas. It therefore provides a theoretical framework
> for examining possible spatial mechanisms, rather than a calibrated estimate of
> the effectiveness of greening in a particular city.

---

## 006 — Verification language in the ODE chapter

**Location:** Chapter 4, Section 4.1.2  
**Decision:** `student_revision`

### Proposed replacement opening

> We assess internal consistency of the model in two limiting cases. First, when
> the mechanisms representing broken windows and near-repeat crime are removed
> and the patches have identical baseline properties, the model admits the
> expected homogeneous equilibrium. Second, we examine the one-patch reduction
> to confirm that it admits a stable equilibrium under the stated parameter
> assumptions. These analyses do not constitute empirical validation; rather,
> they establish that the equations behave consistently with intended limiting
> behavior.

---

## 007 — Scope of the two-patch ODE model

**Location:** Chapter 4, Section 4.1.1  
**Decision:** `advisor_edit`

### Proposed addition after the research questions

> The present two-patch ODE formulation is used to examine the interaction
> between a greened and a non-greened region. Questions concerning the size,
> shape, placement, or number of greened zones require explicit spatial
> representation and are therefore investigated principally with the agent-based
> model in Chapter 5.

---

## 013 — ODE results discussion

**Location:** Chapter 4, Section 4.3  
**Decision:** `advisor_edit`

### Proposed replacement paragraph

> For the illustrative parameter set considered here, the model produces lower
> modeled enticement, criminal density, and crime density in the greened patch
> than in the non-greened patch. Because greening is represented through lower
> baseline enticement and related parameter choices, this result is an expected
> consequence of the model construction. The result is qualitatively consistent
> with empirical studies that report lower crime near greened sites, but it is
> not a calibrated prediction for a particular city.


## 015 — ABM implementation check, not empirical verification

The chapter’s baseline experiment observes lower values in the greened zone than in comparison zones. But the ABM assigns greened sites lower static enticement, and the model’s recruitment/return mechanism also differs by greened versus non-greened area. Lower output values are therefore partly expected from construction.

Suggested replacement for the §5.2 framing:

> We first conduct an implementation and expected-behavior check of the ABM. Because greened sites are assigned lower baseline enticement and associated model parameters, we expect them to exhibit lower modeled enticement and related crime measures than comparable non-greened sites. This experiment confirms that the implemented code produces that intended qualitative behavior. It does not provide empirical validation of the model for a particular city.


## 017 — Fixed total area: configuration comparison

## 2. Define what the experiments isolate

The fixed-total-area experiment compares one 10×1010 \times 1010×10 zone, two 5×105 \times 105×10 zones, and four 5×55 \times 55×5 zones. The greened area remains 100 cells, but the configurations do not differ only in the _number_ of greened zones: splitting a fixed area changes the total green/non-green interface and changes the geometry of the boundary regions.

Suggested replacement for the experiment description:

> We compare three specified spatial configurations with equal total greened area: one 10×1010 \times 1010×10 zone, two 5×105 \times 105×10 zones, and four 5×55 \times 55×5 zones. Because these configurations also differ in perimeter, boundary-zone geometry, and spatial arrangement, the experiment evaluates the combined consequences of these configurations rather than isolating the effect of zone count alone.

This does not weaken the experiment. It makes the spatial mechanism more honestly described.



## 018 — Qualifying citywide size effects

## Qualify citywide size effects

The size experiment changes a greened zone from 1×11 \times 11×1 to 32×3232 \times 3232×32 within the fixed 71-by-71 city, which changes the share of the city assigned to the greened class from roughly 0.03% to 27.52%. The draft’s conclusions already partly recognize this compositional issue, but Chapter 5 should introduce it before interpreting falling citywide means as an increasingly strong intervention effect.

Because city size is fixed while greened area increases, citywide averages necessarily incorporate a growing proportion of sites assigned to the greened class. Accordingly, citywide outcomes should be interpreted alongside zone-specific and boundary-versus-reference comparisons, which better address local spatial effects beyond this compositional change.


## 016 — Simulation protocol and summary statistics

The student should add a short subsection—perhaps **“Simulation protocol and summary statistics”**—before presenting the first results. It should answer, in one place:

- How many independent replications were run for each configuration?
    
- Were random seeds fixed, recorded, or varied?
    
- How many daily steps did each run contain?
    
- What period was treated as transient/burn-in, and why?
    
- Were reported values time averages, spatial averages, replication averages, or all three?
    
- What is one point in each identity plot: one replication, one parameter combination, or another summary?
    
- What confidence level and method generated the confidence intervals or error ellipses?
    
- Which output is used: mean enticement, active-criminal density, crime-event density, cumulative crimes, or something else?
    

The chapter shows a greened zone added at day 3000 and says output reaches a stationary solution after about 360 days, so the simulation timing is evidently meaningful and should be described explicitly as methodology rather than left mainly in figure interpretation.

## 027 — Questing-time parameter r

**Location:** Chapter 6, Section 6.6  
**Decision:** `student_revision`  
**Purpose:** Correct the interpretation of the questing-time calculation.

### Student instruction

> Please revise the derivation of the questing-rate parameter \(r\). The current
> calculation averages reciprocal times and then interprets the result as an
> average questing time. Either compute and use a weighted mean completion time,
> or retain \(r=1\) as a modeling choice and describe the literature as providing
> an order-of-magnitude justification rather than a direct estimate.

### Optional replacement language

> The available behavioral evidence indicates that many burglaries are completed
> on short time scales, but it does not uniquely determine a questing-time
> distribution for the modeled population. We therefore use \(r=1\) per day as
> an illustrative baseline consistent with the model’s daily time step. The
> interval considered in the parametric study represents plausible variation
> around this modeling choice rather than a city-specific calibrated estimate.

### Advisor note

Confirm whether the selected baseline \(r=1\) and its study range remain unchanged
after the calculation is corrected.

## 028 — Resting-rate parameter gamma

**Location:** Chapter 6, Section 6.7  
**Decision:** `student_revision`  
**Purpose:** Correct the offending-frequency conversion and define gamma consistently.

### Student instruction

> Please recompute the conversion from 5.5 offenses per active offender per year
> to a daily rate and revise the resulting resting-time calculation. Also confirm
> whether gamma is a total return rate, a per-unit-area rate, or a patch-specific
> rate in each model. Use the same definition and units in Chapters 4–7.

### Proposed dissertation language

> An estimated offending frequency of 5.5 offenses per active offender per year
> corresponds to approximately \(5.5/365 \approx 0.015\) offenses per day, or one
> offense every 66 days. If the questing period is modeled separately as \(\nu\),
> the remaining interval is represented as a resting period of approximately
> \(66-\nu\) days. We use this calculation to identify an order-of-magnitude range
> for \(\gamma\), not as a city-specific calibration.

### Advisor note

Use the final selected value only after the student verifies the area scaling.


## 029 — Meaning of beta in the ABM

**Location:** Chapter 6, Section 6.2  
**Decision:** `advisor_edit`  
**Purpose:** Describe beta accurately as a scale parameter.

### Proposed replacement language

> In the ABM, \(\beta\) is a scale parameter governing the magnitude of the
> crime-related enticement term. Because \(F>0\), the value of
> \(E_{\mathrm{Crime}}(0)\) is \(\beta/(1+F)\), rather than \(\beta\). Moreover,
> this term decreases toward zero as time since the most recent crime increases.
> Thus, \(\beta\) should not be interpreted as a long-run enticement level
> sustained by the city.

### Advisor note

If the calculation uses \(F \approx 0.07\), report whether the selected
\(\beta=0.02\) is a rounded baseline value or replace it with the derived value.


## 030 — ODE parameter theta

**Location:** Chapter 6, Section 6.3  
**Decision:** `student_revision`  
**Purpose:** Describe theta as a cross-model matching choice rather than an empirical estimate.

### Proposed replacement language

> We select the baseline value of \(\theta\) by matching the ODE’s enticement
> scale to a simplified ABM benchmark. This procedure is not an empirical
> calibration to a particular city. It is a cross-model matching choice made under
> the assumptions of a background-only ABM, a specified criminal population, an
> approximately one-crime-per-day regime, and the simplified ODE condition
> \(E_0=0\).

### Student instruction

> State the ABM benchmark configuration completely, including lattice size,
> criminal population, number of replications, averaging procedure, and how the
> approximate one-crime-per-day regime was established.



## 026 — Relating ABM and ODE diffusion

**Location:** Chapter 6, Section 6.4.2  
**Decision:** `discuss_with_student`  
**Purpose:** Request confirmation before inserting final language.

### Student instruction

> Please verify the derivation relating the ABM diffusion coefficient \(\zeta\)
> to the ODE mixing parameter \(\eta\). Explain whether the goal is an exact
> coefficient match, an order-of-magnitude match, or a reference-geometry match.
> In particular, address how one shared value of \(\eta\) is used when the
> greened and non-greened patches have different areas and therefore different
> factors \(L/A_i\).

### Advisor note

Do not finalize replacement dissertation language until the intended mathematical
mapping is confirmed.



## 035 — Framing the parametric study

**Location:** Chapter 7, Sections 7.1–7.3  
**Decision:** `advisor_edit`  
**Purpose:** Present the chapter as a sensitivity comparison rather than a
demonstration of parameter equivalence.

### Proposed replacement language

> The purpose of this parametric study is to compare qualitative sensitivity
> patterns in the ODE and ABM under related parameter regimes. Because the models
> represent space, diffusion, and crime-related enticement differently, identical
> numerical parameter values are not expected to produce identical outputs.
> Accordingly, we examine whether the models exhibit similar directional trends,
> identify parameter regimes in which their behavior differs, and use those
> differences to clarify the effects of the respective modeling assumptions.

## 034 — Parametric-study protocol

**Location:** Chapter 7, Section 7.1  
**Decision:** `student_revision`  
**Purpose:** Make the ABM sensitivity study reproducible and qualify uncertainty.

### Student instruction

> Add a compact experimental-design table that lists every value used for
> \(\beta\), \(\theta\), \(\gamma\), and the diffusion parameter; identifies which
> parameters were held fixed in each figure; and gives the number of independent
> ABM replications, random-seed treatment, transient/burn-in period, sampling
> window, and summary statistic for every parameter combination.

> Replace “a few simulations” with the exact number of independent replications.
> If computational limits prevented enough replications to resolve a pattern,
> state that limitation directly and avoid strong conclusions about the affected
> ABM behavior.

## 036 — Interpretation of low gamma

**Location:** Chapter 7, Section 7.3.2.1  
**Decision:** `advisor_edit`  
**Purpose:** Avoid unsupported real-world analogies.

### Proposed replacement language

> At the smallest values of \(\gamma\), the modeled return of removed criminals to
> active behavior is sufficiently low that few crimes occur during the simulated
> time horizon. Consequently, the dynamic enticement term remains low even as the
> crime-related enticement parameter increases. This is a property of the modeled
> recruitment-and-removal mechanism; it should not be interpreted as a direct
> representation of policing, guardianship, or a crime-free real-world setting.


## 042 — Reframed conclusion

**Location:** Chapter 8, final paragraphs  
**Decision:** `student_revision`  
**Purpose:** State the dissertation’s contribution accurately.

### Proposed replacement conclusion

> This dissertation develops and analyzes complementary ODE and agent-based models
> of a stylized greening intervention. Within the model structures and parameter
> regimes considered, lower baseline enticement in a greened region produces lower
> modeled enticement and crime-related outcomes in that region. The agent-based
> model further produces lower modeled enticement in a boundary region than in a
> matched reference region, a qualitative spatial pattern consistent with empirical
> studies reporting benefits near greened sites.
>
> These findings are theoretical and assumption-dependent. The models are not
> calibrated to a particular city and do not estimate the causal effect of a specific
> real-world greening program. Instead, they provide a framework for studying how
> assumptions about spatial structure, movement, enticement dynamics, and greened
> area may influence modeled crime patterns. Empirical calibration, validation, and
> additional spatial experiments are necessary before drawing implementation-specific
> recommendations for cities.

## 044 — Size of a greened zone

**Location:** Chapter 8, discussion of Experiment 1  
**Decision:** `student_revision`  
**Purpose:** State the fixed-city size result without overclaiming.

### Proposed replacement language

> In the fixed-city simulations, larger greened areas were associated with lower
> citywide modeled enticement, criminal density, and crime density. This pattern
> must be interpreted cautiously because increasing greened area also increases the
> proportion of sites assigned to the lower-enticement greened class. The
> boundary-versus-reference comparison provides more direct evidence of a local
> spatial pattern: within the modeled configurations, boundary regions often had
> lower enticement than matched nonadjacent reference regions.
>
> The simulations therefore do not identify a universal minimum effective size for
> real-world greening interventions. Rather, they show how modeled spatial outcomes
> change as greened area varies under the assumptions of this ABM.



## 044 — Distribution of a fixed greened area

**Location:** Chapter 8, discussion of Experiment 2  
**Decision:** `student_revision`  
**Purpose:** Accurately describe the configuration comparison.

### Proposed replacement language

> For the three configurations studied—one \(10 \times 10\) zone, two
> \(5 \times 10\) zones, and four \(5 \times 5\) zones—the citywide outcomes showed
> relatively small differences. Because these configurations differ not only in the
> number of greened zones but also in perimeter, boundary-zone geometry, and spatial
> arrangement, the experiment does not isolate the effect of zone count alone.
> Within the modeled cases considered, the results do not strongly favor one of the
> three configurations. Further experiments would be needed before drawing a
> general conclusion about the preferred spatial distribution of real-world
> greening efforts.



| ID | Scope | Research question | Approach | Varied feature | Primary outputs | Intended contribution |
|---|---|---|---|---|---|---|
| EXP-01 | Completed | How do modeled outcomes change as greened area increases? | ABM simulation experiment | Greened-area size | Enticement; criminal density; crime density | Examine local boundary patterns and fixed-city composition effects |
| EXP-02 | Completed | How do specified configurations with equal total greened area compare? | ABM configuration comparison | Number, geometry, and placement of greened zones | Enticement; criminal density; crime density | Compare one large zone with several smaller configurations; identify spatial questions for further study |
| EXP-03 | Completed | Does the ODE have the expected homogeneous stable limiting behavior when specified mechanisms are removed? | ODE limiting-case equilibrium analysis | Broken-windows and near-repeat mechanisms removed | Equilibrium; stability; enticement; criminal density | Establish internal consistency of the ODE |
| EXP-04 | Completed | Does the one-zone ODE reduction admit a stable equilibrium? | ODE limiting-case equilibrium analysis | One-zone reduction | Equilibrium; stability; enticement; criminal density | Establish bounded long-run model behavior |
| EXP-05 | Future work | Does the size result persist as city size changes? | ABM sensitivity study | City size with greened-zone size controlled | Enticement; criminal density; crime density | Separate greened-area effects from fixed-city composition effects |
| EXP-06 | Future work | How far does the modeled boundary effect extend? | ABM spatial-extension study | Number and width of boundary zones | Zone-specific enticement; criminal density; crime density | Characterize modeled spatial range of the boundary effect |
| EXP-07 | Future work | Can a multi-patch ODE reproduce relevant qualitative ABM patterns? | ODE model extension and comparison | Patch areas, interfaces, and zone number | Enticement; criminal density; crime density | Clarify which ABM spatial patterns persist in a reduced ODE framework |













































































