<h1>Unlock a User Account in PowerShell</h1>

 

<h2>Description</h2>
In an IT helpdesk environment, user accounts may get locked due to multiple failed login attempts, security policies, or administrative actions. Instead of using the Active Directory Users and Computers (ADUC) GUI, IT professionals can efficiently unlock accounts using PowerShell.

PowerShell provides a quick, automated way to identify locked accounts and unlock them, improving response time and minimizing user downtime.
<br />


<h2>Utilities Used</h2>

- <b>PowerShell</b> 


<p align="center">
Users Account is locked due to multiple wrong password attempt: <br/>
<img src="https://imgur.com/BFsYmVY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Quick Steps to Unlock a User Account Using PowerShell <br />
1.Open PowerShell – Run PowerShell as Administrator. <br />
<p align="center">
<img src="https://imgur.com/CwczycY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p align="center">
2.Check Locked Accounts – Run:  <br />
Search-ADAccount -LockedOut <br />
<p align="center">
<img src="https://imgur.com/lcVpjJ0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p align="center">
3.Unlock a Specific User – Run: <br />
Unlock-ADAccount -Identity "username" <br />
(Replace "username" with the actual username or use their SamAccountName.) <br />
<p align="center">
<img src="https://imgur.com/SghSONW.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p align="center">
4.Verify Unlock Status – Run: <br />
Get-ADUser -Identity "username" -Properties LockedOut <br />
(Ensure LockedOut is False.) <br />
<p align="center">
<img src="https://imgur.com/TMwhLYI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p align="center">
5.Inform the User – Confirm with the user that they can log in successfully.  <br/>
<p align="center">
<img src="https://imgur.com/WSdZV27.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
