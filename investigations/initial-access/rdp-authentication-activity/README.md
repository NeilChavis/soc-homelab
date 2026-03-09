# RDP Authentication Activity

This investigation documents Remote Desktop Protocol (RDP) authentication activity from a Kali attacker system to a Windows endpoint.

The goal is to observe how RDP login attempts appear in Windows logs and how they can be investigated using Splunk SIEM.

Screenshots in this folder show:
- RDP login attempt from Kali
- Windows authentication activity
- Splunk log investigation

## Evidence

### 1. RDP Connection Attempt from Kali

The attacker system attempted to initiate an RDP connection to the Windows victim machine.

![RDP Connection Attempt](rdp_connection_kali.png)

---

### 2. Windows Authentication Events

Windows Security logs show multiple authentication attempts recorded by Event IDs 4624 and 4625.

![Authentication Events](rdp_authentication_events.png)

These events indicate both successful and failed authentication attempts originating from the attacker IP address.

---

### 3. Network Telemetry (Suricata)

Network monitoring detected RDP traffic between the attacker and the victim system.

![Suricata Network Logs](rdp_suricata_network_logs.png)

Key indicators:

• Source IP: 192.168.136.132  
• Destination Port: 3389  
• Protocol: RDP  

---

### 4. Authentication Event Summary

Splunk aggregation shows the number of authentication events observed during the activity.

![Authentication Event Count](rdp_events_count.png)
