<h1>Microsoft Azure Sentinal SEIM Honeypot Lab</h1>



<h2>Description</h2>
<b>This lab was conducted to set up a Honeypot, attracting attackers for data collection. We utilized Microsoft Azure Sentinal (SEIM) to create a Virtual Machine as the bait. The Powershell script in this repository extracts Windows Event Log data for failed RDP attacks and uses a third-party API to gather attacker location details. This information is then visualized on a map to show potential attacker locations.
</b>
<br />
<br />
<h2>Languages Used</h2>

- <b>PowerShell:</b> Extract RDP failed logon logs from Windows Event Viewer 
- <b>Kusto Query Language (KQL):</b> Extract Logs from VM to Azure and assign values to map 
<h2>Utilities Used</h2>

- <b>Microsoft Azure Sentinal (SEIM):</b> Host for most of the resources
- <b>ipgeolocation.io:</b> IP Address to Geolocation API

<h2>The Virtual Machine in Azure  </h2>
I made sure to Disable the firewall or made and inbound rule to allow any traffic. This attracts the Attackers as a vulnerable system.
<br />
<br />
<i>When I set up the Virtual Machine, I accidentally gave it only 1 GB of RAM and a single CPU. As I worked on the lab,
I couldn't figure out why the virtual machine was running so slowly. It didn't take long for me to realize the problem and fix it by adjusting the settings. 
This whole process taught me that trial and error can be the best way to learn!
</i>

![InkedVirtual Machine](https://github.com/Sansantv/Microsoft-Sentinel-Lab/assets/143445179/36343956-d507-413f-81ec-66d765a11078)


<h2>Attacks from India coming in; Custom logs being output with geodata</h2>

![Attackattempts](https://github.com/Sansantv/Microsoft-Sentinel-Lab/assets/143445179/18c630bd-de00-4503-ae5e-483a0e184a77)

<h2>Failed Login Attempts shown on Vm's Event Viewer</h2>

![Event Viewer Failed Loggins](https://github.com/Sansantv/Microsoft-Sentinel-Lab/assets/143445179/e1c43035-fadf-4ad4-bce7-df0356fd528a)

<h2>Log Data from VM Being imported into Azure</h2>

![image](https://github.com/Sansantv/Microsoft-Sentinel-Lab/assets/143445179/87e48518-4cd9-4fa1-a59f-5576a60f0ffe)

<h2>The KQL For the Map using the data from the Custome Log</h2>

![query for map code](https://github.com/Sansantv/Microsoft-Sentinel-Lab/assets/143445179/891bb676-2e52-476f-ae74-cf0c20e39233)


<h2>World map of incoming attacks over time</h2>

![Map Progression](https://github.com/Sansantv/Microsoft-Sentinel-Lab/assets/143445179/cfe52627-8389-44d6-b19e-6d6834963105)
![8-28](https://github.com/Sansantv/Microsoft-Sentinel-Lab/assets/143445179/33fbb589-7c09-49ba-8626-fcd55ca05cad)
![8-28-2](https://github.com/Sansantv/Microsoft-Sentinel-Lab/assets/143445179/3b9f5380-6640-4dd2-8203-e71bae9fa95f)
![8-28-3](https://github.com/Sansantv/Microsoft-Sentinel-Lab/assets/143445179/f31c2dd9-3bb7-49df-9dd7-2aedf156e1be)



<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
