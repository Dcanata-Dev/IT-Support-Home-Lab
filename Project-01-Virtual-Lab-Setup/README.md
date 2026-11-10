# Project 01 – Virtual Lab Setup

## Objective

Build a virtual IT support environment using Oracle VirtualBox with Windows 11 and Windows Server 2025. This environment will be used to practice networking, systems administration, and common helpdesk support tasks.

## Lab Environment

### Virtualization Software
- Oracle VirtualBox

### Windows 11 Client
- Operating System: Windows 11
- RAM: Approximately 4 GB
- Purpose: Client workstation for helpdesk testing and troubleshooting.

### Windows Server
- Operating System: Windows Server 2025 Standard Evaluation (Desktop Experience)
- Computer Name: HELPDESK-SRV01
- RAM: 4 GB
- Processors: 2
- Virtual Disk: 60 GB (dynamically allocated)
- Purpose: Server environment for learning Windows Server administration and Active Directory.

## Network Configuration

- Network Type: VirtualBox NAT Network
- DHCP: Enabled
- Windows 11 IP Address: 10.0.2.3
- Windows Server IP Address: 10.0.2.4
- Both virtual machines connected to the same NAT Network.

## Completed Tasks

- Created Windows 11 virtual machine.
- Created and installed Windows Server 2025 virtual machine.
- Configured server hostname.
- Configured shared NAT Network.
- Verified IP address assignments.
- Tested communication between both virtual machines.

## Current Status

Initial virtual lab setup completed.

## Next Steps

- Document network troubleshooting.
- Configure Active Directory Domain Services.
- Create domain users and groups.
- Practice common helpdesk support scenarios.
