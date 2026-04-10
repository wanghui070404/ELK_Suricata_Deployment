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
- [Lab Setup](#lab-setup)
- [Skills Demonstrated](#skills-demonstrated)
- [Future Improvements](#future-improvements)

---

### 📖 Overview

This project demonstrates a Security Operations Center (SOC) monitoring lab built using the Elastic Stack and Suricata. This project demonstrates a Security Operations Center (SOC) monitoring lab built using the Elastic Stack and Suricata. 
The goal of this project is to demonstrate how a SOC analyst can:
**Monitor system and network activities**
**Detect suspicious behaviors**
**Detect suspicious behaviors**
**Investigate security alerts**

### 🏗 Architecture

The following architecture illustrates how logs flow from monitored systems to the SIEM platform.

## Architecture Diagram
![Architecture](https://github.com/wanghui070404/ELK_Suricata_Deployment/blob/main/src/Screenshot%202026-04-10%20141535.png?raw=true)

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


