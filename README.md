# ELK_Suricata_Deployment
Lab environment for deploying Suricata as Network Intrusion Detection/Prevention System (IDS/IPS) integrated with Elastic Stack (ELK).

## Architecture Diagram
![Architecture](https://github.com/wanghui070404/ELK_Suricata_Deployment/blob/main/src/Screenshot%202026-04-10%20141535.png?raw=true)

**Main Components:**

- **Kali Linux** (192.168.85.129) – Attacker Machine
![Attacker]()
- **Ubuntu IDS** (192.168.85.136) – Suricata (IDS/IPS)
- **Ubuntu ELK** (192.168.85.137) – Elasticsearch + Logstash + Kibana (SIEM)
- **Windows Server 2022** (192.168.85.139) – Victim 1
- **Ubuntu Server** – Victim 2
