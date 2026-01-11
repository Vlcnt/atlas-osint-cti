# Graph — Maltego Visual Analysis (Case A)

## Purpose of the graph
The Maltego graph supports **visual reasoning**: it maps how official information connects:
**CVEs → product → official advisories → exploitation status**

This is not an “OSINT hunt” for victims and does not attempt attribution.

## Graph model (minimal, defensible)

### Core entities
- **CVE:** CVE-2023-46805
- **CVE:** CVE-2024-21887
- **Product:** Ivanti Connect Secure
- **Source:** Ivanti Security Advisory
- **Source:** CISA Known Exploited Vulnerabilities (KEV)
- **Source:** CERT-EU Security Advisory

### Relationship types (what edges mean)
- *affects* (CVE → Product)
- *documented_by* (CVE/Product → Source)
- *exploitation_confirmed* (CVE → CISA KEV)

## Screenshot placement
Store screenshots in:
- [images/case-a/](../../images/case-a/)

Current screenshot:
- [graph_overview.png](../../images/case-a/graph_overview.png)


## Notes
The graph is intentionally small and curated to remain **defensible and explainable**.

**Boundary note:** response priority (P1/P2) remains part of the written analysis; it is not encoded as a graph node or edge.
