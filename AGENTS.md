# Codex Reporting Workspace

This repository is a Codex-focused workspace for report generation in three areas:

- finance
- anti-money laundering and compliance
- tracking, logistics, and investigation workflows

## Core Contract

Unless the user explicitly asks for code or configuration changes, the default job in this repository is to produce report content.

Every reporting task must produce two deliverables:

1. Main report
2. Analysis report

If the user does not specify an output format, default the main report to **Word**.

## Output Format Rules

- **Word**: Write a document-style report with a title, executive summary, findings, interpretation, recommendations, and appendices when needed.
- **Excel**: Produce workbook-ready content with sheet names, column definitions, formulas or flag logic, and Excel-ready tables. If native `.xlsx` generation is not practical, state that clearly and provide content that can be moved into Excel directly.
- **PPTX**: Produce deck-ready content with slide titles, key messages, supporting evidence, suggested visuals, and speaker notes. If native `.pptx` generation is not practical, state that clearly and provide a slide-by-slide outline.

Unless the user requests otherwise, keep the analysis report in a memo-style Word format even when the main deliverable is Excel or PPTX.

## Analysis Report Requirements

The analysis report must always include:

- result analysis and interpretation
- the reasoning behind the report structure and writing choices
- references to the exact files and specific sections used
- fact vs inference vs assumption labeling where needed
- open gaps, uncertainty, or unresolved conflicts in the evidence

## Source Priority

Use sources in this order unless the user says otherwise:

1. files the user uploads or creates in this repository
2. repository instructions and agent configuration files
3. repository-local reference materials under folders such as `input/`, `cases/`, `evidence/`, `references/`, and `output/` when present
4. current external sources when the request requires up-to-date facts or local material is insufficient

Prefer repository-local material before browsing.

## Citation Standard

For every substantive section in the main report and analysis report, cite:

- the exact file path
- the specific heading, section, or subsection used
- whether that source informed facts, structure, terminology, or judgment

Do not claim support from a file unless the relevant content is actually present there.

## Domain Guidance

- Finance reports should emphasize numerical consistency, decision relevance, trend interpretation, and explicit assumptions.
- AML reports should separate observed facts, red flags, interpretation, and recommended actions. Do not treat suspicion as proof.
- Tracking and investigation reports should prioritize timeline clarity, evidence logs, impact assessment, and unresolved questions.

## Guardrails

- Mirror the user's language when practical. If no preference is given, use clear English.
- Do not invent financial figures, case facts, compliance conclusions, or regulatory outcomes.
- Separate observed facts from risk indicators, interpretation, and recommendations.
- If evidence is weak or conflicting, say so directly and lower confidence instead of smoothing it over.
- Keep every report traceable so another reviewer can reproduce the reasoning from the cited files and sections.
