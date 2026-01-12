# Maltego — Setup (Atlas command library)

## Purpose
This document defines the **standard Maltego setup and modeling conventions** used across Atlas cases, to ensure **consistency, portability, and defensibility**.

It intentionally focuses on standards and guardrails and omits step-by-step instructions.

## Environment
- Maltego Graph (Desktop) 4.x
- Maltego ID (Community or higher)
- Validated on **Kali Linux (VM)** (VMware-based lab environment)
- Commodity hardware is sufficient (Atlas graphs are intentionally small)

## Scope
Atlas uses Maltego strictly for **visual correlation of public, official information**.  
No transforms or enrichment are required by default.

## Minimal configuration
- Default installation is sufficient
- Optional: install **Utilities** from the Data Hub
- Avoid additional data packages unless explicitly required by a case

## Required UI components
The following panels must be visible:
- Entity Palette
- Detail / Property View
- Overview

If panels are missing, restore them via the View / Windows menus.

## Modeling conventions (mandatory)

### Entity usage
Only built-in entity types are used:
- **CVE** — vulnerability identifiers
- **Software** — affected product
- **Phrase** — advisory / source labels

Custom entity types are intentionally avoided.

### Naming
Entities must use **human-readable, exact names**:
- CVEs: `CVE-2023-46805`, `CVE-2024-21887`
- Software: `Ivanti Connect Secure`
- Sources (Phrase):
  - `Ivanti Security Advisory`
  - `CISA Known Exploited Vulnerabilities (KEV)`
  - `CERT-EU Security Advisory` (or `UK NCSC Advisory` when applicable)

URLs belong in `sources.md`, not as graph labels.

### Relationships
Only the following link labels are permitted:
- `affects` — CVE → Software
- `documented_by` — CVE / Software → Source
- `exploitation_confirmed` — CVE → CISA KEV

Analytical conclusions (e.g., priority/severity) are not encoded as nodes or edges.

## Output
Graphs are exported as static PNG images and stored under:
- `images/<case>/graph_overview.png`

Graphs must remain explainable in under one minute.

## Guardrails
- Defensive analysis only
- No victim identification
- No attribution
- Graphs represent **relationships between official sources**, not conclusions
