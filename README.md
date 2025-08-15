# 🖥️ Windows Server 2019 – Active Directory, DNS & Network Configuration Lab 🚀

This project showcases the **deployment and configuration** of a Windows Server 2019 environment with:

- 🗂️ **Active Directory Domain Services (AD DS)**
- 🌐 **DNS Server**
- 📡 **Static IP Configuration**
- 🔄 **Routing & Remote Access**
- 👥 **User & Group Management**
- 🔐 **Security Policies**
- 📁 **File Sharing**
- 🛡️ **Auditing & Logging**

📸 All steps include **real screenshots** to demonstrate configuration and results.
Note: Some names and IP addresses may differ between screenshots or configurations because multiple virtual machines were used during testing.

## 1️⃣ Static IP Address Configuration
  <img width="1023" height="733" alt="Screenshot_20250815_095425" src="https://github.com/user-attachments/assets/6f12a8e4-2d2a-4e79-b719-4929721260ef" />

- 🏷️ **IP Address:** `192.168.23.10`  
- 📏 **Subnet Mask:** `255.255.255.0`  
- 🌐 **Preferred DNS:** `127.0.0.1`
  
## 2️⃣ Alternate NIC Settings 
<img width="1022" height="731" alt="Screenshot_20250815_095526" src="https://github.com/user-attachments/assets/159e0eb1-3b54-4840-81af-107964a8a459" />

## 3️⃣ Network Interfaces Overview
<img width="1013" height="646" alt="Screenshot_20250815_095750" src="https://github.com/user-attachments/assets/c82707d4-b2a1-4f3b-bcef-285492d13d08" />
Verified **Host-Only** + **NAT** adapters for flexibility.


## 4️⃣ ipconfig Check
<img width="995" height="712" alt="Screenshot_20250815_095933" src="https://github.com/user-attachments/assets/864db6c6-28be-4d73-89e8-cc86addc531d" />
🛠️ Confirmed:
- Static IP  
- Loopback DNS  
- NetBIOS over TCP/IP enabled

## 5️⃣ Installing AD DS, DNS, DHCP
 <img width="1011" height="767" alt="Screenshot_20250815_100348" src="https://github.com/user-attachments/assets/b5972201-80e5-489a-89a0-5f6fbe8007fd" />
📦 Installed:
- 🗂️ Active Directory Domain Services
- 🌐 DNS Server
- 📡 DHCP Server

## 6️⃣ Domain Controller Options
<img width="1025" height="763" alt="Screenshot_20250815_102320" src="https://github.com/user-attachments/assets/4a5fc68d-9d3d-416c-bd56-3a4aaa175f4e" />

- 🏛️ Forest Level: **Windows Server 2016**  
- 🏛️ Domain Level: **Windows Server 2016**  
- 📌 Enabled **Global Catalog** & **DNS**  
- 🔑 Set **DSRM** password

  ## 7️⃣ Review Domain Setup
 <img width="1025" height="772" alt="Screenshot_20250815_102618" src="https://github.com/user-attachments/assets/9f7bbf1a-158b-4b0c-99a1-8397d5eb2162" />
📜 Verified:
- Domain: `test.local`  
- NetBIOS: `TEST`

  ## 8️⃣ Routing Role
<img width="893" height="673" alt="Screenshot_20250815_113329" src="https://github.com/user-attachments/assets/2b8b21ba-fceb-4134-bc9f-ef7027ead469" />
⚙️ Enabled **Routing & Remote Access** for NAT/LAN.

## 9️⃣ DNS Lookup Test
 <img width="997" height="741" alt="Screenshot_20250815_115044" src="https://github.com/user-attachments/assets/8e2b7c71-8de0-48f1-9b63-52a184939ae5" />
```powershell


```

# 1️⃣0️⃣ Reverse DNS Lookup Test



## 🔟 Create Global Security Group for HR


![Create HR Group] <img width="1005" height="726" alt="Screenshot_20250815_115858" src="https://github.com/user-attachments/assets/22d2de1d-6d2b-45de-a522-d7eb494379da" />





📜 Configured:


- **Group Name:** `GG_HR`


- **Location:** `t8ddy.com/HR` OU


- **Group Scope:** Global


- **Group Type:** Security


- **Purpose:** Manage access rights for HR resources centrally





## 1️⃣1️⃣ Create New User in IT OU


![Create IT User] <img width="1005" height="726" alt="Screenshot_20250815_120031" src="https://github.com/user-attachments/assets/a84aace4-b6e3-4a0a-af43-50c60423591b" />





📜 Configured:


- **First Name:** Alex


- **Last Name:** T


- **Full Name:** Alex T


- **User Logon Name:** alext@t8ddy.com


- **Pre-Windows 2000 Logon Name:** T8DDY\alext


- **Location:** `t8ddy.com/IT` OU


- **Purpose:** Create a domain user account for IT department access





## 1️⃣2️⃣ Create Global Security Group for IT


![Create IT Group] <img width="1005" height="726" alt="Screenshot_20250815_121458" src="https://github.com/user-attachments/assets/4fb4da4d-41d7-4a2e-b8c1-46bcac37e691" />





📜 Configured:


- **Group Name:** `GG_IT`


- **Location:** `t8ddy.com/IT` OU


- **Group Scope:** Global


- **Group Type:** Security


- **Purpose:** Manage access rights for IT department resources centrally





## 1️⃣3️⃣ Create New GPO for Corporate Login Banner


![Create Corp Login Banner GPO] <img width="1005" height="726" alt="Screenshot_20250815_121114" src="https://github.com/user-attachments/assets/43d7035b-f03f-466a-a047-c80a8d512e6a" />





📜 Configured:


- **GPO Name:** `Corp-Login Banner`


- **Location:** Starter GPOs in `t8ddy.com` domain


- **Source Starter GPO:** None


- **Purpose:** Enforce a corporate login banner across domain-joined systems





## 1️⃣4️⃣ Configure Security Account Lockout and Password Policies via GPO


![Create Security Account Lockout GPO] <img width="956" height="755" alt="Screenshot_20250815_121941" src="https://github.com/user-attachments/assets/225e3d54-2bec-43ad-9be5-e1af4a872688" />


![Set Account Lockout Duration] <img width="956" height="755" alt="Screenshot_20250815_122247" src="https://github.com/user-attachments/assets/9ae818bf-b9d3-4ada-8dbb-177e885125c1" />


![Account Lockout Policy Overview] <img width="956" height="755" alt="Screenshot_20250815_122316" src="https://github.com/user-attachments/assets/aeabf88f-ba04-4c3e-9414-366e011f740d" />


![Password Policy Settings]<img width="956" height="755" alt="Screenshot_20250815_122408" src="https://github.com/user-attachments/assets/2d6b2f69-a7a0-48dd-8d19-26f0e90e902e" />








📜 Configured:


- **GPO Name:** `Security-Account Lockout`


- **Location:** Group Policy Objects in `t8ddy.com` domain


- **Account Lockout Duration:** 30 minutes  


- **Account Lockout Threshold:** 5 invalid logon attempts  


- **Allow Administrator Account Lockout:** Enabled  


- **Reset Lockout Counter After:** 30 minutes  


- **Password Complexity:** Enabled  


- **Minimum Password Length:** 12 characters  


- **Minimum/Maximum Password Age:** 29 / 30 days  


- **Password History:** 0 remembered  


- **Store Passwords Using Reversible Encryption:** Disabled


- **Purpose:** Protect domain accounts by enforcing strong lockout and password policies





## 1️⃣5️⃣ Configure Security Audit for Logon Events via GPO


![Create Security Audit Logon Events GPO] <img width="956" height="755" alt="Screenshot_20250815_122705" src="https://github.com/user-attachments/assets/efdb0efb-1b14-4814-8e2f-0737edf76328" />


![Audit Policy Settings] <img width="956" height="755" alt="Screenshot_20250815_122846" src="https://github.com/user-attachments/assets/6a5f8fc9-f621-40df-ba63-d83523d2d246" />





📜 Configured:


- **GPO Name:** `Security-Audit Logon Events`


- **Location:** Group Policy Objects in `t8ddy.com` domain


- **Audit Account Logon Events:** Success, Failure  


- **Audit Account Management:** Success, Failure  


- **Audit Directory Service Access:** Success, Failure  


- **Audit Logon Events:** Success, Failure  


- **Audit Object Access:** Success, Failure  


- **Audit Policy Change:** Not Defined  


- **Audit Privilege Use:** No Auditing  


- **Audit Process Tracking:** Failure  


- **Audit System Events:** Success, Failure  


- **Purpose:** Enable auditing for key account and logon activities to monitor and investigate security-related events





## 1️⃣6️⃣ Configure Drive Mapping for Department Shares via GPO


![Create Drive Mapping GPO] <img width="956" height="755" alt="Screenshot_20250815_122940" src="https://github.com/user-attachments/assets/30b983ef-a2aa-44ef-b783-e8d658129276" />


![Drive Mapping Properties - HR Share]<img width="956" height="755" alt="Screenshot_20250815_123054" src="https://github.com/user-attachments/assets/55b98128-2f0c-44f0-871a-a629a7d74176" />


![Security Group Targeting - GG_HR] <img width="956" height="755" alt="Screenshot_20250815_123135" src="https://github.com/user-attachments/assets/da404576-c444-483c-886e-dce5a837cb0d" />


![Drive Maps Overview] <img width="956" height="755" alt="Screenshot_20250815_123152" src="https://github.com/user-attachments/assets/40853e22-1671-4641-bb3b-aad84dd6b604" />





📜 Configured:


- **GPO Name:** `Drive Mapping-Department Shares`


- **Location:** Group Policy Objects in `t8ddy.com` domain


- **Drive Mapping Path:** `\\<DC-HOSTNAME>\HR$`


- **Label:** HR Shared Folder


- **Drive Letter:** H:


- **Reconnect:** Disabled


- **Action:** Update


- **Security Group Targeting:** Only applies if user is a member of `GG_HR`


- **Purpose:** Automatically map HR department shared drive to users in the HR group


- **Purpose:** Automatically map HR department shared drive to users in the HR group
## 1️⃣7️⃣ Configure Local Administrator Group Membership via GPO



![Create Local Admin Control GPO] <img width="956" height="755" alt="Screenshot_20250815_123213" src="https://github.com/user-attachments/assets/72ac4103-e0ac-4fc1-b8a0-484b5cf6f811" />


![Administrators Group Properties] <img width="956" height="755" alt="Screenshot_20250815_123309" src="https://github.com/user-attachments/assets/4a8e941d-e3da-4baf-aec1-35a0b87a8ece" />





- **GPO Name:** `Security-Local Admin Control`


- **Location:** Group Policy Objects in `t8ddy.com` domain


- **Configured Group:** Local Administrators


- **Members Added:**  


  - Domain Admins  


  - GG_IT (IT Security Group)





## 1️⃣8️⃣ Add DNS A Record for Intranet


![Add Intranet DNS Record] <img width="956" height="755" alt="Screenshot_20250815_123454" src="https://github.com/user-attachments/assets/6cb784d4-a813-4438-b263-b05f56a4c8ce" />





📜 Configured:


- **Record Type:** A (Host)


- **Host Name:** intranet


- **FQDN:** intranet.t8ddy.com


- **IP Address:** 172.17.1.2.3


- **PTR Record Creation:** Disabled


- **Authenticated Update:** Disabled


- **Purpose:** Create an internal DNS entry to resolve `intranet.t8ddy.com` to the specified internal IP





## 🏆 Credits


- **Configuration & Implementation:** t8ddy


- **Environment:** Windows Server 2019 Standard Evaluation  


- **Domain:** t8ddy.com
