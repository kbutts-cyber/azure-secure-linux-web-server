# Secure Linux Web Server on Azure (No Public IP)

## Overview
This project demonstrates deploying and securing a Linux web server on Microsoft Azure using enterprise-style networking and access controls.  
The virtual machine has **no public IP** and is accessed securely using **Azure Bastion**.

---

## Architecture
- Azure Virtual Network with dedicated subnets
- Network Security Groups (NSGs)
- Ubuntu Linux VM (D-series)
- Azure Bastion
- NGINX web server
- No public IP assigned to the VM

---

## Technologies Used
- Microsoft Azure (VMs, VNets, NSGs, Bastion)
- Linux (Ubuntu 22.04 LTS)
- NGINX
- SSH
- Bash

---

## Security Design
- VM has **no public IP**
- HTTP (port 80) allowed from Internet
- SSH (port 22) restricted to Virtual Network only
- Administrative access via Azure Bastion
- Default NSG deny rules preserved

---

## Validation
The following validations were performed:
- NGINX service running and enabled
- HTTP 200 response confirmed via curl
- Bastion-based SSH access verified
- No public exposure of VM management ports

---

## Author
**Kobe Butts**  
Cloud & Infrastructure Technician  
GitHub: https://github.com/kbutts-cyber  
LinkedIn: https://linkedin.com/in/kobe-butts-7a54b1385

---

## Screenshots

### Azure Networking
![VNet](screenshots/vnet.png)
![Subnets](screenshots/subnets.png)

### Network Security Groups
![NSG Rules](screenshots/nsg_final.png)

### Azure Bastion
![Bastion Overview](screenshots/bastionoverview.png)
![Bastion SSH](screenshots/bastion-ssh.png)

### Web Server Validation
![NGINX Status](screenshots/nginxstatus.png)
![HTTP 200](screenshots/curl-200.png)
