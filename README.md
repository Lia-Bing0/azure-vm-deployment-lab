# Azure Virtual Machine Deployment Lab

## Objective

Deploy and configure a Linux Virtual Machine in Microsoft Azure, implement secure network access, configure inbound security rules, deploy a basic web server, and validate external connectivity.

This project demonstrates foundational cloud infrastructure deployment, network security configuration, SSH access management, troubleshooting, and service validation.

## Tools Used

- Microsoft Azure Portal
- Azure Resource Groups
- Azure Virtual Machine (Linux)
- Network Security Groups (NSG)
- SSH (Key-based authentication)
- Ubuntu 24.04
- HTML configuration

## Architecture Overview

**Components:**

- Resource Group
- Virtual Network
- Subnet
- Network Security Group
- Public IP
- Linux Virtual Machine
- Inbound Rules (Port 22 & 80)

The VM is accessed securely via SSH and exposed externally through controlled inbound rules.

## Documentation Structure

**Full step-by-step documentation is organized inside:**
`/docs/steps/`

- 01-prereqs-and-deployment.md
- 02-ssh-and-web-setup.md
- 03-network-security-and-troubleshooting.md
- 04-validation-and-teardown.md

**Screenshots are located in:**
`/docs/images/`

## Key Implementation Highlights

- Created and validated Azure Resource Group
- Configured VM size, disk, and networking
- Generated and used SSH key pair for secure login
- Installed and configured Ubuntu 24.04 + Nginx web server
- Diagnosed connection failures
- Implemented and adjusted NSG inbound rules
- Validated successful external HTTP access
- Security Considerations
- Used SSH key authentication instead of password login
- Limited inbound access to required ports only (22, 80)
- Troubleshot and validated NSG configuration before exposing HTTP
- Avoided unnecessary public exposure of services
- Troubleshooting Performed
- SSH connection validation
- NSG inbound rule misconfiguration resolution
- HTTP port validation
- Connectivity re-testing after security adjustments

**Successful validation included:**

- SSH connection confirmation
- Web server installation verification
- Public IP HTTP access confirmation
- Edited HTML page rendering correctly

## Lessons Learned

Azure networking layers directly impact connectivity
NSG configuration must align with intended exposure
