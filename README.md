## Honeynet in Azure (Live Traffic)

![FullDisplay](https://github.com/JordanBuring/Files/blob/main/AzureFullDisplay.png)

![Microsoft Sentinel Data Flow](https://github.com/JordanBuring/Files/blob/main/MicrosoftSentinelFlowChart.jpg)

## Description 

**Creating a Honeynet with virtual machine's hosted on Azure and utilizing Microsoft Sentinel to map the location and magnitude of the Malicious Attacks on the VM, and VM Authentication Failures to the entire Log(N) Pacific's Cyber Range Virtual Machines.**

For this project, I used 2 Virtual Machines that have an allow all RDP inbound/outbound traffic rule to fully expose the 2 Virtual Machines to attacks on the Internet. I then used the Log's in the Log Analytics Workspace in Azure to ingest the logs containing the geographic information (latitude, longitude, state/province, and country) of the attacks on the VM's. Within Microsoft Sentinel's workbooks I added KQL queries such as this and json code to create maps:
![KQLQuery](https://github.com/JordanBuring/Files/blob/main/KQLquery1.jpg)



## Microsoft Sentinel World Map Displaying Attacks and their Magnitude on the VM
![MaliciousTraffic](https://github.com/JordanBuring/Files/blob/main/MaliciousTraffic.jpg)

Here is the workbook that was built in order to show the global brute force attacks on the VM's in order to indicate the physical location of the attacks and their magnitude.


## Microsoft Sentinel World Map Displaying VM Authentication Failures
![VMAuthFailures](https://github.com/JordanBuring/Files/blob/main/VMAuthFailures.jpg)


This map shows the location of many incoming brute force attacks failing to connect to the entire Cyber Range's Virtual Machines. You can see the location and IP address's of many bad actors.

Hardening of the network was performed to prevent full exposure to the Virtual Machines. The RDP allow all inbound/outbound traffic rule was removed. This closed off the network which rehardened the network.
