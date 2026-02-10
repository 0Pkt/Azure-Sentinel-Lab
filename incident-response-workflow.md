# Incident Response Playbook: RDP Brute Force

## Trigger
**Alert Rule:** `High_Volume_Failed_Logins_RDP`
**Severity:** High
**Threshold:** > 20 failed attempts in 10 minutes

## Triage Process (SOC Analyst View)
1.  **Verification:**
    * Query `SecurityEvent` to confirm if the `Account` exists or is a generic name (e.g., "admin", "root").
    * Check `IpAddress` against Threat Intelligence feeds (e.g., VirusTotal) to see if it is a known malicious IP.

2.  **Containment:**
    * If the attack is ongoing, trigger Azure Logic App `Block-IP-NSG` to automatically add the source IP to the Network Security Group deny list.
    * Reset the user password if a successful login followed the failed attempts.

3.  **Documentation:**
    * Log the incident in the ticketing system with the Source IP, Timeframe, and Target Accounts.
    * Tag as "True Positive" to refine future ML models.
