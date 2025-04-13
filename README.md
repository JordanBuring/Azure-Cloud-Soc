## Honeynet in Azure (Live Traffic)

![Microsoft Sentinel Data Flow](https://github.com/JordanBuring/Files/blob/main/MicrosoftSentinelFlowChart.jpg)

## Description 

**Creating a Honeypot with a virtual machine's hosted on Azure and utilizing Microsoft Sentinel to map the location and magnitude of the RDP Malicious Attacks on the VM, VM Authentication Failures, and Azure Resource Creation**

For this project, I used 2 Virtual Machines that have specific inbound rules set to fully expose the 2 Virtual Machines to attacks on the Internet. I then used the Log's in the Log Analytics Workspace in Azure to ingest the custom logs containing the geographic information (latitude, longitude, state/province, and country) of the Remote Desktop(RDP) attacks on the VM's. Within Microsoft Sentinel's workbooks I added KQL queries such as this and json code to create maps:
![KQLQuery](https://github.com/JordanBuring/Files/blob/main/KQLquery1.jpg)



## Microsoft Sentinel World Map Displaying RDP Attacks and their Magnitude on the VM
![MaliciousTraffic](https://github.com/JordanBuring/Files/blob/main/MaliciousTraffic.jpg)

Here is the workbook that was built in order to show the global RDP brute force attacks on the VM in order to indicate the physical location of the attacks and their magnitude.

My next map shows the location of many incoming brute force attacks failing to connect to the virtual machines. You can see the location and IP addres of some bad actors.
![VMAuthFailures]()


