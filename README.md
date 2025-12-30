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
<div style="display: flex; justify-content: space-around; align-items: center;">
  <img src="step4-iis1.png" width="45%" alt="IIS Windows Features"/>
  <img src="step4-iis2.png" width="45%" alt="CGI Enabled"/>
</div>

<p>
Enable IIS through Windows Features and ensure CGI support is selected.
</p>

---

### **Step 5: Install IIS Dependencies**
<div style="display: flex; justify-content: space-around; align-items: center;">
  <img src="step5-dependencies1.png" width="45%" alt="PHP Manager"/>
  <img src="step5-dependencies2.png" width="45%" alt="IIS URL Rewrite Module"/>
</div>

<p>
Install PHP Manager for IIS and the IIS URL Rewrite Module.
</p>

---

### **Step 6: Install PHP Runtime**
<p>
  <img src="step6-php.png" width="80%" alt="PHP Install"/>
</p>
Create `C:\PHP`, extract PHP 7.3.8, and install the Visual C++ Redistributable.

---

### **Step 7: Install Microsoft Visual C++ Redistributable**
<p>
  <img src="step6-php.png" width="80%" alt="PHP Install"/>
</p>
Install the **Microsoft Visual C++ Redistributable** to satisfy runtime dependencies required by PHP and MySQL. This ensures that the osTicket application and its supporting services function correctly on Windows.

---

### **Step 8: Install MySQL Server**
<p>
  <img src="step7-mysql.png" width="80%" alt="MySQL Install"/>
</p>
Install MySQL Server to support osTicket’s backend database.

---

### **Step 9: Register PHP in IIS**

<p align="center">
  <img src="step8-iis-manager.png" width="80%" alt="IIS Manager with PHP Manager Highlighted"/>
</p>
<p align="center">
  <img src="step8-register-php.png" width="80%" alt="Register PHP Version in PHP Manager"/>
</p>

Use PHP Manager to register <code>php-cgi.exe</code> with IIS and restart the web server. The first screenshot shows PHP Manager inside IIS, and the second shows the registration of the PHP executable.

---

### **Step 10: Deploy osTicket Application Files**

This step demonstrates moving the osTicket installation files into IIS’s web root and preparing the application for the browser-based installer.

<p align="center">
  <img src="52. Taking (upload) folder and adding it to the wwwroot folder.png" width="80%" alt="Initial Folder Setup"/>
</p>

**Step 10a – Initial Folder Structure:**  
Shows the extracted `osTicket-v1.15.8` folder containing `upload` and `scripts`, and the `wwwroot` folder with only the default `iisstart` file.

<p align="center">
  <img src="53. upload in wwwroot.png" width="80%" alt="Moving Upload Folder"/>
</p>

**Step 10b – Moving Upload Folder:**  
Copy or move the `upload` folder from `osTicket-v1.15.8` into the `C:\inetpub\wwwroot` directory.

<p align="center">
  <img src="54. Change upload name to osTicket.png" width="80%" alt="Renamed Upload Folder"/>
</p>

**Step 10c – Final Deployment:**  
Rename the `upload` folder to `osTicket` inside `wwwroot`. This completes the deployment of the application files, making it ready to access via the web installer.

---

### **Step 11: Launch osTicket Web Installer**
<p>
  <img src="58. osTicket installer Prerequisites with missing some extensions.png" width="80%" alt="Installer"/>
</p>
Access the osTicket installer through the browser and verify system readiness.

---

### **Step 12: Configure PHP Extensions**
<p>
  <img src="63. Refresh osTicket installer page and extensions are added. .png" width="80%" alt="PHP Extensions"/>
</p>
Enable required PHP extensions and reload IIS as needed.

---

### **Step 13: Configure osTicket Settings**
<p>
  <img src="69. Advanced Security settings for ost-config.php.png" width="80%" alt="Config File"/>
</p>
Rename `ost-sampleconfig.php` to `ost-config.php` and assign temporary write permissions.

---

### **Step 13a: osTicket Installer Database Requirement**
<p>
  <img src="76. osTicket system_admin user_database settings basic installation setup.png" width="80%" alt="Installer Missing Database Info"/>
</p>
Before you can proceed with osTicket installation, the web installer requires database details.  
This includes:

- MySQL Hostname  
- MySQL Database  
- MySQL Username  
- MySQL Password  
- Table Prefix (optional)  

This screenshot highlights that the installer cannot continue until a database and user are created.

---

### **Step 14: Create Database with HeidiSQL**
<p>
  <img src="87. Refresh osTicket in HeidiSQL and see that it's not emoty anymore.png" width="80%" alt="Database Setup"/>
</p>
Use HeidiSQL to create the osTicket database and database user.

---

### **Step 15: Complete Browser-Based Installation**
<p>
  <img src="90. osTicket installed.png" width="80%" alt="Install Complete"/>
</p>
Finish the installer and confirm osTicket installs successfully without errors.

---

### **Step 16: Verify End-User Portal**
<p>
  <img src="91. Support center_Support ticket system .png" width="80%" alt="End User Portal"/>
</p>
Confirm the osTicket end-user portal loads and is ready to accept support tickets.

---

<hr/>

## ✅ Outcome

This project resulted in a fully operational osTicket help desk deployed on Azure, demonstrating hands-on experience with virtual machines, IIS, PHP, MySQL, and real-world help desk system installation.
