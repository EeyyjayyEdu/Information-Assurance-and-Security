# INFORMATION ASSURANCE AND SECURITY - FINAL PROJECT DOCUMENTATION
by **Group 2 - BSCS 3B**
- Quiaño, Ydonna  Pearl B.
- Redulfin, Maria Yvette A.
- Relles, Adrian James
- Ruin, Joy Ann M.

## STEP BY STEP PROCEDURE

### 1. Install Headless Raspbian OS into Raspberry Pi

 - Raspberry Pi Imager is a quick and easy way to install Raspberry Pi OS and other operating systems to a microSD card, ready to use with your Raspberry Pi.
 Here is the link for the [Raspberry Pi Imager](https://www.raspberrypi.com/software/)
 ![Screenshot 2023-12-15 212836.png](https://github.com/EeyyjayyEdu/Information-Assurance-and-Security/blob/main/Relles/Screenshot%202023-12-15%20212836.png)

 - Open Raspberry Pi Imager. Choose Raspberry Pi Device, Operating System, and Storage.
 ![Screenshot 2023-12-15 213312.png](https://github.com/EeyyjayyEdu/Information-Assurance-and-Security/blob/main/Relles/Screenshot%202023-12-15%20213312.png)

 - In this project, we choose **_Raspberry Pi 3_** as device, **_Raspberry Pi OS (Legacy)_** as operating system, and our **_8GB SD Card_** as storage.

 - After choosing the preferred device, OS, and storage, click **Next**.

 - Click **Edit Settings** to customize the OS Settings.

 - In the OS Customization, set the host, username, and password as **preferred username**. Configure your wireless LAN available which is **your wifi ssid and password** and set the wireless LAN   country to **PH.** Lastly, set your timezone to **Asia/Shanghai** since they have the same timezone (GMT+8) as Manila, then click **Save**.
   
 - Don't forget to enable SSH and use password authentication, then click **Save**.

 - Click **Yes** to apply our customized settings.
   
 > [!WARNING]
 > Make sure to backup all existing data in the SD card to avoid deletion while formatting.

 - A warning will appear that all existing data on our SD card will be erased if we continue on our installation. Click **Yes** since our SD card has no existing files that need to be backed up.

 - OS writing on our SD card will then start

 - After writing, verification will start (just cancel it).
  
 - A write successful prompt will appear. In this part, it's now safe to eject our SD card from the PC.

> [!NOTE]
> Plug in the SD card first on Raspberry Pi before proceeding to the next step.

### 2. Connect to Raspberry Pi via SSH (Secure Socket Shell) then update the OS ###
 - In the command prompt, type SSH to access the network protocol. Then type the following command:
   - ssh username@hostname (e.g. eeyyjayy@raspberrypi)
   - sudo apt update
   - sudo apt upgrade

 ![1.png](https://github.com/EeyyjayyEdu/Information-Assurance-and-Security/blob/main/Relles/1.png)
 
 ![2.png](https://github.com/EeyyjayyEdu/Information-Assurance-and-Security/blob/main/Relles/2.png)

 ![3.png](https://github.com/EeyyjayyEdu/Information-Assurance-and-Security/blob/main/Relles/3.png)

### 3. Install LAMP Stack. LAMP stands for Linux, Apache, MySQL, and PHP. 
 - This stack is typically installed together in order to enable a server to host dynamic websites and web apps written in PHP.
Here are the tutorials on how to install LAMP stack [[1]](https://ostechnix.com/install-apache-mysql-php-lamp-stack-on-ubuntu-18-04-lts/)[[2]](https://linuxhint.com/install-phpmyadmin-raspberry-pi/)
 - To install the stack, type the following commands on our command prompt connected to Raspberry Pia via SSH.
   + **_sudo apt install apache2_**
     ![4.png](https://github.com/EeyyjayyEdu/Information-Assurance-and-Security/blob/main/Relles/4.png)
   + **_sudo apt install mariadb-server_**
     ![5.png](https://github.com/EeyyjayyEdu/Information-Assurance-and-Security/blob/main/Relles/5.png)
   + **_sudo mysql_secure_installation_**
     ![6.png](https://github.com/EeyyjayyEdu/Information-Assurance-and-Security/blob/main/Relles/6.png)
   + **_sudo apt install php libapache2-mod-php php-mysql_**
     ![7,png](https://github.com/EeyyjayyEdu/Information-Assurance-and-Security/blob/main/Relles/7.png)
   + **_sudo apt-get install php_**
     ![8.png](https://github.com/EeyyjayyEdu/Information-Assurance-and-Security/blob/main/Relles/8.png)
   + sudo apt install phpmyadmin
     ![9.png](https://github.com/EeyyjayyEdu/Information-Assurance-and-Security/blob/main/Relles/9.png)
   + apache2 then ok
     ![10.png](https://github.com/EeyyjayyEdu/Information-Assurance-and-Security/blob/main/Relles/10.png)
   + click no
     ![11.png](https://github.com/EeyyjayyEdu/Information-Assurance-and-Security/blob/main/Relles/11.png)

### 4. Connect to Raspberry Pi via VNC
 - Install RealVNC® Viewer to the device you want to control from via this [link](https://www.realvnc.com/en/connect/download/viewer/)
 
- On the device you will use to take control, run RealVNC Viewer and enter the private IP address in the search bar. If the screen of the Raspberry Pi appeared on RealVNC, it means that it already established connection and control on the Raspberry Pi.
   + click no
   ![12.png](https://github.com/EeyyjayyEdu/Information-Assurance-and-Security/blob/main/Relles/12.png)
