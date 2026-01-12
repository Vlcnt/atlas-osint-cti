# Findings — Key Takeaways (Case B)

## What this case demonstrates
1) **Management plane exposure is decisive.**  
The same CVE can be P1 or P2 depending on whether the management interface is reachable from untrusted networks.

2) **Exploitation signals change posture.**  
When exploitation is reported / KEV-listed, vulnerability management often shifts toward an “assume risk is operational” stance until exposure and integrity are verified.

3) **Small, explainable graphs support decisions.**  
A minimal Maltego graph can compress “why is this urgent?” into a 60-second explanation for SOC/Vuln Mgmt stakeholders.

## Practical guidance (SOC/Vuln Mgmt oriented)
A defensible response typically includes:
- confirm inventory and management interface exposure
- apply vendor updates/mitigations as per official guidance
- restrict management interface access to trusted sources (segmentation/ACL)
- if exposure is confirmed, run internal checks to reduce uncertainty (logs, integrity, config changes)
- document actions and decision boundary clearly (what was verified vs unknown)

## Recruiter-friendly takeaway
This case shows the ability to:
- reason like a SOC / vulnerability analyst
- prioritize based on context and evidence
- communicate risk and uncertainty clearly
- translate official advisories into operational triage steps
