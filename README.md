# 🔐 Cybersecurity Home Lab (SOC Practice Environment)

## 📌 Overview
This project showcases the design and implementation of a personal cybersecurity home lab built using virtualization technologies. The lab simulates a small network environment where offensive and defensive security techniques can be practiced safely.

The goal of this lab is to develop hands-on skills relevant to a SOC Analyst role, including network scanning, system monitoring, and basic attack simulation.

---

## 🧱 Lab Architecture

The lab consists of three virtual machines connected within a private network:

| Machine        | Role            | IP Address       |
|----------------|-----------------|------------------|
| Kali Linux     | Attacker        | 192.168.56.128    |
| Ubuntu Server  | Target Server   | 192.168.56.129    |
| Windows 7      | Victim Machine  | 192.168.56.20    |

All machines are connected using a Host-Only network to ensure isolated and secure communication.

---

## 🖥️ Technologies Used

- Virtualization: VirtualBox / VMware Workstation Player  
- Attacking Machine: Kali Linux  
- Server: Ubuntu Server  
- Client Machine: Windows 7  
- Tools:
  - Nmap (Network Scanning)
  - SSH (Remote Access)
  - Windows Event Viewer (Log Analysis)

---

## 🌐 Network Configuration

A Host-Only Adapter was used to create a private internal network.

- Subnet: 192.168.56.0/24
- Communication verified using ICMP (ping)

---

## 🛠️ Setup Process

### 1. Virtual Machine Setup
- Installed virtualization software
- Created 3 virtual machines
- Allocated RAM, CPU, and storage resources
- Installed operating systems

### 2. Network Configuration
- Configured all VMs to use Host-Only Adapter
- Assigned static IP addresses manually

### 3. Connectivity Testing
- Verified communication using ping between all machines

---

## ⚔️ Attack Simulation

### 🔍 Nmap Scan

The Kali Linux machine was used to scan the Ubuntu Server:

```bash
nmap -sV 192.168.56.20
