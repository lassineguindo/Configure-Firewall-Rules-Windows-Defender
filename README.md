# Configure Firewall Rules – Windows Defender

## Overview
This project walks through how to configure firewall rules using **Windows Defender Firewall** on a **Windows 10 Virtual Machine**. You'll learn how to turn the firewall on or off, understand default settings, and manually allow traffic through specific ports like FTP (port 21). This kind of setup is useful for understanding how firewalls control traffic into and out of a system.

## What You’ll Need
- VirtualBox installed on your host machine
- A Windows 10 Virtual Machine
- Basic understanding of ports and services (like FTP)

## Project Steps

### Step 1: Set Up the Virtual Machine
Launch your **Windows 10 VM** in **VirtualBox**. If it’s not set up yet, install VirtualBox, create the VM, and finish the OS installation. Make sure to allocate enough RAM and storage. Set the **network adapter to “Bridged Adapter”** so it can communicate on the same network as your host machine.

### Step 2: Open Windows Defender Firewall
Click the **Windows Search Bar** and type **Windows Defender Firewall** to open it. On the left side, click **“Turn Windows Defender Firewall on or off.”** You’ll see options for **Private** and **Public** networks. Leave both turned **on** for this project to ensure the firewall is active for all types of connections.

### Step 3: Open Advanced Settings
Sometimes apps don’t work because a needed port is blocked. To fix this, go back to the firewall window and click **“Advanced settings”** on the left. This opens the full firewall management panel where you can view, edit, and create rules.

### Step 4: View Current Rules
By default, Windows Firewall **blocks most inbound traffic** and **allows outbound traffic**. Click **Inbound Rules** and **Outbound Rules** to see what connections are currently being allowed or blocked.

### Step 5: Create a Rule to Allow FTP
The firewall doesn’t allow FTP traffic in by default. To allow it, click **“New Rule…”** on the right, choose **“Port”**, and click **Next**.  
Select **TCP**, enter **21** for the port number, and continue. Choose **“Allow the connection”**, then click **Next** through the rest of the options. Name the rule **“FTP Server”** and click **Finish**. The rule will now appear in your inbound rules list.

### Step 6: Close All Tabs
Once you're finished, close all the open windows to wrap up the project. Your firewall is now configured to allow FTP traffic.

## License
This project is for educational use.
