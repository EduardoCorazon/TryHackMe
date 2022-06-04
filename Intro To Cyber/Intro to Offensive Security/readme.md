# Intro to Offensive Security

# Web Application Security

It’s important to protect the database servers from attacks like cross site scripting (JavaScript injection), SQL injection, or other areas that might be vulnerable

![Untitled](Intro%20to%20Offensive%20Security%204981bd9f29a4473b8af32da0c6403218/Untitled.png)

Potential attack vectors:

- Log in at the website: try to find crack password via bruteforce
- Search for the product: SQL or Cross Site Script injection
- Provide payment details: see if details are sent in cleartext or using weak encryption

Make sure Access Control is set up following the principle of least privilege, meaning a user will only the given the minimum amount of privileges based on their occupation

## Insecure Direct Object References (IDOR)

Can be exploited is access control is broken. It allows you to access other users and information simply by modifying the url. 

https://store.tryhackme.thm/customers/user?id=16

^here we modify the id# to gain access to other accounts

# Operating System Security

## CIA

The 3 aspects of security

- Confidentiality: private files and info are only available to intended persons
- Integrity: No one can tamper with files on system or when being transferred
- Availability: System should be available when needed

![Untitled](Intro%20to%20Offensive%20Security%204981bd9f29a4473b8af32da0c6403218/Untitled%201.png)

## Targets for attack

Malicious users usually try to take advantage of the following

- Authentication and weak passwords: users usually use weak passwords or passwords associated with personal information
- Weak File permissions: get access to files without authorization and modify them
- Malicious Programs: Using trojan horses for backdoors, ransomware, etc

# Network Security

Hardware solutions:

- Firewall (physical) : restrict what enter and leaves a network
- Intrusion Detection System (IDS): Detect network intrusion attempts
- Intrusion Preventions System (IPS): Blocks detected intrusions
- Virtual Private Network (VPN): ensure network traffic cannot be read or altered by a third party

Software solutions:

- Antivirus software: prevent malicious programs from running
- Host firewall: program part of OS (for ex. Windows Firewall)

## Steps to Attack

![Untitled](Intro%20to%20Offensive%20Security%204981bd9f29a4473b8af32da0c6403218/Untitled%202.png)

1. Recon: learn as much as possible about the target
2. Weaponization: prepare or make the payload
3. Delivery: send the payload to the victim 
4. Exploitation: Victim runs the payload
5. Installation: Payload installs itself unto the system
6. Command & Control (C2): System connects back to attacker and now attacker can control it
7. Actions on Objectives: do what you intended, for ex. stealing data