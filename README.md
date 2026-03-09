# SOC Homelab Investigations

This repository documents security investigations conducted within a personal SOC homelab environment. The lab simulates attacker behavior across multiple systems and demonstrates how security analysts detect and investigate malicious activity using endpoint telemetry, network monitoring, and SIEM analysis.

## Lab Environment

The homelab environment consists of several systems used to simulate attacker activity and collect security telemetry.

• Kali Linux – attacker simulation  
• Windows 10 – monitored endpoint  
• Suricata / Zeek – network monitoring and traffic analysis  
• Splunk – centralized log collection and investigation

## Investigation Categories

The following investigations demonstrate how common attacker techniques appear in logs and how they can be analyzed from a SOC perspective.

### Initial Access

Simulated attacker entry techniques and the resulting endpoint and network activity.

Investigations included:

- [Malicious LNK Execution](investigations/initial-access/malicious-lnk-execution)
- [RDP Authentication Activity](investigations/initial-access/rdp-authentication-activity)

Location:

`investigations/initial-access/`

## Goal of the Repository

The goal of this repository is to demonstrate practical SOC investigation skills, including:

• Log analysis  
• Process chain investigation  
• Authentication analysis  
• SIEM-based detection and investigation  
• Correlating endpoint and network telemetry
