# Terraform-GCP-Network-Modules
Automating Google Cloud network and compute infrastructure using Terraform modules, variables, and implicit dependencies.

# Terraform Modules for Google Cloud Network and Compute Resources

This project demonstrates how to design and deploy **Google Cloud infrastructure**
using **Terraform modules**, **input variables**, and **implicit dependencies**.

The configuration provisions a custom VPC network, firewall rules, and multiple
Compute Engine virtual machines using reusable Terraform modules.

---

## 🛠 Technologies Used

- Terraform
- Google Cloud Platform (GCP)
- Google Compute Engine
- Google VPC Networking
- HashiCorp Configuration Language (HCL)
- Google Cloud Shell

---

## 📐 Infrastructure Components

- Auto‑mode VPC network
- Firewall rule allowing HTTP, SSH, RDP, and ICMP traffic
- Two Compute Engine VM instances deployed in different regions
- Reusable Terraform module for VM creation

---

## 📂 Project Structure
- tfinfra
-- provider.tf 
-- mynetwork.tf 
-- variables.tf 
-- instance 
---- main.tf 
---- variables.tf


---

## 🚀 Implementation Overview

### Network Configuration
- Created an auto‑mode VPC network
- Enabled automatic subnet creation across regions
- Defined a firewall rule allowing:
  - TCP ports 22, 80, and 3389
  - ICMP traffic
- Used implicit dependencies to ensure the network is created before dependent resources

### Module‑Based VM Deployment
- Built a reusable Terraform module for Compute Engine instances
- Parameterized instance name, zone, machine type, and network
- Deployed two VM instances using the same module with different configurations
- Ensured correct resource creation order through attribute references

### Terraform Workflow
- Formatted configuration using `terraform fmt`
- Initialized providers and modules with `terraform init`
- Reviewed execution plan using `terraform plan`
- Applied infrastructure changes using `terraform apply`

---

## 🧠 Key Learnings

- How Terraform modules enable reusable infrastructure patterns
- Using input variables to customize module behavior
- Managing implicit dependencies through resource references
- Deploying multi‑region infrastructure from a single configuration
- Understanding Terraform’s execution plan and dependency graph

---

## 📎 Notes

This project was completed as part of the **Google Cloud Skills Boost**
learning path focused on **Infrastructure as Code with Terraform**.



