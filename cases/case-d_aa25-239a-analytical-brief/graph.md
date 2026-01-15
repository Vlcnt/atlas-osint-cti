# Graph — Maltego Visual Correlation (AA25-239A Analytical Brief)

## Purpose
This Maltego graph supports fast explanation of the advisory by mapping:

**Official reporting → activity characterization → TTP themes → defensive priorities**

The graph is not a victim map and does not attempt independent attribution.

## Graph model (richer than Atlas cases, still explainable)
### Core source node
- **AA25-239A (Joint Cybersecurity Advisory, TLP:CLEAR)**

### Activity nodes (what the advisory describes)
- **PRC state-sponsored activity (as described in official reporting)**
- **Global targeting (multi-sector)**
- **Primary focus: network infrastructure / telecom routing environment**
- **Long-term access**

### TTP theme nodes (high-level)
- **Initial access via known vulnerabilities / avoidable weaknesses**
- **Persistence via configuration/account-level mechanisms**
- **Pivot via trusted connections / network position**
- **Threat hunting + mitigation guidance included**
- **IOC packages (STIX) referenced**

### Framework nodes (taxonomy)
- **MITRE ATT&CK (Enterprise / ICS)**
- **MITRE D3FEND countermeasures (as referenced)**

## Screenshot (clickable)
- [graph_overview.png](../../../images/intelligence-briefs/aa25-239a_cti-brief/graph_overview.png)

## Notes
The graph is intentionally curated: it should be quick to brief while still showing the structure (activity, targets, TTP themes, and defensive guidance) without becoming an “attack diagram.”

