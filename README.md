# AMJ AE Coach

`amj-ae-coach` is a Codex Agent Skill for authors developing empirical manuscripts for the *Academy of Management Journal* (AMJ).

It distills the seven-part AMJ "Publishing in AMJ" editorial series into a quantitative-first developmental workflow, calibrated against current AMJ/AOM submission, transparency, style, and AI-responsibility guidance.

## What it does

- Pressure-tests topic significance, novelty, curiosity, scope, and actionability.
- Audits research-question, theory, design, data, and method alignment before data collection.
- Diagnoses introductions, theory and hypotheses, methods, results, and discussions.
- Performs a full-manuscript pre-submission red-team audit.
- Diagnoses in Chinese and produces English candidate prose only after explicit authorization.
- Uses evidence labels to distinguish AMJ guidance, current policy, methodological norms, and coaching inference.

## Install

Download or clone this repository, then copy:

```text
skills/amj-ae-coach
```

to your user-level Codex skills directory:

```text
~/.agents/skills/amj-ae-coach
```

Codex normally detects skill changes automatically. Restart Codex if it does not appear.

## Use

Invoke it explicitly:

```text
$amj-ae-coach 按 AMJ 标准评估这个研究选题
```

It can also trigger from requests such as:

- 按 AMJ 标准审查我的研究设计
- 帮我诊断这篇论文的引言
- 对整稿做 AMJ 投稿前红队审计
- Audit this quantitative manuscript against AMJ standards

## Contents

```text
skills/amj-ae-coach/
├── SKILL.md
├── agents/openai.yaml
└── references/
    ├── current-policy-and-ai.md
    ├── evidence-base.md
    ├── quantitative-audit.md
    └── workflows-and-outputs.md
```

## Source boundary

The repository does not redistribute the original AMJ PDFs. It contains original, source-attributed paraphrases and workflow guidance. Users remain responsible for verifying current journal requirements, citations, empirical claims, and any AI-use disclosure required by AOM.

## Status

Current-policy layer last verified: 2026-07-03.
