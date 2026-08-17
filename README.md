# Academic Paper Coach Skills

This repository contains two complementary Codex Agent Skills for developing management and entrepreneurship manuscripts.

| Skill | Primary use |
|---|---|
| `amj-ae-coach` | AMJ-specific developmental review, current AOM policy checks, quantitative-first design auditing, and submission preparation |
| `entrepreneurship-paper-coach` | Reviewer-style coaching for entrepreneurship topics, positioning, theory, design, sections, full manuscripts, and journal fit across ETP, JBV, SEJ, AMJ, and related journals |

## Entrepreneurship Paper Coach

`entrepreneurship-paper-coach` combines the connected AMJ author-development logic with entrepreneurship-specific craft guidance from Shepherd and Wiklund (2020), while keeping their experience-based heuristics separate from current journal policy.

It:

- tests whether the entrepreneurial phenomenon is theoretically central rather than merely present in the sample;
- replaces gap spotting with an explicit conversation-change test;
- maps theory input, entrepreneurial transformation, and theory output;
- distinguishes deductive, inductive, abductive, mixed, conceptual, review, methods, and design-science work;
- audits the full chain from phenomenon and question to evidence and bounded contribution;
- verifies current journal scope before fit or readiness conclusions;
- diagnoses before rewriting and requires explicit authorization for manuscript prose.

For AMJ entrepreneurship papers, use both skills: `amj-ae-coach` governs journal mission, policy, readiness gates, and AI disclosure; `entrepreneurship-paper-coach` supplies the domain lens.

## Install

Copy either or both skill folders into the user-level Codex skills directory:

```text
skills/amj-ae-coach
skills/entrepreneurship-paper-coach
```

Typical destination:

```text
~/.codex/skills/
```

Restart Codex if a newly installed skill does not appear automatically.

## Use

```text
$entrepreneurship-paper-coach Assess whether this entrepreneurship topic has top-journal potential
$entrepreneurship-paper-coach Diagnose this manuscript's introduction and theoretical contribution
$entrepreneurship-paper-coach Run a pre-submission red-team review of this ETP manuscript
$amj-ae-coach Evaluate this research topic against AMJ standards
```

## Contents

```text
skills/
├── amj-ae-coach/
│   ├── SKILL.md
│   ├── agents/openai.yaml
│   └── references/
└── entrepreneurship-paper-coach/
    ├── SKILL.md
    ├── agents/openai.yaml
    └── references/
        ├── entrepreneurship-craft.md
        ├── journal-and-output-protocols.md
        ├── paradigm-routing.md
        └── reviewer-logic.md
```

## Source boundary

The repository does not redistribute the source PDFs. It contains original, source-attributed paraphrases and workflow guidance. Users remain responsible for checking current journal requirements, verifying citations and empirical claims, protecting confidential data, and disclosing AI use when required.

## Status

- AMJ current-policy layer last verified: 2026-07-03.
- Entrepreneurship journal boundary snapshot last verified: 2026-08-17.
