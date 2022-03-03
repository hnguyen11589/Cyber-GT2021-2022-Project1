# Cyber-GT2021-2022-Project1

### Summary:
In this project, the files in this repository will be used to deploy the network below.

![Complete_Diagram](Diagrams/Complete_Diagram_P1.png)

These files has been tested and deployed with the VM on Azure. They can be used to recreate the network above with the step by step below. 
These playbook-files (filebeat-playbook.yml, Install-elk.yml, metricbeat-playbook.yml, pentest-playbook.yml) can be used to deploy Container DVWA Application Web 1, 2, 3, Elk Server which including Metricbeat and Filebeat 

This document will contain the following 
+ The Topology 
+ Inbound/Outbound Rules 
+ Tutorial to provision Virtual-Machines, Virtual-Network, Network-Security-Group, Load-Balancer on Azure. 
+ How to use Ansible/Playbook to configure Elk Server, Web 1 2 3, Filebeat, and Metricbeat





+ Elk Server (will be receive logs monitor from Web 1, 2, 3)  
+ Metricbeat (will fetch metrics of Web 1, 2, 3 send to Elk server) 
+ Filebeat (will collect syslog form Web 1, 2, 3 send to ELK Server)

#### Step.1 Deploy Resource-Group, Vnet, and Network-Security-Groups on Azure. 
1. Create Resource Group: 
+ Name: Red_Team (This will be use for entire project) 
+ Timezone: East US
+ Default: The rest of the setting. 
![RG](Images/Resource_Groups.png)
2. Create Virtual Network: 
+ Resource Group: Red_Team
+ Name Red_Team_Net
+ Regions: East US
+ IP Addresses: 10.0.0.0/16
+ Default: The rest of the setting. 
![Vnet1](Images/Virtual_network.png)
3. Create Network Security groups
+ Resource Group: Red_Team
+ Name: Red_Team_NSG
+ Regions: East US
+ Default: The rest of the setting.
![Vnet1](Images/NSG.png)

+ Rules: 
| Name     | Function | IP Address | Operating System |
|----------|----------|------------|------------------|
| Jump Box | Gateway  | 10.0.0.1   | Linux            |
| TODO     |          |            |                  |
| TODO     |          |            |                  |
| TODO     |          |            |                  |

