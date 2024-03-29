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
<p align="center">
<h1>Statistics before attack </h1>
<br> I compared these patterns with the ones after the attack and analyzed the deviation from normal later in this project.</p>
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

<img src="https://i.imgur.com/IT9cvMY.png" height="80%" width="80%" />
<br />
<br />
👌Report-2: A report that shows the top 10 domains that refer to VSI’s website. This assisted VSI with identifying suspicious referrers: <br/>
<img src="https://i.imgur.com/IAjJe2b.png" height="80%" width="80%" />
<br />
<br />
👌Report-3: A report that shows the count of each HTTP response code. This provided insight into any suspicious levels of HTTP
responses: <br/>
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
⬇️Designed the following visualizations and added them to a dashboard called “Apache Web Server Monitoring.
<br />
<br />
 👌<br/>
<img src="https://i.imgur.com/UJZ5ink.png" height="80%" width="80%" />
<br />
<br >
<p align="center">
<h1> 🎯Attack Summary—Windows </h1 
<br> I uploaded after-attack logs provided by UofT Bootcamp and compared their statistics with reports prior to the attack. </p> 

- <b> Severity Report:
<br >The ratio of informational to high severity changed from 13:1 to 4:1 (6.91% to 29.22% High Severity)
This is what we expect to see when under attack:
<br />
<img src="https://i.imgur.com/9kpUlGl.png" height="80%" width="80%" />
<br />

- <b> Failed Activities Report: 
<br >The ratio of success to failure changed from 38:1 to 63:1 (2.98% to 1.56% failure).
This is suspicious because we know we were under attack, so there should ideally be more failures: <br />
<img src="https://i.imgur.com/5UNpnUl.png" height="80%" width="80%" />
<br />

- <b> Failed Windows Activity Alert: 
<br >35 failed attempts from 8:00-9:00 AM on March 25
Our alert was triggered as the threshold was 4
Would increase the threshold to 8 <br />

- <b> Successful Logins Alert:
<br >11 logins from User_a between 2:00-3:00 AM on March 25
Didn’t trigger our alert since our threshold was 15 per hour - there were 14 logins, including the 11 from User_a
Would edit the alert to be 7 logins per user per hour 

- <b> Deleted Accounts Alert (I ended up this was not an indicator of an attack unless a significant deviation would happen):
<br > No suspicious volume of deleted accounts; the number of deleted accounts dropped from 318 to 130, though.
<img src="https://i.imgur.com/5dAHCSX.png" height="80%" width="80%" />
<img src="https://i.imgur.com/1xTzZgS.png" height="80%" width="80%" />
<br />

<h1> 📆Time Chart of Signatures:</h1>
<br /> Between 12:00-3:00 AM on March 25 influx of “User account locked out” signatures - peaked at 896 
<br />Between 8:00-11:00 AM on March 25 influx of “User attempted to change password” signatures  - peaked at 1258 

<h1> 📆Time Chart of Users:</h1>
<br /> Between 1:40-2:40 AM on March 25, there was an influx of User_a logins - peaking at 785 
<br /> Between 9:10-11:00 AM on March 25, there was an influx of User_k logins  - peaking at 397 
<br />
<br />
 👌<br/> 
<img src="https://i.imgur.com/nSKHfqq.png" height="80%" width="80%" />
<br />
<br >
<p align="center">
<h1> 🎯Attack Summary—Apache </h1 
<br> I uploaded after-attack logs provided by UofT Bootcamp and compared their statistics with reports prior to the attack. </p>

- <b> HTTP Methods Report:
<br >POST method usage increased from 1.06% to 29.44%. It was suspected that a bad actor was uploading harmful data to resources:
<img src="https://i.imgur.com/fEOIgVz.png" height="80%" width="80%" />

- <b> Referrer Domains Report:
<br >No suspicious changes to referrer domains as ratios remained within 2% of non-attack logs:
<img src="https://i.imgur.com/k3M1NQj.png" height="80%" width="80%" />

- <b> Response Codes Report:
<br >404 Error codes increased from 2.13% to 15%. This is good because it likely minimized damage:
<img src="https://i.imgur.com/bHg1iHS.png" height="80%" width="80%" />

- <b> International Activity Alert: 
<br > There was an influx of international activity From 8:00-9:00 PM on March 25.
Our alert wasn't triggered as the threshold was 100.
Would decrease the threshold to 60 since I expect less international activity. <br />

- <b> HTTP POST Alert: 
<br > 1296 instances of HTTP POST between 8:00-9:00 PM on March 25.
Our alert was triggered as the threshold was 2.
Wouldn’t change our threshold since it aligned with the non-attack data when the attack was not in progress. <br />
<img src="https://i.imgur.com/407L9yL.png" height="80%" width="80%" />
<br />

<h1> 📆Time Chart of Clustermap:</h1>
<br /> Data showed Ukraine suddenly becoming the highest country on the site aside from the US, as it Had 439 uses in Kyiv, Ukraine and 433 uses in Kharkiv, Ukraine.
<br />
<br /><img src="https://i.imgur.com/6k4o4dy.png" height="80%" width="80%" />
<br />
<h1> URI Data statistics:</h1>
<br /> Observed increased use of /VSI_Account_logon.php 
<br />
<br /><img src="https://i.imgur.com/ARxDX6P.png" height="80%" width="80%" />
<br />
<h1> Summary:</h1>
<br /> 

- Attacks occurred on March 25 involving the Windows and Apache servers suspected from Kiev and Kharkiv, Ukraine.

- This resulted in many user accounts being locked, and password change attempts resulted in fewer users being able to log in later in the day.

- Attacks were focused on logging in and usage of VSI_Account_logon.php 

<h1> Future Mitigations:</h1>
<br /> 

- Improving Web Application firewall

- Increasing server capacity to prevent overloading 

- Better password setup protocol, such as stronger and more unique passwords to combat account compromise.

- Implementing multi-factor authentication makes it harder to compromise accounts. 

  
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
