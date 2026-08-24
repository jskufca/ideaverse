Here is the system of four coupled differential equations you provided:

$$
\(\begin{split}\.{c}_{g}&=\frac{\lambda }{A_{g}}\left(-L\frac{E_{n}}{E_{g}}c_{g}+L\frac{E_{g}}{E_{n}}c_{n}\right)+\gamma _{g}\left(N-c_{g}A_{g}-c_{n}A_{n}\right)-rE_{g}c_{g}\\ \.{E}_{g}&=\theta rE_{g}c_{g}+\frac{\eta L}{A_{g}}\left(E_{n}-E_{g}\right)-\omega \left(E_{g}-E_{g_{o}}\right)\\ \.{c}_{n}&=\frac{\lambda }{A_{n}}\left(-L\frac{E_{g}}{E_{n}}c_{n}+L\frac{E_{n}}{E_{g}}c_{g}\right)+\gamma _{n}\left(N-c_{g}A_{g}-c_{n}A_{n}\right)-rE_{n}c_{n}\\ \.{E}_{n}&=\theta rE_{n}c_{n}-\frac{\eta L}{A_{n}}\left(E_{n}-E_{g}\right)-\omega \left(E_{n}-E_{n_{o}}\right)\end{split}\)
$$
This looks like a system modeling population dynamics, resource consumption, or economic/ecological migration between two groups or regions (\(g\) and \(n\)).

If you are ready to analyze this system, I can help you:

- Find the **steady-state equilibria** by setting the derivatives to zero.
- Linearize the system to analyze **local stability**.
- Identify the **physical meaning** of specific parameters like \(\lambda \), \(\gamma \), or \(\theta \).
    

How would you like to proceed with these equations?

Good interpretation. subscript g stands for green. Lets assume there is no green area (green area goes to 0) ... and consequently to opportunity for transport between two areas. Then this simplifies the dynamics on the n (normal area) and i think we have a system of two equations. Give me that resultant system.

The simplified system for the normal area consists of these two equations:

\(\begin{split}\.{c}_{n}&=\gamma _{n}\left(N-c_{n}A_{n}\right)-rE_{n}c_{n}\\ \.{E}_{n}&=\theta rE_{n}c_{n}-\omega \left(E_{n}-E_{n_{o}}\right)\end{split}\)

Key Changes Made

- **Removed Transport Terms**: All terms containing \(L\) (representing cross-area transport or exchange) drop to zero.
- **Removed Green Variables**: The green area population size (\(c_{g}A_{g}\)) becomes zero.
- **Isolated Normal Dynamics**: The remaining terms focus solely on internal growth, consumption, and resource depletion within the normal area.

If you are ready to study this simplified model, we can:

- Find the **nullclines** to graph the phase portrait.
- Calculate the **equilibria** positions.
- Determine if it exhibits **bistability** or a single steady state.

Which of these analytical steps should we take next?

For simplicity, remove the n subscript as non informative

The resulting system of equations simplifies to:

\(\begin{split}\.{c}&=\gamma \left(N-cA\right)-rEc\\ \.{E}&=\theta rEc-\omega \left(E-E_{o}\right)\end{split}\)

Elements Retained

- **Internal growth / replenishment**: Driven by \(\gamma \) and \(\omega \) terms.
- **Resource consumption / depletion**: Driven by the \(rEc\) interaction terms.
- **Steady-state reference points**: Retained the baseline value \(E_{o}\).

To advance our analysis, I can help you:

- Solve for the **steady-state equilibria** by setting \(\dot c = 0\) and \(\dot E = 0\).
- Derive the **Jacobian matrix** to prepare for stability analysis.
- Plot the **nullclines** to map out the system's trajectories.

Which of these steps would you like to take next?

can you solve for equilibria. you may assume all parameters are constant and non-negative.

To find the equilibria of the system, we set the time derivatives to zero (\(\dot c = 0\) and \(\dot E = 0\)) and solve for the state variables. The system possesses a **single physically meaningful equilibrium** given by: [[1](https://www.vaia.com/en-us/textbooks/math/nonlinear-dynamics-and-chaos-with-applications-to-physics-biology-chemistry-and-engineering-1994-edition/chapter-7/problem-8-consider-ddotxa-dotxleftx2dotx2-1rightx0-wherea0-a/), [2](https://mathinsight.org/assess/math1241/discrete_dynamical_system_elementary_biology_problems?seed=72017580&n=1)]

\(E^{*}=\frac{-(\omega \gamma A-\omega rE_{o}-\theta r\gamma N)+\sqrt{(\omega \gamma A-\omega rE_{o}-\theta r\gamma N)^{2}+4\omega ^{2}r\gamma AE_{o}}}{2\omega r}\)

\(c^{*}=\frac{\gamma N}{\gamma A+rE^{*}}\)

---

1. Set Derivatives to Zero

To find the steady-state equilibria, set both differential equations equal to zero: [[1](https://pmc.ncbi.nlm.nih.gov/articles/PMC4559563/), [2](https://math.stackexchange.com/questions/1383611/equilibrium-points-second-order-differential)]

\(\gamma (N-cA)-rEc=0\)  
\(\theta rEc-\omega (E-E_{o})=0\)

2. Isolate the Population Variable

From the first equation, we group the terms containing \(c\) to express it as a function of \(E\):

\(\gamma N-\gamma Ac-rEc=0\)  
\(c(\gamma A+rE)=\gamma N\)  
\(c=\frac{\gamma N}{\gamma A+rE}\)

3. Substitute into Resource Equation

Substitute the expression for \(c\) into the second equation:

\(\theta rE\left(\frac{\gamma N}{\gamma A+rE}\right)-\omega (E-E_{o})=0\)

To eliminate the denominator, multiply the entire equation by \((\gamma A + r E)\):

\(\theta r\gamma NE-\omega (E-E_{o})(\gamma A+rE)=0\)

4. Formulate the Quadratic Equation

Expand and rearrange the terms into standard quadratic form (\(aE^2 + bE + c_{quadratic} = 0\)): [[1](https://www.vaia.com/en-us/textbooks/math/calculus-and-its-applications-10-edition/chapter-0/problem-94-find-the-equilibrium-point-for-each-pair-of-deman/)]

\(\theta r\gamma NE-\omega \left(rE^{2}+\gamma AE-rE_{o}E-\gamma AE_{o}\right)=0\)  
\(-\omega rE^{2}-(\omega \gamma A-\omega rE_{o}-\theta r\gamma N)E+\omega \gamma AE_{o}=0\)

Multiplying by \(-1\) gives:

\(\omega rE^{2}+(\omega \gamma A-\omega rE_{o}-\theta r\gamma N)E-\omega \gamma AE_{o}=0\)

5. Solve for the Positive Root

Apply the quadratic formula \(E = \frac{-b \pm \sqrt{b^2 - 4ac_{quadratic}}}{2a}\) where: [[1](https://www.pearson.com/channels/calculus/study-guides/step-by-step-guidance-for-differential-calculus)]

- \(a = \omega r\)
- \(b = \omega \gamma A - \omega r E_o - \theta r \gamma N\)
- \(c_{quadratic} = -\omega \gamma A E_o\)

\(E^{*}=\frac{-b\pm \sqrt{b^{2}-4ac_{quadratic}}}{2a}\)

Because the product of the roots \(\frac{c_{quadratic}}{a} = \frac{-\omega \gamma A E_o}{\omega r}\) is strictly negative, one root is always positive and one is negative. Since \(E\) represents a resource/energy level, only the positive root is physically valid: [[1](https://roymech.org/Related/Control/Routh_Criteria.html), [2](https://www.themathdoctors.org/challenging-inverse-trig-and-polynomial-equations/)]

\(E^{*}=\frac{-(\omega \gamma A-\omega rE_{o}-\theta r\gamma N)+\sqrt{(\omega \gamma A-\omega rE_{o}-\theta r\gamma N)^{2}+4\omega ^{2}r\gamma AE_{o}}}{2\omega r}\)

Substituting \(E^{*}\) back into the expression from Step 2 yields the corresponding equilibrium value for \(c^{*}\):

\(c^{*}=\frac{\gamma N}{\gamma A+rE^{*}}\)

---

✅ Equilibrium Solution

The system possesses a single unique, physically realistic equilibrium point \((c^*, E^*)\) defined by:

\(E^{*}=\frac{-(\omega \gamma A-\omega rE_{o}-\theta r\gamma N)+\sqrt{(\omega \gamma A-\omega rE_{o}-\theta r\gamma N)^{2}+4\omega ^{2}r\gamma AE_{o}}}{2\omega r}\)

\(c^{*}=\frac{\gamma N}{\gamma A+rE^{*}}\)

If you want to continue evaluating this model, I can help you:

- Linearize the system around this equilibrium using the **Jacobian matrix**
- Analyze the **stability conditions** (e.g., whether it is a stable node or an attractor)
- Evaluate the system under specific **parameter limits** (such as when consumption \(r \to 0\)) [[1](https://www.vaia.com/en-us/textbooks/math/differential-equations-with-boundary-value-problems-2-edition/chapter-10/problem-11-show-that-the-origin-is-an-equilibrium-point-and-/), [2](https://www.sciencedirect.com/science/article/pii/S0264999314001825)]

What would you like to investigate next?

![](https://encrypted-tbn3.gstatic.com/faviconV2?url=https://www.vaia.com&client=AIM&size=128&type=FAVICON&fallback_opts=TYPE,SIZE,URL)![](https://encrypted-tbn2.gstatic.com/faviconV2?url=https://mathinsight.org&client=AIM&size=128&type=FAVICON&fallback_opts=TYPE,SIZE,URL)![](https://encrypted-tbn1.gstatic.com/faviconV2?url=https://pmc.ncbi.nlm.nih.gov&client=AIM&size=128&type=FAVICON&fallback_opts=TYPE,SIZE,URL)

10 sites

- [](https://www.vaia.com/en-us/textbooks/math/nonlinear-dynamics-and-chaos-with-applications-to-physics-biology-chemistry-and-engineering-1994-edition/chapter-7/problem-8-consider-ddotxa-dotxleftx2dotx2-1rightx0-wherea0-a/)
    
    Problem 8 Consider \(\ddot{x}+a \dot{x}\le... [FREE SOLUTION]
    
    Fixed Points Fixed points, sometimes referred to as equilibria in dynamical systems, are points in phase space where the system do...
    
    ![](https://encrypted-tbn3.gstatic.com/faviconV2?url=https://www.vaia.com&client=AIM&size=128&type=FAVICON&fallback_opts=TYPE,SIZE,URL)
    
    www.vaia.com
    
- [](https://mathinsight.org/assess/math1241/discrete_dynamical_system_elementary_biology_problems?seed=72017580&n=1)
    
    Elementary discrete dynamical system biology problems
    
    Hint Just plug in a variable (we often use E) for all values of the state variables in the dynamical system. Solving for that vari...
    
    ![](https://encrypted-tbn2.gstatic.com/faviconV2?url=https://mathinsight.org&client=AIM&size=128&type=FAVICON&fallback_opts=TYPE,SIZE,URL)
    
    Math Insight
    
- [](https://pmc.ncbi.nlm.nih.gov/articles/PMC4559563/)
    
    Competition for resources: complicated dynamics in the simple Tilman model
    
    In a stability analysis we first find the stationary or equilibrium states of the system of equations by solving the dynamical equ...
    
    ![](https://encrypted-tbn1.gstatic.com/faviconV2?url=https://pmc.ncbi.nlm.nih.gov&client=AIM&size=128&type=FAVICON&fallback_opts=TYPE,SIZE,URL)
    
    National Institutes of Health (NIH) | (.gov)
    

Show all

briefly ... why only one "physically meaningful". I assume that means you are requiring E and c to be real and non-negative

Yes, "physically meaningful" means both \(c^{*}\) and \(E^{*}\) must be real and non-negative (\(c^* \ge 0, E^* \ge 0\)). Here is exactly why only one root qualifies:

- **The resource equation is a quadratic with a negative \(y\)-intercept:** In our quadratic equation, the constant term (\(c_{quadratic} = -\omega \gamma A E_o\)) is strictly negative because all parameters are positive.
- **Opposite signs rule:** By Descartes' Rule of Signs (or via the product of the roots \(\frac{c_{quadratic}}{a} < 0\)), any quadratic equation with a negative constant term and a positive leading coefficient _must_ have exactly one positive real root and one negative real root. [[1](https://www.themathdoctors.org/exploring-descartes-rule-of-signs/)]
- **Negative root discarded:** The negative root for \(E^{*}\) is non-physical because resource levels cannot be below zero.
- **Guaranteed positive population:** Plugging the single positive root \(E^{*}\) back into \(c^* = \frac{\gamma N}{\gamma A + r E^*}\) guarantees that \(c^{*}\) is also real, positive, and non-zero.

Would you like to analyze the **stability** of this single equilibrium, or should we look at how it behaves under specific **parameter limits**?

![](https://encrypted-tbn1.gstatic.com/faviconV2?url=https://www.themathdoctors.org&client=AIM&size=128&type=FAVICON&fallback_opts=TYPE,SIZE,URL)

1 site

- [](https://www.themathdoctors.org/exploring-descartes-rule-of-signs/)
    
    Exploring Descartes’ Rule of Signs – The Math Doctors
    
    Mar 20, 2026 — Descartes' Rule of Signs mentions only POSITIVE and NEGATIVE roots! So it tells us that your equation has 0 positive roots and 0 n...
    
    ![](https://encrypted-tbn3.gstatic.com/images?q=tbn:ANd9GcR_aWP7AjTyWRLwRRH8aKFtV6MKaBqhjLEpNhiDdMDxyE0INTqAp3j2TeRvH-xR6Yg1DtyYhg)
    
    ![](https://encrypted-tbn1.gstatic.com/faviconV2?url=https://www.themathdoctors.org&client=AIM&size=128&type=FAVICON&fallback_opts=TYPE,SIZE,URL)
    
    The Math Doctors
    

I would like to analyze stability (or, equivalently) give conditions for stability of that fixed point. Linear stability analysis is sufficient.

The equilibrium point \((c^*, E^*)\) is **always locally asymptotically stable** for all positive, non-negative parameter values. No additional parameter conditions are required.

---

1. The Jacobian Matrix

To perform linear stability analysis, we construct the Jacobian matrix \(J\) by taking the partial derivatives of our system: [[1](https://www.vaia.com/en-us/textbooks/math/notes-on-diffy-qs-differential-equations-for-engineers-2020-edition/chapter-8/problem-1-for-the-systems-below-find-and-classify-the-critic/)]

- \(f(c, E) = \gamma(N - cA) - rEc\)
- \(g(c, E) = \theta r Ec - \omega(E - E_o)\)

Evaluating these partial derivatives at the equilibrium point \((c^*, E^*)\) yields:

\(J=\left(\begin{matrix}\frac{\partial f}{\partial c}&\frac{\partial f}{\partial E}\\ \frac{\partial g}{\partial c}&\frac{\partial g}{\partial E}\end{matrix}\right)=\left(\begin{matrix}-(\gamma A+rE^{*})&-rc^{*}\\ \theta rE^{*}&\theta rc^{*}-\omega \end{matrix}\right)\)

2. Simplifying the Elements Using Equilibrium Conditions

We can simplify the diagonal elements by using the fact that at equilibrium, \(\dot E = 0\).  
From \(\theta r E^* c^* - \omega(E^* - E_o) = 0\), we isolate \(\theta r c^*\): [[1](https://www.chegg.com/homework-help/questions-and-answers/2-let-demand-supply-qd-50-2p-qs-10-3p-market-price-adjustment-process-proportional-excess--q48857937)]

\(\theta rc^{*}=\frac{\omega (E^{*}-E_{o})}{E^{*}}=\omega -\frac{\omega E_{o}}{E^{*}}\)

Substitute this into the \(\frac{\partial g}{\partial E}\) term:

\(\frac{\partial g}{\partial E}=\left(\omega -\frac{\omega E_{o}}{E^{*}}\right)-\omega =-\frac{\omega E_{o}}{E^{*}}\)

This simplifies the Jacobian to:

\(J=\left(\begin{matrix}-(\gamma A+rE^{*})&-rc^{*}\\ \theta rE^{*}&-\frac{\omega E_{o}}{E^{*}}\end{matrix}\right)\)

3. Stability Criteria

A 2-dimensional system is locally asymptotically stable if and only if the Jacobian satisfies two conditions:

1. **Trace is negative** (\(\text{Tr}(J) < 0\))
2. **Determinant is positive** (\(\text{Det}(J) > 0\))

Condition 1: Trace

\(\text{Tr}(J)=-(\gamma A+rE^{*})-\frac{\omega E_{o}}{E^{*}}\)  
Because all parameters (\(\gamma, A, r, \omega, E_o\)) and the equilibrium value \(E^{*}\) are positive, both terms in the sum are negative.

- \(\text{Tr}(J) < 0\) is **always true**.

Condition 2: Determinant

\(\text{Det}(J)=\left[-(\gamma A+rE^{*})\cdot \left(-\frac{\omega E_{o}}{E^{*}}\right)\right]-\left[(-rc^{*})\cdot (\theta rE^{*})\right]\)  
\(\text{Det}(J)=\frac{\omega E_{o}(\gamma A+rE^{*})}{E^{*}}+\theta r^{2}c^{*}E^{*}\)  
Every individual parameter and variable in this expression is strictly positive.

- \(\text{Det}(J) > 0\) is **always true**.

---

✅ Conclusion

Because \(\text{Tr}(J) < 0\) and \(\text{Det}(J) > 0\) hold universally for any valid physical parameters, the system **never undergoes a bifurcation** or becomes unstable. The fixed point is unconditionally stable.

If you want to explore further, I can help you:

- Determine whether the approach to equilibrium is **exponentially damped** or **oscillatory** (by checking if the eigenvalues have imaginary parts).
- Check the sensitivity of the system to changes in a specific parameter like \(\theta \) or \(r\). [[1](https://www.sciencedirect.com/topics/mathematics/point-of-equilibrium)]

How would you like to proceed?

![](https://encrypted-tbn3.gstatic.com/faviconV2?url=https://www.vaia.com&client=AIM&size=128&type=FAVICON&fallback_opts=TYPE,SIZE,URL)![](https://encrypted-tbn2.gstatic.com/faviconV2?url=https://www.chegg.com&client=AIM&size=128&type=FAVICON&fallback_opts=TYPE,SIZE,URL)![](https://encrypted-tbn1.gstatic.com/faviconV2?url=https://www.sciencedirect.com&client=AIM&size=128&type=FAVICON&fallback_opts=TYPE,SIZE,URL)

3 sites

- [](https://www.vaia.com/en-us/textbooks/math/notes-on-diffy-qs-differential-equations-for-engineers-2020-edition/chapter-8/problem-1-for-the-systems-below-find-and-classify-the-critic/)
    
    Problem 1 For the systems below, find and ... [FREE SOLUTION]
    
    It ( Jacobian Matrix ) provides a linear approximation to the system at a given point and is constructed using partial derivatives...
    
    ![](https://encrypted-tbn3.gstatic.com/faviconV2?url=https://www.vaia.com&client=AIM&size=128&type=FAVICON&fallback_opts=TYPE,SIZE,URL)
    
    www.vaia.com
    
- [](https://www.chegg.com/homework-help/questions-and-answers/2-let-demand-supply-qd-50-2p-qs-10-3p-market-price-adjustment-process-proportional-excess--q48857937)
    
    Solved 2. Let the demand and supply be Qd = 50 – 2P, Qs =
    
    Apr 29, 2020 — we need to find the equilibrium points. Equilibrium occurs when d P d t = 0 .
    
    ![](https://encrypted-tbn1.gstatic.com/images?q=tbn:ANd9GcTqMd8CWL7scdsTKZ6eyF_D9zUitZ-cfzJXpOcGNbtODJWIfUWNsh_xTFZF70_cy-n-D5gZYQ)
    
    ![](https://encrypted-tbn2.gstatic.com/faviconV2?url=https://www.chegg.com&client=AIM&size=128&type=FAVICON&fallback_opts=TYPE,SIZE,URL)
    
    Chegg
    
- [](https://www.sciencedirect.com/topics/mathematics/point-of-equilibrium)
    
    Point of Equilibrium - an overview
    
    If all the eigenvalues of the matrix are on the imaginary axis, and at least one pair is pure imaginary and nonzero, the equilibri...
    
    ![](https://encrypted-tbn1.gstatic.com/images?q=tbn:ANd9GcSU2ddNrmVw90YKYMN_7Pv2pWLJ5Ln5Tg2fSU8lbfblgTQMxLb3C66c5Te-YW4p1zS1urfWCQ)
    
    ![](https://encrypted-tbn1.gstatic.com/faviconV2?url=https://www.sciencedirect.com&client=AIM&size=128&type=FAVICON&fallback_opts=TYPE,SIZE,URL)
    
    ScienceDirect.com
    

that 2d stability criteria is equivalent to routh horwitz --- short answer please

Yes. For a 2-dimensional system, the conditions \(\text{Tr}(J) < 0\) and \(\text{Det}(J) > 0\) are exactly identical to the Routh-Hurwitz stability criteria for its characteristic polynomial \(s^2 - \text{Tr}(J)s + \text{Det}(J) = 0\).

If you want to look at this further, I can help you:

- Check for **oscillations** using the discriminant.
- Find the **speed of convergence** from the eigenvalues.

What would you like to do next?

yes. tell me whether stable node or stable spiral ... or the differentiating condition.

The system can be **either a stable node or a stable spiral**, depending entirely on the specific parameter values. [[1](https://www.vaia.com/en-us/textbooks/math/differential-equations-with-boundary-value-problems-4-edition/chapter-10/problem-16-classify-if-possible-each-critical-point-of-the-g/), [2](https://sheffield.pressbooks.pub/introducingmathematicalbiology/chapter/the-sir-model-with-demographics/), [3](https://www.vaia.com/en-us/textbooks/math/differential-equations-with-boundary-value-problems-4-edition/chapter-10/problem-18-classify-if-possible-each-critical-point-of-the-g/)]

The differentiating condition is determined by the **discriminant (\(\Delta \))** of the characteristic equation, \(\Delta = \text{Tr}(J)^2 - 4\,\text{Det}(J)\).

---

The Differentiating Condition

By expanding and simplifying the trace and determinant using the equilibrium values, the discriminant takes the following form:

\(\Delta =\left((\gamma A+rE^{*})-\frac{\omega E_{o}}{E^{*}}\right)^{2}-4\theta r^{2}c^{*}E^{*}\)

- **Stable Node (No Oscillations):** Occurs when \(\Delta \ge 0\). This happens when the natural decay/replenishment rates dominate over the consumer-resource interaction. [[1](https://www.cds.caltech.edu/~murray/courses/cds101/fa02/faq/02-10-23_lyapexact.html)]
- **Stable Spiral (Oscillatory Decay):** Occurs when \(\Delta < 0\). This happens when the consumption loop interaction term (\(4 \theta r^2 c^* E^*\)) is larger than the squared difference of the individual system recovery rates. [[1](https://runzhe-yang.science/2019-06-04-E-I/)]

Summary of Behaviors

- **High Consumption / Efficiency (\(\theta, r\) high):** Leads to \(\Delta < 0\). The system will **spiral** inward, meaning the population and resource levels will oscillate dynamically as they settle into equilibrium.
- **High Recovery / Low Interaction (\(\gamma, \omega\) high):** Leads to \(\Delta \ge 0\). The system behaves as a **node**, smoothly and exponentially decaying straight to equilibrium without any oscillatory bouncing.

If you have specific numerical values for your parameters, I can compute the exact value of \(\Delta \) to tell you which regime your specific system falls into. Would you like to test a specific parameter set?

![](https://encrypted-tbn3.gstatic.com/faviconV2?url=https://www.vaia.com&client=AIM&size=128&type=FAVICON&fallback_opts=TYPE,SIZE,URL)![](https://encrypted-tbn1.gstatic.com/faviconV2?url=https://sheffield.pressbooks.pub&client=AIM&size=128&type=FAVICON&fallback_opts=TYPE,SIZE,URL)![](https://encrypted-tbn3.gstatic.com/faviconV2?url=https://www.cds.caltech.edu&client=AIM&size=128&type=FAVICON&fallback_opts=TYPE,SIZE,URL)

5 sites

- [](https://www.vaia.com/en-us/textbooks/math/differential-equations-with-boundary-value-problems-4-edition/chapter-10/problem-16-classify-if-possible-each-critical-point-of-the-g/)
    
    Problem 16 Classify (if possible) each crit... [FREE SOLUTION]
    
    Classify (if possible) each critical point of the given plane autonomous system as a stable node, a stable spiral point, an unstab...
    
    ![](https://encrypted-tbn3.gstatic.com/faviconV2?url=https://www.vaia.com&client=AIM&size=128&type=FAVICON&fallback_opts=TYPE,SIZE,URL)
    
    www.vaia.com
    
- [](https://sheffield.pressbooks.pub/introducingmathematicalbiology/chapter/the-sir-model-with-demographics/)
    
    The SIR model with demographics – Introducing Mathematical Biology
    
    The stable equilibrium can be a node or a spiral depending on the precise parameter values. Generally, high γ , intermediate R 0 a...
    
    ![](https://encrypted-tbn3.gstatic.com/images?q=tbn:ANd9GcQDsqPZ0LBGmoxo_mB9PltpQ3RxmzZI0tCATSn5AJb5HwJ2ohfaq-3NpU54DwEiD4P25H2Msw)
    
    ![](https://encrypted-tbn1.gstatic.com/faviconV2?url=https://sheffield.pressbooks.pub&client=AIM&size=128&type=FAVICON&fallback_opts=TYPE,SIZE,URL)
    
    Pressbooks.pub
    
- [](https://www.vaia.com/en-us/textbooks/math/differential-equations-with-boundary-value-problems-4-edition/chapter-10/problem-18-classify-if-possible-each-critical-point-of-the-g/)
    
    Problem 18 Classify (if possible) each crit... [FREE SOLUTION]
    
    Classify (if possible) each critical point of the given plane autonomous system as a stable node, a stable spiral point, an unstab...
    
    ![](https://encrypted-tbn3.gstatic.com/faviconV2?url=https://www.vaia.com&client=AIM&size=128&type=FAVICON&fallback_opts=TYPE,SIZE,URL)
    
    www.vaia.com
    

Show all

this model is about criminal density and the broken window effect. c is criminal density and E is enticement. rEc gives a crime rate and theta is the impact of those crimes on the enticement level. gamma is related to the resting time (between crime acts). omega governs how quickly the broken window effect dissipates and allows the enticement to return to baseline. Interpret these results in light of that understanding.

Based on your model's definitions, the mathematical stability of this system provides powerful insights into the long-term dynamics of crime and urban decay.

1. The Meaning of Universal Stability

Because the equilibrium point is **unconditionally stable**, the system always reaches a predictable, self-regulating balance of criminal activity and enticement. No matter how high crime rates spike temporarily, or how severely a neighborhood decays, the system will neither explode into an infinite crime loop nor entirely eradicate crime on its own. It always anchors back to a baseline dictated by the local environment.

2. The Stable Spiral: The "Boom-and-Bust" Crime Cycle

When the discriminant is negative (Δ < 0), the neighborhood experiences a **stable spiral**. This happens when crime has a high impact on the environment (θ is large) or criminal activity is highly efficient (r is large).

- **The Dynamic:** A rise in crime (c) drives up enticement (E) via the broken windows effect. The degraded environment then attracts _more_ crime. However, this creates a temporary peak. High crime eventually exhausts the neighborhood's vulnerability, or the criminal population over-saturates the area. Crime then drops, allowing the broken windows effect to slowly dissipate (ω) and the environment to clean up, which drops crime further. [[1](https://climber.uml.edu.ni/HomePages/browse/M3a724/TheBrokenWindowsTheory.pdf), [2](https://study.com/learn/lesson/broken-window-theory.html)]
- **The Result:** The neighborhood undergoes visible cycles of "crisis and recovery"—waves of high crime and decay followed by periods of relative calm—before finally settling into its long-term equilibrium.

3. The Stable Node: Smooth Stabilization

When the discriminant is positive (Δ ≥ 0), the neighborhood undergoes a **stable node** transition. This happens when the baseline recovery rate of the neighborhood (ω) or the criminal resting rate (γ) dominates over the broken window feedback loop.

- **The Dynamic:** If an influx of criminals enters the neighborhood, the environment degrades, but the community's internal resilience or cleanup speed (ω) is strong enough to buffer the shock.
- **The Result:** Instead of oscillating wildly, the criminal density and neighborhood decay adjust smoothly, steadily, and directly toward their final equilibrium values without any temporary "boom" or "bust" periods.

4. Policy and Intervention Implications

- **Altering the Equilibrium Point (\(c^*, E^*\)):** To permanently lower the final resting level of crime, policymakers must target the constants. Decreasing the environmental baseline (\(E_{o}\)) through active cleanup, lowering the total opportunity size (N), or reducing criminal efficiency (r) through policing will successfully shift the equilibrium to a safer state.
- **Altering the Experience (Δ):** If a city wants to avoid the disruptive, volatile cycles of the "stable spiral," they can invest heavily in increasing ω (faster abatement of broken windows, quicker graffiti removal). By doing so, they push the system into the "stable node" regime, ensuring that any localized disruptions dissolve smoothly without triggering a prolonged neighborhood crisis.

If you would like, we can explore how changing a specific policy lever (like increasing **graffiti cleanup speed** ω or changing **policing efficiency** r) shifts the exact **equilibrium coordinates** or changes the **cycle frequency**. What would you like to examine next?