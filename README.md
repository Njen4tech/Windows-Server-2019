# Windows Server 2019 (Active Directory)

## Active Directory

This project consists of a step-by-step guide on building a Virtual Machine and creating an Active Directory home lab environment. Adequate CPU, RAM, and storage resources should be allocated. Networking considerations such as virtual switches and VLANs should be planned before deployment.

---

## Utilities and Tools

- **Download Windows Server ISO file**
- **Setup & Configuration**
- **Configure Windows Server Setup**
- **Boot Windows Server**

## Environments Used

- **Windows Server 2019 ISO**

---

## Program Walk-through

### Step 1: Download Windows Server 2019 ISO

Download the ISO from Microsoft:  
[Windows Server 2019 ISO](https://www.microsoft.com/en-us/evalcenter/download-windows-server-2019)

<img src="https://github.com/user-attachments/assets/7fecb957-eabe-4f60-872b-60ee8935b092" width="60%" />

---

### Step 2: Virtual Machine Creation & OS Installation

- Launch VMware Workstation Pro and begin the setup wizard.

- Create a new virtual machine using the Typical (Recommended) configuration

- Select the Windows Server 2019 ISO as the installation media

- Configure hardware resources (CPU, RAM, storage)

- Complete the Windows Server installation wizard

- (Optional) Enter a license key or continue using the evaluation version


Click **Next** to proceed.  
<img src="https://github.com/user-attachments/assets/82476b3d-1915-4f16-bfec-8e1aa012ddbe" width="60%" />

Select **Typical (Recommended)**.  
<img src="https://github.com/user-attachments/assets/99910378-c61c-4e0a-becd-4760f81f5da3" width="60%" />

Select **Custom Setup** and proceed.  
<img src="https://github.com/user-attachments/assets/e546cb03-f72d-46e2-a060-2f8585919e73" width="60%" />

Configure User Experience settings.  
<img src="https://github.com/user-attachments/assets/ed7eb8a0-7499-4923-bbf2-46cb16ca2d81" width="60%" />

Select application shortcuts.  
<img src="https://github.com/user-attachments/assets/faeaa2d2-0499-4d45-8a19-8bcee419567c" width="60%" />

Click **Install** to begin installation.  
<img src="https://github.com/user-attachments/assets/e92aeca4-d793-4449-a65e-ad83874aee6a" width="60%" />

Wait for the installation to complete.  
<img src="https://github.com/user-attachments/assets/8e4e3eac-dea1-4f2d-a60b-72642ba1710b" width="60%" />

Installation completed.  
<img src="https://github.com/user-attachments/assets/38947d20-1fae-42b7-ac15-3600d446b133" width="60%" />

**(Optional) License Key**  
<img src="https://github.com/user-attachments/assets/64a5d335-12f1-4654-92f8-4afe8187e38e" width="60%" />

---

### Step 3: Initial VMware Setup

Launch VMware Workstation Pro.  
<img src="https://github.com/user-attachments/assets/45578b06-2aae-4694-ba98-236d09497dad" width="60%" />

Continue using the trial or enter a license.  
<img src="https://github.com/user-attachments/assets/c15e8e88-669f-4ddb-a788-f1156c0ed8ec" width="60%" />

Finish initial setup.  
<img src="https://github.com/user-attachments/assets/9a2fd80d-a5dd-4623-84aa-98a646ea35a0" width="60%" />

---

### Step 4: Network Configuration (Static IP & DNS)

Before installing Active Directory, configure a static IP.
<img src="https://github.com/user-attachments/assets/3eb3f987-17a4-4230-a751-2334b2dc14b8" width="60%" />

- Open **Network and Sharing Center**
- Change adapter settings
- Edit IPv4 properties
- Assign a static IP
- Set Preferred DNS to the server’s IP
---

### Step 5: Install Active Directory Domain Services (AD DS)

Open **Server Manager** and select **Add Roles and Features**.  
<img src="https://github.com/user-attachments/assets/8a2cc092-72c4-4373-b0b9-947d0bf6124c" width="60%" />

Wizard steps:
- Before You Begin
- Role-based installation
- Select local server
- Select AD DS
- Add required features

<img src="https://github.com/user-attachments/assets/01d2e9d2-a212-4d10-a8c8-f6d5f02ca503" width="60%" />
<img src="https://github.com/user-attachments/assets/d690e92d-aae2-4a9b-8c26-d18b0aab05e2" width="60%" />

Confirm selections and install.  
<img src="https://github.com/user-attachments/assets/75cec4eb-8ba6-4b88-9bc2-024b1f7c8fbe" width="60%" />

---

### Step 6: Promote Server to Domain Controller

Select **Promote this server to a domain controller**.  
<img src="https://github.com/user-attachments/assets/7e82e3ca-28f5-46a1-b801-88ead1a233c8" width="60%" />

Add a new forest and specify the domain name.  
<img src="https://github.com/user-attachments/assets/076ff3b0-f4d0-467a-9b0b-fec3f0afa1b0" width="60%" />

Configure functional levels and DSRM password.  
<img src="https://github.com/user-attachments/assets/57d56a40-a3ba-4511-aebc-081dbebbec5b" width="60%" />

Accept defaults and complete promotion.  
<img src="https://github.com/user-attachments/assets/6c3c2835-5716-4da3-9c76-793fec2e51c2" width="60%" />

---

### Step 7: Post-Installation Verification

Log in as Domain Administrator.  
<img src="https://github.com/user-attachments/assets/108418ff-05e8-44f5-ac06-c09cacbb0d93" width="60%" />

Verify **Active Directory Users and Computers** opens correctly.  
<img src="https://github.com/user-attachments/assets/884e6dd9-b416-45f6-be14-60b9c8f0c1e1" width="60%" />

---

### Step 8: Organizationals and Users
Create Organizational Units.  
<img width="628" height="748" alt="26" src="https://github.com/user-attachments/assets/11de5f99-7b4c-4bb2-a8df-e94f322c42b7" width="60%" />


Create domain users.  
<img src="https://github.com/user-attachments/assets/29e506e1-cc7f-43de-9f17-e03db2727b9b" width="60%" />

---

### Step 9: Client Domain Join

- Configure the client machine’s DNS to point to the Domain Controller
- Join the client to the domain
- Authenticate using domain credentials

Verify the client appears in Active Directory 
<img src="https://github.com/user-attachments/assets/12905965-53db-4dca-ab75-96aaff899eb2" width="60%" />
<img src="https://github.com/user-attachments/assets/959094ad-a91e-4a9b-85c9-9308e77cc69b" width="60%" />

Authenticate using domain credentials.  
<img src="https://github.com/user-attachments/assets/944a1a3e-30a0-4c57-bd77-cdfed4937650" width="60%" />
<br/><br/>


---

### Step 10: Group Policy Management

Open **Group Policy Management**.  
<img src="https://github.com/user-attachments/assets/40e93fb1-9ec1-4ac3-81e4-86741040f51e" width="60%" />

Verify default policies.  
<img src="https://github.com/user-attachments/assets/9c032974-302f-41a3-845c-a5f2aa825c39" width="60%" />

---

### Step 11: DHCP Server Configuration
<img width="718" height="621" alt="45" src="https://github.com/user-attachments/assets/4427caea-7f4b-4979-9b38-fd3938e57cf5" width="60%" />
<br/><br/>
Configure DHCP to automatically assign IP addresses to domain clients.

- Install **DHCP Server** role
- Authorize DHCP in Active Directory
- Create an IPv4 scope
- Define IP range, subnet mask, exclusions, and lease duration
<br/>
<img width="712" height="632" alt="44" src="https://github.com/user-attachments/assets/ca613825-f2ab-44d2-88f8-48d7c105a289" width="60%" />
<br/><br/>
<img width="1017" height="693" alt="43" src="https://github.com/user-attachments/assets/a33facfa-68d5-4914-a7a7-c5d6d3243ff7" width="40%" />
<br/><br/>

---

### Step 12: Router (Default Gateway) Configuration

Configure **DHCP Option 003 – Router**.

- Specify the router or virtual gateway IP
- Ensures clients can reach external networks
<img width="710" height="625" alt="42" src="https://github.com/user-attachments/assets/e8036fb1-4ce8-4eb5-b957-7e114cc3f993" width="40%" />
<br/><br/>
<img width="888" height="625" alt="41" src="https://github.com/user-attachments/assets/36f74508-31fb-458a-84c4-7920628bb070" width="40%" />
<br/><br/>
<img width="1018" height="681" alt="40" src="https://github.com/user-attachments/assets/82f30dc5-1947-40bd-b7a4-c2f38699ad10" width="40%" />
<br/><br/>
<img width="1012" height="693" alt="39" src="https://github.com/user-attachments/assets/67968193-9b7b-4c2d-a136-2f8e4775c346" width="40%" />
<br/><br/>
<img width="1021" height="710" alt="38" src="https://github.com/user-attachments/assets/5488c742-f3b2-43f6-9058-b3b4c991a535" width="40%" />

---

### Step 13: WINS Server Configuration (Optional)

Install **WINS Server** for legacy NetBIOS support.

- Configure WINS role
- Set DHCP Options 044 and 046
- Used only for legacy compatibility
<br/><br/>
<img width="1018" height="708" alt="37" src="https://github.com/user-attachments/assets/71758bda-958f-4e91-b5e7-7305b2efbbc7" width="40%" />
<br/><br/>
<img width="853" height="376" alt="Screenshot 2026-01-07 030504" src="https://github.com/user-attachments/assets/0976b3f8-eabc-4623-80a0-42d58bc9c04c" width="40%" />
<br/><br/>




---

## Lab Completion Summary

The Active Directory lab environment is fully operational and includes:
