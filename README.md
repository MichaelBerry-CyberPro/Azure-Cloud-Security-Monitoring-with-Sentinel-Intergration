# Azure-Cloud-Security-Monitoring-with-Sentinel-Intergration
Soc Analyst Project 

**Overview: I created a basic home Soc from scratch. I created a Azure subscription, opened up a new VM, used that VM as a honeypot, and forward those logs to a central location. Finally using that info to build a map analyzing real world attacks. This project is great for beginners and professionals looking to practice log analysis, threat dectection, and soc operations within a real world cloud.

**Tools used:**
1) Azure VM
2) Azure Setinel
3) Azure Analytics
4) Network Security Groups
5) Nmap

**Skills learned:**
KQL Language
Azure infrastructure
Network Configuration
Siem Intergration
Log Ingestion
Threat Simulation and Testing
Threat Hunting and Dectection
Workbook and Dashboard creation

<h2>**Step 1: Project Setup**</h2>h2>
<b1>Open up a new in VM, you are able to set up a free trial or pay-as-you-go instance. If you choose pay-as-you-go keep it cheap we can use a bare bones VM and still complete our goal. In this case I went with Windows 10 Pro, Smallest Storage and Disk. *Create an user name and complex password,</b1>

<h3>**Step 2**
Creating a Honey Pot (Azure Virtual Machine)</h3>
<b2>Once the VM is created, click on the VM through the Resource Group. You will need to verify that your public IP address was created alongside with the Network Security Group. In the Event is was not you can create one and this will be how the attackers find our VM across the internet.</b2>
