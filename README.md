# Atlas — OSINT & CTI (Defensive) Visual Correlation

OSINT & CTI project focused on correlating enterprise security signals using **public, official sources** and **visual analysis**.

## Scope & guardrails
- Defensive analysis only (no exploit instructions, no offensive validation)
- No victim identification and no attribution
- Claims are backed by official advisories (vendor/government/EU-UK where available)

## Case index
- **Case A — Ivanti Connect Secure (Enterprise Access Gateway)**
  - [Overview](cases/case-a_ivanti-connect-secure/overview.md)
  - [Graph model](cases/case-a_ivanti-connect-secure/graph.md)
  - [Graph screenshot](images/case-a/graph_overview.png)
  - [Analysis](cases/case-a_ivanti-connect-secure/analysis.md)
  - [Findings](cases/case-a_ivanti-connect-secure/findings.md)
  - [Limitations](cases/case-a_ivanti-connect-secure/limitations.md)
  - [Sources](cases/case-a_ivanti-connect-secure/sources.md)

## Repo structure
- `cases/` — one folder per case (overview, sources, analysis, graph, findings, limitations)
- `images/` — case screenshots referenced by the case markdown

## How to read a case (recommended order)
1. `overview.md`
2. `graph.md` + screenshot
3. `analysis.md`
4. `findings.md`
5. `limitations.md`
6. `sources.md` (with “date accessed”)
