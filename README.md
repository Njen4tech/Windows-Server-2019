<h1>Windows Server 2019 (Active Directory)</h1>


<h2>Active Directory</h2>

This project consists of a step-by-step guide on building a Virtual Machine and creating an Active Directory home lab environment. It’s recommended that adequate resources, such as CPU, RAM, and storage, be allocated to meet your testing and development needs. Additionally, consider networking configurations such as virtual switches and VLANs before setting up your Virtual Machines.
<br />


<h2>Utility and Tools </h2>

- <b>Download Windows Server ISO file</b> 
- <b>Setup & Configuration </b>
- <b>Configure Windows Server Setup</b>
- <b>Boot Windows Server</b>
 
  
<h2>Environments Used </h2>

- <b>WINDOWS ISO</b> (WINDOWS SERVER 2019)

<h2>Program walk-through:</h2>

<p align="center">
Launch the utility. <br/>
<br /> 

Click on this link [Windows Server 2019 ISO](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2019) to download.
<br />
<img src="https://github.com/user-attachments/assets/7fecb957-eabe-4f70-872b-60ee8935b092" height="70%" width="70%" alt=
"Download ISO"/>
<br/>
<br/>
<h5>Process & Installation </h5>
<br />
Virtual Machine Creation. 
<br />
<br />
The Setup Wizard panel will appear, then click <I><b>Next</b></i>. 
<br />
<img src="https://github.com/user-attachments/assets/82476b3d-1915-4f16-bfec-8e1aa012ddbe" height="70%" width="70%" alt=
"Installations"/>
<br />
<br />
Typical(rec) then click <I><b>Next</b></I>. 
<br />
<img src="https://github.com/user-attachments/assets/99910378-c61c-4e0a-becd-4770f81f5da3" height="70%" width="70%" alt=
"End User Licenses Agreement"/>
<br /> 
<br /> 
Custom Setup Make sure that both Boxes are selected then proceed by <I><b>Next</b></I>.
<br />
<img src="https://github.com/user-attachments/assets/e546cb03-f72d-46e2-a060-2f8585919e73" height="70%" width="70%" alt=  
"Custom Setup"/>
<br />
<br />
User Experience Settings will let you choose these options. 
<br />
<img src="https://github.com/user-attachments/assets/ed7eb8a0-7499-4923-bbf2-46cb16ca2d81" height="70%" width="70%" alt=
"User Setup"/>
<br />
<br />
Choose your application shortcut (option) then click <i><b>NEXT</b></i>. 
 <br />
<img src="https://github.com/user-attachments/assets/faeaa2d2-0499-4d45-8a19-8bcee419567c" height="70%" width="70%" alt= 
"Shortcuts" />
<br />
<br />
Click <I><b>Install</b></I>.
<br />
<img src="https://github.com/user-attachments/assets/e92aeca4-d793-4449-a65e-ad83874aee6a" height="70%" width="70%" alt=
"Ready installation"/>
<br />
<br />
Please wait for the process to complete <b>(it may take some time⏲)<b />.
<img src="https://github.com/user-attachments/assets/8e4e3eac-dea1-4f2d-a60b-72642ba1710b" height="70%" width="70%" alt= 
"Installation Processing"/>
<br /> 
  <br />
The setup is complete! If you have a license, please add it at this prompt. 
<img src="https://github.com/user-attachments/assets/38947d20-1fae-42b7-ac15-3600d446b133"  height="70%" width="70%" alt=
"Installation Completed!"/>
<br />
<br />
<br />
<H3>(Optional) License Key</H3>
<img src="https://github.com/user-attachments/assets/64a5d335-12f1-4654-92f8-4afe8187e38e" height="70%" width="70%" alt=
 "License" />
 <br />
 <br />


<br />
<h3>Initial Setup</h3>  <br/>
After the installation is successful.
<br />
<br />
<br />
Start the VMware application from your Desktop:  <br/>
<img src="https://github.com/user-attachments/assets/45578b06-2aae-4694-ba98-236d09497dad" height="30%" width="30%" alt=
 "Desktops" />
<br />
<br />
This will launch VMware Workstation Pro, you are immediately prompted to enter an active licensing key or continue without a license and proceed with a 30-day trial option. Click <i><b>Continue</b></i>.
<br />
<img src="https://github.com/user-attachments/assets/c15e8e88-669f-4ddb-a788-f1156c0ed8ec" height="50%" width="50%" alt=
 "License or Trial" />

<br />
<br />
 Click <I><b>Finish<b/><I/>.
 <br />
 <img src="https://github.com/user-attachments/assets/9a2fd80d-a5dd-4623-84aa-98a646ea35a0" height="50%" width="50%" alt= 
"Finished Configuration" />


<h2>Active Directory Domain Services Configuration</h2>

Log in to Windows Server 2019 using the local <b>Administrator</b> account. Once logged in, <b>Server Manager</b> will launch automatically.
<br /><br />

<img src="https://github.com/user-attachments/assets/99015d54-e091-4448-9591-cb3dba740487" width="70%" />

<br /><br />
Click <b>Add Roles and Features</b> from the Server Manager dashboard.
<br /><br />

<img src="https://github.com/user-attachments/assets/81e182ac-4f91-4d70-b64d-3bd87b6dfe45" width="70%" />

<br /><br />
On the <b>Before You Begin</b> screen, review the checklist and click <b>Next</b>.
<br /><br />

<img src="https://github.com/user-attachments/assets/fe11faf8-34f7-4bc3-87c3-f3f40b723fc9" width="70%" />

<br /><br />
Select <b>Role-based or feature-based installation</b>.
<br /><br />

<img src="https://github.com/user-attachments/assets/3eb3f987-17a4-4230-a751-2334b2dc14b8" width="70%" />

<br /><br />
Select the local server from the server pool.
<br /><br />

<img src="https://github.com/user-attachments/assets/9b701663-f4c8-4dc4-b3ff-7efe7720a1d9" width="70%" />

<br /><br />
Check <b>Active Directory Domain Services</b> and add required features.
<br /><br />

<img src="https://github.com/user-attachments/assets/5b1ce9f4-17ae-48cc-996a-ce57d5608c9e" width="70%" />

<br /><br />
Review the AD DS information screen.
<br /><br />

<img src="https://github.com/user-attachments/assets/64be78e0-7e80-4ece-9176-ac02c0d4ada8" width="70%" />

<br /><br />
Confirm selections and install AD DS.
<br /><br />

<img src="https://github.com/user-attachments/assets/ddde4355-5562-45f3-9c14-75694d384d9d" width="70%" />

<h3>Promote Server to Domain Controller</h3>

Click the notification flag and select <b>Promote this server to a domain controller</b>.
<br /><br />

<img src="https://github.com/user-attachments/assets/31aa3ad4-d0ca-4c68-9ae3-c56c7116e545" width="70%" />

<br /><br />
Select <b>Add a new forest</b> and enter the root domain name.
<br /><br />

<img src="https://github.com/user-attachments/assets/adcafef0-1505-4b28-a63a-2fa55b5ad10c" width="70%" />

<br /><br />
Set forest and domain functional levels and configure the <b>DSRM password</b>.
<br /><br />

<img src="https://github.com/user-attachments/assets/4a5c51b4-7b71-48a4-92aa-2bd330c6c1f3" width="70%" />

<br /><br />
Acknowledge the DNS delegation warning.
<br /><br />

<img src="https://github.com/user-attachments/assets/a984c6d6-18e3-4d87-843f-09a59848cfa3" width="70%" />

<br /><br />
Accept default database, log, and SYSVOL paths.
<br /><br />

<img src="https://github.com/user-attachments/assets/74b45740-0060-4f18-afa9-9c523659135c" width="70%" />

<br /><br />
Review prerequisites and install.
<br /><br />

<img src="https://github.com/user-attachments/assets/58faa33f-41a9-440a-a4c4-b9f49a3859bb" width="70%" />

<br /><br />
The server automatically reboots after promotion.
<br /><br />

<img src="https://github.com/user-attachments/assets/2c91cf38-d0ca-4724-b52f-0a854401da8f" width="70%" />

<h2>Post-Installation Verification</h2>

Log in using the domain Administrator account.
<br /><br />

<img src="https://github.com/user-attachments/assets/a5e8cdaf-8be3-4fa7-9405-3291279e1f0f" width="40%" />

<br /><br />
Verify Active Directory Users and Computers opens successfully.
<br /><br />

<img src="https://github.com/user-attachments/assets/40d5a4dd-f0e7-488d-8391-9b705401c2d7" width="70%" />

<h3>Organizational Units and Users</h3>

Create Organizational Units.
<br /><br />

<img src="https://github.com/user-attachments/assets/902844b7-e6bd-4d9e-9e96-e4ab20498792" width="70%" />

<br /><br />
Create domain users and verify properties.
<br /><br />

<img src="https://github.com/user-attachments/assets/4589cda1-fb84-4469-aa34-bd22b0af9832" width="70%" />

<h2>Client Machine Domain Join</h2>

<h2>DNS Verification and Domain Health</h2>

After the client successfully joins the domain, verify that DNS records were created correctly on the Domain Controller.

Open <b>DNS Manager</b> and confirm that:
<ul>
  <li>The forward lookup zone exists</li>
  <li>The client machine appears as an A record</li>
</ul>

<br /><br />
<img src="https://github.com/user-attachments/assets/9a30a14b-4954-44a6-a374-ab6b1b4547d2" width="70%" />

<h2>Group Policy Management</h2>

Open <b>Group Policy Management</b> from Server Manager or Administrative Tools. Verify that the default domain policies are present.

<br /><br />
<img src="https://github.com/user-attachments/assets/dd6cb5c1-b576-4539-b8d4-ca44ad8be412" width="80%" />

<h3>Create and Link a Group Policy Object (GPO)</h3>

Create a new Group Policy Object to demonstrate centralized policy management. This GPO can include settings such as:
<ul>
  <li>Password policies</li>
  <li>Desktop restrictions</li>
  <li>Security hardening</li>
</ul>

Link the GPO to the appropriate Organizational Unit.

<br /><br />
<img src="https://github.com/user-attachments/assets/3ac88da4-0b4c-4aa7-a415-8446797abee7" width="70%" />

<h3>Apply Group Policy on Client Machine</h3>

On the client machine, force a policy refresh by running:

<pre>gpupdate /force</pre>

This ensures that the newly created Group Policy Object is applied immediately.

<br /><br />
<img src="https://github.com/user-attachments/assets/8ef48793-e8bf-4a65-ade9-0dfa3f65712f" width="70%" />

<h3>Validate Group Policy Application</h3>

Confirm that Group Policy was applied successfully by running:

<pre>gpresult /r</pre>

This command displays all applied policies and verifies proper communication between the client and the Domain Controller.

<br /><br />
<img src="https://github.com/user-attachments/assets/04fb1e2f-9e68-4951-9079-f824673fcc88" width="40%" />

<h2>Lab Completion Summary</h2>

At this stage, the Active Directory lab environment is fully functional and validated. The following components have been successfully implemented:

</p>
