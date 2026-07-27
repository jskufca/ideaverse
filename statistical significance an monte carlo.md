my phd student is doing research involving an ABM. Uses monte carlo to overcome the stochastic element. There are two KPIs that we expect to be the same, and someone on her committee suggested that she need to to a statistical significance test to be able to support that claim. However, I knoww that ... if you collect enough data you can always reach statistical significance, and ... since its simulation ... we could always just get more data. So ... i know the suggested approach (significance testing) is just not meaningful, but I was hoping you could identify a reference that makes this claim explicit.

Completed 7 steps

Both your intuition and the phenomenon are well documented in the statistics and simulation literature. Here are the strongest references to cite in your student's defense of methodology:

## Simulation-specific reference (most directly applicable)

**Kleijnen, J.P.C.** "Verification and Validation of Simulation Models," _European Journal of Operational Research_, 82(1), 1995, pp. 145–162 (earlier working-paper version: Tilburg University, FEW 542, 1992).[](https://pure.uvt.nl/ws/files/1139862/KJ5613411.pdf)

Kleijnen makes the point explicit for simulation output analysis: "Strictly speaking, the simulation is only a model (not reality), so a large enough sample size nn would show that bb is not exactly zero." He goes on to note that with a fixed significance level, increasing nn only trades off Type I vs. Type II error — it doesn't tell you whether the discrepancy is _practically_ meaningful. This is a canonical citation in the discrete-event/ABM validation literature for exactly the argument you're making.[](https://pure.uvt.nl/ws/files/1139862/KJ5613411.pdf)

## General statistics reference (broadly citable, very well known)

**Lin, M., Lucas, H.C., & Shmueli, G.** "Research Commentary—Too Big to Fail: Large Samples and the p-Value Problem," _Information Systems Research_, 24(4), 2013, pp. 906–917.[](https://www.stat.ntu.edu.tw/download/%E6%95%99%E5%AD%B8%E6%96%87%E4%BB%B6/bigdata/Research%20Commentary%20-%20Too%20Big%20to%20Fail%20Large%20Samples%20and%20the%20p-Value%20Problem.pdf)

Their core argument, quoting Cohen: "The null hypothesis, taken literally... is always false in the real world... If it is false, even to a tiny degree, it must be the case that a large enough sample will produce a significant result and lead to its rejection." They show formally that under a consistent estimator, the p-value converges to 0 as n→∞n→∞ unless the parameter is _exactly_ equal to the null value. This is a widely-cited paper in IS/analytics and pairs well with the Kleijnen citation for a broader audience/committee member.[](https://www.stat.ntu.edu.tw/download/%E6%95%99%E5%AD%B8%E6%96%87%E4%BB%B6/bigdata/Research%20Commentary%20-%20Too%20Big%20to%20Fail%20Large%20Samples%20and%20the%20p-Value%20Problem.pdf)

## The original source of the "null is always false" argument

**Cohen, J.** "The Earth Is Round (p < .05)," _American Psychologist_, 49(12), 1994, pp. 997–1003. This is the classic psychology-methodology paper (quoted by Lin et al. above) making the same point in general terms — worth citing if the committee wants the foundational source rather than a domain-specific application.

For the write-up, the strongest framing is: cite Kleijnen for the simulation-specific version of the argument (since replications/sample size in Monte Carlo studies are directly analogous to "just running more replications"), and cite Lin, Lucas & Shmueli (or Cohen) for the general statistical principle that makes it a known, established critique rather than an ad hoc objection. A constructive alternative to offer the committee is to report effect sizes and confidence/tolerance intervals around the KPI difference rather than (or alongside) a p-value — that's the standard remedy proposed in both papers.

## Implications

The suggestion to use [[common language effect size]] matches with above issues.