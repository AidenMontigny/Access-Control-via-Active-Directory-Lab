<h1> Active Control via Active Directory Lab </h1>

<h2>Description</h2>
The Access Control via Active Directory Lab focused on implementing and configuring Active Directory (AD) services in a hybrid network environment to enhance security and resource management. It involved setting up static IP addresses for Windows and Ubuntu VMs, promoting Windows Server 2019 to a domain controller, and integrating various systems into the domain. The lab emphasized the creation and management of user groups, computers, and policies, while addressing challenges such as virtual machine freezing and disk space errors. By leveraging AD for authentication and resource management, the project highlighted the importance of enforcing security policies, optimizing network performance, and successfully managing hybrid network infrastructures.
<br />

<h2>Languages and Utilities Used</h2>

- <b> pfSense </b>
- <b> PowerShell </b>
- <b> VirtualBox </b>
- <b> DNS & DHCP Services </b>
- <b> Nmap </b>

<h2>Environments Used </h2>

- <b> Windows 10 </b>
- <b> Ubuntu 20.04 </b>

<h2>Project walk-through:</h2>
<h3> Part 1 </h3>
<p align="left">
 The IP address of the Windows Server 10 was configured as a static IP address (192.168.1.10) to ensure stable network connectivity. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
The "ipconfig /all" command was executed to verify the new VM IP address configuration. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
The "Add Roles and Features" installation process was initiated to begin configuring the necessary roles and features on the Windows Server. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
The necessary roles and features, including Active Directory, DHCP Server, DNS Server, and others, were selected and are now ready to be installed on the server. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
The installation of the selected roles and features was completed successfully. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
The DHCP configuration has been successfully completed and committed. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
The server has been promoted to a domain controller, with the root domain name set to "Montigny.com." <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
The installation was completed successfully, and the machine is now required to reboot for the changes to take effect. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
The new domain, "Montigny.com," has been successfully created and configured. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
The pfSense firewall's DHCP functionality has been successfully disabled to avoid conflicts with the new DHCP server configuration. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
The new DHCP scope has been successfully implemented, allowing for proper IP address allocation within the designated range. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
The Server Option's 003 Router has been successfully linked to the 192.168.1.1 IP, ensuring proper routing and network communication within the configured range. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
The new IP range has been successfully set to 192.168.1.150, and the nslookup command was executed successfully, confirming the proper configuration and DNS resolution. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>

<h3> Part 2 </h3>
<p align="left">
The Windows 10 VM IP address has been successfully changed to a static IP: 192.168.1.11. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
The "ipconfig /all" command confirms the successful change of the IP address on the Windows 10 VM. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
The command demonstrates the creation of two new groups, "Training Computers" and "Training Department Users," within the Windows Server 2019 VM. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
This step involves creating a new computer object named "Station1" within the Windows Server 2019 VM. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
The Windows 10 VM was renamed to "Station1" to align with the newly created computer object in the Windows Server 2019 VM. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
DDuck was successfully added as a user to the Windows 10 VM, enabling access to resources as per the domain configurations. <br/><br/>
<p align="left">
The screenshot demonstrates the successful establishment of domain communication on the Windows 10 VM, confirming that it is properly joined to the domain and can interact with domain resources. <br/><br/>

<h3> Part 3 </h3>
<p align="left">
The command demonstrates the use of `sudo` followed by the successful download of the required extension on the system. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
The Ubuntu VM IP address was successfully changed to a static IP: 192.168.1.12. <br/><br/>
<p align="left">
The `ifconfig -a` command was executed, confirming that the IP change to the static IP was successful. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
The Windows Server 2019 VM successfully added a second computer, labeled as "Station 2." <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
The Ubuntu VM was renamed to "Station2" and successfully joined the Montigny.com domain. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
The Ubuntu VM was successfully connected to the domain, confirming proper domain integration. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
p align="left">
DDuck was successfully added as a user on the Ubuntu VM, ensuring proper user account creation and management. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
<p align="left">
The report displays login attempts with the event ID criteria ranging from 4624 to 4625, which indicates successful and failed login attempts, providing insights into authentication activities on the system. <br/><br/>
  <img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
  <br/>
