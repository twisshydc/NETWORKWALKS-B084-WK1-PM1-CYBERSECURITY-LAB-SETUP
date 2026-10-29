
# NETWORKWALKS-B084-WK1-PM1-CYBERSECURITY-LAB-SETUP

Good day, everyone! My name is Trisha Dela Cruz, and here are the tasks I completed this week.

## 🔐 Kali Linux Virtual Lab Setup

This week, I set up Kali Linux in Oracle VirtualBox on my laptop to learn more about cybersecurity tools and how they are used in the cybersecurity industry.

## 📌 Project Overview

This project documents the setup of a Kali Linux virtual machine in Oracle VirtualBox.

The main purpose of this project is to create a virtual environment where I can practice using Kali Linux, configure network settings, and perform basic connectivity tests.

This documentation includes the installation process, virtual machine configuration, static IP addressing, network connectivity testing, and problems encountered during the setup.

## 🎯 Objectives

- Download and install the necessary software for Kali Linux.
- Create or import a Kali Linux virtual machine in VirtualBox.
- Review the VM's memory, processor, display, and network settings.
- Configure a NAT Network for virtual machine communication.
- Assign a static IP address to the Kali Linux VM.
- Verify the IP address, gateway, and DNS connectivity.
- Capture and document the completed setup.

## 🛡️ Purpose of the Lab

The Kali Linux VM is intended for coursework and authorized cybersecurity practice. It can support learning activities such as:

- Linux command-line familiarization.
- Network configuration and troubleshooting.
- Cybersecurity tool familiarization.
- Basic network connectivity testing.
- Scanning and testing within an isolated lab.
- Understanding virtual machine networking.

## 🏗️ Lab Architecture

<img width="1346" height="616" alt="Lab Architecture" src="https://github.com/user-attachments/assets/48433ca3-d9cd-41d0-955b-0f6ee9aad26a" />

The Kali Linux virtual machine uses a NAT Network in VirtualBox.

This allows Kali Linux to access external networks while also communicating with other virtual machines connected to the same NAT Network, such as my Windows 10 virtual machine.

## ⚙️ Lab Configuration

| 🧩 Component | ⚙️ Configuration |
|---|---|
| 🖥️ Host OS | Windows 10 |
| 🧠 Host RAM | 8 GB |
| ⚡ Processor | AMD Ryzen 7 |
| 🧰 Hypervisor | VirtualBox 7.2 |
| 🐉 Security OS | Kali Linux 2026.3 |
| 🧠 Kali RAM | 2048 MB |
| 🌐 Virtual Network | NAT Network |
| 📡 Network Address | 10.0.0.0/24 |
| 🐧 Kali IP Address | 10.0.0.2/24 |
| 🚪 Default Gateway | 10.0.0.1 |
| 🌍 DNS Server | 8.8.8.8 |
| 🔮 Future VM Range | 10.0.0.3–10.0.0.99 |

## 🪜 Lab Setup Procedure

### Step 1. Download the Required Software

First, I downloaded the necessary software for creating my Kali Linux virtual machine.

I used Oracle VirtualBox as my virtualization platform and downloaded the Kali Linux prebuilt virtual machine image from the official Kali Linux website.

After downloading the files, I extracted the Kali Linux image and prepared it for installation in VirtualBox.

![VirtualBox Manager File menu](images/virtualbox.png)

![Downloaded Kali and Windows virtual machine files](images/windowsetup2.png)

### Step 2. Set Up the Kali Linux Virtual Machine

After downloading the necessary software, I opened Oracle VirtualBox and added the Kali Linux virtual machine.

I selected the extracted Kali Linux virtual machine file and imported it into VirtualBox.

I also reviewed the virtual machine settings, including the allocated memory, processor, and storage.

![Selecting the Kali virtual machine file](images/kalisetup.png)

![Kali virtual machine running in VirtualBox Manager](images/kalidetails.png)

### Step 3. Configure the NAT Network

After setting up Kali Linux, I configured the NAT Network in VirtualBox.

I used a NAT Network so that my Kali Linux and Windows 10 virtual machines could communicate with each other.

The NAT Network was configured using the following settings:

- Network Address: `10.0.0.0/24`
- Default Gateway: `10.0.0.1`
- Network Mode: NAT Network

![VirtualBox NAT Network configuration](images/kaliNAT.png)

![Kali VM network adapter settings](images/kalisetup2.png)

### Step 4. Start the Kali Linux Virtual Machine

After completing the initial configuration, I started Kali Linux in VirtualBox.

I checked that the virtual machine launched successfully and that I could access the Kali Linux login screen.

After logging in, I accessed the Kali Linux desktop and prepared the system for network configuration.

![Kali Linux login screen](images/kalisignin.png)

### Step 5. Assign the Kali Linux Static IP Address

Next, I configured the network settings of my Kali Linux virtual machine.

I opened the network connection settings by right-clicking the network icon and selecting **Edit Connections**.

From there, I accessed the IPv4 settings and manually assigned the IP address.

The following settings were used:

- IP Address: `10.0.0.2`
- Subnet Mask: `255.255.255.0`
- Default Gateway: `10.0.0.1`
- DNS Server: `8.8.8.8`

Static IP addressing allows my Kali Linux VM to maintain a consistent IP address for network testing and communication with my Windows 10 VM.

### Step 6. Test Kali Linux Network Connectivity

After assigning the IP address, I opened the Kali Linux terminal to verify the network connection.

I performed ping tests to check the Kali Linux IP address, default gateway, and DNS connectivity.

The network configuration used was:

- Kali Linux IP Address: `10.0.0.2`
- Default Gateway: `10.0.0.1`
- DNS Server: `8.8.8.8`

I used the following commands to check my network configuration:

```bash
ip addr
```

```bash
ip route
```

```bash
ping -c 4 10.0.0.1
```

```bash
ping -c 4 8.8.8.8
```

These commands helped me check the assigned IP address, routing information, and network connectivity.

![Kali ping tests for VM IP gateway and public DNS](images/kalipingtest.png)

## 🔎 Lab Verification

To verify my network configuration, I performed connectivity tests using the Kali Linux terminal.

I sent four ping requests to test whether the virtual machine could communicate with the configured network gateway and external DNS server.

The configured network information was:

- IP Address: `10.0.0.2`
- Default Gateway: `10.0.0.1`
- DNS Server: `8.8.8.8`

These tests helped me verify the network connection and check whether the assigned settings were working correctly.

## 🐞 Problems Encountered and Solutions

During the Kali Linux virtual machine setup, I encountered three issues.

### Problem 1. Network Connection Disconnected After Assigning the IP Address

The first issue I encountered was that my network connection became disconnected after assigning a static IP address to Kali Linux.

To resolve this issue, I opened the Kali Linux terminal and entered the following commands:

```bash
sudo nmcli connection modify "Wired connection 1" ipv4.dad-timeout 0
```

```bash
sudo nmcli connection down "Wired connection 1"
```

```bash
sudo nmcli connection up "Wired connection 1"
```

These commands helped me adjust the connection settings and reactivate the network connection.

### Problem 2. Difficulty Finding the IP Address Settings

The second issue I encountered was finding where to assign the IP address in Kali Linux.

At first, I was unfamiliar with the network settings and did not know where to manually configure the static IP address.

To resolve this issue, I right-clicked the network icon and selected **Edit Connections**.

From there, I accessed the IPv4 settings and entered the IP address, subnet mask, gateway, and DNS server.

### Problem 3. Difficulty Downloading Kali Linux

The third issue I encountered was downloading Kali Linux.

I initially tried downloading the latest version, but my computer kept rejecting the file.

To resolve this issue, I temporarily disabled Windows Defender, completed the download, and re-enabled the protection afterward.

This allowed me to continue setting up my Kali Linux virtual machine.

## 💡 What I Learned

Through this lab, I practiced:

1. Downloading and preparing Kali Linux installation files.
2. Creating or importing a Kali Linux virtual machine in VirtualBox.
3. Reviewing virtual machine hardware and network settings.
4. Configuring a NAT Network in VirtualBox.
5. Assigning a static IP address in Kali Linux.
6. Understanding the purpose of IP addresses, subnet masks, gateways, and DNS servers.
7. Using Linux terminal commands for basic network configuration.
8. Performing ping tests to check network connectivity.
9. Troubleshooting network connection problems.
10. Understanding how Kali Linux and Windows 10 can communicate within the same virtual network.

## 🔐 Security and Ethical Use

This environment is for educational use and authorized cybersecurity testing only.

All network configuration and connectivity testing activities were performed within my virtual lab environment.

Do not scan, access, or test systems without permission.

## 🔗 Tools and Resources

- Kali Linux: https://www.kali.org/
- Oracle VirtualBox: https://www.virtualbox.org/

## 👤 Author

Trisha Gayle Dela Cruz

B084
