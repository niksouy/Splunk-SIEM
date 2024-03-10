<h1>Defensive Security by Splunk </h1>

<h2>Client: A fictional organization named VSI</h2>
 
<h2>Description</h2>
I used Splunk to design a custom monitoring environment to protect a fictional organization. I created custom reports, alerts, dashboards, and add-on apps to protect VSI- our mock company. Then I experienced a simulated attack and analyzed the results to determine the effectiveness of my monitoring solutions. I completed the project by showcasing my defensive solution in a class presentation 
<br />


<h2>Utilities Used</h2>

- <b>Splunk Docker Container provided by UofT Bootcamp</b>
- <b>Windows Server Logs
○ This server contains the intellectual property of VSI’s next-generation
virtual-reality programs.
- <b>Apache Server Logs<b>
○ This server is used for VSI’s main public-facing website, vsi-company.com.


<h2>Environments Used </h2>

- <b>Splunk web interface</b>
- <b>Ubuntu Linux-<b> 

<h2>Program walk-through:</h2>

<p align="center">
Launched the Splunk by running script provided by UofT : <br/>
<img src="https://i.imgur.com/kDexMSY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />  
<h2>Part 1: Created Reports, Alerts, and Dashboards for the Windows Logs:</h2>
<br />
<br />
<h2> ✒️📜Reports </h2>
 <br />
 <br />
👌Added provided Windows logs into the Splunk
<img src="https://i.imgur.com/lLYn8pL.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
👌Created a report to show the ID number associated with the specific signature for Windows activity. This will allow VSI to view reports that show the ID number
associated with the specific signature for Windows activity: <br/>
<img src="https://i.imgur.com/KLBhshg.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/kl1w8k6.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
👌Created a report that displays the severity levels, count, and percentage of each. This will allow VSI to understand the severity levels of the quickly
Windows logs are being viewed.  <br/>
<img src="https://i.imgur.com/qIddRR3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
👌Created a report that provides a comparison between the success and failure of Windows activities. This will show VSI if there is a suspicious level of failed activities on
their server:  <br/>
<img src="https://i.imgur.com/qsw36G3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/EG7IyxS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<h2> 🚨🚨🚨Alerts </h2>
⬇️Designed the following alerts to notify VSI of suspicious activity.
<br />
<br />
Created an alert that’s triggered when the threshold has been reached, based on the determined baseline and threshold for the hourly level of failed Windows
activity:  <br/>
<img src="https://i.imgur.com/cfbzpHe.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Observe the wiped disk:  <br/>
<img src="https://i.imgur.com/AeZkvFQ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
