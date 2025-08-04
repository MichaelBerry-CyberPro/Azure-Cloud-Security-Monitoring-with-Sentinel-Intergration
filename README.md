# Azure-Cloud-Security-Monitoring-with-Sentinel-Intergration
Soc Analyst Project 

**Objectives**
- Deploy a public-facing VM in Azure
- Expose the VM to simulate real-world attack conditions
- Capture logs in Microsoft Sentinel
- Visualize attacker behavior using workbooks
- Simulate scans using nmap

**Tools used:**
1) Azure VM                                  
2) Azure Setinel                            
3) Azure Analytics
4) Network Security Groups                  
5) Nmap

**Skills learned:**
1) Kql Language
2) Azure Infrastructure
3) Network Configurations
4) Siem Intergrations
5) Log Ingestion
6) Threat Simulation and Testing
7) Threat Hunting
8) Workbook and Dashboard creation


<h2>Step 1: Project Setup</h2>
<b1>Open up a new in VM, you are able to set up a free trial or pay-as-you-go instance. If you choose pay-as-you-go keep it cheap we can use a bare bones VM and still complete our goal. In this case I went with Windows 10 Pro, smallest storage and disk that worked for Windows 10. You notice the monthly cost of leaving the VM on 24/7. Be mindful of shutting this off when you are done. You can configure you VM to shut off at midnight as a saftey precaution. While in creating the VM, and IP address to be created and  remember the username and password.</b1>

<h2>Step 2:Creating a Honey Pot (Azure Virtual Machine)</h2>
<b2>-Once the VM is created, click on the VM through the Resource Group. You will need to verify that your public IP address was created alongside with the Network Security Group. In the event is was not you can create one and this will be how the attackers find our VM across the internet. Next steps are to open up the VM to world. This is **DANGEROUS** and should only be done to test applications or projects. Delete the first default rule, and set your inbound security rules to allow all traffic from any source. </b2> 

<b3>-Log into your VM using Remote Desktop (you will need the public IP) and you will remove all protection from the Windows Defender firewall. Again this is dangerous and should be handled with care. Open powershell and ping the Ip address to show that it can recieve data.After that log out of the Vm. ** Remember even though you are the logged out the VM it is still running. Let it continue you to run, we need the data that will come from this**.</b3>
 
<h2> Step 3: Forwarding Data and KQL</h2>
<b3>You need to create an Log Analytics Workspace and a Sentinel Instance and connect the two together. While creating these two be these are apart the the same resource group. If you cannot located these two, use the search bar at the top of Azure portal. For the sentinel instance install "Windows Security Events via AMA" Connector. You need to also create Data Collection Rules within sentinel, which fill funnel our event logs.</b3>
