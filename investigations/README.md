# Security Investigations

This section documents simulated security investigations conducted within the SOC homelab environment.

Each investigation recreates attacker activity and demonstrates how a SOC analyst can detect, analyze, and investigate malicious behavior using endpoint telemetry, network monitoring, and SIEM analysis. The investigations are organized according to stages of the attack lifecycle.

---

## Investigation Categories

### Initial Access  (Completed)

Simulations of how attackers first gain entry into a system and how that activity appears in logs.

Current investigations:

• Malicious LNK Execution  
• RDP Authentication Activity

Location:

`investigations/initial-access/`

---

### Execution  (Planned)

Future investigations will demonstrate how malicious code executes on an endpoint and how those activities can be detected through process telemetry and command-line logging.

Examples:

• Suspicious PowerShell execution  
• Malicious process spawning  
• Script-based execution activity

---

### Persistence  (Planned)

These investigations will focus on how attackers maintain access after the initial compromise.

Examples:

• Registry run key persistence  
• Startup folder persistence  
• Scheduled task creation

---

### Command and Control  (Planned)

Future investigations will simulate attacker communication with external infrastructure and how it can be detected through network monitoring.

Examples:

• Suspicious outbound connections  
• DNS beaconing activity  
• Command and control traffic detection
