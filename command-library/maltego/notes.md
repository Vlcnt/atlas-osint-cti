# Maltego — Operational Notes (Atlas Command Library)

This document captures general operational considerations for building **small, defensible** Maltego graphs in Atlas.

These notes are **reusable across all Atlas cases** and are **not tied to any specific case**.  
They are intended for consistency and quality, not as a troubleshooting guide.

Last reviewed: **2026-01-12**

## UI considerations
- Ensure the **Entity Palette** is visible when working on graphs.
- Work inside an active **Graph** tab (not only the Start Page / Data Hub view).
- Keep the default layout unless a case explicitly requires changes.

## Source representation
For Atlas graphs:
- Advisory and reference sources are represented as **Phrase** entities.
- URLs are intentionally kept out of the graph for readability.
- Canonical links are documented in each case’s **sources.md** under the cases directory (see: [cases/](../../cases/)).  
  This improves visual clarity and avoids mixing references with analytical structure.

## Graph scope control
Atlas graphs are intentionally minimal:
- Include only entities required to explain the case.
- Avoid adding nodes that encode analytical conclusions (e.g., priority, severity).
- Prefer fewer nodes with clear relationships over exhaustive enumeration.

## Relationship consistency
Use a limited and consistent set of link labels:
- affects
- documented_by
- exploitation_confirmed

This improves comparability across cases and reduces ambiguity.

## Pre-export review
Before exporting a graph image:
- Verify node naming matches the case documentation.
- Verify link direction and semantics.
- Ensure the graph can be explained clearly in under one minute.
