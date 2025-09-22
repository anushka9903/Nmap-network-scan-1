Network Scanning Project using Nmap
Project Overview

This project demonstrates network scanning using Nmap to identify live hosts, open ports, and running services. The project was performed for educational purposes with ethical cybersecurity practices—only authorized networks were scanned.

Initially, a full default scan was attempted, but due to network configurations and a large subnet, the scan took too long and returned limited results. A fast scan was then used to achieve meaningful results efficiently.

Table of Contents
Objective
Tools
Initial Scan Attempt
Fast Scan Method
Saving Scan Results
Results Interpretation
Alternative Options
References

Objective

Learn how to perform network scanning using Nmap.
Identify online hosts and detect open ports.
Save scan results for documentation and analysis.
Understand the difference between full scans and fast scans.

Tools
Nmap (v7.98) – Network scanning tool
Terminal / Command Prompt – To run commands
Text Editor – For saving scan results
Initial Scan Attempt
The first scan was a full default scan on the subnet:
nmap 192.168.29.0/24


Result:

Nmap scan report for 192.168.29.151
Host is up.
All 1000 scanned ports on 192.168.29.151 are in ignored states.
Not shown: 1000 filtered tcp ports (no-response)

Nmap done: 256 IP addresses (15 hosts up) scanned in 8748.67 seconds


Scan took ~2 hours 25 minutes.

All ports were filtered, so no open ports were detected.

Due to time constraints and filtered ports, this scan was not practical for submission.

Fast Scan Method
To obtain results quickly, a fast scan was used:
Ping scan to detect live hosts:
nmap -sn 192.168.29.0/24
Fast port scan of a single host:
nmap -T4 -F 192.168.29.151
-T4 → faster timing
-F → scan only 100 most common ports

Save results to a text file:
nmap -T4 -F 192.168.29.151 -oN fast_scan.txt
Results are saved in fast_scan.txt, ready for GitHub.
Results Interpretation
Host is up: Device is online.
Filtered ports: Blocked by firewall or network filter.
Fast scan: Completed in minutes, showing online hosts and open ports (if any).
This method was more practical than the full scan.


References
Nmap Official Documentation
Kali Linux Tools
Wireshark User Guide

Author

Name: Anushka Jana
Course: MCA
Project: Network Scanning using Nmap (Full Scan & Fast Scan)# Nmap-network-scan-1
