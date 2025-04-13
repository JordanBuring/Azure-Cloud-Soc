# Building a SOC + Honeynet in Azure (Live Traffic)

![Microsoft Sentinel Data Flow](https://github.com/JordanBuring/Files/blob/main/MicrosoftSentinelFlowChart.jpg)

## Description 

**Creating a Honeypot with a virtual machine's hosted on Azure and utilizing Microsoft Sentinel to map the location and magnitude of the RDP Malicious Attacks on the VM, VM Authentication Failures, and Azure Resource Creation**

For this project, I used 2 Virtual Machines that have specific inbound rules set to fully expose the 2 Virtual Machines to attacks on the Internet. I then used the Log's in the Log Analytics Workspace in Azure to ingest the custom logs containing the geographic information (latitude, longitude, state/province, and country) of the Remote Desktop(RDP) attacks on the VM's. Within Microsoft Sentinel's workbooks I added KQL queries such as:
![KQLQuery](https://github.com/JordanBuring/Files/blob/main/KQLquery1.jpg)

Here is the workbook that was built in order to show the global RDP brute force attacks on the VM in order to indicate the physical location of the attacks and their magnitude.
![MaliciousTraffic]()

A Table was configured in the Log Analytics Workspace to extract the raw data being received by the custom logs and to interpret said data in order to map geo data in Microsoft Sentinel. A Microsoft Sentinel (Azure SIEM) workbook was built in order to overlay the global RDP brute force attacks on the VM to a world map in order to indicate the physical location of the attacks and their magnitude.

## Languages Used

**PowerShell:** Script used to extract and forward Windows Event Viewer metadata of RDP failed logon logs

## Utilities

**ipgeolocation.io:** IP Address to Geolocation API




## Microsoft Sentinel World Map Displaying RDP Attacks and their Magnitude on the VM

![World Map of RDP Attacks on VM](https://github.com/AaronRMartinez/Microsoft-Sentinel-Home-Lab/blob/main/Microsoft_Sentinel_World_Map_RDP_Attacks.jpg)
