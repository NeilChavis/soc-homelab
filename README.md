# SOC Homelab

This project documents a personal SOC homelab used to simulate attacker activity and practice security monitoring and investigation workflows.

The environment was developed to gain hands-on experience with endpoint telemetry, network monitoring, and SIEM-based investigations.

## Lab Components

- Windows 10 endpoint (victim system)
- Kali Linux attacker machine
- Ubuntu monitoring server
- Splunk SIEM
- Sysmon endpoint logging
- Suricata IDS
- Zeek network monitoring
- Winlogbeat log forwarding

## Lab Architecture

The lab simulates a small enterprise network where attacker activity from the Kali system generates telemetry across host and network sensors.

Endpoint activity such as process execution, command line activity, and registry changes are captured by Sysmon.

Network activity is monitored by Suricata and Zeek to detect suspicious traffic and generate alerts.

All telemetry is forwarded to Splunk where it can be searched, correlated, and investigated from a SOC analyst perspective.

## Skills Demonstrated

- SIEM log analysis
- Endpoint telemetry analysis
- Network traffic investigation
- IDS alert investigation
- Incident triage and analysis

## Future Investigations

- Persistence detection via registry run keys
- Command and control detection
- Suspicious PowerShell activity analysis
