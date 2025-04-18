# 🏥Hospital Network Topology

This repository contains the network design and configuration for a simulated hospital environment. The design includes multiple departments such as emergency, ward, pharmacy, laboratory, server room, and office, interconnected via VLANs, routers, and multilayer switches to support secure and efficient communication.

## Network Overview

The network is segmented into various VLANs to isolate traffic and improve security. Key departments and their subnets include:

| Department       | VLAN | Subnet         | Gateway       |
|------------------|------|----------------|---------------|
| Laboratory       | 20   | 192.168.2.0/24 | 192.168.2.1   |
| CARD             | 30   | 192.168.3.0/24 | 192.168.3.1   |
| Ward             | 40   | 192.168.5.0/24 | 192.168.5.1   |
| Emergency        | 50   | 192.168.6.0/24 | 192.168.6.1   |
| Pharmacy         | 10   | 192.168.1.0/24 | 192.168.1.1   |
| Server Room      | 60   | 192.168.7.0/24 | 192.168.7.1   |
| Office           | 70   | 192.168.8.0/24 | 192.168.8.1   |
| Lobby (WiFi)     | 80   | 192.168.9.0/24 | 192.168.9.1   |

Routers:
- `Router10` <--> `Router11` connected via 10.1.1.1 / 10.1.1.2 for inter-network communication.

## Features

- Inter-VLAN Routing using multilayer switches.
- Redundant servers for critical data storage (Main & Backup).
- WiFi access for lobby users via Access Point.
- Segmented VLANs for security and traffic control.
- Printer availability in emergency and office areas.
- Laptops used in pharmacy and emergency for mobility.

## Tools Used

- Cisco Packet Tracer (for simulation)
- Routers: Cisco 2911
- Switches: 2960 & 3650 Series
- PCs, Laptops, Printers, Servers, Access Points



