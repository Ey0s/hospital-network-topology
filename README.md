Hospital Network Topology (DHCP Enabled)

This repository contains the network design and configuration for a simulated hospital environment using DHCP (Dynamic Host Configuration Protocol) to automate IP address allocation. The design includes multiple departments such as Emergency, Ward, Pharmacy, Laboratory, Server Room, and Office, interconnected via VLANs, routers, and multilayer switches to support secure, efficient, and dynamic IP addressing.

Network Overview

Each department operates in its own VLAN and receives IP configurations via a centralized DHCP server (or router-based DHCP service). This setup simplifies network management and allows devices to join and operate on the network without manual IP configuration.

| Department       | VLAN | Subnet         | DHCP Range            | Gateway       |
|------------------|------|----------------|------------------------|---------------|
| Pharmacy         | 10   | 192.168.1.0/24 | 192.168.1.10 - .100    | 192.168.1.1   |
| Laboratory       | 20   | 192.168.2.0/24 | 192.168.2.10 - .100    | 192.168.2.1   |
| CARD             | 30   | 192.168.3.0/24 | 192.168.3.10 - .100    | 192.168.3.1   |
| Ward             | 40   | 192.168.5.0/24 | 192.168.5.10 - .100    | 192.168.5.1   |
| Emergency        | 50   | 192.168.6.0/24 | 192.168.6.10 - .100    | 192.168.6.1   |
| Server Room      | 60   | 192.168.7.0/24 | Static IPs             | 192.168.7.1   |
| Office           | 70   | 192.168.8.0/24 | 192.168.8.10 - .100    | 192.168.8.1   |
| Lobby (WiFi)     | 80   | 192.168.9.0/24 | 192.168.9.10 - .100    | 192.168.9.1   |

### Routers:
- Router10 <--> Router11 connected via 10.1.1.1 / 10.1.1.2 for inter-network communication.

### Features

- Dynamic IP Allocation using DHCP for easier network management.
- Inter-VLAN Routing via multilayer switches.
- Static IPs reserved for critical infrastructure like servers and printers.
- Redundant servers for critical data storage (Main & Backup).
- WiFi access in lobby for mobile users via Access Point.
- Segmented VLANs to isolate traffic per department.

### Tools Used

- Cisco Packet Tracer(for simulation)
- Routers: Cisco 2911 (with DHCP and inter-VLAN config)
- Switches: Cisco 2960 & 3650 Series
- DHCP Server or DHCP-enabled Routers
- Clients: PCs, Laptops, Printers, Servers, Access Points

Created By

### Eyosyas
