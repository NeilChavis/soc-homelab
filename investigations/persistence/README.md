# Persistence Investigations

This section documents simulated persistence techniques observed within the SOC homelab environment.

The goal of these exercises is to understand how attackers maintain access after initial compromise and how those techniques can be investigated using endpoint telemetry, command-line visibility, and SIEM analysis.

Each investigation reconstructs attacker activity, correlates logs, and documents the evidence collected during analysis.

---

## Investigations

### Startup Folder Persistence

This scenario simulates an attacker establishing persistence by placing a malicious Windows shortcut file in the Startup folder. The shortcut launches `cmd.exe`, which then executes PowerShell with an encoded command when the user logs in.

Investigation includes:

- Startup folder persistence using a malicious `.lnk` file
- Command execution through `cmd.exe`
- Encoded PowerShell execution
- Process tree analysis in Splunk
- Sysmon endpoint telemetry review

Location:

[startup-folder-persistence](./startup-folder-persistence)

---

### Registry Run Key Persistence

This scenario will simulate an attacker maintaining persistence through a Windows Run key so that malicious commands or payloads execute when a user logs in.

Investigation will include:

- Registry Run key modification
- Autorun persistence behavior
- Sysmon registry event analysis
- Process execution tracing in Splunk

Location:

[registry-run-key-persistence](./registry-run-key-persistence)

---

### Scheduled Task Persistence

This scenario will simulate an attacker creating a scheduled task to maintain execution on a host at logon or on a defined trigger.

Investigation will include:

- Scheduled task creation
- Persistence through task based execution
- Command line and process telemetry review
- Splunk investigation of related events

Location:

[scheduled-task-persistence](./scheduled-task-persistence)

---

These investigations demonstrate how analysts can identify and investigate common Windows persistence mechanisms using endpoint logs and SIEM based analysis.
