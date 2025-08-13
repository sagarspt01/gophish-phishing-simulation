# 🎯 GoPhish Phishing Simulation & Splunk Analysis Lab

This repository documents a complete **phishing attack simulation** using [GoPhish](https://getgophish.com/) on a Kali Linux VM against a Windows VM, with **log analysis in Splunk**.  
It is designed for **educational cybersecurity training** in a controlled lab environment.

---

## 📌 Project Overview

This project demonstrates:
- Setting up **GoPhish** for phishing simulation
- Launching a phishing campaign from Kali to Windows
- Capturing and analyzing logs with **Splunk**
- Observing attacker-victim network interaction

---

## 🖥 1. Lab Setup & Topology

![Network Topology](assets/network_topology.png)

| Component        | Role        | IP Address       |
|------------------|------------|------------------|
| Kali Linux VM    | Attacker   | `192.168.100.4`  |
| Windows VM       | Victim     | `192.168.100.1`  |
| Network Type     | NAT Network| `192.168.100.0/24`|

Both VMs must be **pingable** to confirm connectivity.

---

## ⚙ 2. Installing GoPhish on Kali

```bash
# 1. Clone the GoPhish repo
git clone https://github.com/gophish/gophish.git
cd gophish

# 2. Edit config.json for logging
nano config.json
