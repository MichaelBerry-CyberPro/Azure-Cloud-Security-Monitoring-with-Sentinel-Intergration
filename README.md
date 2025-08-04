# Azure-Cloud-Security-Monitoring-with-Sentinel-Intergration
Soc Analyst Project 

**Overview:** I created a basic home Soc from scratch. I created a Azure subscription, opened up a new VM, used that VM as a honeypot, and forward those logs to a central location. Finally using that info to build a map analyzing real world attacks. This project is great for beginners and professionals looking to practice log analysis, threat dectection, and soc operations within a real world cloud.

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

<h2>**Step 1: Project Setup**</h2>
<b1>Open up a new in VM, you are able to set up a free trial or pay-as-you-go instance. If you choose pay-as-you-go keep it cheap we can use a bare bones VM and still complete our goal. In this case I went with Windows 10 Pro, Smallest Storage and Disk. You notice the monthly cost of leaving the VM on 24/7. Be mindful of shutting this off when you are done. You can configure you VM to shut off at midnight as a saftey precaution. Remember the username and password.</b1>

<h2>**Step 2:Creating a Honey Pot (Azure Virtual Machine)**</h2>
<b2>1)Once the VM is created, click on the VM through the Resource Group. You will need to verify that your public IP address was created alongside with the Network Security Group. In the Event is was not you can create one and this will be how the attackers find our VM across the internet. Next steps are to open up the VM to world. This is DANGEROUS and should only be done to test applications or projects. Delete the first default rule, and set your inbound security rules to allow all traffic from any source. </b2> 
<l1></l1>

2)Log into your VM using Remote Desktop (you will need the public IP) and you will remove all protection from the Windows defender firewall. 

