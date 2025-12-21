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
<img src="REPLACE_WITH_SERVER_MANAGER_DASHBOARD_SCREENSHOT" height="70%" width="70%" alt="Server Manager Dashboard" />
<br /><br />

Click <b>Add Roles and Features</b> from the Server Manager Dashboard. This launches the Add Roles and Features Wizard.
<br /><br />
<img src="REPLACE_WITH_ADD_ROLES_WIZARD_SCREENSHOT" height="70%" width="70%" alt="Add Roles and Features Wizard" />
<br /><br />

On the <b>Before You Begin</b> screen, review the information and click <i><b>Next</b></i>.
<br /><br />
<img src="REPLACE_WITH_BEFORE_YOU_BEGIN_SCREENSHOT" height="70%" width="70%" alt="Before You Begin" />
<br /><br />

Select <b>Role-based or feature-based installation</b>. This option allows you to install Active Directory on the local server. Click <i><b>Next</b></i>.
<br /><br />
<img src="REPLACE_WITH_ROLE_BASED_SCREENSHOT" height="70%" width="70%" alt="Role-based Installation" />
<br /><br />

Choose the local server from the server pool and click <i><b>Next</b></i>.
<br /><br />
<img src="REPLACE_WITH_SERVER_SELECTION_SCREENSHOT" height="70%" width="70%" alt="Server Selection" />
<br /><br />

On the <b>Server Roles</b> page, check <b>Active Directory Domain Services</b>. When prompted, click <b>Add Features</b>, then click <i><b>Next</b></i>.
<br /><br />
<img src="REPLACE_WITH_ADDS_SELECTION_SCREENSHOT" height="70%" width="70%" alt="AD DS Role Selection" />
<br /><br />

Proceed through the <b>Features</b> and <b>AD DS</b> information screens by clicking <i><b>Next</b></i>.
<br /><br />
<img src="REPLACE_WITH_ADDS_INFO_SCREENSHOT" height="70%" width="70%" alt="AD DS Information" />
<br /><br />

On the <b>Confirmation</b> screen, verify your selections and click <i><b>Install</b></i>. Wait for the role installation to complete.
<br /><br />
<img src="REPLACE_WITH_ADDS_INSTALL_SCREENSHOT" height="70%" width="70%" alt="AD DS Installing" />
<br /><br />

Once installation finishes, click <b>Close</b>.

<h3>Promote Server to Domain Controller</h3>

After AD DS installation, a notification flag will appear in Server Manager. Click the flag and select <b>Promote this server to a domain controller</b>.
<br /><br />
<img src="REPLACE_WITH_PROMOTION_NOTIFICATION_SCREENSHOT" height="70%" width="70%" alt="Promote to Domain Controller" />
<br /><br />

Select <b>Add a new forest</b>, then enter a root domain name (example: <b>lab.local</b>). Click <i><b>Next</b></i>.
<br /><br />
<img src="REPLACE_WITH_NEW_FOREST_SCREENSHOT" height="70%" width="70%" alt="New Forest Configuration" />
<br /><br />

Set the <b>Forest Functional Level</b> and <b>Domain Functional Level</b> to <b>Windows Server 2016</b> or higher. Configure a <b>DSRM password</b>, then click <i><b>Next</b></i>.
<br /><br />
<img src="REPLACE_WITH_DSRM_SCREENSHOT" height="70%" width="70%" alt="DSRM Password" />
<br /><br />

Accept the default DNS delegation warning and click <i><b>Next</b></i>.
<br /><br />
<img src="REPLACE_WITH_DNS_WARNING_SCREENSHOT" height="70%" width="70%" alt="DNS Warning" />
<br /><br />

Leave default database, log, and SYSVOL paths unless customization is required. Click <i><b>Next</b></i>.
<br /><br />
<img src="REPLACE_WITH_PATHS_SCREENSHOT" height="70%" width="70%" alt="AD Paths" />
<br /><br />

Review the configuration summary. Optionally export the configuration script. Click <i><b>Install</b></i> to begin promotion.
<br /><br />
<img src="REPLACE_WITH_PREREQUISITES_SCREENSHOT" height="70%" width="70%" alt="Prerequisites Check" />
<br /><br />

The server will automatically reboot after promotion completes.

<h2>Post-Installation Verification</h2>

Confirm the domain structure is visible and accessible.

<br />

<img src="REPLACE_WITH_ADUC_CONSOLE_SCREENSHOT" height="70%" width="70%" alt="Active Directory Users and Computers Console" />
<br /><br />

<h3>Organizational Units and Users</h3>

Organizational Units (OUs) and user objects were created to simulate a basic enterprise environment.

### Confirmed Actions

- Organizational Units created (e.g., IT, HR, Users, Computers)
- Domain user accounts created
- Objects placed in correct OUs

<br />

<img src="REPLACE_WITH_OU_STRUCTURE_SCREENSHOT" height="70%" width="70%" alt="Organizational Unit Structure" />
<br /><br />

<img src="REPLACE_WITH_USER_CREATION_SCREENSHOT" height="70%" width="70%" alt="New Domain User Creation" />
<br /><br />

<h2>Client Machine Domain Join</h2>

A Windows 10 / Windows 11 client virtual machine was joined to the Active Directory domain.

### Steps Performed

- Client VM connected to the same virtual network as the Domain Controller
- Client DNS manually set to the Domain Controller’s IP address
- Domain join initiated via System Properties
- Client restarted after successful domain join

<br />

<img src="REPLACE_WITH_CLIENT_DNS_CONFIGURATION" height="70%" width="70%" alt="Client DNS Configuration" />
<br /><br />

<img src="REPLACE_WITH_DOMAIN_JOIN_DIALOG" height="70%" width="70%" alt="Domain Join Dialog" />
<br /><br />

<img src="REPLACE_WITH_DOMAIN_JOIN_SUCCESS" height="70%" width="70%" alt="Domain Join Successful" />
<br /><br />

<h2>Post-Lab Expansion and Validation</h2>

<h3>Step 1: Create Organizational Units (OUs)</h3>

Open <b>Active Directory Users and Computers</b>. Create a logical OU structure to simulate an enterprise environment. Recommended OUs include <b>Servers</b>, <b>Workstations</b>, <b>Users</b>, and <b>Admins</b>. This structure will be used later for Group Policy scoping and delegation.

<p align="center">
<img src="REPLACE_WITH_CREATE_OU_SCREENSHOT" height="70%" width="70%" alt="Create Organizational Units" />
</p>

<h3>Step 2: Create Domain Users and Security Groups</h3>

Within the <b>Users</b> OU, create standard domain user accounts. Create security groups such as <b>IT_Admins</b>, <b>HR_Users</b>, or <b>Standard_Users</b>, then assign users to the appropriate groups to demonstrate role-based access control.

<p align="center">
<img src="REPLACE_WITH_CREATE_USER_AND_GROUP_SCREENSHOT" height="70%" width="70%" alt="Create Users and Groups" />
</p>

<h3>Step 3: Join a Client Machine to the Domain</h3>

Ensure the Windows 10/11 client VM is using the same virtual network as the Domain Controller and that its DNS is pointed to the DC’s IP address. Join the client to the domain and reboot when prompted.

<p align="center">
<img src="REPLACE_WITH_DOMAIN_JOIN_SCREENSHOT" height="70%" width="70%" alt="Domain Join" />
</p>

<h3>Step 4: Verify Domain Authentication</h3>

Log in to the client machine using a newly created domain user account. Successful login confirms proper authentication between the client and the Domain Controller.

<p align="center">
<img src="REPLACE_WITH_DOMAIN_LOGIN_SCREENSHOT" height="70%" width="70%" alt="Domain User Login" />
</p>

<h3>Step 5: Verify DNS and AD Health</h3>

Open <b>DNS Manager</b> on the Domain Controller and confirm that forward and reverse lookup zones exist. Use <b>nslookup</b> or <b>ping</b> from the client to verify name resolution.

<p align="center">
<img src="REPLACE_WITH_DNS_VERIFICATION_SCREENSHOT" height="70%" width="70%" alt="DNS Verification" />
</p>

<h3>Step 6: Create and Link Group Policy Objects (GPOs)</h3>

Open <b>Group Policy Management</b>. Create GPOs for password policies, account lockout policies, or desktop restrictions. Link the GPOs to the appropriate OUs created earlier.

<p align="center">
<img src="REPLACE_WITH_GPO_CREATION_SCREENSHOT" height="70%" width="70%" alt="Group Policy Management" />
</p>

<h3>Step 7: Validate Group Policy Application</h3>

On the client machine, run <b>gpupdate /force</b> followed by <b>gpresult /r</b> to confirm that Group Policies are successfully applied.

<p align="center">
<img src="REPLACE_WITH_GPRESULT_SCREENSHOT" height="70%" width="70%" alt="Group Policy Results" />
</p>

<h3>Step 8: Backup and Document the Environment</h3>

Install <b>Windows Server Backup</b> and perform a <b>System State Backup</b> of the Domain Controller. Finalize documentation by capturing screenshots, recording configurations, and outlining future expansion plans such as adding DHCP, File Services, or a second Domain Controller.

<p align="center">
<img src="REPLACE_WITH_BACKUP_AND_DOCUMENTATION_SCREENSHOT" height="70%" width="70%" alt="Backup and Documentation" />
 
</p>
 <br />
 

</p>
