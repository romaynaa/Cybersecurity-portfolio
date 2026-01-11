# CYBER SECURITY PORTFOLIO
## Roma Yana Pasaribu
Hi! My name is Roma Yana Pasaribu, and I am a cybersecurity enthusiast to learning and applying best practice to protect data and systems. Currently, I am a bachelor's student majoring in Information Technology, with a focus on penetration testing and threat analysis.
Current Role: Student

## Executive Summary
This activity was conducted to identify security vulnerabilities within internal system using an authorized TrayHackMe lab environment. The assessment focused on the SMB (Server Message Block) service running on a window-based system.

The result of the assessment revealed that the target system was still using SMBv1 and was vulnerable to a Remote Code Execution (RCE) flaw known as MS17-010 (EternalBlue). This vulnerability allows an attacker to execute arbitrary commands remotely without authentication and may lead to full system.

## Testing Scope & Environment
- Platform: TryHackMe
- Assessment Type: Internal Penetration Testing
- Approach: Black Box
-	Target System: Windows-based host
-	Critical Service: SMB (Server Message Block)

## Methodology
###  Reconnaissance
Initial information gathering was performed to identify active hosts and exposed network service.

###  Scanning
Network scanning identified multiple open ports, with particular attention to port 445, which was running outdated SMBv1 service.

###  Vulnerability Analysis
Based on the scanning results, the identified services were analyzed to determine potential security weaknesses. The SMB service running on port 445 was identified as using SMBv1, which is known to be vulnerable to MS17-010 (EternalBlue). This vulnerability was assessed in terms of potential impact, exploitability, and overall risk level.

###  Exploitation
A controlled exploitation was performed to validate the impact of the identified vulnerability. The exploitation confirmed that vulnerability could lead to Remote Code Execution (RCE) with administrative privileges.

###  Tools & Skills Demonstrated
#### Tools
-	Nmap
Used for Reconnaissance and Scanning phase
-	Windows SMB Analysis
Used for Vulnerability Analysis phase
- Metasploit Framework
Used for Exploitation

#### Skills
-	Vulnerability Analysis
-	CVSS v3.1 Risk Scoring
-	Security Documentation

## Key Security Finding
Remote Code Execution – SMBv1 (MS17-010 EternalBlue)
The assessment identified that the target system was running the legacy SMBv1 protocol, which is vulnerable to MS17-010 (EternalBlue). This vulnerability allows an attacker to remotely execute arbitrary code on the target system without authentication by sending specially crafted network packets to the SMB service.

### How It Works
-	The attacker scans the internal network to identify system exposing the SMN service on port 445.
-	The attacker determines that the target system is using SMBv1, an outdated and insecure protocol.
-	A flaw in SMBv1’s handling of specially crafted packets allows memory corruption.
-	By exploiting this flaw, the attacker can trigger RCE
-	Successfull exploitation results in system-level access, allowing full control of the affected system.

### Risk Level
-	CVSS v3.1 Base Score: 9.8 (Critical)
-	Vector: AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:H/A:H

### Potential Impact
-	Complete system compromise
-	Unauthorized access to sensitive data
-	Lateral movement across the internet network
-	Malware or ransomware deployment
-	Disruption of business operations
 
## Evidence
Sanitized evidence was collected to support this finding, including:
-	SMB service discovery results
-	Vulnerability validation output
-	Proof of administrative-level access

## Security Recommendations
Based on the assessment, the following defensive measures are recommended:
-	Disable legacy SMBv1
-	Apply security patches (MS17-010)
-	Update SMBv1 to SMB2 / SMBv3
-	Restrict SMB access via firewall rules
-	Implement routine patch management
-	Conduct regular security assessments






