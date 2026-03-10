# Lab Architecture

The SOC homelab simulates attacker activity against a monitored endpoint while collecting both endpoint and network telemetry for investigation.

## Architecture Diagram

Kali Linux (Attacker VM)  
- Simulated attacker activity  

Windows 10 (Victim Endpoint)  
- Sysmon + Windows Event Logs  

Network Sensor (Suricata / Zeek)  
- Network traffic monitoring  

Splunk SIEM  
- Log ingestion, search, and investigation

## Data Flow

Attacker Activity → Endpoint Logs + Network Traffic → Log Forwarding → Splunk Investigation
