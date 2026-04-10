# Test Codex Reporting Workspace

This repository is a Codex-focused reporting workspace for three primary use cases:

- finance reports
- anti-money laundering and compliance reports
- tracking, logistics, and investigation reports

## Core Contract

Unless the user explicitly asks for code changes, the default job here is to generate report content and report packages.

Every reporting task must produce two outputs:

1. Main report
2. Analysis report

If the user does not specify an output format, default the main report to **Word**.

## Output Format Rules

- **Word**: Write a document-style report with title, executive summary, findings, interpretation, recommendations, and appendices where useful.
- **Excel**: Build an Excel-oriented deliverable with workbook structure, sheet names, column definitions, formulas or flag logic, and Excel-ready tables. If native `.xlsx` generation is not practical, produce workbook-ready source content and say so explicitly.
- **PPTX**: Build a slide-by-slide deck structure with slide titles, key points, supporting evidence, suggested visuals, and speaker notes. If native `.pptx` generation is not practical, produce a deck-ready outline and say so explicitly.

Unless the user requests otherwise, keep the analysis report as a Word-style memo even when the main deliverable is Excel or PPTX.

## Analysis Report Requirements

The analysis report must always include:

- result analysis and interpretation
- the reasoning behind how the report was written
- references to which files and specific sections were used
- fact vs inference vs assumption labeling where it matters
- open gaps, uncertainty, or unresolved conflicts in the evidence

## Source Priority

Use sources in this order unless the user says otherwise:

1. files the user provides inside this repository
2. repository-local files in `test-codex/`
3. parent-workspace reference materials listed below
4. current external sources when the request needs up-to-date facts or local material is insufficient

Prefer local and parent-workspace materials before browsing.

## Parent Workspace Reference Materials

These materials are available from the parent workspace and should be used when relevant:

- `../AGENTS.md`
- `../.codex/AGENTS.md`
- `../.agents/skills/market-research/SKILL.md`
- `../.agents/skills/investor-materials/SKILL.md`
- `../.agents/skills/article-writing/SKILL.md`
- `../.agents/skills/deep-research/SKILL.md`
- `../.agents/skills/exa-search/SKILL.md`
- `../.agents/skills/security-review/SKILL.md`
- `../skills/customs-trade-compliance/SKILL.md`
- `../skills/logistics-exception-management/SKILL.md`
- `../skills/carrier-relationship-management/SKILL.md`

## Citation Standard

For every substantive section in the main report and analysis report, cite:

- the exact file path
- the specific heading, section, or subsection used
- whether that source informed facts, structure, terminology, or judgment

Do not claim support from a file unless the relevant content is actually present there.

## Domain Routing

- Finance prompts: use market research, investor materials, article writing, and deep research patterns.
- AML prompts: use deep research, market research, security review, and customs or sanctions-style compliance materials.
- Tracking prompts: use logistics exception management, carrier relationship management, article writing, and research materials.

## Guardrails

- Mirror the user's language when practical. If no preference is given, use English.
- Do not invent financial figures, case facts, compliance conclusions, or regulatory outcomes.
- Separate observed facts from risk indicators, interpretation, and recommendations.
- If evidence is weak or conflicting, say so directly and lower confidence instead of smoothing it over.
- Keep the report traceable so another agent can reproduce the reasoning from the cited files and sections.
