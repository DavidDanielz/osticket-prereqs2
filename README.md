<p align="center">
  <img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1 align="center">osTicket – Prerequisites & Installation</h1>

<p align="center">
  <b>End-to-end deployment of the osTicket help desk system on Microsoft Azure</b><br/>
  Windows Virtual Machine • IIS • PHP • MySQL
</p>

<div align="center">
  
  ![Azure](https://img.shields.io/badge/Microsoft_Azure-0089D6?style=for-the-badge&logo=microsoft-azure&logoColor=white)
  ![Windows](https://img.shields.io/badge/Windows-0078D6?style=for-the-badge&logo=windows&logoColor=white)
  ![IIS](https://img.shields.io/badge/IIS-5E5E5E?style=for-the-badge)
  ![PHP](https://img.shields.io/badge/PHP-777BB4?style=for-the-badge&logo=php&logoColor=white)
  ![MySQL](https://img.shields.io/badge/MySQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)

</div>

---

## 📌 Overview

This project demonstrates the **full technical installation and configuration** of **osTicket**, an open-source help desk ticketing system, deployed on a **Microsoft Azure-hosted Windows virtual machine**.

The walkthrough reflects real-world IT support responsibilities, including server provisioning, dependency installation, web server configuration, database setup, and application deployment.

---

## 🖥️ Environment & Technologies

- Microsoft Azure (Virtual Machines)
- Windows 11 Pro
- Internet Information Services (IIS) with CGI
- PHP 7.3.8
- MySQL 5.5
- Remote Desktop Protocol (RDP)
- HeidiSQL

---

## ⚙️ Installation & Configuration (15 Steps)

---

### **Step 1: Provision Azure Virtual Machine**
<p>
  <img src="step1-vm.png" width="80%" alt="Azure VM Creation"/>
</p>
Create a Windows 11 virtual machine in Azure and verify successful Remote Desktop access.

---

### **Step 2: Connect via Remote Desktop**
<p>
  <img src="step2-rdp.png" width="80%" alt="RDP Login"/>
</p>
Log into the VM using administrator credentials to begin configuration.

---

### **Step 3: Download osTicket Installation Files**
<p>
  <img src="step3-files.png" width="80%" alt="Download Files"/>
</p>
Download and extract the osTicket installation package within the Azure VM.

---

### **Step 4: Install IIS with CGI Enabled**
<p>
  <img src="step4-iis.png" width="80%" alt="IIS CGI"/>
</p>
Enable IIS through Windows Features and ensure CGI support is selected.

---

### **Step 5: Install IIS Dependencies**
<p>
  <img src="step5-dependencies.png" width="80%" alt="PHP Manager and Rewrite"/>
</p>
Install PHP Manager for IIS and the IIS URL Rewrite Module.

---

### **Step 6: Install PHP Runtime**
<p>
  <img src="step6-php.png" width="80%" alt="PHP Install"/>
</p>
Create `C:\PHP`, extract PHP 7.3.8, and install the Visual C++ Redistributable.

---

### **Step 7: Install MySQL Server**
<p>
  <img src="step7-mysql.png" width="80%" alt="MySQL Install"/>
</p>
Install MySQL Server to support osTicket’s backend database.

---

### **Step 8: Register PHP in IIS**
<p>
  <img src="step8-register-php.png" width="80%" alt="Register PHP"/>
</p>
Use PHP Manager to register `php-cgi.exe` with IIS and restart IIS.

---

### **Step 9: Deploy osTicket Application Files**
<p>
  <img src="step9-osticket-files.png" width="80%" alt="osTicket Files"/>
</p>
Copy osTicket files into `C:\inetpub\wwwroot\osTicket`.

---

### **Step 10: Launch osTicket Web Installer**
<p>
  <img src="step10-installer.png" width="80%" alt="Installer"/>
</p>
Access the osTicket installer through the browser and verify system readiness.

---

### **Step 11: Configure PHP Extensions**
<p>
  <img src="step11-extensions.png" width="80%" alt="PHP Extensions"/>
</p>
Enable required PHP extensions and reload IIS as needed.

---

### **Step 12: Configure osTicket Settings**
<p>
  <img src="step12-config.png" width="80%" alt="Config File"/>
</p>
Rename `ost-sampleconfig.php` to `ost-config.php` and assign temporary write permissions.

---

### **Step 13: Create Database with HeidiSQL**
<p>
  <img src="step13-database.png" width="80%" alt="Database Setup"/>
</p>
Use HeidiSQL to create the osTicket database and database user.

---

### **Step 14: Complete Browser-Based Installation**
<p>
  <img src="step14-complete.png" width="80%" alt="Install Complete"/>
</p>
Finish the installer and confirm osTicket installs successfully without errors.

---

### **Step 15: Verify End-User Portal**
<p>
  <img src="step15-end-user.png" width="80%" alt="End User Portal"/>
</p>
Confirm the osTicket end-user portal loads and is ready to accept support tickets.

---

<hr/>

## ✅ Outcome

This project resulted in a fully operational osTicket help desk deployed on Azure, demonstrating hands-on experience with virtual machines, IIS, PHP, MySQL, and real-world help desk system installation.
