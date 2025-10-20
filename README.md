# 🛡️ Cybersecurity Internship - Task 1  
### **Network Port Scanning using Nmap and Wireshark**

**Student:** Muthukumaran R 
**Task Title:** Scan Your Local Network for Open Ports  
**Objective:** Learn to discover open ports on devices in your local network using Nmap and understand network exposure.

---

## 🔍 Objective
The goal of this task was to perform **network reconnaissance** using **Nmap** and optionally analyze network traffic with **Wireshark**.  
This helps understand how open ports reveal running services and potential vulnerabilities in a network.

---

## ⚙️ Tools Used
- **Nmap** — for scanning IP ranges and detecting open ports  
- **Wireshark** — for capturing and analyzing network packets  
- **Operating System:** Windows

---

## 🧠 Key Concepts
- Port Scanning  
- TCP SYN Scan  
- IP Ranges & Subnets  
- Network Reconnaissance  
- Service Detection  
- Network Security Basics

---

## 🧩 Steps Performed

### Steps Performed (Windows)

1. Install tools on Windows

 Nmap

 1. Download the Windows installer from: https://nmap.org/
 2. Run the installer (keep default options).
 3. Verify installation in PowerShell:
    nmap --version

 Wireshark (optional, recommended for packet capture)

 1. Download the Windows installer from: https://www.wireshark.org/download.html
 2. Run the installer. Allow WinPcap/Npcap when prompted (required for capturing).
 3. Launch Wireshark from Start Menu.


 2.Identify your local IP & subnet (Windows PowerShell)

   Open PowerShell and run: 
     ipconfig 
   Look for your active adapter’s IPv4 address (example: IPv4 Address. . . . . . . . . . : 192.168.1.45 
   Determine the subnet (usually /24). Example subnet: 192.168.1.0/24. 
   Save the subnet to a file: 
     "192.168.1.0/24" | Out-File -Encoding utf8 detected_subnet.txt 


3. Run a TCP SYN scan with Nmap (Windows PowerShell or CMD) 

   Open PowerShell (Run as Administrator if necessary). 
   Run the scan (replace subnet with your detected subnet): 
    nmap -sS 192.168.1.0/24 
   Save results to a file: 
    nmap -sS 192.168.1.0/24 -oN scan_results.txt 
   Optional: service/version detection: 
    nmap -sS -sV 192.168.1.0/24 -oN scan_results_with_services.txt 


