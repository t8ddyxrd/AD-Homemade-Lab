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
  ![Static IP]<img width="1023" height="733" alt="Screenshot_20250815_095425" src="https://github.com/user-attachments/assets/6f12a8e4-2d2a-4e79-b719-4929721260ef" />

- 🏷️ **IP Address:** `192.168.23.10`  
- 📏 **Subnet Mask:** `255.255.255.0`  
- 🌐 **Preferred DNS:** `127.0.0.1`
  
## 2️⃣ Alternate NIC Settings 
![Alternate NIC]<img width="1022" height="731" alt="Screenshot_20250815_095526" src="https://github.com/user-attachments/assets/159e0eb1-3b54-4840-81af-107964a8a459" />

## 3️⃣ Network Interfaces Overview
![Network Interfaces]<img width="1013" height="646" alt="Screenshot_20250815_095750" src="https://github.com/user-attachments/assets/c82707d4-b2a1-4f3b-bcef-285492d13d08" />
Verified **Host-Only** + **NAT** adapters for flexibility.


## 4️⃣ ipconfig Check
![ipconfig]<img width="995" height="712" alt="Screenshot_20250815_095933" src="https://github.com/user-attachments/assets/864db6c6-28be-4d73-89e8-cc86addc531d" />
🛠️ Confirmed:
- Static IP  
- Loopback DNS  
- NetBIOS over TCP/IP enabled

## 5️⃣ Installing AD DS, DNS, DHCP
![Roles Install] <img width="1011" height="767" alt="Screenshot_20250815_100348" src="https://github.com/user-attachments/assets/b5972201-80e5-489a-89a0-5f6fbe8007fd" />
📦 Installed:
- 🗂️ Active Directory Domain Services
- 🌐 DNS Server
- 📡 DHCP Server

## 6️⃣ Domain Controller Options
![DC Options]<img width="1025" height="763" alt="Screenshot_20250815_102320" src="https://github.com/user-attachments/assets/4a5fc68d-9d3d-416c-bd56-3a4aaa175f4e" />

- 🏛️ Forest Level: **Windows Server 2016**  
- 🏛️ Domain Level: **Windows Server 2016**  
- 📌 Enabled **Global Catalog** & **DNS**  
- 🔑 Set **DSRM** password

  ## 7️⃣ Review Domain Setup
![Review Domain] <img width="1025" height="772" alt="Screenshot_20250815_102618" src="https://github.com/user-attachments/assets/9f7bbf1a-158b-4b0c-99a1-8397d5eb2162" />
📜 Verified:
- Domain: `test.local`  
- NetBIOS: `TEST`

  ## 8️⃣ Routing Role
![Routing]<img width="893" height="673" alt="Screenshot_20250815_113329" src="https://github.com/user-attachments/assets/2b8b21ba-fceb-4134-bc9f-ef7027ead469" />
⚙️ Enabled **Routing & Remote Access** for NAT/LAN.

## 9️⃣ DNS Lookup Test
![nslookup] <img width="997" height="741" alt="Screenshot_20250815_115044" src="https://github.com/user-attachments/assets/8e2b7c71-8de0-48f1-9b63-52a184939ae5" />
```powershell
nslookup t8ddy.com




