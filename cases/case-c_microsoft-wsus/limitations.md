# Limitations (Case C)

## Limitations of this analysis
This case is based on **public, official sources only**, therefore:
- it cannot confirm compromise in any specific environment
- it cannot establish an internal incident timeline for any organization
- it cannot support attribution claims beyond what authorities explicitly state

## What would increase confidence (in a real SOC)
To move from “risk assessment” to “confirmed incident / ruled out,” a SOC would typically require:
- verified asset inventory (which hosts run WSUS)
- exposure confirmation (reachability from untrusted networks)
- patch/mitigation state verification
- administrative/audit log review
- correlated authentication and network telemetry
- post-remediation validation evidence (integrity checks, configuration review)

## Scope guardrails
No exploit testing and no offensive procedures are included.  
The purpose is to demonstrate **triage, prioritization, and defensible documentation**.
