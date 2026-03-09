# Malicious LNK Execution

## Scenario Overview

This scenario simulates a malicious Windows shortcut (LNK) file delivered through a phishing-style HTML page. When the user downloads and executes the shortcut, it launches a command chain that ultimately runs a payload.

The goal of this exercise was to observe how user execution appears in endpoint telemetry and investigate the activity using Splunk.

## Attack Flow

HTML lure page  
→ User downloads malicious LNK file  
→ LNK executes cmd.exe  
→ cmd.exe launches powershell.exe with ExecutionPolicy bypass  
→ PowerShell launches calc.exe

## Detection Investigation

The activity was investigated using Splunk by analyzing Sysmon Event ID 1 (Process Creation).

The process chain observed:
explorer.exe
→ cmd.exe
→ powershell.exe
→ calc.exe

Indicators of suspicious behavior included:

- PowerShell execution with `ExecutionPolicy Bypass`
- Hidden PowerShell window execution
- Unusual process parent-child relationships

## Evidence

Screenshots in this folder demonstrate:

1. The phishing-style HTML lure page
2. Execution of the malicious LNK file
3. The resulting process chain visible in Splunk
