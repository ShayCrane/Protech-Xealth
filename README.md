# OPS 401d5 Midterm Project Scenario and Guidelines

## grepTribe Team Members
- Jonathan Salhus
- Ariel Doyle
- Shannon Crane
- James Moring

## Scenario & Problem Domain
The COVID-19 pandemic has greatly accelerated the adoption of digital tools by healthcare providers. In 2020, Seattle-based company Xealth teamed up with Cerner, a leading electronic health record company, to work with hospitals on implementing digital health programs.

Xealth is a digital health prescribing platform that enables clinicians to easily integrate, prescribe and monitor digital health tools for patients from their electronic health record (EHR) workflows. These can include patient education, online third-party apps and programs, device monitoring, and non-clinical services such as ride shares, food delivery, and e-commerce product recommendations. Using the Xealth platform, care teams and physicians can monitor patient engagement and analyze the effects of more engaged patients. Xealth spun out of Providence St. Joseph Health (PSJH) in 2017, raising $9 million from a variety of investors including Providence Ventures and other health systems such as UPMC and Froedtert Medical College of Wisconsin. -Xealth

## Project Requirements
Due to a recent audit, a number of internal processes and systems were found to be in need of revision. Your team has been contracted to provide ongoing cyber security monitoring and incident response services to Xealth as its platform grows. You'll need to implement the following in the AWS Cloud to demonstrate to Xealth how you'll protect their systems:
 
### Proper IAM for all team members must be implemented using AWS best practices
- Use root sparingly and with MFA
- Administrator permissions OK

### CIS-compliant Windows Server DC
- Windows Server hosts controlled patient data on a private subnet of a VPC only accessible via VPN tunneling (add additional instances or services as necessary)
- Patient data needs to be encrypted at rest and encrypted in transit
- Deploy Sysmon to generate security-relevant system logs

### SIEM/log aggregation system
- Options include Splunk Enterprise (Trial), CloudWatch, and Elastic Stack
- Configure to ingest event logs in real-time from key assets
- Demonstrate an attack TTP with the goal of HIPAA data exfiltration. The attack methodology must incorporate a Python script utilizing a new library you have not worked with yet. This should trigger an event that gets ingested by the SIEM.

### Network traffic monitoring
- Using a packet capture tool, capture malicious network traffic associated with your attack as a PCAP.
- Analyze the packets and identify HIPAA data being exfiltrated. Apply your encryption and security schemes, then re-analyze the traffic to demonstrate effective countermeasures.
- Incorporate the PCAP analysis into your demonstration.

### DLP controls
- Implement a DLP solution of your choosing on a transport protocol of your choosing
- Configured to detect and prevent the exfiltration of HIPAA data classes from the Windows Server

Here is a copy of the [Xealth Network Security Assessment.](https://www.icloud.com/iclouddrive/0xI962tCmPxawI5W_clmCAHhw#Network_Security_Assessment_-_Xealth)
 
Sincerely, 
Julia Chi, CTO Xealth
 
## Team Signups
  - Proper IAM: Shay
  - CIS-compliant Windows Server DC: Shay
  - SIEM/log aggregation system: Jon
  - Network traffic monitoring: Jon
  - DLP controls: James
  - Deliverables: Ariel

## Team Project Resources and Deliverables
- [OPS 401 Project Guidelines](https://github.com/codefellows/seattle-ops-401d5/blob/main/class-20/project-guidelines.md)
- [Trello Project Management Page](https://trello.com/b/3hQApNiW/protech-xealth)
- [Google Drive Project Documentation Folder](https://drive.google.com/drive/folders/10q1iTIIHyK_R2-ltvlMJH7dfzzKp7_BJ?usp=sharing)
- [Project Whiteboard](https://miro.com/app/board/uXjVPUzvjBI=/)
