# vm-traffic-distribution-azurelb
# 🔄 Azure Load Balancer Setup - Hands-On Project

This repository documents my hands-on experience setting up a **Load Balancer** using Microsoft Azure. The goal of this project was to demonstrate how to distribute incoming traffic between multiple virtual machines for high availability and scalability.

---

## 📌 Objectives

- Create and configure a Load Balancer
- Set up a secure virtual network
- Deploy multiple Virtual Machines (VMs)
- Enable NAT Gateway for external communication
- Test traffic distribution across VMs
- Securely connect using Azure Bastion

---

## 🧰 Tools & Services Used

- Microsoft Azure Portal  
- Azure Load Balancer  
- Azure Virtual Network (VNet)  
- Azure Virtual Machines (Windows/Linux)  
- NAT Gateway  
- Azure Bastion  

---

## ⚙️ Steps Performed

### 1️⃣ Create Resource Group
- Navigate to Azure Portal
- Create a new **Resource Group** to manage all components

### 2️⃣ Set Up a Virtual Network
- Define address space and subnets
- Ensure subnets are configured to support Load Balancer and Bastion

### 3️⃣ Deploy Two Virtual Machines
- VM1 and VM2 in the same VNet
- Assign NSGs and Public IPs if needed

### 4️⃣ Create a Load Balancer
- Choose "Standard" SKU for production-grade setup
- Configure:
  - **Frontend IP configuration**
  - **Backend pool** with both VMs
  - **Health probe** (TCP/HTTP)
  - **Load balancing rules** to forward traffic

### 5️⃣ Set Up NAT Gateway
- Assign NAT Gateway to subnet
- Ensure outbound internet access for VMs

### 6️⃣ Configure Azure Bastion
- Create Bastion host
- Connect securely to VM1 and VM2 from Azure Portal without public IPs

### 7️⃣ Validate Load Balancer
- Fetch **Frontend IP**
- Access service from browser or terminal
- Confirm traffic is distributed (optional: set up IIS or Apache to return VM-specific pages)

---

## 🧪 Challenges Faced

- Correct subnet association for Bastion and NAT Gateway
- Ensuring backend pool VMs respond correctly to probe
- Verifying IP-level routing and NAT behavior
- Load Balancing not working until health probe was properly configured

---

## ✅ Learnings

- Azure Load Balancer efficiently handles traffic when backend and probe settings are correct  
- Bastion provides secure access without exposing VMs to the internet  
- NAT Gateway simplifies outbound connectivity while maintaining security

---

## 📁 Files

- `LoadBalancer.pdf`: Step-by-step notes and screenshots from the actual setup process

---

## 📎 License

This project is for learning and demonstration purposes only. Feel free to fork or reference.

---

## 🔗 Connect with Me

📫 ankitaykher99@gmail.com/www.linkedin.com/in/ankita-kher-96a657227


