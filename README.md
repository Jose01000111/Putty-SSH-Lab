# 🧪 PuTTY SSH Lab with Hyper-V Linux VMs

<p align="center">
<img src="https://i.imgur.com/aXtdOEg.png" alt="osTicket logo"/>
</p>

### 🖼️ Lab Overview
In this lab, I practiced using PuTTY to connect from my Windows machine to a CentOS virtual machine running in Hyper-V. My goal was to understand how to securely access and manage a remote Linux system over SSH, starting from verifying the SSH service to running commands from my Windows desktop.

#### 🛠️ Step 1: Making Sure SSH Is Running on CentOS
I started by logging directly into the CentOS VM through the Hyper-V console. Once inside the terminal, I checked if the SSH service (sshd) was running by using this command: sudo systemctl status sshd

<p align="center">
<img src="https://i.imgur.com/Tu9XxGF.png" alt="osTicket logo"/>
</p>

#### 🌐 Step 2: Finding the CentOS VM’s IP Address
Next, I needed the VM’s IP address so I could connect to it from PuTTY. I ran:
From the output, I looked for the inet address under the network adapter (for me, it was ens33). That IP address is what I used later in PuTTY.

<p align="center">
<img src="https://i.imgur.com/65WHg5J.png" alt="osTicket logo"/>
</p>

#### 🧩 Step 3: Confirming Hyper-V Networking
Before jumping into PuTTY, I made sure the VM was using the right network settings in Hyper-V Manager. I checked that the virtual network adapter was connected to an External Virtual Switch. This lets the VM share the host’s network and makes it reachable from my Windows machine.

<p align="center">
<img src="https://i.imgur.com/gxiVLWG.png" alt="osTicket logo"/>
</p>

<p align="center">
<img src="https://i.imgur.com/dZblRwm.png" alt="osTicket logo"/>
</p>

#### 🖥️ Step 4: Using PuTTY to Connect
On my Windows machine, I opened PuTTY. In the “Host Name” field, I typed the IP address of my CentOS VM. I made sure the connection type was set to SSH and the port was 22. Then I clicked Open.
Everything worked as expected. It was cool being able to manage the CentOS VM entirely from a PuTTY terminal.

<p align="center">
<img src="https://i.imgur.com/CEcM02M.png" alt="osTicket logo"/>
</p>

#### ⌨️ Step 5: Running Commands in the Remote Session
Now that I was connected, I ran a few Linux commands to test things out:

#### whoami: Displays the username of the currently logged-in user.

<p align="center">
<img src="https://i.imgur.com/kOFzxBl.png" alt="osTicket logo"/>
</p>

#### hostname: Shows the name of your machine.

<p align="center">
<img src="https://i.imgur.com/lmEwfjq.png" alt="osTicket logo"/>
</p>

#### pwd: Prints the full path of your current working directory.

<p align="center">
<img src="https://i.imgur.com/yjhEsph.png" alt="osTicket logo"/>
</p>

#### ls -l ~/: Lists all files and directories in your home folder in long (detailed) format.

<p align="center">
<img src="https://i.imgur.com/STBFsH5.png" alt="osTicket logo"/>
</p>

#### df -h: Displays disk-usage statistics for all mounted filesystems in a human-readable format.

<p align="center">
<img src="https://i.imgur.com/y5Ux4V8.png" alt="osTicket logo"/>
</p>

#### free -h: Shows total, used, and free memory (RAM) in a human-readable format.

<p align="center">
<img src="https://i.imgur.com/Q1djTw0.png" alt="osTicket logo"/>
</p>

Everything worked as expected. It was cool being able to manage the CentOS VM entirely from a PuTTY terminal.

### 🏁 Goals Accomplished
##### ✅Set up and verified SSH access on two Linux VMs.

##### ✅Successfully connected to both VMs using PuTTY from a Windows host.

##### ✅Practiced common Linux commands in a remote shell session.

##### ✅Gained hands-on experience with remote system administration.

### ⚙️ Technology Stack
##### ✅Host OS: Windows 10/11

##### ✅Virtualization: Hyper-V

##### ✅Linux Distributions: Ubuntu (with OpenSSH), CentOS (with OpenSSH)

##### ✅SSH Client: PuTTY

##### ✅Network Mode: External Virtual Switch on Hyper-V

##### ✅Terminal Commands: SSH service management, IP identification, Linux command-line basics

