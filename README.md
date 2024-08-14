Assessing and Securing Systems on a Wide Area Network (WAN) 

## Overview
The Objective in this lab was to use Nmap OS Scan to discover vulnerabilities on an already compromised system.  Then harden the system and reduce the attack surface of the network asset

---

## Lab Steps

### Step 1: Decoy IP address 
**Description:** At the TargetNMAP command prompt execute tcpdump - r phillip_capture_s2, then
At the vWorkstation command prompt execute the Nmap command to detect the operating system of the TargetVulnerable01 machine with increased output verbosity

![Decoy IP address](https://github.com/user-attachments/assets/9260d479-5c0b-4fcd-8daf-812f0dd06b40)

---

### Step 2: Results of Scan
**Description:**Results of the Nmap OS scan for TargetVulnerable01 .

![Results of the Nmap OS scan for TargetVulnerable01](https://github.com/user-attachments/assets/da5a2991-836c-4297-9748-b96e47eb6613)

*Here you can see that port 3389/tcp is open on 100.15.15.50.  The OS of the scanned asset is Microsoft Windows 2003.*
---

### Step 3: Details of the threat to TargetWindows04 
**Description:** suedo anti virus scan was used to show the details of the threat to TargetWindows04 asset. Of the 347 scanned files 6 were found to be infected and needed to be eradicated from the system.

![Details of the threat to TargetWindows04](https://github.com/user-attachments/assets/5fb8b922-c42a-4de4-b3db-e2d3ccebdb8f)

*Results of the scan before eradication and resolution.*

---

### Step 4:	Details of the threat to TargetWindows05  
**Description:* The AVG Business tool was used to run a scan on a specific file/folder on the Administrator desktop.

![Details of the threat to TargetWindows05](https://github.com/user-attachments/assets/f6da14eb-3d76-4352-bb8f-aaed134328ec)


*This screen indicates 2 threats were found.*

---
### Step 5: Timed out ping of TargeVulnerable01
**Description:** In order to harden the network new fire wall rules were put into place to limit some traffic and disable ping traffic. Thereby mitigated DDOS attacks to the network

![Timed out ping of TargetVulnerable01](https://github.com/user-attachments/assets/30638fd0-1ac3-4b8d-9b74-6400384e1a49)


*After so many pings the firewall rule initiated and timed out ping request.*

---
### Step 6: New Nmap scan results for TargetVulerable01 and the reduced attack surface 
**Description:** New network rules were put into effect.  Closing ports that should be closed but leaving the remote desktop service (3389) open. The windows 2003 server/vWorkstation was the only asset allowed to connect

![New Nmap scan results for TargetVulerable01 and the reduced attack surface](https://github.com/user-attachments/assets/3e937623-6b01-409b-b45d-06fa4de1afda)

*Results of scan showing 1 IP address (1 host up) and no other ports open.*

---
### Step 7: Remote Desktop rule within the rules.txt file 
**Description:** This shows the fire wall rules there were put into place to reduce the attack surface on the windows server.

![Remote Desktop rule within the rules txt file](https://github.com/user-attachments/assets/942c7c75-a32e-48b1-8afd-e3e1b8bdd4dc)


*Highlighted portion shows the Remote desktop rule within a txt.file.*

---
### Step 8: Timed out ping of TargetWindows04 
**Description:*Reduce the attack Surface on other asset connected to windows 2008 server* 

![Timed out ping of TargetWindows04](https://github.com/user-attachments/assets/ad4beac8-2e4c-472f-a036-aef81a33e3b0)

*Verfying the set rules to disable ICMP traffic are indeed working.*

---
### Step 9: Nmap scan results and the reduced attack surface for TargetWindows04 
**Description:*Re-ran the Nmap operating system detection scan on TargetWindows04* 

![Nmap scan results and the reduced attack surface for TargetWindows04](https://github.com/user-attachments/assets/9380a46b-6edf-4bdd-885d-cc64110965ea)


*Showing that attack surface has indeed been reduced for TargetWindows04 asset.*

---


## Results
We essentially enhanced our network security by reconfiguring the firewall to block traffic through a specific port, thereby hardening the network and reducing potential vulnerabilities.

---
