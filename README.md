# taskthirteen
# Setting Up and Interacting with a Free Cloud VM

## Overview
This repository contains the steps and screenshots for creating a free Virtual Machine (VM) in the cloud, connecting to it from Kali Linux, and performing basic network interactions.

## Steps to Create and Interact with the VM

### 1. Create a Free Cloud Account
- Sign up for a free account on Azure (or GCP/AWS).
- Verify your account and complete the setup process.

### 2. Create a Virtual Machine
- Select a free-tier VM configuration with the following specifications:
  - **OS**: Linux (Ubuntu preferred)
  - **Instance Size**: B1s (1 vCPU, 1 GiB memory) or equivalent
  - **Region**: Closest available region
- Note down the public IP address of the VM once it is up and running.

### 3. Allow Network Access
- Configure firewall settings to allow inbound SSH (port 22) and ICMP (ping) traffic.

### 4. Ping the VM from Kali Linux
- Open the terminal on Kali Linux and ping the VM's public IP address:
  ```bash
  ping <VM Public IP>
  ```

### 5. SSH into the VM
- Log into the VM using SSH from Kali Linux with the following command:
  ```bash
  ssh -i <path to the private key file> <username>@<VM Public IP>
  ```
- Once logged in, run the following command to display the network interfaces:
  ```bash
  ip a
  ```
- Capture a screenshot of the result.

### 6. Ping Your Public IP from the VM
- Find the public IP address of your Kali Linux machine.
- From the VM, ping your public IP:
  ```bash
  ping <Your Public IP>
  ```
- Capture a screenshot of the result.

### 7. Deleting the VM
- Navigate to the **Overview** section in Azure.
- Click on **"Delete"** to remove the VM.

