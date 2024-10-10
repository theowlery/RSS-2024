Visibility Beyond EDR
---------------------

Logic App to grab logs from CrowdStrike will be uploaded soon

Other Key Items:

- Turn on PowerShell Script Block Logging and send logs back to SIEM
- New Scheduled Task - forward Event ID 4698 (Security) to the SIEM
- New Service Created - forward Event ID 7045 (System) to the SIEM
- EDR Bypass events to send to SIEM:
	- Event ID 5001 (Windows Defender/Operational)
	- Event ID 5013 (Windows Defender/Operational)
	- Event ID 7063 (System)
- Log Tampering:
	- Clearing Logs - Event ID 1102 (Security) or Event ID 104 (System) or 
	- Monitor command line using the following Event ID 4104 (PowerShell) to monitor Script Block Logs
		- Can monitor for: wevtutil cl Security, Clear-EventLog, Remove-EventLog
	- Disable Event Log Service
		- Service Control Manager Event ID 7035 (monitor for stopping of EventLog service)
