
# Initial Access Investigations

This section documents simulated initial access techniques observed within the SOC homelab environment.

The goal of these exercises is to understand how common attacker entry techniques appear in endpoint telemetry and how they can be investigated using SIEM tools such as Splunk.

Each investigation reconstructs attacker activity, correlates logs, and documents the evidence collected during analysis.

---

## Investigations

### Malicious LNK Execution

This scenario simulates a phishing-style attack where a user downloads and executes a malicious Windows shortcut file. The shortcut launches a command that generates observable process activity on the endpoint.

Investigation includes:

• Phishing style HTML lure  
• LNK execution behavior  
• Process chain analysis

Location:

`rdp-authentication-activity/`

---

### RDP Authentication Activity

This scenario simulates an attacker attempting to authenticate to a Windows system using Remote Desktop Protocol (RDP).

Investigation includes:

• RDP connection attempt from Kali attacker  
• Windows authentication logs (Event ID 4624 / 4625)  
• Network telemetry from Suricata  
• Splunk log investigation

Location:

'rdp-authentication-activity/'

---

These investigations demonstrate how analysts can correlate endpoint logs, network telemetry, and SIEM data to investigate suspicious activity.
