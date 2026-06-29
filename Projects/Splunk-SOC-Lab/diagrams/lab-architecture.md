# Lab Architecture

## Environment

The lab consists of two virtual machines hosted on VMware Workstation.

### Ubuntu VM
- Splunk Enterprise
- Receives logs from Windows endpoint
- Hosts dashboards and searches

### Windows 10 VM
- Sysmon installed
- Splunk Universal Forwarder installed
- Sends Windows Event Logs and Sysmon logs to Splunk

## Data Flow

Windows 10
      │
      │ Windows Event Logs
      │ Sysmon Logs
      ▼
Splunk Universal Forwarder
      │
      ▼
Splunk Enterprise (Ubuntu)
      │
      ▼
Dashboards • Searches • Alerts
