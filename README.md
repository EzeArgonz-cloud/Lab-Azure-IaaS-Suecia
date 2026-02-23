# Lab-Azure-IaaS-Suecia
# Azure IaaS Web Infrastructure - Sweden Central Region

## 🎯 Overview
This project demonstrates the deployment of a robust and cost-effective Cloud infrastructure on Microsoft Azure. It features a Linux-based web server (Nginx) following security and governance best practices.

## 🏗️ Architecture & Resources
The following resources were provisioned in the **Sweden Central** region:

* **Compute:** Virtual Machine (Ubuntu 24.04 LTS) using a **Burstable B2ats_v2** instance for cost-efficiency.
* **Networking:** Virtual Network (VNet) and Subnet architecture.
* **Security:** Network Security Group (NSG) acting as a firewall, configured with the **Principle of Least Privilege**:
    * **Port 22 (SSH):** Restricted to my specific Public IP.
    * **Port 80 (HTTP):** Open for public web traffic.
* **Identity:** RSA Public/Private Key pair (.pem) for secure, passwordless authentication.

## 💰 Cost Optimization & Governance
To ensure financial accountability and prevent unexpected charges, the following controls were implemented:

* **Auto-shutdown:** Configured to deallocate the VM daily at 6:00 PM (ART) to minimize compute costs.
* **Azure Cost Management:** Established a monthly budget with **Forecasted Alerts** (100% threshold) to proactively monitor spending trends.
* **Metric Monitoring:** Deployed **Azure Monitor** alert rules to track CPU performance and system health.

## 🚀 Technical Implementation
1.  **Provisioning:** Resources deployed via Azure Portal ensuring regional redundancy.
2.  **Configuration:** Remote management performed via SSH for system hardening.
3.  **Web Deployment:** Installation and customization of **Nginx** to serve a personalized landing page.
4.  **Verification:** Validated public accessibility via the VM's Public IP address.

---
*This lab was developed as part of my technical preparation for the **Microsoft Azure Fundamentals (AZ-900)** certification.*
