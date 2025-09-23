# Network Scanning Project using Nmap - Internship Task 1

## Introduction
Network scanning is a fundamental cybersecurity technique used to discover live hosts, detect open ports, and identify running services on a network. Nmap is one of the most popular tools for this purpose.  

This project demonstrates how to perform network scanning ethically, with the aim of learning security concepts rather than attacking unauthorized systems. Only authorized networks were scanned for educational purposes.  

## Objective
- Learn how to perform network scanning using **Nmap**.  
- Identify online hosts and detect open ports.  
- Save scan results for documentation and analysis.  
- Compare the effectiveness of **full scans vs. fast scans**.  

## Tools Used
- **Nmap (v7.98)** – Network scanning tool.  
- **Terminal / Command Prompt** – To run commands.  
- **Text Editor** – For saving and reviewing scan results.  


## Initial Scan Attempt (Full Scan)
Command:
nmap <host_ip>

**Result:**
Nmap scan report for <host_ip>
Host is up.
All 1000 scanned ports on <host_ip> are in ignored states.
Not shown: 1000 filtered tcp ports (no-response)
Nmap done: 256 IP addresses (15 hosts up) scanned in 8748.67 seconds

- Scan duration: **~2 hours 25 minutes**.  
- All ports were filtered (likely due to firewall/network rules).  
- **Limitation:** Too time-consuming and produced limited usable data.  

## Fast Scan Method
To achieve results more efficiently, a fast scan was performed:  

1. **Ping Scan (live hosts detection):**
nmap -sn <host_ip>.0/24

2. **Fast Port Scan of a Single Host:**
nmap -T4 -F <host_ip>

markdown
Copy code
- `-T4` → faster timing.  
- `-F` → scans only the 100 most common ports.  

3. **Save Results:**
nmap -T4 -F <host_ip> -oN fast_scan.txt

**Outcome:** Results were successfully saved in `fast_scan.txt` for documentation and submission.  

## Results Interpretation
- **Host is up** → Target device is online.  
- **Filtered ports** → Firewall or security filters blocked responses.  
- **Fast Scan** → Completed within minutes and provided practical results compared to the full scan.  

## References
- [Nmap Official Documentation](https://nmap.org/book/)  
- Kali Linux Tools Documentation  
- Wireshark User Guide
- 
## Author
- **Name:** Anushka Jana  
- **Project:** Network Scanning using Nmap (Full Scan & Fast Scan)  
