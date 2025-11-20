# Standard Operating Procedure (SOP)
## *Setup of a Virtual Linux Server for Web Application Testing*

**MITT** 

*130 Henlow Bay*  

*+1 123 456 7890*

---

**Approved Table:**
| Name | Title | Date |
|:---|:---:|---:|
| Jaered Bacolod | CEO | 11/19/2025 |
| Jane Doe | Executive Officer | 11/19/2025 |

---

**Purpose:**
</p> I made this SOP to explain how to set up a virtual Linux server for testing web applications. This helps everyone follow the same steps and avoid mistakes.

---

**SCOPE**
</p> This document is for IT staff, students, devs who will need a test server.
</p> This can help:

* Create a Linux Server  
* Install software
* Prepares the server for the app testing

---

**Accountability Matrix**

| Role | Tasks | Contact at | 
|:---|:---:|:---:|
| System Admin | Create the server | sysadmins@mitt.ca |
| Devs | Create the web apps | devs@mitt.ca |
| Students | test the web app functionality | students@mitt.ca |
| IT | Quality Assurance | IT@mitt.ca |

---

**Definitions**
* LAMP
  * Linux, Apache, MariaDB, PHP.
* VM
  * Virtual Machine
* Package Manager
  * Software Installer
 
---

# **Steps:**
</p>

**STEP 1:** *The Creation of the VM*
* Open VMware or any other virtualization software
* Create the VM needed
  * **CPU:** 2 Cores, **RAM:** 4 GB, **Storage:** 30 GB
  * Install **Ubuntu Server 22.04 LTS**
* Set the hostname to **WEB_TESTING** or Any Proper Identifier

**STEP 2:** *Network Setup*
* Use NAT or Bridged mode
* Set Static IP to subnet **192.168.100.0/24**
* Lastly, update the */etc/hosts* to match the hostname and IP

**STEP 3:** *System Update*
* Run:
  * > **>sudo apt update && sudo apt upgrade -y**

**STEP 4:** *Software Installation*
* Run the commands
* To Install Apache:
  * > **>sudo apt install apache2 -y**
* To Install MariaDB:
  * > **>sudo apt install mariadb-server -y**
* To Install PHP:
  * > **>sudo apt install php php-mysql php-cli -y**

**STEP 5:** *Web app test*
* Check the Apache:
  * > **>systemctl status apache2**






















  
  
