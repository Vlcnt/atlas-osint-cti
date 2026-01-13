# Graph — Maltego Visual Correlation (Case C)

## Purpose of the graph
This Maltego graph supports **fast, defensible visual reasoning** for triage. It shows how a WSUS patch-infrastructure risk story can be backed by official documentation:

**WSUS (patch infrastructure) → public signal (out-of-band update / reliability concern) → official sources → triage relevance**

The underlying issue is tracked as **CVE-2025-59287**, but the graph is intentionally **product-centered** to keep it explainable in under a minute. CVE-level details and links are captured in [Sources](./sources.md).

## Graph model (minimal, explainable)
### Core nodes
- **Software:** Microsoft WSUS
- **Context (Phrase):** Patch infrastructure; Update distribution service
- **Public signals (Phrase):** Out-of-band security update; Security update reliability concern
- **Sources (Phrase):** Microsoft Security Advisory; Microsoft Support / KB guidance; NVD (NIST)

### Relationship types (what edges mean)
- **affects** → context/signal related to WSUS
- **documented_by** → official source documenting WSUS and the associated security situation

## Screenshot
- [graph_overview.png](../../images/case-c/graph_overview.png)

## Notes
The graph is intentionally **small and curated** to support communication and prioritization.
It represents **relationships between official reporting and the affected asset**, not conclusions about any specific environment.
