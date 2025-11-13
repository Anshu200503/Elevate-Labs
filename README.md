# Elevate-Labs

# Overview

This project is part of my Cyber Security Internship. The objective of Task 1 is to perform a TCP SYN scan on my local network using Nmap, identify open ports, analyze active services, and understand the associated security risks.

# Objective

To discover active devices in the local network and identify their open ports using Nmap.

# Tools Used

Nmap – Port scanning & reconnaissance

Step 1: Identify IP Range

# Use the command:

ipconfig


Network identified:

192.168.x.0/24

# Step 2: Perform TCP SYN Scan

Command used:

nmap -sS 192.168.x.0/24 -oN scan-results.txt


This command scans all devices in the subnet and logs results into a text file.

#Scan Results
Nmap scan report for 192.168.1.1  
PORT    STATE SERVICE  
53/tcp  open  domain
80/tcp  open  http
443/tcp open  https

Nmap scan report for 192.168.1.7  
PORT    STATE SERVICE  
554/tcp  open  rtsp
8000/tcp open  http-alt

Nmap scan report for 192.168.1.10  
PORT    STATE SERVICE  
22/tcp  open  ssh

# Risk Analysis

SSH (22): Brute-force attack risk
HTTP (80): Unencrypted traffic
SMB (445): Vulnerable to major exploits
RTSP (554): Camera/stream access vulnerability

# Outcome

Completed full network scanning
Analyzed open ports
Understood service exposure
