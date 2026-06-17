# SOC-Automation-Home-Lab

## Objective

Build and operate an automated Security Operations Center (SOC) environment using three virtual machines: a Windows 10 endpoint VM, a Splunk server VM, and an n8n automation server VM. The lab collects Windows security telemetry in Splunk, detects simulated brute-force login activity, sends triggered alerts to n8n through a webhook, enriches source IP addresses with AbuseIPDB, analyzes alerts with OpenAI, and delivers structured notifications to Slack for analyst review. The project provides hands-on experience with virtualized SOC infrastructure, security monitoring, detection engineering, webhook integration, threat-intelligence enrichment, API integration, and automated alert-triage workflows.

### Lab Environment

Windows 10 VM – Monitored endpoint used to generate security telemetry and simulated failed login activity. The system was administered remotely using Remote Desktop Protocol (RDP).
Splunk VM – Dedicated server used for log ingestion, searching, detection, and alerting. The server was administered remotely through SSH.
n8n VM – Dedicated automation server used to process alerts and integrate OpenAI, AbuseIPDB, and Slack. The server was administered remotely through SSH.

### Skills Learned

- Created and managed a multi-VM SOC home-lab environment.
- Configured network communication between the Windows 10, Splunk, and n8n virtual machines.
- Remotely administered Linux-based Splunk and n8n servers through SSH.
- Remotely administered the Windows 10 endpoint through RDP.
- Installed and configured Splunk on a dedicated virtual machine.
- Installed and configured n8n on a separate virtual machine.
- Forwarded Windows security telemetry from the Windows 10 VM to the Splunk VM.
- Searched and analyzed Windows authentication logs in Splunk.
- Simulated repeated failed login attempts in a controlled lab environment.
- Created a Splunk detection for potential brute-force activity.
- Configured a Splunk alert to trigger a webhook hosted on the n8n VM.
- Installed and configured n8n on a dedicated virtual machine.
- Parsed and normalized Splunk alert data in n8n.
- Integrated AbuseIPDB API for source-IP reputation enrichment.
- Integrated OpenAI for AI-assisted alert analysis.
- Integrated Slack for automated SOC notifications.
- Worked with virtual networking, webhooks, REST APIs, JSON, and API credentials.
- Practiced SOC alert triage, enrichment, escalation, and analyst notification workflows.

### Tools Used

- Virtualization software
- Windows 10 Virtual Machine
- Splunk Server Virtual Machine
- n8n Server Virtual Machine
- Splunk Enterprise
- Splunk Web
- Splunk Universal Forwarder
- Windows Security Event Logs
- n8n
- OpenAI API
- AbuseIPDB API
- Slack
- Webhooks
- REST APIs
- JSON
- PowerShell
- Windows Command Line
- Linux Command Line

## Steps

1. Created three virtual machines to separate endpoint monitoring, log analysis, and workflow automation.
   <img width="1236" height="176" alt="Screenshot 2026-06-16 225806" src="https://github.com/user-attachments/assets/d9d7790a-2e53-486b-a398-349e1b19a383" />
   *Ref 1: SOC Home-Lab Virtual Machines.*
   This screenshot shows the Windows 10 endpoint VM, Splunk server VM, and n8n automation VM used in the SOC automation environment.

2. Connected to the Splunk virtual machine through SSH to install, configure, and administer the Splunk server.
   <img width="949" height="631" alt="image" src="https://github.com/user-attachments/assets/bf9ebe2d-82a8-4333-82aa-742cb297d739" />
   *Ref 2: SSH Access to Splunk VM.*
   This screenshot demonstrates a successful SSH connection to the Splunk virtual machine and confirms that the server was remotely accessible for installation, configuration, and troubleshooting.

3. Accessed the Splunk web interface from a browser to configure data ingestion, searches, detections, and alerts.
  <img width="1907" height="946" alt="image" src="https://github.com/user-attachments/assets/c906b965-0ed4-43a2-8de1-c9c3af8f2f20" />
  *Ref 3: Splunk Web Interface.*
  This screenshot shows the Splunk graphical interface used to verify incoming Windows telemetry and configure the brute-force alert.

4. Connected to the n8n virtual machine through SSH to install, configure, and administer the n8n automation platform.
  <img width="842" height="532" alt="image" src="https://github.com/user-attachments/assets/a245613e-75d6-4cb1-a024-92d69b706873" />
  *Ref 4: SSH Access to n8n VM.*
  This screenshot demonstrates a successful SSH connection to the n8n server and confirms that the system was remotely accessible for installation, service management, and troubleshooting.

5. Accessed the n8n web interface from a browser to build and test the SOC automation workflow.
  <img width="1007" height="469" alt="Screenshot 2026-06-16 223333" src="https://github.com/user-attachments/assets/56cdac6a-1191-453b-8689-9d036de2d669" />
  *Ref 5: n8n Web Interface.*
  This screenshot shows the workflow containing the Splunk webhook, AbuseIPDB enrichment, OpenAI analysis, and Slack notification nodes.

6. Connected to the Windows 10 virtual machine using Remote Desktop Protocol to configure the endpoint and generate test activity.
  <img width="873" height="470" alt="image" src="https://github.com/user-attachments/assets/2f157af6-973d-4cd0-a643-c43fbcdd28b1" />
  *Ref 6: RDP Access to Windows 10 VM.*
  This screenshot demonstrates a successful Remote Desktop connection to the Windows 10 endpoint used to configure telemetry forwarding and simulate failed login attempts.

7. Installed and configured the Splunk Universal Forwarder on the Windows 10 VM to send Windows security logs to the Splunk VM.
  <img width="1310" height="629" alt="image" src="https://github.com/user-attachments/assets/980476ea-ff75-4a8a-9d07-5d361e2a4026" />
  *Ref 7: Windows Telemetry Forwarding.*
  This screenshot shows the Windows endpoint configuration used to forward security events to Splunk.

8. Executed the complete SOC automation workflow and verified that the processed alert was successfully delivered to the designated Slack channel.
  <img width="1370" height="534" alt="Screenshot 2026-06-16 223221" src="https://github.com/user-attachments/assets/c640aaf5-6b06-4fa6-adc0-e81fa472a302" />
  <img width="1333" height="150" alt="Screenshot 2026-06-16 223251" src="https://github.com/user-attachments/assets/0a91ae45-f5d9-4ad7-8a62-1df75ca74700" />
  *Ref 8: Automated SOC Alert in Slack.*
   This screenshot shows the final alert output delivered to Slack after the workflow completed. The notification includes the Splunk alert details, affected computer, username, source IP address, AbuseIPDB enrichment results, AI-generated summary, severity assessment, and recommended response actions. This confirms successful end-to-end communication between Splunk, n8n, AbuseIPDB, OpenAI, and Slack.

## References

Splunk Enterprise, Available:
https://www.splunk.com/en_us/download.html

Slack Apps, Available:
https://api.slack.com/apps

Ubuntu VM, Available:
https://ubuntu.com/download/server

Windows VM, Available:
https://www.microsoft.com/en-ca/software-download/windows10

SOC Automation Project 2.0: How To Use AI in Your SOC Workflow, Available:
https://www.youtube.com/watch?v=Xh9AP-x06jU
