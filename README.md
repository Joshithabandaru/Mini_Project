# Secure Campus Network Using Cisco Packet Tracer

## Project Overview
This mini project demonstrates the design, configuration, and security of a small campus network using Cisco Packet Tracer. The network connects two LANs through a router and uses security features to protect network devices and restrict unauthorized access.

## Objectives
- Design a campus network using a router, two switches, and six PCs.
- Configure IP addresses and default gateways.
- Secure console and privileged EXEC access.
- Enable SSH for secure remote device administration.
- Implement switch port security using sticky MAC addresses.
- Disable unused switch ports and save device configurations.
- Test connectivity between devices and networks.

## Network Topology
- **Router:** Cisco 1941 (hostname `R1`)
- **Switches:** Two Cisco 2960 switches (`S1` and `S2`)
- **End Devices:** Six PCs
- **Network 1:** `192.168.10.0/24`
- **Network 2:** `192.168.20.0/24`

## IP Addressing

| Device | IP Address | Default Gateway |
|---|---|---|
| R1 — G0/0 | `192.168.10.1` | — |
| R1 — G0/1 | `192.168.20.1` | — |
| S1 — VLAN 1 | `192.168.10.2` | `192.168.10.1` |
| S2 — VLAN 1 | `192.168.20.2` | `192.168.20.1` |
| PC1 | `192.168.10.10` | `192.168.10.1` |
| PC2 | `192.168.10.11` | `192.168.10.1` |
| PC3 | `192.168.10.12` | `192.168.10.1` |
| PC4 | `192.168.20.10` | `192.168.20.1` |
| PC5 | `192.168.20.11` | `192.168.20.1` |
| PC6 | `192.168.20.12` | `192.168.20.1` |

Subnet mask for both networks: `255.255.255.0`.

## Security Features Implemented

### 1. Console and Privileged EXEC Security
Configured console passwords and `enable secret` to protect device access and privileged configuration mode.

### 2. SSH Remote Access
Enabled SSH version 2, created a local administrative account, generated RSA keys, and restricted remote terminal access to SSH.

### 3. Password Encryption
Enabled `service password-encryption` and used `enable secret` to improve password protection in device configurations.

### 4. Switch Port Security
Configured access ports to learn sticky MAC addresses, allow a maximum of one MAC address per port, and shut down a port when a security violation occurs.

### 5. Unused Port Shutdown
Disabled unused switch ports to reduce the risk of unauthorized devices connecting to the network.

## Connectivity and Security Testing
The following tests were performed:
- Ping from a PC to its default gateway.
- Ping between PCs on different networks.
- SSH access to the router and switches.
- Verification of port security and learned MAC addresses.
- Testing an unauthorized device on a secured switch port.
- Saving configurations using `copy running-config startup-config`.

## Results
- Router interfaces were configured for both networks.
- Connectivity between the two LANs was verified.
- SSH access to the router and switches was tested.
- Sticky MAC learning and port security were verified.
- An unauthorized device triggered a port-security violation.
- Unused switch ports were shut down.

## Technologies Used
- Cisco Packet Tracer
- Cisco IOS CLI
- IPv4 addressing and subnetting
- SSH version 2
- Switch port security
- MAC address learning

## Conclusion
The project provided practical experience in configuring a campus network and implementing essential network security controls. Router and switch configuration, SSH administration, password protection, port security, and connectivity testing helped demonstrate how a small university network can be made more secure.

## Project Files
- [`Secure_Campus_Network_Mini_Project_Report.pdf`](Secure_Campus_Network_Mini_Project_Report.pdf) — Detailed documentation and screenshots.
- `MiniProject.pkt` — Cisco Packet Tracer topology file, if included in this repository.
