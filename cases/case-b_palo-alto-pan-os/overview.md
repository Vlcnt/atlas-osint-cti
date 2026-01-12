# Case B — Palo Alto Networks PAN-OS (Management Web Interface)
**CVE:** CVE-2025-0108

## Case snapshot (SOC-style)
- **Category:** Vulnerability Intelligence / Triage (public sources)
- **Environment at risk:** PAN-OS devices where the **management web interface** is reachable from untrusted networks
- **Priority (guidance):**
  - **P1 (High/Critical)** if the management interface is Internet-exposed or broadly reachable from untrusted segments
  - **P2 (High)** if management access is restricted but still reachable from large/internal networks (segmentation/hardening risk)
- **Confidence:** Medium (OSINT + official sources; no internal telemetry)
- **Scope:** Defensive analysis only (no exploit, no offensive validation)

## Executive summary
This case documents **CVE-2025-0108**, an **authentication bypass** affecting the **PAN-OS management web interface**. Public, official reporting indicates **active exploitation signals** (KEV inclusion / vendor-observed attempts), making this a triage priority for organizations operating PAN-OS in enterprise environments.

The goal is to demonstrate SOC-grade logic for:
- prioritizing risk based on **asset role + exposure + exploitation status**
- correlating **official sources**
- documenting what can be stated confidently vs what requires internal verification

## What this case is (and is not)
**This case is:**
- an evidence-based correlation of official advisories
- a prioritization and triage narrative suitable for SOC / vulnerability management

**This case is not:**
- a technical exploitation guide
- an attempt to identify victims or attribute threat actors

## Expected outputs
- A Maltego graph showing the key relationships (CVE → product → management interface → sources → exploitation signal)
- A concise written assessment (risk framing + triage guidance + decision boundary)
- A traceable list of sources (with “date accessed”)

## File map (quick)
- [graph.md](./graph.md) → graph model + screenshot pointer
- [analysis.md](./analysis.md) → reasoning and triage logic
- [findings.md](./findings.md) → key takeaways (SOC-grade)
- [limitations.md](./limitations.md) → scope + what would increase confidence
- [sources.md](./sources.md) → official references


