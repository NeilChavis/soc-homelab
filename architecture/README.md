# Lab Architecture

This folder contains diagrams and screenshots that describe the SOC homelab architecture.

Components include:

- Windows victim endpoint
- Kali Linux attacker system
- Ubuntu monitoring server
- Splunk SIEM
- Sysmon endpoint logging
- Suricata IDS
- Zeek network monitoring

                ┌─────────────────┐
                │   Kali Linux    │
                │   (Attacker)    │
                └────────┬────────┘
                         │
                         │ Simulated attacks
                         ▼
                ┌─────────────────┐
                │   Windows 10    │
                │   Victim Host   │
                │ Sysmon Logging  │
                └────────┬────────┘
                         │
                         │ Network traffic
                         ▼
                ┌─────────────────┐
                │ Suricata / Zeek │
                │ Network Sensor  │
                └────────┬────────┘
                         │
                         │ Log forwarding
                         ▼
                ┌─────────────────┐
                │      Splunk     │
                │   SIEM Server   │
                └─────────────────┘
