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

# Data Quality & ECS Mapping
<img width="1619" height="1083" alt="Image" src="https://github.com/user-attachments/assets/afe0118d-0cd9-456e-a252-d233b41ce575" />

This visualization shows a breakdown of logs ingested by the Elastic Agent on the Kali Linux VM. The majority of the data (over 90%) comes from process events, indicating that command-line activity and application execution were actively monitored. Additional telemetry includes network and file activity, all of which were validated and mapped correctly to the Elastic Common Schema (ECS). This ensures accurate threat detection, rule matching, and compatibility with Elastic SIEM’s detection logic.

# Raw Endpoint Process Events from Kali
<img width="1622" height="750" alt="Image" src="https://github.com/user-attachments/assets/14a4d9fc-6ef4-48ce-9045-f9c686755665" />

This table displays detailed logs captured by the Elastic Agent during a simulated attack on the Kali Linux VM. It shows process-level activity such as fork, exec, and end actions executed by the laxxy user. These logs provide critical visibility into command-level operations, making it possible to attribute behavior to specific users and sessions — essential for both threat hunting and forensic investigations.

# Host Overview Dashboard
<img width="1633" height="779" alt="Image" src="https://github.com/user-attachments/assets/ee1d8add-c3e7-40c1-a12e-6e5b1aafc569" />

This dashboard presents a visual summary of endpoint activity collected by Elastic SIEM. It includes host counts, source and destination IPs, and a timeline of recorded events. The graph shows real-time ingestion of telemetry data from the monitored Kali VM, confirming that log correlation is functioning correctly. This enables analysts to monitor live endpoint behavior and detect abnormal trends or suspicious activity across the network.

# Summary

This project demonstrated how Elastic SIEM can be used to simulate a real-world SOC environment for monitoring endpoint activity. By installing Elastic Agent on a Kali Linux VM, I was able to collect and visualize security telemetry, including process execution, network flows, and user activity. These events were then analyzed using Kibana dashboards to detect potential threats and investigate suspicious behavior. The experience reinforced the importance of endpoint monitoring, log normalization using ECS, and building visual workflows for threat detection. Overall, this project helped solidify core SOC concepts like threat visibility, data ingestion, and incident investigation using open-source tools.
