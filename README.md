<h1>🛡️ Security Operations Center (SOC) Home Lab</h1>

<h2><br />Description</h2>
This SOC Simulation Home Lab was my attempt on getting hands-on experience with SOC and SIEM workflows in the cloud. I deployed a Windows VM in Microsoft Azure, configured log forwarding into Log Analytics, and enabled Microsoft Sentinel for monitoring and alerting. To generate real-world data, I exposed the VM to the internet for several hours and allowed brute-force login attempts to occur. I configured Sentinel to not only detect and alert on these attempts, but also plot the attacker IP addresses on a world map, giving me visibility into where the activity was originating globally. I then used KQL queries to investigate the events further, which helped me practice log analysis, detection engineering, and incident response techniques.
<br />


<h2>Languages and Utilities Used</h2>

- KQL (Kusto Query Language)
- Microsoft Sentinel (SIEM platform)
- Azure Log Analytics Workspace
- Windows Event Viewer
- Remote Desktop Protocol

<h2>Environments Used </h2>

- Microsoft Azure
- Windows 10 (Virtual Machine)
- Windows 11 (Local Machine)

<h2>Simulation walk-through:</h2>

**Created Azure Resources** - Set up a Resource Group and Virtual Network in Microsoft Azure.
<br />
<br />
<img src="https://i.imgur.com/jo9LTdf.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br />
<br />
**Deployed Windows VM** - Launched a Windows 10 virtual machine, configured credentials, and enabled RDP access via a Network Security Group (port 3389).
<br />
<br />
<img src="https://i.imgur.com/zeV8Tme.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br />
<br />
**Connected Logs to Azure Monitor** - Installed/activated the Azure Monitor agent and linked the VM to a Log Analytics Workspace.
<br/>
<br/>
<img src="https://i.imgur.com/wokRp3w.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br />
<br/>
**Enabled Microsoft Sentinel** – Activated Sentinel on the workspace to provide SIEM functionality.
<br/>
<br/>
<img src="https://i.imgur.com/RHffboX.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br />
<br/>
**Configured Data Collection** - Forwarded Windows Security Event Logs (failed/successful logins, account activity) into Log Analytics.
<br/>
<br/>
<img src="https://i.imgur.com/PpziEU7.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br/>
<br />
**Exposed the VM** - Left RDP open to the internet for several hours to attract real brute-force login attempts.
<br/>
<br/>
<img src="https://i.imgur.com/6wSWfh5.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<img src="https://i.imgur.com/J4OgDpB.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br/>
<br />
**Generated and Collected Attack Data** - Allowed unsolicited login attempts to accumulate, producing authentic attack traffic.
<br/>
<br/>
<img src="https://i.imgur.com/DU4K6DD.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<img src="https://i.imgur.com/9D4Xiqe.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<img src="https://i.imgur.com/Oajigt0.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<img src="https://i.imgur.com/eFMNBq1.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br/>
<br />
**Detection in Sentinel** – Verified that Sentinel fired security alerts based on the failed logins and suspicious authentication patterns.
<br/>
<br/>
<img src="https://i.imgur.com/c4GeLdF.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br/>
<br />
**Geographic Mapping** – Used Sentinel’s built-in map feature to visualize attacker IP addresses by country/region.
<br/>
<br/>
<img src="https://i.imgur.com/Fl6hbAs.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br />
<br/>
**Investigated with KQL** – Queried the log data using Kusto Query Language to dig deeper into failed logins, attacker IPs, and timelines.
<br/>
<br/>
<img src="https://i.imgur.com/A7gGSwi.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br/>
<br />
**Validated End-to-End Workflow** – Confirmed that log collection, alerting, visualization, and investigation worked together like a real SIEM environment.
<br/>
<br/>
<img src="https://i.imgur.com/EoR0b5h.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<img src="https://i.imgur.com/ZIjjwQy.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br />
<br/>
<br />
<br />
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

