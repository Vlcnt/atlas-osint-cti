# Maltego — Setup (Atlas Command Library)

## Purpose
This document defines the standard Maltego setup and modeling conventions used across Atlas cases, to ensure consistency, portability, and defensibility.

It intentionally focuses on standards and guardrails and omits step-by-step instructions.

This guidance is **reusable across all Atlas cases** and is **not tied to any specific case**.

Last reviewed: **2026-01-12**

## Environment
- Maltego Graph (Desktop) 4.x
- Maltego ID (Community or higher)
- Validated on Kali Linux (VM) in a lab environment
- Commodity hardware is sufficient (Atlas graphs are intentionally small)

## Scope
Atlas uses Maltego strictly for visual correlation of public, official information.  
No transforms or enrichment are required by default.

## Minimal configuration
- Default installation is sufficient.
- Optional: install Utilities from the Data Hub.
- Avoid additional data packages unless explicitly required by a case.

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
- **Phrase** — surface/component labels and advisory/source labels

Custom entity types are intentionally avoided.

### Naming
Entities must use human-readable, exact names.

Examples:
- **CVEs:** CVE-2023-46805, CVE-2024-21887, CVE-2025-0108
- **Software:** Ivanti Connect Secure; Palo Alto Networks PAN-OS
- **Sources (Phrase):**
  - Vendor Security Advisory
  - CISA Known Exploited Vulnerabilities (KEV)
  - NVD (NIST) entry
  - National / regional CERT advisory (e.g., CERT-EU, UK NCSC, Canadian Centre for Cyber Security)

URLs belong in each case’s **sources.md** (not as graph labels).

### Relationships
Only the following link labels are permitted:
- **affects** — CVE → Software or relevant surface/component label (Phrase)
- **documented_by** — CVE / Software → Source (Phrase)
- **exploitation_confirmed** — CVE → CISA KEV (Phrase)

Analytical conclusions (e.g., priority/severity) are not encoded as nodes or edges.

## Output
Graphs are exported as static PNG images and stored under:
- images/<case>/graph_overview.png (see: [images/](../../images/))

Graphs must remain explainable in under one minute.

## Guardrails
- Defensive analysis only
- No victim identification
- No attribution
- Graphs represent relationships between official sources, not conclusions
