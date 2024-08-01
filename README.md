# Cybersecurity Lab Setup

## Introduction
 This report will guide you through the steps to set up and use the lab environment, highlighting the tools and software used, and providing detailed steps.

## Tools and Software
The following tools and software will be used in this project:
- Kali Linux
- Security Onion
- pfSense
- Metasploit
- Nmap
- Wireshark
- OpenVAS
- Burp Suite
- VMware
- OpenVPN

## Lab Environment Setup

### Step 1: Install VMware
1. **Download VMware Workstation Pro**:
   - Go to the [VMware website](https://www.vmware.com/products/workstation-pro/workstation-pro-evaluation.html).
   - Download the installer for your operating system.
2. **Install VMware Workstation Pro**:
   - Run the downloaded installer.
   - Follow the installation wizard to complete the installation.

### Step 2: Create Virtual Machines (VMs)
1. **Create a Kali Linux VM**:
   - Download the Kali Linux ISO from the [official website](https://www.kali.org/downloads/).
   - Open VMware Workstation Pro.
   - Click on "Create a New Virtual Machine".
   - Select "Installer disc image file (iso)" and browse to the Kali Linux ISO.
   - Follow the prompts to configure the VM settings and complete the installation.

   ![Kali Linux VM](images/kali-linux-vm.png)

2. **Create a Security Onion VM**:
   - Download the Security Onion ISO from the [official website](https://securityonionsolutions.com/software/).
   - Repeat the steps above to create a Security Onion VM.

3. **Create a pfSense VM**:
   - Download the pfSense ISO from the [official website](https://www.pfsense.org/download/).
   - Repeat the steps above to create a pfSense VM.

4. **Create a Windows VM**:
   - Use a Windows installation ISO or download a Windows evaluation ISO from the [Microsoft Evaluation Center](https://www.microsoft.com/en-us/evalcenter/).
   - Repeat the steps above to create a Windows VM.

5. **Create an Ubuntu VM**:
   - Download the Ubuntu ISO from the [official website](https://ubuntu.com/download/desktop).
   - Repeat the steps above to create an Ubuntu VM.

### Step 3: Network Configuration
1. **Create Network Segments**:
   - In VMware Workstation Pro, go to "Edit" > "Virtual Network Editor".
   - Add new network segments for internal, DMZ, and external networks.

   ![Network Segments](images/network-segments.png)

2. **Configure pfSense**:
   - Start the pfSense VM.
   - Follow the setup wizard to configure the internal and external network interfaces.
   - Assign the internal network segment to the LAN interface and the external network segment to the WAN interface.
   - Configure the DMZ network segment as an optional interface.

   ![pfSense Configuration](images/pfsense-config.png)

3. **Connect VMs to Network Segments**:
   - Assign the internal network segment to the internal-facing VMs (e.g., Windows, Ubuntu).
   - Assign the DMZ network segment to the VMs that will reside in the DMZ (e.g., web server, database server).
   - Assign the external network segment to the Security Onion VM for monitoring purposes.

   ![VM Network Configuration](images/vm-network-config.png)

### Step 4: Install and Configure Security Tools
1. **Kali Linux**:
   - Pre-installed with tools like Metasploit, Nmap, Wireshark, and Burp Suite.
   - Update and upgrade the system: `sudo apt update && sudo apt upgrade -y`.

2. **Security Onion**:
   - Follow the setup instructions on the [Security Onion documentation](https://docs.securityonion.net/en/2.3/quick-install.html) to complete the installation and configuration.

3. **pfSense**:
   - Access the pfSense web interface.
   - Configure firewall rules and VPN settings as needed.

4. **OpenVAS**:
   - Install OpenVAS on the Kali Linux VM: `sudo apt install openvas`.
   - Follow the setup instructions: `sudo gvm-setup`.
   - Start OpenVAS services: `sudo gvm-start`.
   - Access the OpenVAS web interface and configure it for vulnerability scanning.

   ![OpenVAS Configuration](images/openvas-config.png)

5. **Burp Suite**:
   - Open Burp Suite on the Kali Linux VM.
   - Configure Burp Suite settings for web application security testing.

   ![Burp Suite Configuration](images/burp-suite-config.png)

## Conclusion
This report provides a comprehensive guide to setting up a cybersecurity lab environment using VMware and various security tools. The lab environment will enable you to apply principles of cybersecurity, conduct risk assessments, analyze threats, perform security evaluations, develop policies, mitigate social engineering, investigate cybercrimes, and conduct reconnaissance.


---
George Ofosu, CASP
