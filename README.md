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
"End User License Agreement"/>
<br /> 
<br /> 
Custom Setup Make sure that both Boxes are selected, then proceed by <I><b>Next</b></I>.
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
Choose your application shortcut (option), then click <i><b>NEXT</b></i>. 
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
This will launch VMware Workstation Pro. You are immediately prompted to enter an active licensing key or continue without a license and proceed with a 30-day trial option. Click <i><b>Continue</b></i>.
<br />
<img src="https://github.com/user-attachments/assets/c15e8e88-669f-4ddb-a788-f1156c0ed8ec" height="50%" width="50%" alt=
 "License or Trial" />

<br />
<br />
 Click <I><b>Finish<b/><I/>.
 <br />
 <img src="https://github.com/user-attachments/assets/9a2fd80d-a5dd-4623-84aa-98a646ea35a0" height="50%" width="50%" alt= 
"Finished Configuration" />

<h3>Network Configuration (Static IP & DNS)</h3>

Before installing Active Directory Domain Services, the server network configuration must be updated. A static IP address is required to ensure consistent DNS resolution and domain stability.

<br /><br />

Open <b>Network and Sharing Center</b> → <b>Change adapter settings</b>.  
Right-click the active network adapter and select <b>Properties</b>.  
Select <b>Internet Protocol Version 4 (TCP/IPv4)</b> and click <b>Properties</b>.

<br /><br />

Configure the following:
<ul>
  <li>Assign a <b>static IP address</b></li>
  <li>Set the <b>Preferred DNS server</b> to the server’s own IP address</li>
</ul>

This configuration ensures the Domain Controller can properly resolve and register DNS records.

<br /><br />

<img src="https://github.com/user-attachments/assets/3eb3f987-17a4-4230-a751-2334b2dc14b8"
     height="70%" width="70%"
     alt="Static IP and DNS Configuration" />

<br /><br />

<h2>Active Directory Domain Services Configuration</h2>

A new virtual machine was created in VMware Workstation Pro using the Windows Server 2019 ISO. Hardware resources such as CPU, memory, and disk size were allocated based on lab requirements. The VM was configured to use a compatible virtual network adapter.

<br /><br />

<img width="786" height="602" alt="5" src="https://github.com/user-attachments/assets/40053442-2e76-4f38-ac1b-63ef976ef2cf" />

<br /><br />

<img width="1012" height="700" alt="Check IP  config Command prompt" src="https://github.com/user-attachments/assets/2ac30297-eec7-437f-ae2c-6ee4eb932d20" />

<br /><br />
Click <b>Add Roles and Features</b> from the Server Manager dashboard.
<br /><br />

<img width="1007" height="755" alt="server mangaer dashboard" src="https://github.com/user-attachments/assets/8a2cc092-72c4-4373-b0b9-947d0bf6124c" />

On the <b>Before You Begin</b> screen, review the checklist and click <b>Next</b>.
<br /><br />

<img src="https://github.com/user-attachments/assets/d782457d-9c45-43e8-bce8-8f2c14a4f2df" />
" width="70%" />

<br /><br />
Select <b>Role-based or feature-based installation</b>.
<br /><br />
<img  src="https://github.com/user-attachments/assets/01d2e9d2-a212-4d10-a8c8-f6d5f02ca503" />
 
<br /><br />
Select the local server from the server pool.
<br /><br />

<img src="https://github.com/user-attachments/assets/aa9a36f6-7d53-449d-9992-d4718cdcb1da" />
 width="70%" />

<br /><br />
Check <b>Active Directory Domain Services</b> and add required features.
<br /><br />

<img width="1013" height="635" alt="9" src="https://github.com/user-attachments/assets/d690e92d-aae2-4a9b-8c26-d18b0aab05e2" />
" width="70%" />

<br /><br />
Review the AD DS information screen.
<br /><br />

<img src="https://github.com/user-attachments/assets/3d96701b-c8c8-44dc-a0bc-eac2c63f5b93" />

<br /><br />

<img width="1012" height="642" alt="11" src="https://github.com/user-attachments/assets/cc261f95-7507-4108-aa3f-068c94f8f283" />

Confirm selections and install AD DS.
<br /><br />

<img width="1002" height="637" alt="13" src="https://github.com/user-attachments/assets/75cec4eb-8ba6-4b88-9bc2-024b1f7c8fbe" />
<br /><br />
<img width="1011" height="700" alt="14" src="https://github.com/user-attachments/assets/2ca60865-e96f-42d3-82fd-2ebc6c663a2a" />
<br /><br />
<img width="1012" height="692" alt="15" src="https://github.com/user-attachments/assets/5577a080-29cb-44c3-b9eb-7dc480a5505f" />

<h3>Promote Server to Domain Controller</h3>

<img width="1008" height="143" alt="16" src="https://github.com/user-attachments/assets/b65d48e6-bad7-4cc1-8189-a1d3039e6f93" />

Click the notification flag and select <b>Promote this server to a domain controller</b>.
<br /><br />

<img width="1017" height="736" alt="17" src="https://github.com/user-attachments/assets/7e82e3ca-28f5-46a1-b801-88ead1a233c8" />
<br /><br />
<br /><br />
Select <b>Add a new forest</b> and enter the root domain name.
<br /><br />
<img width="1011" height="715" alt="18" src="https://github.com/user-attachments/assets/076ff3b0-f4d0-467a-9b0b-fec3f0afa1b0" />

<br /><br />

Set forest and domain functional levels and configure the <b>DSRM password</b>.
<br /><br />

<img width="1008" height="723" alt="19" src="https://github.com/user-attachments/assets/57d56a40-a3ba-4511-aebc-081dbebbec5b" />


<br /><br />
Acknowledge the DNS delegation warning.
<br /><br />

<br /><br />
Accept default database, log, and SYSVOL paths.
<br /><br />

<img width="1002" height="642" alt="20" src="https://github.com/user-attachments/assets/6c3c2835-5716-4da3-9c76-793fec2e51c2" />

<br /><br />
Review prerequisites and install.
<br /><br />
<img width="1011" height="683" alt="21" src="https://github.com/user-attachments/assets/69aed358-45b9-49cb-a317-bfe0304e1291" />

<br /><br />
The server automatically reboots after promotion.
<br /><br />

<h2>Post-Installation Verification</h2>

Log in using the domain Administrator account.
<br /><br />

<img width="2015" height="645" alt="47" src="https://github.com/user-attachments/assets/108418ff-05e8-44f5-ac06-c09cacbb0d93" />

<br /><br />
Create a new 
<br /><br />
Verify that Active Directory Users and Computers opens successfully.
<br /><br />

<img width="1017" height="492" alt="423" src="https://github.com/user-attachments/assets/884e6dd9-b416-45f6-be14-60b9c8f0c1e1" />

<h3>Organizational Units and Users</h3>

Create Organizational Units.
<br /><br />

<img width="628" height="748" alt="26" src="https://github.com/user-attachments/assets/e859a755-0ce0-4196-ada3-44d69e870472" />


<br /><br />

Create domain users and verify properties.
<br /><br />

<img width="1017" height="760" alt="23" src="https://github.com/user-attachments/assets/29e506e1-cc7f-43de-9f17-e03db2727b9b" />
<br /><br />

<img width="1006" height="763" alt="24" src="https://github.com/user-attachments/assets/12905965-53db-4dca-ab75-96aaff899eb2" />


<h2>DNS Verification and Domain Health</h2>

<br /><br />

After the client successfully joins the domain, verify that DNS records were created correctly on the Domain Controller.

Open <b>DNS Manager</b> and confirm that:
<ul>
  <li>The forward lookup zone exists</li>
  <li>The client machine appears as an A record</li>
</ul>

<br /><br />

<img src="Missing" width="70%" />

<h2>Group Policy Management</h2>

Open <b>Group Policy Management</b> from Server Manager or Administrative Tools. Verify that the default domain policies are present.

<br /><br />

<img width="1017" height="492" alt="423" src="https://github.com/user-attachments/assets/9c032974-302f-41a3-845c-a5f2aa825c39" />

<h3>Create and Link a Group Policy Object (GPO)</h3>

Create a new Group Policy Object to demonstrate centralized policy management.

<br /><br />

<img src="Missing" width="70%" />

<h3>Apply Group Policy on Client Machine</h3>

On the client machine, force a policy refresh by running:

<pre>gpupdate /force</pre>

<br /><br />

<img src="Missing" width="70%" />

<h3>Validate Group Policy Application</h3>

Confirm that Group Policy was applied successfully by running:

<pre>gpresult /r</pre>

<br /><br />

<img src="MISSING" width="70%" />

<h2>Lab Completion Summary</h2>

At this stage, the Active Directory lab environment is fully functional and validated.

<img width="303" height="145" alt="50" src="https://github.com/user-attachments/assets/b187d15a-3010-4c7b-8d91-ae0106c0bf34" />

</p>
