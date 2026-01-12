# Graph — Maltego Visual Correlation (Case B)

## Purpose of the graph
The Maltego graph supports **visual reasoning for triage**. It maps how official information connects:
**CVE → product → management interface → advisories → exploitation signal**

This is not an OSINT hunt for victims and does not attempt attribution.

## Graph model (minimal, defensible)
### Core nodes
- **CVE:** CVE-2025-0108
- **Product:** Palo Alto Networks PAN-OS
- **Surface (Phrase):** Management Web Interface
- **Source (Vendor):** Palo Alto Networks Security Advisory
- **Source (Gov/Authoritative):** CISA Known Exploited Vulnerabilities (KEV) Catalog (referenced via NVD/official reporting)

### Relationship types (link labels)
(Aligned to Atlas Maltego conventions.)
- *affects* (CVE → Product)
- *affects* (CVE → Management Web Interface)
- *documented_by* (CVE → Vendor advisory)
- *exploitation_confirmed* (CVE → KEV signal)

## Screenshot
The exported Maltego graph will be stored here:

- [Graph overview image](../../images/case-b/graph_overview.png)


Reference image (relative path from this file):
- [graph_overview.png](../../images/case-b/graph_overview.png)


## Notes
The graph is intentionally **small** and curated.  
A SOC-grade graph is not “big”; it is **explainable** in under 60 seconds.

