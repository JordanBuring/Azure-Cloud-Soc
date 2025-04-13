# Azure-Cloud-Soc

# Microsoft-Sentinel-Home-Lab

## Description 

**Creating a Honeypot with a virtual machine hosted on Azure and utilizing Microsoft Sentinel to map the location and magnitude of the RDP attacks on the VM**

I utilized a custom PowerShell script to extract and forward Windows Event Viewer metadata of failed remote desktop log ins on the virtual machine(VM) to a third party API to derive the geolocation data of where the failed attempts occurred. I then created a Log Analytics Workspace in Azure to ingest the custom logs containing the geographic information (latitude, longitude, state/province, and country) of the Remote Desktop(RDP) attacks on VM. A Table was configured in the Log Analytics Workspace to extract the raw data being received by the custom logs and to interpret said data in order to map geo data in Microsoft Sentinel. A Microsoft Sentinel (Azure SIEM) workbook was built in order to overlay the global RDP brute force attacks on the VM to a world map in order to indicate the physical location of the attacks and their magnitude.

## Languages Used

**PowerShell:** Script used to extract and forward Windows Event Viewer metadata of RDP failed logon logs

## Utilities

**ipgeolocation.io:** IP Address to Geolocation API




## Microsoft Sentinel World Map Displaying RDP Attacks and their Magnitude on the VM

![World Map of RDP Attacks on VM](https://github.com/AaronRMartinez/Microsoft-Sentinel-Home-Lab/blob/main/Microsoft_Sentinel_World_Map_RDP_Attacks.jpg)
