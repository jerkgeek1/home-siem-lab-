# home-siem-lab-
A home SIEM lab using Wazuh to collect and investigate Windows security events.

# Home SIEM Lab Using Wazuh

## Overview

This project demonstrates a home Security Information and Event Management
lab using Wazuh and a Windows endpoint.

## Objectives

- Deploy Wazuh in VirtualBox
- Connect a Windows endpoint
- Collect Windows security logs
- Investigate failed and successful logons
- Monitor process creation events
- Practice SOC alert investigation and documentation

## Lab Architecture

- Wazuh Manager, Indexer, and Dashboard: Wazuh OVA
- Endpoint: Windows 11 laptop
- Virtualization: Oracle VirtualBox
- Agent: Wazuh Windows Agent

## Investigations Performed

### 1. Failed Logon Investigation

- Windows Event ID: 4625
- Wazuh Rule ID: 60122
- Activity: Failed interactive logons
- Source IP: 127.0.0.1
- Assessment: Benign local authentication testing

### 2. Successful Logon Investigation

- Windows Event ID: 4624
- Wazuh Rule ID: 60118
- Activity: Successful interactive logon
- Assessment: Successful login after intentional failed attempts

### 3. Process Creation Investigation

- Windows Event ID: 4688
- Wazuh Rule ID: 67027
- Processes observed:
  - powershell.exe
  - WmiPrvSE.exe
  - BraveUpdate.exe

## Findings

The lab successfully collected Windows security events and allowed
investigation of authentication and process creation activity.

The observed failed logons originated from localhost and were followed
by a successful login. No evidence of remote brute-force activity was found.

## Skills Demonstrated

- Wazuh SIEM
- Windows Event IDs
- Log analysis
- Alert triage
- Process investigation
- Basic incident documentation
- Security monitoring
