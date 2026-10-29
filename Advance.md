
# NETWORKWALKS-B084-WK1-PM1-CYBERSECURITY-LAB-SETUP

Good Day Everyone, my name is Trisha Dela Cruz, and this week here is the finished task I have done so far.

## 🔐 Windows 10 Virtual Lab Setup

This week, I set up Windows 10 in Oracle VirtualBox on my laptop to learn more about virtual machines, network configuration, and how Windows and Kali Linux can communicate within an isolated cybersecurity lab environment.

## 📌 Project Overview

This project documents the setup of a Windows 10 virtual machine in Oracle VirtualBox. The main purpose is to configure the Windows VM and test its network connectivity with my existing Kali Linux virtual machine.

This documentation includes the installation process, network settings, IP address configuration, and connectivity verification.

## 🎯 Objectives

- Download and install the necessary software for the Windows 10 VM.
- Create and configure Windows 10 in VirtualBox.
- Review the VM's memory, processor, display, and network settings.
- Assign a static IP address to the Windows VM.
- Connect Windows 10 and Kali Linux to the same NAT Network.
- Verify connectivity by pinging Kali Linux from Windows.
- Capture and document the completed setup.

## 🛡️ Purpose of the Lab

The Windows 10 VM is intended for coursework and authorized cybersecurity practice. It can support learning activities such as:

- Windows operating system familiarization.
- Network configuration and troubleshooting.
- IP address and DNS configuration.
- Communication between virtual machines.
- Network connectivity testing.
- Security testing within an isolated lab environment.

## 🏗️ Lab Architecture

<img width="1346" height="616" alt="Lab Architecture" src="https://github.com/user-attachments/assets/48433ca3-d9cd-41d0-955b-0f6ee9aad26a" />

Both the Windows 10 and Kali Linux virtual machines are connected to the same NAT Network in VirtualBox. This allows the two virtual machines to communicate with each other using their assigned IP addresses.

## ⚙️ Lab Configuration

| 🧩 Component | ⚙️ Configuration |
|---|---|
| 🖥️ Host OS | Windows 10 |
| 🧠 Host RAM | 8 GB |
| ⚡ Processor | AMD Ryzen 7 |
| 🧰 Hypervisor | VirtualBox 7.2 |
| 💻 Virtual Machine OS | Windows 10 |
| 🐉 Security Testing OS | Kali Linux 2026.3 |
| 🧠 Kali RAM | 2048 MB |
| 🌐 Virtual Network | NAT Network |
| 📡 Network Address | 10.0.0.0/24 |
| 🪟 Windows 10 IP Address | 10.0.0.10/24 |
| 🐧 Kali IP Address | 10.0.0.2/24 |
| 🚪 Default Gateway | 10.0.0.1 |
| 🌍 DNS Server | 8.8.8.8 |
| 🔮 Future VM Range | 10.0.0.3–10.0.0.99 |

## 🪜 Lab Setup Procedure

### Step 1. Download the Required Software

First, I downloaded the necessary software for creating my Windows 10 virtual machine.

I used Oracle VirtualBox as the virtualization platform and downloaded the Windows 10 installation image for the guest operating system.

After downloading the required files, I prepared them for the virtual machine installation.

![VirtualBox Manager interface](images/virtualbox.png)

### Step 2. Set Up the Windows 10 Virtual Machine

After downloading the necessary software, I opened Oracle VirtualBox and started creating a new virtual machine.

I selected Windows 10 as the operating system, configured the virtual machine settings, and allocated the necessary system resources.

I also prepared the virtual hard disk where Windows 10 would be installed.

![Virtual machine installation files in Windows](images/windowsetup2.png)

![Windows 10 virtual machine installation wizard](images/windowsetup.png)

### Step 3. Configure the NAT Network

After setting up the Windows 10 VM, I configured the virtual network in VirtualBox.

I used a NAT Network so that both my Windows 10 and Kali Linux virtual machines could communicate with each other.

The NAT Network was configured using the network address `10.0.0.0/24`.

![NAT Network and IPv4 prefix configuration](images/kaliNAT.png)

![Network adapter NAT Network selection](images/kalisetup2.png)

### Step 4. Start the Windows 10 Virtual Machine

After completing the initial configuration, I started the Windows 10 VM in VirtualBox.

I checked that Windows 10 launched successfully and that I could access the desktop.

![Windows 10 virtual desktop](images/windowscreen.png)

### Step 5. Assign the Windows 10 IP Address

Next, I configured the Windows 10 virtual machine's network settings.

I opened the Ethernet adapter settings and manually assigned a static IPv4 address.

The following settings were used:

- IP Address: `10.0.0.10`
- Subnet Mask: `255.255.255.0`
- Default Gateway: `10.0.0.1`
- Preferred DNS Server: `8.8.8.8`

This configuration allows the Windows VM to communicate with Kali Linux within the same virtual network.

![Windows Ethernet static IPv4 address and DNS configuration](images/windowIP.png)

### Step 6. Test Network Connectivity with Kali Linux

After configuring the network settings, I opened Command Prompt in the Windows 10 virtual machine.

I performed a ping test using the IP address of my Kali Linux VM.

The command I used was:

```cmd
ping 10.0.0.2
```

I sent four ping requests from the Windows 10 VM to the Kali Linux VM.

The Windows VM was able to ping Kali Linux successfully, confirming that the two virtual machines could communicate through the NAT Network.

![Windows ping tests for network and internet connectivity](images/windowpingtest.png)

## 🔎 Lab Verification

To verify the network configuration, I performed a ping test from Windows 10 to Kali Linux.

I used Command Prompt and entered the Kali Linux IP address `10.0.0.2`.

The ping test was successful, and Windows 10 was able to communicate with my Kali Linux virtual machine.

The configured IP addresses are:

- Windows 10 IP Address: `10.0.0.10`
- Kali Linux IP Address: `10.0.0.2`
- Default Gateway: `10.0.0.1`
- DNS Server: `8.8.8.8`

**Result:** The Windows 10 VM was able to ping the Kali Linux VM successfully.

This confirms that the two virtual machines can communicate within the configured NAT Network.

## 🐞 Problems Encountered and Solutions

The main issue I encountered during the Windows 10 virtual machine setup was assigning the IP address.

It was challenging since I am used to Windows 11 OS rather than Windows 10.

The solution appperently  is going to prefference then  clicking properties finally internet protocol version 4 (tcp/ipv4) properties. 

## 💡 What I Learned

Through this lab, I practiced:

1. Downloading and preparing Windows 10 installation files.
2. Creating and configuring a Windows 10 virtual machine in VirtualBox.
3. Setting up a NAT Network for multiple virtual machines.
4. Assigning a static IPv4 address in Windows 10.
5. Understanding the purpose of IP addresses, subnet masks, gateways, and DNS servers.
6. Using Command Prompt to perform network connectivity tests.
7. Testing communication with pings between Windows 10 and Kali Linux.
8. Troubleshooting basic network configuration issues.

## 🔐 Security and Ethical Use

This environment is for educational use and authorized cybersecurity testing only.

All network configuration and connectivity tests were performed within my virtual lab environment.

Do not scan, access, or test systems without permission.

## 🔗 Tools and Resources

- Oracle VirtualBox https://www.virtualbox.
- Windows 10 installation https://www.microsoft.com/en-us/software-download/windows10
- Windows Command Prompt
- Windows Network Settings

## 👤 Author

Trisha Gayle Dela Cruz

B084
