# ELK_Suricata_Deployment
Lab environment for deploying Suricata as Network Intrusion Detection/Prevention System (IDS/IPS) integrated with Elastic Stack (ELK).

## Architecture Diagram
![Architecture](https://github.com/wanghui070404/ELK_Suricata_Deployment/blob/main/src/Screenshot%202026-04-10%20141535.png?raw=true)

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
