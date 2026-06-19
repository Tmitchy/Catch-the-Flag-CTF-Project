# Catch-the-Flag-CTF-Project


# 🛡️ Two Tulip Estates - Ethical Hacking & CTF Assessment

![Kali Linux](https://img.shields.io/badge/Kali-Linux-blue)
![Ubuntu](https://img.shields.io/badge/Ubuntu-Server-orange)
![CTF](https://img.shields.io/badge/Capture-The%20Flag-red)
![Status](https://img.shields.io/badge/Status-Completed-success)

## 📖 Overview

This repository documents an Ethical Hacking and Capture The Flag (CTF) assessment conducted against a vulnerable Ubuntu-based virtual machine simulating a real estate company environment called **Two Tulip Estates**.

The objective was to perform reconnaissance, identify vulnerabilities, exploit weaknesses, obtain challenge flags, escalate privileges, and recommend security improvements.

---

## 🎯 Objectives

* Perform network reconnaissance
* Enumerate services and applications
* Identify security vulnerabilities
* Exploit weaknesses to obtain flags
* Escalate privileges where possible
* Demonstrate post-exploitation techniques
* Recommend remediation measures

---

## 🛠️ Tools Used

| Tool            | Purpose                        |
| --------------- | ------------------------------ |
| Nmap            | Network Scanning & Enumeration |
| Metasploit      | Exploitation & Enumeration     |
| SQLMap          | SQL Injection Testing          |
| Burp Suite      | Web Application Testing        |
| Hydra           | Password Auditing              |
| John The Ripper | Password Cracking              |
| CeWL            | Password Profiling             |
| SSH             | Remote Access                  |
| Docker          | Privilege Escalation Analysis  |
| Kali Linux      | Attack Platform                |

---

## Project Files

Inside this repository, you'll find:

| File/Folder | Description |
|-------------|-------------|
| `images-files/` | [📂 Directory containing`image` files](https://github.com/Tmitchy/Catch-the-Flag-CTF-Project/tree/main/images)|
| `.docx` | 🧪 [A report providing an overview of the analysis conducted on the Vulnerable virtual machine using the mentioned tools.](https://github.com/Tmitchy/Catch-the-Flag-CTF-Project/blob/main/CT5049_EthicalHackingAssessment_s4417613.docx) |

<br><br>

# 🔍 Methodology

## Phase 1 – Reconnaissance & Enumeration

The first stage involved discovering live hosts and identifying exposed services running on the target machine.

### Actions Performed

* Identified attacker and target IP addresses
* Conducted host discovery
* Enumerated open ports
* Identified running services
* Detected service versions
* Performed vulnerability scans

### Commands Used

```bash
ip a

nmap -sn 192.168.56.0/24

nmap -sC -sV -p- 192.168.56.200
```

### Screenshot

![Nmap Enumeration](https://github.com/Tmitchy/Catch-the-Flag-CTF-Project/blob/main/images/Reconnaissance%20%26%20Enumeration.png)

---

## Phase 2 – Web Application Enumeration

The web server hosted a WordPress application that provided valuable information about users and available services.

### Actions Performed

* Identified the website
* Collected employee information
* Enumerated directories
* Located authentication portals
* Identified valid usernames

### Screenshot

![Directory Enumeration](https://github.com/Tmitchy/Catch-the-Flag-CTF-Project/blob/main/images/Directory%20Enumeration.png)

---

## Phase 3 – Credential Discovery

Reconnaissance findings were leveraged to identify valid credentials and gain access to the web application.

### Actions Performed

* User enumeration
* Password profiling
* Login testing
* Account validation

### Screenshot

![WordPress Access](https://github.com/Tmitchy/Catch-the-Flag-CTF-Project/blob/main/images/WordPress%20Access.png)

---

## Phase 4 – Privilege Escalation

User permissions were reviewed to identify privilege escalation opportunities.

A Docker misconfiguration allowed escalation from a standard user account to root privileges.

### Actions Performed

* Enumerated user groups
* Identified Docker membership
* Exploited Docker privileges
* Obtained root access

### Screenshot

![Docker Privilege Escalation](https://github.com/Tmitchy/Catch-the-Flag-CTF-Project/blob/main/images/Docker%20Privilege%20Escalation.png)

---

## Phase 5 – Database Security Testing

A custom web application was tested for SQL Injection vulnerabilities.

### Actions Performed

* Tested application inputs
* Confirmed SQL Injection vulnerability
* Enumerated database tables
* Retrieved application data

### Screenshot

![SQL Injection](https://github.com/Tmitchy/Catch-the-Flag-CTF-Project/blob/main/images/SQL%20Injection.png)

---

## Phase 6 – Post Exploitation

Post-exploitation techniques were demonstrated to assess the overall impact of a successful compromise.

### Activities

* SSH Configuration
* SSH Key Authentication
* User Management
* Log Analysis
* Persistence Demonstration

### Screenshot

![SSH Access](https://github.com/Tmitchy/Catch-the-Flag-CTF-Project/blob/main/images/SSH%20Access.png)

---

# 🚩 Key Findings

| Vulnerability               | Severity    |
| --------------------------- | ----------- |
| SQL Injection               | 🔴 High     |
| Weak Credentials            | 🔴 High     |
| Information Disclosure      | 🟠 Medium   |
| Docker Privilege Escalation | 🔴 Critical |
| Excessive User Permissions  | 🔴 High     |

---

# 🔒 Security Recommendations

## SQL Injection

* Use prepared statements
* Validate all user input
* Implement parameterized queries

## Cross-Site Scripting (XSS)

* Sanitize user input
* Encode application output
* Apply secure coding practices

## Docker Security

* Use Rootless Docker
* Restrict Docker group membership
* Apply least-privilege principles

## Authentication

* Enforce strong password policies
* Implement Multi-Factor Authentication (MFA)
* Review user permissions regularly

---

# 📚 Skills Demonstrated

* Ethical Hacking
* Vulnerability Assessment
* Penetration Testing
* Web Application Security
* SQL Injection Testing
* Privilege Escalation
* Linux Administration
* SSH Configuration
* Security Hardening
* Security Reporting

---

# ⚠️ Disclaimer

This project was conducted in a controlled laboratory environment for educational purposes only. All testing was performed on authorized systems designed for ethical hacking and cybersecurity training.
