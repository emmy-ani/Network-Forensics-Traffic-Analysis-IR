# Network Forensics & Incident Response Lab

## 📌 Project Overview
This repository contains hands-on network forensics and incident response investigations completed as part of cybersecurity training and lab exercises. The projects focus on analyzing web application compromises, identifying attacker activity, reconstructing attack timelines, and recommending security controls to prevent future incidents.

---

## 🛠️ Skills, Tools & Technologies
### Core Skills Demonstrated
* **Network Traffic Analysis** (Wireshark PCAP)
* **Incident Response & Investigation**
* **Log Analysis & IOC Identification**
* **Web Application Attack Analysis**
* **Attack Timeline Reconstruction**
* **Security Control Recommendations**

### Tools & Frameworks Used
* **Analysis Tools:** Wireshark, Linux CLI, Apache Web Server Logs
* **Protocols:** HTTP/TCP Protocol Analysis
* **Frameworks:** Cyber Kill Chain Framework

---

## 📂 Case Studies

### Case Study 1: Web Application Compromise Investigation
* **Objective:** Analyze packet captures from a compromised web application environment and identify the attack path used by the threat actor.
* **Key Findings:**
  * Identified SQL injection activity targeting the application database.
  * Observed directory enumeration and credential abuse.
  * Tracked malicious PHP web shell deployment.
  * Reconstructed the attack chain from initial access to remote command execution.
  * Documented indicators of compromise (IOCs) and remediation recommendations.
* **📄 Report:** [View Full PDF Report](./documentation/SOC_PCAP%20analysis%20Operation%20Silent%20Intrusion.pdf)

### Case Study 2: File Upload Exploitation Incident Response
* **Objective:** Investigate a web server compromise resulting from insecure file upload functionality.
* **Key Findings:**
  * Identified malicious file upload activity.
  * Tracked attacker actions under the `www-data` service account.
  * Reconstructed the sequence of events leading to unauthorized system access.
  * Documented evidence of sensitive file access and data exposure.
  * Provided mitigation recommendations to strengthen upload security controls.
* **📄 Report:** [View Full PDF Report](./documentation/SOC%20Incident%20Report_Operation%20Shadow%20Drop.pdf)

---

## 📈 Security Recommendations
1. **Implement Parameterized Queries:** Prevent SQL injection at the database level.
2. **Secure File Uploads:** Enforce strict file validation and storage controls.
3. **Restrict Script Execution:** Disable script execution rights globally within public upload directories.
4. **Enforce Least Privilege:** Strictly limit permissions bound to the `www-data` service account.
5. **Egress Filtering:** Restrict unnecessary outbound connections to mitigate Command-and-Control (C2) reverse-shell risks.
