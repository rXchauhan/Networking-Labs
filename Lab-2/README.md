# Networking-Lab
This repo covers the **Basics of Networking** with theory, practical task, and a mini project.  

**Goal**- Build a strong foundation in Networking.
<br>
<br>
## Topics 
- LAN & IP Basics
- Subnetting 
- System IP Check (Window & Linux)
- Ping & connectivity testing
- Packet Tracer lab
- Subnetting Table Project

# Networking Foundations -Notes  

---

## 1 LAN ( Local Area Network)
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

# Networking Practical Commands


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
- Topology Image
- <img width="712" height="592" alt="Screenshot 2025-09-07 213139" src="https://github.com/user-attachments/assets/da3d8aea-95aa-4e98-8163-9784f17ca264" />
- <img width="1054" height="865" alt="Screenshot 2025-09-07 212747" src="https://github.com/user-attachments/assets/64f2b2c9-a2d0-4af8-b773-e785b335e70a" />

---

## Networking Lab 1 - Tasks

A test of practical hands-on tasks to understand networking fundamentals.

---

**Task 1:**
Run the following commands to check system IP details:
 - Window = 'ipconfig -all'
 - <img width="1237" height="992" alt="Screenshot 2025-09-07 211112" src="https://github.com/user-attachments/assets/d9f79c31-6940-4eeb-b03f-c5e67443abd5" />

 - Linux = 'ifconfig' or 'ip a'(Modern)
 - <img width="1920" height="1080" alt="Screenshot_2025-09-07_07_26_17" src="https://github.com/user-attachments/assets/4c711212-d361-4181-8fe9-e03bf337017a" />

 ---

**Task 2:**
Ping Google DNS(8.8.8.8) continuously to test connectivity: 
- ping -t 8.8.8.8    (Window)
- <img width="1350" height="1001" alt="Screenshot 2025-09-07 211432" src="https://github.com/user-attachments/assets/869b09fe-b2fa-47db-97c9-474f426d139b" />

- ping 8.8.8.8       (Linux)
- <img width="1920" height="1080" alt="Screenshot_2025-09-07_07_26_17" src="https://github.com/user-attachments/assets/c650e7dc-2a59-4e61-a192-0cde3977a730" />

---

**Task 3:**
Check route for Cloud flare DNS:
- tracert 1.1.1.1 (Window)
- <img width="1004" height="902" alt="Screenshot 2025-09-07 211708" src="https://github.com/user-attachments/assets/c50e14c0-506b-4a1b-af91-a42c16de8694" />

- traceroute 8.8.8.8 (Linux)
- <img width="1920" height="1080" alt="Screenshot_2025-09-07_07_26_21" src="https://github.com/user-attachments/assets/b861f4ca-c037-4aea-845c-5d94630ad8a2" />

---

**Task 4:**

Subnetting Exercise:

### /25 (2 Subnets)
| Subnet | Network ID    | Broadcast    | Host Range                    | Total Hosts |
|--------|---------------|--------------|-------------------------------|-------------|
| 1      | 192.168.1.0   | 192.168.1.127| 192.168.1.1 – 192.168.1.126   | 126 |
| 2      | 192.168.1.128 | 192.168.1.255| 192.168.1.129 – 192.168.1.254 | 126 |

### /26 (4 Subnets)
| Subnet | Network ID    | Broadcast    | Host Range                   | Total Hosts |
|--------|---------------|--------------|------------------------------|-------------|
| 1      | 192.168.1.0   | 192.168.1.63 | 192.168.1.1 – 192.168.1.62   | 62 |
| 2      | 192.168.1.64  | 192.168.1.127| 192.168.1.65 – 192.168.1.126 | 62 |
| 3      | 192.168.1.128 | 192.168.1.191| 192.168.1.129 – 192.168.1.190| 62 |
| 4      | 192.168.1.192 | 192.168.1.255| 192.168.1.193 – 192.168.1.254| 62 |

### /28 (16 Subnets)
| Subnet | Network ID    | Broadcast    | Host Range                   | Total Hosts |
|--------|---------------|--------------|------------------------------|-------------|
| 1      | 192.168.1.0   | 192.168.1.15 | 192.168.1.1 – 192.168.1.14   | 14 |
| 2      | 192.168.1.16  | 192.168.1.31 | 192.168.1.17 – 192.168.1.30  | 14 |
| 3      | 192.168.1.32  | 192.168.1.47 | 192.168.1.33 – 192.168.1.46  | 14 |
| ...    | ...           | ...          | ...                          | ... |
| 16     | 192.168.1.240 | 192.168.1.255| 192.168.1.241 – 192.168.1.254| 14 |
