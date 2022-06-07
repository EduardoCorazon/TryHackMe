# Intro to Defensive Security

It prevents intrusions from occurring as well as detecting when a system has been compromised and responding properly to minimize the damage.

Some of the common tasks are:

- Training users about how to defend themselves
- Manage business assets
- Updating and patching systems
- Set up Preventative security devices such as firewalls and intrusion prevention systems (IPS), which block unwanted traffic and traffic with attack signatures
- Set up Logging and monitoring devices

# Security Operations Center (SOC)

A team of cyber professionals that monitor network traffic and systems to detect security events such as vulnerabilities, Policy violations, unauthorized activity, and network intrusions. 

Security Information and Event Management (SIEM) - presents user with various security information related events

## Services

SOC collects data from sources like Server logs, DNS activity, Firewall logs, and DHCP logs

Reactive services:

task initiated after detecting an intrusion or malicious event

- Monitor security posture ← primary role, monitor network and systems for alters and responding appropriately
- Vulnerability management ← finding vulnerabilities in the system and patching (fixing) them
- Malware analysis ← send SOC to advanced analysis for reverse engineering
- Intrusion detection system (IDS) ← detect and log intrusions of suspicious network traffic
- Reporting ← compliance requirements to report incident and alarms

Proactive services: 

handles by the SOC without any indicator of an intrusion

- Network Security Monitoring (NSM) ←  monitoring network data ana analyzing the traffic to detect sign of intrusions
- Threat hunting ← SOC assumes intrusion has already taken place and tries to find if that’s actually true
- Threat intelligence ← learn about potential adversaries and tactics
- Cyber security training ← train employees to use solid security methods

## Threat Intelligence

Use information gathered about current and potential enemies to create a threat-informed defense, aka defend targets that are more likely to be attacked

You can use tools like AbuseIPDB or Cisco Talos Intelligence to check IP address reputation

# Digital Forensics and Incident Response (DFIR)

Focus on the digital aspect of things

## Digital Forensics

Analyses evidence of an attack by looking at the File system, System memory, System logs, and network logs

- Public-sector investigation - carried out by government and law enforcement
- Private-sector investigation - carried out by corporate bodies, triggered by corporate policy violations

### Required Steps

At the scene:

1. Collect evidence like laptops, storage devices, and cameras
2. Establish a chain of custody so only authorized investigators have access and fill out related form
    
    [Sample-Chain-of-Custody-Form.docx](Intro%20to%20Defensive%20Security%20fa775dcaffb44812a0b822e7abbe6219/Sample-Chain-of-Custody-Form.docx)
    
3. Place evidence in a secure container
4. Transport evidence to lab

At the lab:

1. Retrieve the digital evidence from the secure container
2. Create forensic copy of evidence
3. Return digital evidence to the secure container
4. start processing the copy on your workstation

## Incident Response

Methods and plans in place in order to minimize the damage done by an attack and recover as quickly as possible. 

1. Preparation ← Team to handle and prevent incidents
2. Detection and analysis ← Team has resources to detect incident and analyze its severity
3. Containments, Eradiation, and recovery ← Stop the incident from affecting other systems
4. Post-incident activity ← report is produced and noted in order to prevent similar incidents

![Untitled](Intro%20to%20Defensive%20Security%20fa775dcaffb44812a0b822e7abbe6219/Untitled.png)

## Malware Analysis

Static analysis - inspect malicious program without running it

Dynamic analysis - running malware in a controlled environment and monitoring its activities

- Virus ← designed make the system slow or unusable and spreads from computer
- Trojan ← fakes being a useful program in order to install a backdoor
- Ransomware ← encrypts files and money is demanded