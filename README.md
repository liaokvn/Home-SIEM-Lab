# Home-SIEM-Lab

# Objective

This project showcases the deployment and configuration of a cloud-based Security Information and Event Management (SIEM) solution using the Elastic Stack within a home lab environment. The primary objective was to simulate real-world security operations center (SOC) workflows by integrating endpoint telemetry, ingesting system and network logs, and leveraging Elastic Agent for scalable data collection.

A Kali Linux virtual machine was configured to simulate adversarial behavior using tools like Nmap, generating suspicious network activity and command-line executions. These events were forwarded to the Elastic SIEM for real-time log analysis, threat hunting, and event correlation.

The project emphasizes key blue team skills such as log ingestion pipelines, alert rule development, dashboard visualization, and incident detection and response reinforcing the principles of network monitoring, host-based intrusion detection (HIDS), and proactive threat identification in a modern SIEM ecosystem.


<img width="1536" height="1024" alt="Image" src="https://github.com/user-attachments/assets/1add0aff-e7f5-4f09-8829-4e09e97ae9de" />

Core Components of the SIEM Lab Environment

- ELastic Cloud Deployment (Kibana + Elasticsearch)
- Kali Linux Virutal Machine
- Elastic Agent (Endpoint Security Module)
- Log Piplines with ECS Mapping
- Data Quality Validation via Kibana
- Security Events & Raw Logs Viewer
- SIEM Dashboards & Visualiations
- Event Correlation & Detection Readiness 

<img width="1633" height="779" alt="Image" src="https://github.com/user-attachments/assets/efbd1d0b-b7a9-40b4-88dc-20c5f3559d31" />

This visualization shows a breakdown of logs ingesting by the Elastic Agent on the Kali Linux VM. The majority of the data (90%) comes from proccess events, indicating that command line activity and application execution were actively monitored. Additional logs include network and file telemetry, all validated and mapped correctly to the Elastic Common Schema (ECS), enabling accurate threat detection and rule matching. 

<img width="1619" height="1083" alt="Image" src="https://github.com/user-attachments/assets/afe0118d-0cd9-456e-a252-d233b41ce575" />

The data displays detailed logs captured by the Elastic Agent during attack simulation. The event show for, exec, and end actions executed  by the laxxy user on the Kali VM. These logs provide visibility into command level activity and serve as eveidence of potenital malicious behavior, essentialy for threat hunting and incident investigation. 

<img width="1633" height="779" alt="Image" src="https://github.com/user-attachments/assets/ee1d8add-c3e7-40c1-a12e-6e5b1aafc569" />

This dashboard presents an overview of endpoint activity collected by Elastic SIEM. It summarizes event counts, source/destination IPs, and the number of monitored hosts. This confirms that the SIEM is successfully receiving and correlating telemetry data from Kali Linux VM, enabling real-time visbility into host behaviro and potential threats.
