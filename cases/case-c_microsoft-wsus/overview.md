# Case C — Microsoft WSUS (Patch Infrastructure)
**Primary identifier:** CVE-2025-59287

## Case snapshot (SOC-style)
- **Category:** Vulnerability Intelligence / Triage (public, official sources)
- **Asset at risk:** Microsoft **Windows Server Update Services (WSUS)** on Windows Server systems where the **WSUS Server Role** is enabled
- **Exposure concern:** WSUS services reachable from **untrusted networks** (Internet-facing or broadly reachable internal segments)
- **Exploitation status:** **Known exploited** (CISA KEV)
- **Priority guidance:**
  - **P1 (High/Critical):** WSUS reachable from the Internet or from untrusted/broad segments
  - **P2 (High):** WSUS restricted but still reachable from large internal networks (segmentation/hardening risk)
- **Confidence:** Medium (official sources only; no internal telemetry)
- **Scope:** Defensive analysis only (no exploit instructions, no offensive validation)

## Executive summary
This case documents a critical vulnerability affecting **WSUS**, tracked as **CVE-2025-59287**. Official reporting indicates the issue is **actively exploited** (KEV inclusion) and Microsoft released **out-of-band** updates to fully address it.

WSUS is a high-value enterprise component because it supports **centralized patch distribution**. A compromise of patch infrastructure can become a trust problem, not just a “patch-and-move-on” task. For this reason, exploited WSUS vulnerabilities should be treated as **operationally urgent** until exposure and integrity are verified.

## Why this matters (context)
Patch infrastructure sits on a privileged path:
- it supports trusted update workflows
- it commonly touches many systems across the estate
- compromise can create outsized impact compared to “normal” server vulnerabilities

For SOC/Vuln Mgmt, the correct posture is driven by:
- **asset role (patch infrastructure)**
- **reachability/exposure**
- **official exploitation signal (KEV)**

## What this case is (and is not)
**This case is:**
- a defensible triage narrative built from official sources
- an example of how to prioritize based on role + exposure + exploitation signal
- a concise, explainable Maltego correlation graph

**This case is not:**
- an exploitation guide
- a victim hunt
- an attribution exercise

## File map
- [Graph](./graph.md)
- [Analysis](./analysis.md)
- [Findings](./findings.md)
- [Limitations](./limitations.md)
- [Sources](./sources.md)

