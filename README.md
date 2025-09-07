# Networking-Lab
This repo covers the **Basics of Networking** with theory, practical task, and a mini project.  

**Goal**- Build a strong foundatation in Networking.
<br>
<br>
## Topics 
- LAN & IP Basics
- Subnetting 
- System IP Check (Window & Linux)
- Ping & connectivity testing
- Packet Tracer lab
- Subnetting Table Project

# Netwtoking Foundations -Notes  

---

## 1 LAN ( Local Area Netwrok)
- Covers a *Small geographical area* like home & office
- High Speed, low latency
- Devices- Switch, Router, PCs

  ---
## 2 IP Addressing
- Unique logical address of a device in a network
- **IPv4**: 32-bit, 4-octet, (each octet have 8 bits), eg. '10.0.0.1'
- **IPv6**: 128-bit, 16-octet, ( " ), eg. '2001:0db8:85a3:0000:8a2e:0370:7334'

---
## 3 Subnetting
- Process of dividing a network into smaller networks
- Example '192.168.1.0/24' can be divided into
- '/25' -2 subnets (128 hosts each)
- '/26' -4 subnets (64 hosts each)
- '/28' -16 subnets (16 hosts each)

---

📌 **Tip:** Always calculate subnet mask - No. of subnets - Hosts per subnet  

---

# Netwroking Practical Commands


This document contains commonly used **Window & Linux networking commands** along with a basic lab exercise in Cisco Packet Tracer.

---

## Windows CMD
- `ipconfig /all`  -> View system IP, Mac address, Gateway, and DNS
- `ping -t <IP>`   -> Continuous ping test (until STOPPED)
- `tracert <IP>`   -> Trace route to a destination host

---

## Linux CMD
- `ip a`       -> Show IP addresses & interface
- `ping <IP>`   -> Ping a host
- `traceroute <IP>` -> Trace the path of an packet take to destination
- `netstat -tulnp`  -> Show active ports and listening services

---

## 🧪 Lab Exercise -Basic LAN Setup (Cisco Packet Tracer)

1. Open **Cisco Packet Tracer**
2. Add **2-PCs + Switch**
3. Assign Ips:
   - PC1:- '192.168.1.10/24
   - PC2:- '192.168.1.11/24
   - Gateway:- '192.168.10.1' (Optional)
4. Test connectivity using:
   - '''bash
   - ping 192.168.1.11

---

## Netwotking Lab 1 - Tasks

A test of practical hands-on tasks to understand networking fundamentals.

---

**Task 1:**
Run the following commands to check system IP details:
 - Window = 'ipconfig -all'
 - Linux = 'ifconfig' or 'ip a'(Modern)

---

**Task 2:**
ping Google DNS(8.8.8.8) continuously to test connectivity:
'''bash  
- ping -t 8.8.8.8    (Window)
- ping 8.8.8.8       (Linux)
