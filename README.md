<h1>Windows Server 2019 (Active Directory)</h1>

<h2>Active Directory</h2>

<p>
This project consists of a step-by-step guide on building a Virtual Machine and creating
an Active Directory home lab environment. Adequate CPU, RAM, and storage resources should
be allocated. Networking considerations such as virtual switches and VLANs should be
planned before deployment.
</p>

<hr />

<h2>Utilities and Tools</h2>
<ul>
  <li><b>Download Windows Server ISO file</b></li>
  <li><b>Setup & Configuration</b></li>
  <li><b>Configure Windows Server Setup</b></li>
  <li><b>Boot Windows Server</b></li>
</ul>

<h2>Environments Used</h2>
<ul>
  <li><b>Windows Server 2019 ISO</b></li>
</ul>

<hr />

<h2>Program Walk-through</h2>

<h3>Step 1: Download Windows Server 2019 ISO</h3>

<p>
Download the ISO from Microsoft:
<a href="https://www.microsoft.com/en-us/evalcenter/download-windows-server-2019">
Windows Server 2019 ISO
</a>
</p>

<img src="https://github.com/user-attachments/assets/7fecb957-eabe-4f70-872b-60ee8935b092" width="70%" />

<hr />

<h3>Step 2: Virtual Machine Creation & OS Installation</h3>

<p>Launch VMware Workstation Pro and begin the setup wizard.</p>

<p>Click <b>Next</b> to proceed.</p>
<img src="https://github.com/user-attachments/assets/82476b3d-1915-4f16-bfec-8e1aa012ddbe" width="70%" />

<p>Select <b>Typical (Recommended)</b>.</p>
<img src="https://github.com/user-attachments/assets/99910378-c61c-4e0a-becd-4770f81f5da3" width="70%" />

<p>Select <b>Custom Setup</b> and proceed.</p>
<img src="https://github.com/user-attachments/assets/e546cb03-f72d-46e2-a060-2f8585919e73" width="70%" />

<p>Configure User Experience settings.</p>
<img src="https://github.com/user-attachments/assets/ed7eb8a0-7499-4923-bbf2-46cb16ca2d81" width="70%" />

<p>Select application shortcuts.</p>
<img src="https://github.com/user-attachments/assets/faeaa2d2-0499-4d45-8a19-8bcee419567c" width="70%" />

<p>Click <b>Install</b> to begin installation.</p>
<img src="https://github.com/user-attachments/assets/e92aeca4-d793-4449-a65e-ad83874aee6a" width="70%" />

<p>Wait for installation to complete.</p>
<img src="https://github.com/user-attachments/assets/8e4e3eac-dea1-4f2d-a60b-72642ba1710b" width="70%" />

<p>Installation completed.</p>
<img src="https://github.com/user-attachments/assets/38947d20-1fae-42b7-ac15-3600d446b133" width="70%" />

<h4>(Optional) License Key</h4>
<img src="https://github.com/user-attachments/assets/64a5d335-12f1-4654-92f8-4afe8187e38e" width="70%" />

<hr />

<h3>Step 3: Initial VMware Setup</h3>

<p>Launch VMware Workstation Pro.</p>
<img src="https://github.com/user-attachments/assets/45578b06-2aae-4694-ba98-236d09497dad" width="70%" />

<p>Continue using trial or enter license.</p>
<img src="https://github.com/user-attachments/assets/c15e8e88-669f-4ddb-a788-f1156c0ed8ec" width="70%" />

<p>Finish initial setup.</p>
<img src="https://github.com/user-attachments/assets/9a2fd80d-a5dd-4623-84aa-98a646ea35a0" width="70%" />

<hr />

<h3>Step 4: Network Configuration (Static IP & DNS)</h3>

<p>
Configure a static IP before installing Active Directory.
</p>

<ul>
  <li>Open Network and Sharing Center</li>
  <li>Change adapter settings</li>
  <li>Edit IPv4 properties</li>
  <li>Assign static IP</li>
  <li>Set Preferred DNS to server IP</li>
</ul>

<img src="https://github.com/user-attachments/assets/3eb3f987-17a4-4230-a751-2334b2dc14b8" width="70%" />

<hr />

<h3>Step 5: Install Active Directory Domain Services (AD DS)</h3>

<p>Open Server Manager and select <b>Add Roles and Features</b>.</p>
<img src="https://github.com/user-attachments/assets/8a2cc092-72c4-4373-b0b9-947d0bf6124c" width="70%" />

<p>Proceed through the wizard:</p>
<ul>
  <li>Before You Begin</li>
  <li>Role-based installation</li>
  <li>Select local server</li>
  <li>Select AD DS</li>
  <li>Add required features</li>
</ul>

<img src="https://github.com/user-attachments/assets/01d2e9d2-a212-4d10-a8c8-f6d5f02ca503" width="70%" />
<img src="https://github.com/user-attachments/assets/d690e92d-aae2-4a9b-8c26-d18b0aab05e2" width="70%" />

<p>Confirm and install.</p>
<img src="https://github.com/user-attachments/assets/75cec4eb-8ba6-4b88-9bc2-024b1f7c8fbe" width="70%" />

<hr />

<h3>Step 6: Promote Server to Domain Controller</h3>

<p>Select <b>Promote this server to a domain controller</b>.</p>
<img src="https://github.com/user-attachments/assets/7e82e3ca-28f5-46a1-b801-88ead1a233c8" width="70%" />

<p>Add a new forest and define a domain name.</p>
<img src="https://github.com/user-attachments/assets/076ff3b0-f4d0-467a-9b0b-fec3f0afa1b0" width="70%" />

<p>Configure functional levels and DSRM password.</p>
<img src="https://github.com/user-attachments/assets/57d56a40-a3ba-4511-aebc-081dbebbec5b" width="70%" />

<p>Accept defaults and complete promotion.</p>
<img src="https://github.com/user-attachments/assets/6c3c2835-5716-4da3-9c76-793fec2e51c2" width="70%" />

<hr />

<h3>Step 7: Post-Installation Verification</h3>

<p>Log in as Domain Administrator.</p>
<img src="https://github.com/user-attachments/assets/108418ff-05e8-44f5-ac06-c09cacbb0d93" width="70%" />

<p>Verify Active Directory Users and Computers.</p>
<img src="https://github.com/user-attachments/assets/884e6dd9-b416-45f6-be14-60b9c8f0c1e1" width="70%" />

<hr />

<h3>Step 8: Organizational Units and Users</h3>

<p>Create Organizational Units.</p>
<img src="https://github.com/user-attachments/assets/e859a755-0ce0-4196-ada3-44d69e870472" width="70%" />

<p>Create domain users.</p>
<img src="https://github.com/user-attachments/assets/29e506e1-cc7f-43de-9f17-e03db2727b9b" width="70%" />

<hr />

<h3>Step 9: Client Domain Join</h3>

<p>Join the client machine to the domain.</p>
<img src="https://github.com/user-attachments/assets/12905965-53db-4dca-ab75-96aaff899eb2" width="70%" />

<img width="431" height="558" alt="Screenshot 2026-01-06 222020" src="https://github.com/user-attachments/assets/959094ad-a91e-4a9b-85c9-9308e77cc69b" width="70%" />

<p>Domain join successful.</p>
<img src="https://github.com/user-attachments/assets/944a1a3e-30a0-4c57-bd77-cdfed4937650" width="70%" />

<hr />

<h3>Step 10: Group Policy Management</h3>

<p>Open Group Policy Management.</p>
<img src="https://github.com/user-attachments/assets/40e93fb1-9ec1-4ac3-81e4-86741040f51e" width="70%" />

<p>Verify default policies.</p>
<img src="https://github.com/user-attachments/assets/9c032974-302f-41a3-845c-a5f2aa825c39" width="70%" />

<hr />

<h2>Lab Completion Summary</h2>

<p>
The Active Directory lab is fully operational with DNS, AD DS, user management,
and Group Policy successfully validated.
</p>


