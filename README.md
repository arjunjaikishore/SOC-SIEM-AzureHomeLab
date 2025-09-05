<h1>🛡️ Security Operations Center (SOC) Home Lab</h1>


<h2>Description</h2>
For this project, I exploited the Kioptrix Level 1 vulnerable VM using Kali Linux. I started with pre-engagement steps like confirming my IP with ifconfig and scanning the network with Nmap to find live hosts and fingerprint the operating system. From there, I ran a full port scan and focused on services running on ports like 22, 80, 111, 139, 443, and 32768. After identifying versions of these services, I used Nessus to help confirm possible vulnerabilities and zeroed in on Samba. I researched known Samba exploits with Searchsploit, set up the right Metasploit module and payload, and was able to successfully gain root access. This project walked me through the full penetration testing workflow—recon, scanning, enumeration, exploitation, and post-exploitation—while giving me hands-on practice with tools like Nmap, Nessus, and Metasploit.
<br />


<h2>Languages and Utilities Used</h2>

- <b>Bash</b> 
- <b>Kali Linux</b>
- <b>VMware</b>

<h2>Environments Used </h2>

- <b>Linux</b>
- <b>Windows 11</b>

<h2>Exploitation walk-through:</h2>

<p align="center">
Confirm local IP Configuration using “ifconfig” <br/>
<img src="https://i.imgur.com/jo9LTdf.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br />
Discover live hosts on the network using “nmap -sn”  <br/>
<img src="https://i.imgur.com/zeV8Tme.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br />
Finding out what operating system Kioptrix is using “nmap -o” (it's using 2.4.9 - 2.4.18) <br/>
<img src="https://i.imgur.com/wokRp3w.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br />
Performed a full port scan using “nmap -p- -sV”  <br/>
<img src="https://i.imgur.com/RHffboX.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br />
Focus scan on known open ports (not the full 6553 ports) using “nmap -p 22,80,111,139,443,32768  -sV -sC  192.168.244.131”  <br/>
<img src="https://i.imgur.com/PpziEU7.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br />
Installing Nessus on Kali Linux  <br/>
<img src="https://i.imgur.com/6wSWfh5.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<img src="https://i.imgur.com/J4OgDpB.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br />
Results from Nessus Scan  <br/>
<img src="https://i.imgur.com/DU4K6DD.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<img src="https://i.imgur.com/9D4Xiqe.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<img src="https://i.imgur.com/Oajigt0.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<img src="https://i.imgur.com/eFMNBq1.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br />
Searching up Kioptrix port 443  <br/>
<img src="https://i.imgur.com/c4GeLdF.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br />
Identified port 80 and port 443 as possible vulnerabilities “nmap -sn”  <br/>
<img src="https://i.imgur.com/Fl6hbAs.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br />
Utilizing Metaspoit tool  <br/>
<img src="https://i.imgur.com/A7gGSwi.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br />
Utilizing Auxiliary Scanner  <br/>
<img src="https://i.imgur.com/EoR0b5h.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<img src="https://i.imgur.com/ZIjjwQy.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br />
Using Searchsploit tool to for Samba 2 exploits  <br/>
<img src="https://i.imgur.com/kWm6M0e.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br />
Getting the correct exploit command from Rapid7.   <br/>
<img src="https://i.imgur.com/JBuhxWN.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br />
Configure correct payload to exploit  <br/>
<img src="https://i.imgur.com/tFSIfQg.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<br />
<br />
Gained root access to Kioptrix  <br/>
<img src="https://i.imgur.com/42V2JHC.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
<img src="https://i.imgur.com/hTTW84N.png" height="80%" width="80%" alt="Kioptrix Exploitation Steps"/>
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

