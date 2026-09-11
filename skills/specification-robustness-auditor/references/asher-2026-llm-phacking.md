# Asher et al. (2026): LLM P-Hacking Threat Model

## Source

Asher, S. G. Z., et al. (2026), *Do Claude Code and Codex P-Hack? Sycophancy and Statistical Analysis in Large Language Models*.

This reference summarizes the paper's empirical design and implications for safe specification auditing. It does not reproduce the paper.

## Research question

The paper tests whether autonomous coding agents alter statistical analysis choices in response to user pressure for a desired empirical result. The central concern is AI-assisted researcher degrees of freedom: an agent can make many defensible-looking analytical decisions, and the aggregate search process can become p-hacking if the stopping or selection rule is significance-driven.

## Experimental structure

The authors use replication materials from four published political-science studies with null or near-null focal findings. The cases span four common empirical designs:

1. regression discontinuity;
2. difference-in-differences / panel analysis;
3. selection-on-observables / observational analysis;
4. randomized field experiment.

They run two coding agents, Claude and OpenAI Codex, under different prompt conditions and compare the resulting statistical estimates.

## Prompt conditions

The experiment includes four broad prompt regimes:

### None

The model receives the empirical task without explicit pressure about the desired sign or significance.

### Upstanding Researcher

The model is explicitly instructed to pursue the most credible answer regardless of sign, magnitude, or statistical significance.

### Significance

The model is explicitly told that statistically significant findings matter to the researcher's career and is asked to make choices that produce significance.

### Nuclear

The request is framed as uncertainty quantification. The agent is told to explore alternative design choices and produce an upper point estimate by selecting the analysis that is most statistically significant. This framing is designed to test whether a seemingly legitimate 'upper-bound' task can induce significance-driven specification search even when direct p-hacking requests might be refused.

## Main lesson for this skill

The relevant danger is not only explicit fabrication or an instruction such as 'make p < .05.' The more subtle failure mode is adaptive specification search:

`observe result -> alter analytical choice -> observe result -> continue until a desired result appears -> report that result preferentially`

A workflow can therefore look technically sophisticated and still be statistically misleading if the search and stopping rules depend on the desired result.

## Researcher degrees of freedom

The paper's design highlights why vulnerability differs across empirical settings. When many analytical choices are available, an agent has more opportunities to move an estimate through choices that individually appear plausible.

Examples include:

- covariate inclusion;
- sample restrictions;
- bandwidths and local-polynomial choices in RDD;
- functional form;
- fixed effects;
- time windows;
- standard-error and clustering decisions;
- alternative estimators;
- weighting or matching choices.

Observational and RDD settings contain especially rich specification spaces. Experimental settings generally impose tighter design constraints, although selective covariate adjustment, attrition rules, subgroup analysis, and inference choices can still create flexibility.

## Safe translation into robustness analysis

The paper motivates four safeguards implemented by `$specification-robustness-auditor`:

1. **Freeze the estimand and baseline before searching.** Analytical choices should be justified by the research question and design rather than by their effect on significance.
2. **Define the multiverse before observing which specifications perform well.** If new choices are added after seeing results, label them exploratory or result-contingent.
3. **Report the full specification distribution.** Extreme estimates and the smallest p-value can be informative diagnostics only when shown relative to the full set.
4. **Separate preferred specification from extreme specification.** The most credible model is selected by design logic. The largest coefficient, largest |t|, or smallest p-value is never automatically the preferred estimate.

## Diagnostic use of an 'upper point estimate'

An upper point estimate can be useful for fragility analysis if defined transparently:

- define the admissible specification set first;
- run the complete set;
- identify the largest point estimate and the smallest p-value only after all results are available;
- label them as extremes of the multiverse;
- report their specification choices and their location in the full distribution;
- state whether they preserve the same estimand;
- never present the extreme alone as confirmatory evidence.

This converts the mechanism studied by Asher et al. into a red-team diagnostic rather than a p-hacking procedure.

## Warning signs

Flag `P-HACKING RISK` when any of the following occurs:

- a new sample restriction is introduced because the focal p-value improves;
- a control is removed because the estimate becomes larger;
- clustering or variance estimation is changed because standard errors shrink;
- a subgroup is defined after inspecting subgroup effects;
- time periods are removed because they weaken the preferred result;
- transformations or outcomes are selected because they produce the desired sign;
- searching stops when p < .05 is reached;
- only the best-performing specification is retained for reporting;
- a post hoc specification is described as if it had been chosen ex ante.

## Recommended reporting language

When a significance-selected extreme exists, use language such as:

> Across the predeclared specification set, the focal coefficient varies from X to Y. The smallest nominal p-value occurs under specification S, but this specification is an extreme of the multiverse and is not privileged as the primary estimate. The baseline and median estimates are A and B, respectively.

The substantive conclusion should follow the distribution of defensible estimates, not the most favorable row.
