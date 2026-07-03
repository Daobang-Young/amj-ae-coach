# Workflows and Output Templates

## Diagnostic template

Use Chinese unless the author requests otherwise.

```markdown
结论门槛：<1–4 and label>
核心判断：<one sentence with evidence labels>

致命问题
- <issue -> why it matters -> evidence needed/repair -> label>

主要问题
- ...

次要问题
- ...

优先修改顺序
1. <highest-leverage action>

需要作者补充
- <missing fact/evidence, not a request to repeat supplied content>

下一版验收标准
- <observable test>

下一步
<one smallest useful action or authorization request>
```

Omit empty issue categories. Do not soften a fatal design issue into a stylistic suggestion.

## Topic pressure-test output

Return:

1. Gate and five-criterion verdict: significance, novelty status, curiosity, scope, actionability.
2. Current conversation and proposed change.
3. Strongest rival framing.
4. Minimum empirical leverage needed.
5. A one-sentence topic thesis with verification markers.
6. Go, redesign, narrow claim, or redirect-journal recommendation.

## Design pre-mortem output

Use this table:

| Threat | Claim affected | Why current design cannot resolve it | Repair before data | Residual risk | Permitted wording |
|---|---|---|---|---|---|

Then identify:

- decisions that become irreversible after data collection;
- measures/instruments needing validation;
- analyses that must be planned rather than retrofitted;
- complementary evidence that would change the inference.

## Section-coach output

Before any rewrite, provide:

1. Section job and whether the draft performs it.
2. Argument map or evidence map.
3. Fatal/major/minor issues with sentence or paragraph anchors.
4. Proposed structural moves in order.
5. Explicit authorization request naming the exact scope, for example: “如果你确认，我下一步只重写第 2–4 段，保留研究问题与两项贡献声明不变。”

An initial request to “rewrite directly” does not bypass this checkpoint.

## Authorized rewrite output

After a new explicit authorization, return:

```markdown
### English candidate text
<authorized prose only>

### 改动说明
- [Wording] <clarity/flow change>
- [Structure] <argument-order change>
- [Substantive—author approval required] <claim change>

### 待作者核实
- [[AUTHOR VERIFY: exact item]]

### AI 使用记录增量
| Stage | Model/tool | Purpose | Author verification required |
|---|---|---|---|
```

Do not silently strengthen causal language, novelty, generalizability, or effect interpretation.

## Full-manuscript red-team output

Return:

1. Gate and desk-screen rationale.
2. A promise-delivery matrix:

| Front-end promise | Theory mechanism | Design test | Result | Discussion delivery | Status |
|---|---|---|---|---|---|

3. Fatal, major, and minor issues.
4. A revision sequence separated into theory, new evidence/analysis, writing, and compliance.
5. The maximum defensible claim under the current evidence.
6. Submission-readiness checklist after live policy verification.

## Evidence-label style

Place labels immediately after the claim they support:

- `横截面设计无法有力识别所声称的时间性中介过程。[AMJ-P2][COACH-INFERENCE]`
- `该引言目前证明了“尚未研究”，但没有证明该问题为什么重要。[AMJ-P3][COACH-INFERENCE]`

If a judgment combines sources and interpretation, include both. Never attach `[AMJ-CURRENT]` to a recommendation that is only preferred practice.

## Novelty verification record

Record:

- research question/claim checked;
- databases or search systems;
- query families and synonyms;
- date range and search date;
- inclusion/exclusion boundary;
- nearest prior studies;
- conclusion: verified within scope, weakened, contradicted, or unresolved.

Avoid “no studies exist.” Prefer: “Within the stated search boundary, no directly matching study was located as of <date>.”
