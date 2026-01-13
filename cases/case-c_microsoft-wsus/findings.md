# Findings — Key Takeaways (Case C)

## What this case demonstrates
1) **Patch infrastructure changes the stakes.**  
WSUS is not “just another server.” It supports trusted update distribution and can amplify impact if compromised.

2) **Known exploitation changes posture.**  
When an issue is KEV-listed, organizations typically move from “patch when possible” to an **urgent operational response** until exposure and integrity are validated.

3) **Exposure drives priority (P1 vs P2).**  
The same vulnerability can be P1 or P2 depending on whether WSUS is reachable from untrusted networks or segmented appropriately.

4) **Small, explainable graphs support decisions.**  
A minimal Maltego model can help communicate urgency and source traceability quickly to SOC/Vuln Mgmt stakeholders.

## Practical guidance (SOC/Vuln Mgmt oriented)
A defensible response typically includes:
- confirm WSUS inventory
- validate reachability and segmentation assumptions
- apply vendor updates / mitigations per official guidance
- if exposure is confirmed, perform internal checks to reduce uncertainty (logs, config integrity, anomalous activity)
- document what was verified vs what remains unknown

## Recruiter-friendly takeaway
This case shows the ability to:
- reason like a SOC / vulnerability analyst
- translate official advisories into operational triage steps
- communicate uncertainty clearly
- prioritize based on role, exposure, and exploitation signal

