# Atlas — OSINT & CTI (Defensive) Visual Correlation

OSINT & CTI project focused on correlating enterprise security signals using public, official sources and visual analysis.

## Scope & guardrails
- Defensive analysis only (no exploit instructions, no offensive validation)
- No victim identification and no attribution
- Claims are backed by public, official advisories (vendor/government; EU/UK/Canada where available)

## Command library (reusable standards)
Reusable conventions and guardrails applied across Atlas cases:
- [Maltego — Setup](./command-library/maltego/setup.md)
- [Maltego — Operational Notes](./command-library/maltego/notes.md)

## Case index

### Case A — Ivanti Connect Secure (Enterprise Access Gateway)
- [Overview](./cases/case-a_ivanti-connect-secure/overview.md)
- [Graph model](./cases/case-a_ivanti-connect-secure/graph.md)
- [Graph screenshot](./images/case-a/graph_overview.png)
- [Analysis](./cases/case-a_ivanti-connect-secure/analysis.md)
- [Findings](./cases/case-a_ivanti-connect-secure/findings.md)
- [Limitations](./cases/case-a_ivanti-connect-secure/limitations.md)
- [Sources](./cases/case-a_ivanti-connect-secure/sources.md)

### Case B — Palo Alto Networks PAN-OS (Management Web Interface)
- [Overview](./cases/case-b_palo-alto-pan-os/overview.md)
- [Graph model](./cases/case-b_palo-alto-pan-os/graph.md)
- [Graph screenshot](./images/case-b/graph_overview.png)
- [Analysis](./cases/case-b_palo-alto-pan-os/analysis.md)
- [Findings](./cases/case-b_palo-alto-pan-os/findings.md)
- [Limitations](./cases/case-b_palo-alto-pan-os/limitations.md)
- [Sources](./cases/case-b_palo-alto-pan-os/sources.md)

Additional cases will be added following the same methodology and standards.

## Repo structure
- [cases/](./cases/) — one folder per case (overview, sources, analysis, graph, findings, limitations)
- [images/](./images/) — case screenshots referenced by the case markdown
- [command-library/](./command-library/) — reusable setup, conventions, and guardrails

## How to read a case (recommended order)
1. overview.md  
2. graph.md + screenshot  
3. analysis.md  
4. findings.md  
5. limitations.md  
6. sources.md (with “date accessed”)

