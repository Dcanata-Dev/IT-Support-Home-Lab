# Project 02 – Network Connectivity & Troubleshooting

## Objective

Configure network communication between a Windows 11 client and a Windows Server 2025 virtual machine. Troubleshoot connectivity issues using IP configuration, ping tests, and Windows Defender Firewall.

## Lab Environment

- Virtualization Software: Oracle VirtualBox
- Client: Windows 11
- Server: Windows Server 2025
- Server Hostname: HELPDESK-SRV01

## Network Configuration

Both virtual machines were connected to the same VirtualBox NAT Network with DHCP enabled.

| Machine | IP Address |
|---|---|
| Windows 11 | 10.0.2.3 |
| Windows Server | 10.0.2.4 |

## Troubleshooting Process

### 1. Initial Connectivity Testing

Used the `ipconfig` command to identify the IP addresses assigned to each virtual machine.

Used `ping` to test communication between the Windows 11 client and Windows Server.

Initial tests resulted in request timeouts in both directions.

### 2. Server Firewall Investigation

Inspected Windows Defender Firewall settings on the server.

Identified that the network was classified as Public and that the inbound ICMPv4 Echo Request rule was not enabled.

Changed the server's network classification to Private and enabled the appropriate inbound ICMPv4 rule.

### 3. Client Firewall Investigation

Tested communication again from Windows 11.

The client could successfully ping the server, but the server could not yet ping the client.

Inspected the Windows 11 inbound firewall rules and enabled the appropriate ICMPv4 Echo Request rule.

### 4. Final Connectivity Testing

Repeated ping tests in both directions.

Both virtual machines successfully received ping replies.

## Results

- Confirmed both machines were connected to the same NAT Network.
- Verified unique IP addresses for both virtual machines.
- Identified firewall rules as the cause of blocked ping requests.
- Configured inbound ICMPv4 rules on both machines.
- Successfully established two-way ping communication.
- Kept Windows Defender Firewall enabled throughout troubleshooting.

## Skills Practiced

- Basic network troubleshooting
- IP address identification
- Command Prompt and PowerShell
- ICMP and ping testing
- Windows Defender Firewall
- Inbound firewall rule configuration
- Troubleshooting and verification

## Key Takeaway

A computer can be connected to a network while its firewall prevents certain types of communication. Successful troubleshooting requires checking both network connectivity and firewall configuration.
