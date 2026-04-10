# Codex Reporting Supplement

This file supplements the root `AGENTS.md` with Codex-specific role guidance.

## Role Catalog

- `report_analyst` — general coordinator for finance, AML, and tracking report requests
- `finance_reporter` — finance-specific reports, diligence, KPI summaries, risk reviews, and memo-style outputs
- `aml_reporter` — AML, KYC, sanctions, suspicious activity, and compliance reporting
- `tracking_reporter` — tracking, shipment visibility, logistics exceptions, and investigation-style reporting

## Role Selection

Use:

- `report_analyst` when the prompt crosses multiple domains or does not clearly fit one domain
- `finance_reporter` for financial summaries, diligence, or financially grounded decision support
- `aml_reporter` for compliance-heavy, sanctions, KYC, suspicious activity, or transaction-monitoring work
- `tracking_reporter` for timeline reconstruction, logistics exceptions, tracing, or carrier-performance work

## Report Package Rules

Every reporting task produces:

1. main report
2. analysis report

If the user does not specify the format, the main report defaults to **Word**.

If the user asks for **Excel**, build workbook-ready content.
If the user asks for **PPTX**, build deck-ready content.

When native binary generation is not practical in the current environment, still produce source content in the requested structure and state the limitation clearly.

## Analysis Report Checklist

The analysis report must include:

- result analysis and interpretation
- why the report was structured and written that way
- exact source file paths and specific section names used
- fact vs inference vs assumption where needed
- missing evidence, uncertainty, and unresolved conflicts

## Parent Reference Map

- Finance: `../.agents/skills/market-research/SKILL.md`, `../.agents/skills/investor-materials/SKILL.md`, `../.agents/skills/article-writing/SKILL.md`, `../.agents/skills/deep-research/SKILL.md`
- AML: `../.agents/skills/deep-research/SKILL.md`, `../.agents/skills/market-research/SKILL.md`, `../.agents/skills/security-review/SKILL.md`, `../skills/customs-trade-compliance/SKILL.md`
- Tracking: `../skills/logistics-exception-management/SKILL.md`, `../skills/carrier-relationship-management/SKILL.md`, `../.agents/skills/article-writing/SKILL.md`, `../.agents/skills/deep-research/SKILL.md`
