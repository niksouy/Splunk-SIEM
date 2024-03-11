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
Launched the Splunk by running script provided by UofT: <br/>
<img src="https://i.imgur.com/kDexMSY.png" height="80%" width="80%" />
<br />
<br />  
<h2>Part 1: Created Reports, Alerts, and Dashboards for the Windows Logs:</h2>
<br />
<br />
<h2> ✒️📜Reports </h2>
 <br />
 <br />
👌Windows Logs: Added provided Windows logs into the Splunk
<img src="https://i.imgur.com/lLYn8pL.png" height="80%" width="80%" />
<br />
<br />
👌Report-1: Created a report to show the ID number associated with the specific signature for Windows activity. This will allow VSI to view reports that show the ID number
associated with the specific signature for Windows activity: <br/>
<img src="https://i.imgur.com/KLBhshg.png" height="80%" width="80%" />
<img src="https://i.imgur.com/kl1w8k6.png" height="80%" width="80%" />
<br />
<br />
👌Report-2: Created a report that displays the severity levels, count, and percentage of each. This will allow VSI to understand the severity levels of the quickly
Windows logs are being viewed.  <br/>
<img src="https://i.imgur.com/qIddRR3.png" height="80%" width="80%" />
<br />
<br />
👌Report-3: Created a report that provides a comparison between the success and failure of Windows activities. This will show VSI if there is a suspicious level of failed activities on
their server:  <br/>
<img src="https://i.imgur.com/qsw36G3.png" height="80%" width="80%" />
<img src="https://i.imgur.com/EG7IyxS.png" height="80%" width="80%" />
<br />
<br />
<h2> 🚨🚨🚨Alerts </h2>
⬇️Designed the following alerts to notify VSI of suspicious activity.
 <br /> 📜I emailed all Alarms to "SOC@VSI-company.com", SOC manager at VSI.
<br />
<br />
👌Alert-1: Created an alert that’s triggered when the threshold has been reached, based on the determined baseline and threshold for the hourly level of failed Windows
activity: Greater than 9 <br/>
<img src="https://i.imgur.com/cfbzpHe.png" height="80%" width="80%" />
<br />
<br >
👌Alert-2: Created an alert that’s triggered when the threshold has been reached based on the determined baseline and threshold for the hourly count of the signature
“an account was successfully logged on”: Greater than 18 <br/>
 <br >
  ✒️As "signature name" sometimes changes when the Windows system updates, I was noticed to consider "signature ID" instead.
<img src="https://i.imgur.com/VtdVaOO.png" height="80%" width="80%" />
<br />
<br />
👌Alert-3: Created an alert that’s triggered when the threshold has been reached based on the determined baseline and threshold for the hourly count of the signature “a
user account was deleted”: Greater than 17  <br/>
<img src="https://i.imgur.com/VH3TvmG.png" height="80%" width="80%" />
<br /> 
<br />
<h2> 🔍🔍🔍Visualizations and dashboards </h2>
⬇️Designed the following visualizations and added them to a dashboard called “Windows Server Monitoring”.
<br />
<br />
 👌A line chart that displays the different “signature” field values over time. <br/>
<img src="https://i.imgur.com/YOyrP9k.png" height="80%" width="80%" />
<br />
<br >
👌A line chart that displays the different “user” field values over time. <br/>
<img src="https://i.imgur.com/TarN5V5.png" height="80%" width="80%" alt="Disk />
<br />
<br >
👌Illustrated the count of different signatures. <br/>
<img src="https://i.imgur.com/pdPVS8U.png" height="80%" width="80%" />
<br />
<br >
👌Illustrated the count of different users. <br/>
<img src="https://i.imgur.com/yN6yiYc.png" height="80%" width="80%" />
<br />
<br >
👌A single-value "Radial Gauge" visualization for on-time monitoring of a specific malicious signature("A log on was attempted using explicit credential")  <br/>
<img src="https://i.imgur.com/iOiD1HZ.png" height="80%" width="80%" />
<br />
<br >
<h2>Part 2: Load and Analyze Apache Logs:</h2>
<br />
<br />
<h2> ✒️📜Reports </h2>
 <br />
 <br />
👌Apache Logs: Added provided Apache logs into the Splunk
<img src="https://i.imgur.com/sPHAn4U.png" height="80%" width="80%"/>
<br />
<br />
👌Report-1: A report that shows a table of the different HTTP methods. This provided insight into the type of HTTP activity being
requested against VSI’s web server: <br/>
<img src="https://i.imgur.com/fEOIgVz.png" height="80%" width="80%" />
<img src="https://i.imgur.com/IT9cvMY.png" height="80%" width="80%" />
<br />
<br />
👌Report-2: A report that shows the top 10 domains that refer to VSI’s website. This assisted VSI with identifying suspicious referrers: <br/>
<img src="https://i.imgur.com/k3M1NQj.png" height="80%" width="80%" />
<img src="https://i.imgur.com/IAjJe2b.png" height="80%" width="80%" />
<br />
<br />
👌Report-3: A report that shows the count of each HTTP response code. This provided insight into any suspicious levels of HTTP
responses: <br/>
<img src="https://i.imgur.com/bHg1iHS.png" height="80%" width="80%" />
<img src="https://i.imgur.com/nMpXb3i.png" height="80%" width="80%" />
<br />
<br />
<h2> 🚨🚨🚨Alerts </h2>
⬇️Designed the following alerts to notify VSI of suspicious activity.
 <br /> 📜I emailed all Alarms to "SOC@VSI-company.com", SOC manager at VSI.
<br />
<br />
👌Alert-1: Created an alert that’s triggered when the threshold has been reached based on the determined baseline and threshold for hourly activity from any
country besides the United States: Greater than 100 <br/>
<img src="https://i.imgur.com/tPPA3H6.png" height="80%" width="80%" />
<br />
<br >
👌Alert-2: Created an alert that’s triggered when the threshold has been reached based on the appropriate baseline and threshold for the hourly
count of the HTTP POST method: Greater than 2 <br/>
<img src="https://i.imgur.com/x6cP7zo.png" height="80%" width="80%" />
<br />
<br >
<h2> 🔍🔍🔍Visualizations and dashboards </h2>
⬇️Designed the following visualizations and added them to a dashboard called “Apache Web Server Monitoring”.
<br />
<br />
 👌A line chart that displays the different “signature” field values over time. <br/>
<img src="https://i.imgur.com/YOyrP9k.png" height="80%" width="80%" />
<br />
<br >


 
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
