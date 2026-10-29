# NETWORKWALKS-B084-WK1-PM1-CYBERSECURITY-LAB-SETUP


Good Day Everyone my name is Trisha Dela Cruz and this week here is the finished task I have done so far.


🔐 Kali Linux Virtual Lab Setup
This week I set up Kali Linux in Oracle VirtualBox in my laptop to learn more about cybersecurity tools and the usage of it in the cybersecurity industry. 




📌 Project Overview
This project documents the setup of a Kali Linux virtual machine in Oracle VirtualBox in my laptop 

This README is to 


🎯 Objectives
- Install or import Kali Linux in VirtualBox.
- Review the VM’s memory, processor, display, and network settings.
- Confirm Kali starts successfully.
- Check the VM’s IP address, route, and DNS resolution.
- Capture and document the completed setup.

  
🛡️ Purpose of the Lab
The VM is intended for coursework and authorized practice. It can support learning activities such as:
- Linux command-line use.
- Network configuration and troubleshooting.
- Security-tool familiarization.
- Scanning and testing within an isolated lab.
- Documenting results and restoring a clean VM state.

  
🏗️ Lab Architecture
<img width="1346" height="616" alt="image" src="https://github.com/user-attachments/assets/48433ca3-d9cd-41d0-955b-0f6ee9aad26a" />









The Kali VM’s network mode should match the lab requirements. NAT is suitable for basic internet access; use a shared private lab network only when VMs need to communicate with each other.
⚙️ Lab Configuration
🧩 Component	⚙️ Configuration
🖥️ Host OS	Windows 10
🧠 Host RAM	8 GB
⚡ Processor	AMD Ryzen 7
🧰 Hypervisor	VirtualBox 7.2
🐉 Security OS	Kali Linux 2026.3
🧠 Kali RAM	2048 MB
🌐 Virtual Network	NAT Network
📡 Network Address	10.0.0.0/24
🐧 Kali IP Address	10.0.0.2/24
🚪 Default Gateway	10.0.0.1
🌍 DNS Server	8.8.8.8
🔮 Future VM Range	10.0.0.3–10.0.0.99


🪜 Lab Setup Procedure
Step 1. Install VirtualBox
Install Oracle VirtualBox on the Windows host.


Step 2. Download the Kali VirtualBox image
Download the prebuilt VirtualBox image from the official Kali website. Extract the downloaded archive if needed.



Step 3. Add the Kali VM
In VirtualBox Manager, add or import the Kali virtual machine, then review its hardware settings before starting it.


Step 4. Configure the network adapter
Open Settings → Network → Adapter 1 and record the Attached to mode used for this lab.
- Use NAT for basic outbound internet access.
- Use NAT Network or Host-only Adapter when the lab requires communication between VMs.
- Leave IPv4 on Automatic (DHCP) unless the lab specifically requires a static address.

- 
Step 5. Start Kali and check connectivity
Start the VM and sign in. Run the verification commands below, then record the results in this README.
Step 6. Take a clean snapshot
After the initial setup is complete, take a VirtualBox snapshot so the VM can be restored to a known-good state.

Suggested snapshot name: Clean Kali Lab Setup
🔎 Lab Verification
Check	Command	Record the result
IP address	

Example Results
Fill these in with your actual output:
- Kali IP address: [
- Default gateway: [Your result]
- DNS resolution: [Your result]
- Internet test: [Your result]
🖼️ Screenshot

Figure 1. Kali Linux virtual machine running in Oracle VirtualBox.

Save your screenshot as screenshots/kali-linux.png, or change the image path above to match its actual filename.
🐞 Problems Encountered and Solutions
Document only issues you actually encountered.
Problem	Solution
The first issue I encountered is after assigning the IP address my wifi connection is gone or the port disconnected.
I resolved it by doing this. 

sudo nmcli connection modify "Wired connection 1" ipv4.dad-timeout 0
sudo nmcli connection down "Wired connection 1"
sudo nmcli connection up "Wired connection 1"

The second issue is assigning in kali linux it's ip address. This issue stems in not finding where is the place to change ip address. 
The simple solution is to right click near the the port icon and it appeared the edit connections.

The third issue is downloading kali linux. I opted to use the latest version and my computer kept rejecting it. The solutuon to that will be
to turn off windows defense and reapply later 
[Describe an issue, if applicable]	[Describe how you resolved it]

Assigning The IP address






💡 What I Learned
Through this lab, I practiced:
1. Creating or importing a Linux virtual machine.
2. Reviewing VM hardware and network settings.
3. Checking IP addressing, routing, and DNS from Kali.
4. Using a VM snapshot as a recovery point.
5. Testing in Linux
🔐 Security and Ethical Use
This environment is for educational use and authorized testing only. Do not scan, access, or test systems without permission.
🔗 Tools and Resources
- Kali Linux downloads
- Oracle VirtualBox downloads
👤 Author
Trisha Gayle Dela Cruz
B084
