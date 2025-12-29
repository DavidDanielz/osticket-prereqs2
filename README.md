<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1 align="center">osTicket – Prerequisites & Installation</h1>

<p align="center">
  <b>End-to-end deployment of the osTicket help desk system on Microsoft Azure</b><br/>
  Windows VM • IIS • Remote Desktop
</p>
<div align="center">
  
  ![Azure](https://img.shields.io/badge/Microsoft_Azure-0089D6?style=for-the-badge&logo=microsoft-azure&logoColor=white)
  ![IIS](https://img.shields.io/badge/IIS-5E5E5E?style=for-the-badge)
  ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)
  ![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)
  ![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)
  ![PowerShell](https://img.shields.io/badge/PowerShell-5391FE?style=for-the-badge&logo=powershell&logoColor=white)

</div>

<hr/>

## 📌 Overview

This tutorial walks through the **prerequisites, configuration, and installation** of the open-source help desk ticketing system **osTicket** within a Microsoft Azure virtual machine environment.  
It is designed as a **portfolio-ready project** demonstrating foundational IT support and system administration skills.

---

## 🧰 Environments & Technologies Used

- **Microsoft Azure** (Virtual Machines / Compute)
- **Remote Desktop Protocol (RDP)**
- **Internet Information Services (IIS)**

---

## 💻 Operating System

- **Windows 10 Pro** (21H2)

---

## 📋 Prerequisites

Before beginning the installation, ensure the following are in place:

- Azure Virtual Machine (Windows-based)
- Administrator access to the VM
- Remote Desktop enabled
- IIS installed and configured
- Required osTicket dependencies available

---

## ⚙️ Installation Steps

### Step 1: Create an Azure Virtual Machine Windows 10, 4 vCPUs

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Environment Preparation"/>
</p>

<p>
Confirm that the virtual machine is running, Remote Desktop access is functional, and IIS is installed.
This establishes the foundation required for hosting the osTicket web application.
</p>

<br/>

---

### Step 2: Log into the VM with Remote Desktop

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Installing Dependencies"/>
</p>

<p>
Install and configure the necessary services and dependencies required for osTicket to function properly
within the IIS environment.
</p>

<br/>

---

### Step 3: Within the VM (osticket-vm), download the osTicket-Installation-Files.zip and unzip it onto your desktop.

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="osTicket Installation"/>
</p>

<p>
Deploy the osTicket files, configure permissions, and complete the browser-based setup to finalize
the installation.
</p>

---

### Step 4: Install / Enable IIS in Windows WITH CGI

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Environment Preparation"/>
</p>

<p>
Confirm that the virtual machine is running, Remote Desktop access is functional, and IIS is installed.
This establishes the foundation required for hosting the osTicket web application.
</p>

<br/>

---

### Step 5: From the “osTicket-Installation-Files” folder, install PHP Manager for IIS 

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Installing Dependencies"/>
</p>

<p>
Install and configure the necessary services and dependencies required for osTicket to function properly
within the IIS environment.
</p>

<br/>

---

### Step 6: From the “osTicket-Installation-Files” folder install the Rewrite Module 

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="osTicket Installation"/>
</p>

<p>
Deploy the osTicket files, configure permissions, and complete the browser-based setup to finalize
the installation.
</p>

---

### Step 7: Create the directory C:\PHP

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Environment Preparation"/>
</p>

<p>
Confirm that the virtual machine is running, Remote Desktop access is functional, and IIS is installed.
This establishes the foundation required for hosting the osTicket web application.
</p>

<br/>

---

### Step 8: From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Installing Dependencies"/>
</p>

<p>
Install and configure the necessary services and dependencies required for osTicket to function properly
within the IIS environment.
</p>

<br/>

---

### Step 9: From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="osTicket Installation"/>
</p>

<p>
Deploy the osTicket files, configure permissions, and complete the browser-based setup to finalize
the installation.
</p>

---

### Step 10: From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Environment Preparation"/>
</p>

<p>
Confirm that the virtual machine is running, Remote Desktop access is functional, and IIS is installed.
This establishes the foundation required for hosting the osTicket web application.
</p>

<br/>

---

### Step 11: Open IIS as an Admin

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Installing Dependencies"/>
</p>

<p>
Install and configure the necessary services and dependencies required for osTicket to function properly
within the IIS environment.
</p>

<br/>

---

### Step 12: Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="osTicket Installation"/>
</p>

<p>
Deploy the osTicket files, configure permissions, and complete the browser-based setup to finalize
the installation.
</p>

---

### Step 13: Reload IIS (Open IIS, Stop and Start the server)

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Environment Preparation"/>
</p>

<p>
Confirm that the virtual machine is running, Remote Desktop access is functional, and IIS is installed.
This establishes the foundation required for hosting the osTicket web application.
</p>

<br/>

---

### Step 14: Install osTicket v1.15.8

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Installing Dependencies"/>
</p>

<p>
Install and configure the necessary services and dependencies required for osTicket to function properly
within the IIS environment.
</p>

<br/>

---

### Step 15: Reload IIS (Open IIS, Stop and Start the server)

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="osTicket Installation"/>
</p>

<p>
Deploy the osTicket files, configure permissions, and complete the browser-based setup to finalize
the installation.
</p>

---

### Step 16: Go to sites -> Default -> osTicket

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Environment Preparation"/>
</p>

<p>
Confirm that the virtual machine is running, Remote Desktop access is functional, and IIS is installed.
This establishes the foundation required for hosting the osTicket web application.
</p>

<br/>

---

### Step 17: Note that some extensions are not enabled

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Installing Dependencies"/>
</p>

<p>
Install and configure the necessary services and dependencies required for osTicket to function properly
within the IIS environment.
</p>

<br/>

---

### Step 18: Rename: ost-config.php

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="osTicket Installation"/>
</p>

<p>
Deploy the osTicket files, configure permissions, and complete the browser-based setup to finalize
the installation.
</p>

---

### Step 19: Assign Permissions: ost-config.php

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Environment Preparation"/>
</p>

<p>
Confirm that the virtual machine is running, Remote Desktop access is functional, and IIS is installed.
This establishes the foundation required for hosting the osTicket web application.
</p>

<br/>

---

### Step 20: Continue Setting up osTicket in the browser (click Continue)

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Installing Dependencies"/>
</p>

<p>
Install and configure the necessary services and dependencies required for osTicket to function properly
within the IIS environment.
</p>

<br/>

---

### Step 21: From the “osTicket-Installation-Files” folder, install HeidiSQL.

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="osTicket Installation"/>
</p>

<p>
Deploy the osTicket files, configure permissions, and complete the browser-based setup to finalize
the installation.
</p>

---

### Step 22: Continue Setting up osTicket in the browser

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Environment Preparation"/>
</p>

<p>
Confirm that the virtual machine is running, Remote Desktop access is functional, and IIS is installed.
This establishes the foundation required for hosting the osTicket web application.
</p>

<br/>

---

### Step 23: Congratulations, hopefully it is installed with no errors!

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Installing Dependencies"/>
</p>

<p>
Install and configure the necessary services and dependencies required for osTicket to function properly
within the IIS environment.
</p>

<br/>

---

### Step 24: End Users osTicket URL:

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="osTicket Installation"/>
</p>

<p>
Deploy the osTicket files, configure permissions, and complete the browser-based setup to finalize
the installation.
</p>

---

### Step 25: Prepare the Environment

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Environment Preparation"/>
</p>

<p>
Confirm that the virtual machine is running, Remote Desktop access is functional, and IIS is installed.
This establishes the foundation required for hosting the osTicket web application.
</p>

<br/>

---

### Step 26: Install Required Components

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Installing Dependencies"/>
</p>

<p>
Install and configure the necessary services and dependencies required for osTicket to function properly
within the IIS environment.
</p>

<br/>

---

### Step 27: Deploy osTicket

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="osTicket Installation"/>
</p>

<p>
Deploy the osTicket files, configure permissions, and complete the browser-based setup to finalize
the installation.
</p>

---

### Step 28: Prepare the Environment

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Environment Preparation"/>
</p>

<p>
Confirm that the virtual machine is running, Remote Desktop access is functional, and IIS is installed.
This establishes the foundation required for hosting the osTicket web application.
</p>

<br/>

---

### Step 29: Install Required Components

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="Installing Dependencies"/>
</p>

<p>
Install and configure the necessary services and dependencies required for osTicket to function properly
within the IIS environment.
</p>

<br/>

---

### Step 30: Deploy osTicket

<p align="center">
  <img src="https://i.imgur.com/DJmEXEB.png" width="80%" alt="osTicket Installation"/>
</p>

<p>
Deploy the osTicket files, configure permissions, and complete the browser-based setup to finalize
the installation.
</p>

---

<hr/>

## ✅ Outcome

By the end of this project, you will have:

- A fully functional **osTicket help desk**
- Hands-on experience with **Azure VMs**
- Practical exposure to **IIS configuration**
- A strong **Help Desk / IT Support portfolio project**

---

<p align="center">
  <i>Project created for hands-on learning and professional portfolio development</i>
</p>
