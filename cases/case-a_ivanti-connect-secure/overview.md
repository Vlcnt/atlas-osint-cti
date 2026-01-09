# Case A — Ivanti Connect Secure (Enterprise Access Gateway)
**CVE:** CVE-2023-46805 / CVE-2024-21887

## Case snapshot (SOC-style)
- **Category:** Vulnerability Intelligence / Triage (public sources)
- **Environment at risk:** Internet-facing remote access / VPN gateway
- **Priority (guidance):**
  - **P1 (High/Critical)** if Ivanti Connect Secure is/was exposed to the Internet during the exploitation window
  - **P2 (High)** if not exposed but present in the environment (risk of misconfiguration / future exposure)
- **Confidence:** Medium (OSINT + vendor/government advisories; no internal telemetry)
- **Scope:** Defensive analysis only (no exploit, no offensive validation)

## Executive summary
This case documents a **widely exploited vulnerability chain** affecting Ivanti Connect Secure, a component often deployed as a **central access point** for remote users. Vulnerabilities on this layer are high impact because they can translate into **initial access** to enterprise networks.

The goal of this case is to show how a SOC/vulnerability team:
- prioritizes risk based on **asset role + exposure + exploitation status**
- correlates **multiple official sources**
- documents what can be stated confidently vs what requires internal verification

## What this case is (and is not)
**This case is:**
- an evidence-based correlation of official advisories
- a prioritization and triage narrative suitable for SOC/Vuln Mgmt

**This case is not:**
- a technical exploitation guide
- an attempt to identify victims or attribute threat actors

## Expected outputs
- A Maltego graph showing the **information relationships** (CVE → product → official advisories → exploitation status)
- A concise written assessment (risk + triage guidance)
- A traceable list of sources

