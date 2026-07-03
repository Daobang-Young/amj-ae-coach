# Quantitative AMJ Audit

Use the checks that match the manuscript's design. A check is a diagnostic question, not a ritual requirement.

## Mode 1: Topic pressure test

1. **Problem**: What consequential management phenomenon or theoretical puzzle is unresolved? `[AMJ-P1]`
2. **Conversation change**: Which belief, mechanism, boundary, or disagreement would change? `[AMJ-P1][AMJ-P3]`
3. **Curiosity**: What plausible competing expectation makes the answer non-obvious? `[AMJ-P1][AMJ-P4]`
4. **Scope**: Are the constructs, mechanisms, levels, and context sufficient for the promise? `[AMJ-P1]`
5. **Actionability**: What decision, practice, or organizational understanding could improve? `[AMJ-P1][AMJ-CURRENT]`
6. **Empirical leverage**: What observation could discriminate among explanations? `[AMJ-P2][AMJ-FTE-2025]`
7. **Novelty status**: Verified by scoped search, plausible but unverified, contradicted, or not needed because the contribution is boundary clarification/replication. `[AMJ-CURRENT]`

Return a one-sentence topic thesis: `By examining [phenomenon] through [mechanism/design], the study revises [conversation] by showing [bounded advance].` Mark every unsupported slot.

## Mode 2: Design pre-mortem

### Question, time, and causality

- Translate the verbal theory into units, timing, treatment/exposure, mechanism, outcome, boundary conditions, and plausible functional form.
- Separate descriptive, associational, predictive, causal, process, and change claims.
- Check temporal ordering and whether measurement occasions match the proposed process.
- Treat cross-sectional mediation or change claims as a major design mismatch unless the claim is narrowed and limitations are explicit. `[AMJ-P2]`
- Identify selection, simultaneity, reverse causality, omitted variables, history, maturation, attrition, and spillover threats as applicable. `[METHOD-NORM]`

### Sample and data

- Explain why this population, setting, level, time window, and inclusion process can answer the question.
- Document sampling frame, exclusions, missingness, attrition, clustering, and final analytic sample.
- Check whether convenience samples or simulated tasks preserve the decision context required by the theory.
- For secondary/new data, trace provenance, construction, coding judgments, legal/ethical access, and data overlap.

### Constructs and measures

- Lock constitutive definitions and boundaries before choosing measures.
- Map each construct to its operationalization; flag label drift, proxy overreach, and jingle-jangle risks.
- For shortened, translated, adapted, or new measures, require item disclosure and fit-for-purpose validation.
- Check reliability, dimensionality, discriminant/convergent evidence, measurement invariance when comparing groups/time, and common-method threats where applicable. `[AMJ-P2][AMJ-FTE-2024]`

### Model and inference

- Derive controls from a causal/theoretical rationale; flag indiscriminate control accumulation and post-treatment controls.
- Measure central mediators rather than relying on an untested process story.
- Match estimator to outcome distribution, nesting, repeated measures, selection, censoring, and identification assumptions.
- Specify alternative explanations and the evidence capable of weakening them.
- Plan robustness, sensitivity, specification, falsification, and practical-magnitude checks before seeing preferred results when feasible.
- Consider complementary studies only when they materially offset the central design weakness. `[AMJ-P2]`

End with a **design repair table**: threat, consequence for the claim, repair before data, residual risk, and claim permitted after repair.

## Mode 3: Section coach

### Introduction

- Does the opening make a broad AMJ reader care without jargon?
- Does it establish what is known, what remains puzzling/deficient/contested, and why that matters?
- Does it state the research question and preview the actual theoretical advance, context, and empirical approach?
- Flag gap-only motivation, novelty-by-absence, too many conversations, overclaiming, and promises unsupported by later sections.

### Theory and hypotheses

- For each hypothesis, extract: starting premise, mechanism, boundary, predicted relationship, and plausible rival/null.
- Flag citation chains without explanatory logic, theory-name substitution, construct slippage, missing mediators, and disconnected hypotheses.
- Ask why these variables and theories—and not obvious alternatives—form one coherent model.
- Check that a hypothesis is specific enough to test yet not tautological or obvious.

### Methods

- Apply completeness, clarity, and credibility to sample/data, procedure, measures, coding, model specification, estimation, ethics, exclusions, and missingness.
- Require enough detail for a knowledgeable researcher to reconstruct the data and analysis.
- Separate what was planned from what was exploratory or post hoc.

### Results

- Ensure descriptive statistics and distributions allow credibility checks.
- Identify unit, N, dependent variable, model, and uncertainty for each analysis.
- Report every hypothesis outcome, including null and opposite-sign findings.
- Verify that interactions, mediation, nonlinear effects, and simple effects are interpreted from appropriate quantities/plots.
- Report effect magnitude and practical meaning, not significance alone.
- Distinguish robustness evidence from repeated variants that do not address a real threat.

### Discussion

- Synthesize findings around the original puzzle instead of repeating coefficients hypothesis by hypothesis.
- Identify two or three deepest theoretical implications and connect each to the front-end promise.
- Explain unexpected/null results without HARKing or disguising speculation as evidence.
- Bound claims by design, measures, sample, setting, and uncertainty.
- Flag rehashing, meandering, new theories introduced too late, generic limitations, and overreach.

## Mode 4: Full-manuscript red team

Run these passes in order:

1. **Mission/desk screen**: substantial empirics; strong theoretical and practical relevance; broad accessibility.
2. **Promise-delivery trace**: map each introduction promise to theory, design, result, and discussion delivery.
3. **Theory-method-data alignment**: identify the weakest link and the maximum claim the chain supports.
4. **Credibility/transparency**: reconstruct sample, measures, analytic decisions, alternatives, and all results.
5. **Contribution-to-length**: remove repetition and technical detail that does not improve inference; preserve necessary transparency.
6. **Originality and integrity**: data/text overlap disclosure, source verification, authorship, ethics, anonymization, and AI log.
7. **Submission mechanics**: apply current policy only after live recheck.

The final recommendation must name the single highest-leverage revision and distinguish prose repairs from changes requiring new theory, analysis, data, or design.
