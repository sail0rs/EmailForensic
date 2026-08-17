# **🕵️‍♂️ Automated Phishing Email Analyzer (eIOC)**

**A Zero-Trust, Zero-Execution initial reconnaissance utility for cybercrime investigators and DFIR first responders.**

The Automated Phishing Email Analyzer (eIOC) acts as an isolated operational buffer between a digital forensics investigator and weaponized email payloads. It parses raw `.eml` files, extracts hidden network indicators, safely maps remote infrastructure via `urlscan.io`, and correlates attachment hashes against `VirusTotal`—reducing a 45-minute manual triage process to a safe, 30-second automated scan.

## **📸  Previews**

### **Live Threat Intelligence Terminal Output**

<img width="1410" height="279" alt="Screenshot 2026-08-17 143716" src="https://github.com/user-attachments/assets/5f97ce9f-bf1c-45c2-9a45-5d99794604e8" />

<img width="1898" height="898" alt="Screenshot 2026-06-20 212334" src="https://github.com/user-attachments/assets/dc94b672-2f9c-4d1e-9618-6b1d5932327c" />

<img width="1898" height="971" alt="Screenshot 2026-06-20 212439" src="https://github.com/user-attachments/assets/ba19b6bf-8d04-4f03-b72d-5686eb06fbde" />

<img width="918" height="691" alt="Screenshot 2026-06-20 212513" src="https://github.com/user-attachments/assets/18d4c9e0-091a-48a3-825f-a942ba25ef67" />



> 

## 

## **✨ Key Features & Capabilities**

* **🛡️ Zero-Execution File Processing:** Analyzes `.eml` and binary attachments statically. Malicious payloads are never executed locally.  
* **🔗 Link Defanging & Tracking Resolution:** Automatically neutralizes raw URLs (`hxxps[://]malicious[.]com`) and passively resolves marketing redirectors without loading client-side exploits.  
* **🗺️ Remote Infrastructure Mapping (`urlscan.io`):** Dispatches target links to unlisted cloud sandboxes to map connected IPs, Autonomous System Numbers (ASNs), and domains.  
* **📸 Automated Evidence Preservation:** Safely fetches and stores live webpage screenshots of phishing sites directly to your local case folder.  
* **🦠 Cryptographic Fingerprinting (`VirusTotal`):** Extracts attachments and queries their SHA-256 signatures against global threat databases to retrieve malware detection stats and known file aliases.  
* **🕵️‍♂️ 100% OPSEC Safe:** Prevents threat actors from identifying law enforcement IP addresses during the initial reconnaissance phase.

## **⚙️ Prerequisites**

Pre-compiled executables for Windows and Linux are now available as an alternative to the Python-based installation. To run the tool from source, you will need **Python 3.11+** installed on your computer.

**🚀 Installation & Setup**

### **Option 1: Using Pre-compiled Executables**

1. Download the respective executable for your operating system (`eIOC.exe` for Windows or `eIOC` for Linux).  
2. For Linux, ensure the file has execute permissions by running: `chmod +x eIOC`

## **💻 Usage**

Run the tool by pointing the `-f` flag to your suspicious email file using the following syntax:

*eIOC \[flags\] \<file\_path\>*

**Execution Commands:**

* **Windows:**

  `eIOC.exe -f <path_to_email_file>`

* **Linux:**

  `./eIOC -f <path_to_email_file>`

## **⚖️ Legal & Disclaimer**

**For Authorized Use Only.** This tool is intended for digital forensics, incident response triage, and academic research. The developer assumes no liability for the misuse of this utility or for actions taken against infrastructure mapped by this tool. Always practice strict OPSEC when handling weaponized malware and phishing campaigns.

