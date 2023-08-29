<h1>Microsoft Azure Sentinal SEIM Honeypot Lab</h1>


 ### [YouTube Demonstration (@16:20)](https://youtu.be/RoZeVbbZ0o0?t=980)


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
<h2>Attacks from China coming in; Custom logs being output with geodata</h2>

<p align="center">
![Attackattempts](https://github.com/Sansantv/Microsoft-Sentinel-Lab/assets/143445179/18c630bd-de00-4503-ae5e-483a0e184a77)

</p>

<h2>World map of incoming attacks after 24 hours (built custom logs including geodata)</h2>

<p align="center">
<img src="https://i.imgur.com/krRFrK5.png" height="85%" width="85%" alt="Image Analysis Dataflow"/>
</p>


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
