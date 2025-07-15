# Optimal-Network-Design-for-a-University-Campus

A VLAN-based network infrastructure designed for a university campus. This project demonstrates an optimized and scalable network topology using VLANs, Layer 2/3 switches, and structured IP addressing to ensure efficient data flow and logical separation of departments and offices.

## Project Overview

The design simulates a real-world university network, with each department or administrative unit segmented using VLANs. A multilayer switch provides inter-VLAN routing, while access switches connect multiple end devices per department. This structured topology improves manageability, performance, and security.

## Features

- VLAN segmentation for 7 major areas
- Centralized inter-VLAN routing using a multilayer switch
- Fixed IP subnet for each VLAN
- Scalable and modular design for future departments
- Hierarchical structure: Core → Distribution → Access layers
- Static IP addressing for clarity and control

## Components Used

- Cisco 2911 Router
- Cisco 3560 Multilayer Switch (Core Layer)
- Cisco 2960 Access Switches (One per department/office)
- End Devices: PC-PT and Laptop-PT (Two per VLAN)
- Ethernet cables (Straight-through and cross-over)
- Packet Tracer software for simulation

## VLAN Structure

| VLAN Name      | VLAN ID | Subnet           | Assigned To         |
|----------------|---------|------------------|----------------------|
| Department-1   | 10      | 192.168.1.0/24   | PC0, Laptop0         |
| Department-2   | 20      | 192.168.2.0/24   | PC1, Laptop1         |
| Department-3   | 30      | 192.168.3.0/24   | PC2, Laptop2         |
| Department-4   | 40      | 192.168.4.0/24   | PC3, Laptop3         |
| Library        | 50      | 192.168.5.0/24   | PC4, Laptop4         |
| Admin Office   | 60      | 192.168.6.0/24   | PC5, Laptop5         |
| Office-1/2     | 70      | 192.168.7.0/24   | PC6–7, Laptop6–7     |

## How It Works

1. All end devices connect to access switches configured with their respective VLANs.
2. Access switches are trunked to the central multilayer switch.
3. The multilayer switch is configured with SVIs (Switched Virtual Interfaces) for inter-VLAN routing.
4. A static IP is assigned to each device within its subnet.
5. Inter-department communication is routed through the core switch using Layer 3 capabilities.

## Limitations

- No DHCP server — requires manual IP assignment
- No wireless access points implemented
- No redundancy (single multilayer switch as core)
- No ACLs or firewall rules defined

## Future Improvements

- Add DHCP server for dynamic IP allocation
- Implement security policies using Access Control Lists (ACLs)
- Introduce wireless access points for campus-wide Wi-Fi
- Add STP or redundant links to avoid single points of failure
- Enable SNMP or NetFlow for network monitoring and analysis

## License

This network design project is open for educational and academic use.
