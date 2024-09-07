# HomeSOClab-SIEM-


<h2>Description</h2>
In this project i set out with the aim of setting up a home lab using Elastic SIEM and a Kali Linux VM. The data gathered was forwarded from the Kali VM to the SIEM using the Elastic Beats agent, I then generated security events on the Kali VM by using Nmap and Ping commands, and queried and analyzed the logs in the SIEM using the Elastic web interface. I also created a dashboard to visualize security events and then created an alert to detect security events which would email me if a specified alert was triggered.

<h2>Languages and Utilities Used</h2>

- <b>Elastic SIEM</b> 
- <b>Kali Linux</b>

<h2>Environments Used </h2>

- <b>Kali Linux OS</b> 

<h2>Program walk-through:</h2>

<p align="center">
Install a Kali Linux VM: <br/>
<img width="807" alt="Screenshot 2024-09-07 at 12 49 02" src="https://github.com/user-attachments/assets/2d769eb3-4f72-4011-9f1b-3e872f5984b8">
<br />
<br />
Download and Install Elastic Agent: <br/>
<img width="911" alt="Screenshot 2024-09-07 at 12 57 31" src="https://github.com/user-attachments/assets/ac623195-8eac-4bcf-a62c-b7355c76b429">
<img width="1552" alt="Screenshot 2024-09-06 at 18 54 00" src="https://github.com/user-attachments/assets/2aeb33e6-9373-4301-9ff4-bfa722293b81">
<br />
<br />
Run a variety of nmap scans in the Kali terminal to generate security alerts on the Elastic SIEM:  <br/>
<img width="869" alt="Screenshot 2024-09-06 at 19 00 37" src="https://github.com/user-attachments/assets/85c65404-68d1-44a4-a320-31207f1994e3">
<br />
<br />
Now I went back to the SIEM log data to analyze if it had detected any Nmap scans being executed, as you can see it did detect scans: <br/>
<img width="1291" alt="Screenshot 2024-09-07 at 13 29 07" src="https://github.com/user-attachments/assets/ab56e0c8-4345-4686-9828-8292643ae9b2">
<br />
<br />
Next I created a visialization dashboard to visualize the detected events:  <br/>
<img width="1429" alt="Screenshot 2024-09-06 at 19 19 32" src="https://github.com/user-attachments/assets/071c911a-5148-4888-b8b4-690616f9303a">
<br />
<br />
I now set out to create a rule to alert me via email when the SIEM detects Nmap scans being conducted :  <br/>
<img width="1414" alt="Screenshot 2024-09-07 at 13 41 30" src="https://github.com/user-attachments/assets/6fa271f5-e481-4408-a126-709f94195443">
<br />
<br />
I once again began to run various nmap commands in the Kali OS to see if the SIEM will detect and alert me via email about these commands being ran. As we can see from the email and security dashboard below it worked:  <br/>
<img width="1429" alt="Screenshot 2024-09-07 at 11 31 33" src="https://github.com/user-attachments/assets/3e97e918-fbc5-4d10-8c17-fe7ecd8bc5c4">
<img width="1429" alt="Screenshot 2024-09-07 at 11 34 13" src="https://github.com/user-attachments/assets/41696c31-2ccf-4ef7-8e79-4b640d002b71">
<br />
<br />
Finally I decided to create another alert which was set up to detect when the ping command was being executed on the host. This alert also worked as you can see the security dashboard presenting the 200 nmap alerts and 2 ping alerts below:  <br/>
<img width="1429" alt="Screenshot 2024-09-07 at 11 41 20" src="https://github.com/user-attachments/assets/bf5a2bf2-c0d2-4652-be9f-22d00b388885">

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
