# Wireless Security & AAA (RADIUS / TACACS+)

An enterprise wireless network simulation built in Cisco Packet Tracer, 
implementing centralized authentication, authorization, and accounting (AAA) 
with VLAN segmentation and comprehensive security policies.

## Overview

This project simulates a secure enterprise wireless environment with three 
segmented SSIDs managed through a Cisco WLC, centralized AAA via RADIUS and 
TACACS+, and layered security including ACL, Port Security, and Syslog monitoring.

## Technologies Used

- **AAA:** RADIUS, TACACS+
- **Wireless:** Cisco WLC-3504, Lightweight Access Points
- **VLANs:** VLAN 10 (Personel), VLAN 20 (Yönetim), VLAN 30 (Misafir), VLAN 99 (MGMT)
- **Security:** ACL, Port Security, MAC Address Filtering
- **Monitoring:** Syslog
- **Services:** DHCP, Inter-VLAN Routing

## Network Topology

| Segment | VLAN | Subnet | Ports |
|---------|------|--------|-------|
| Personel | 10 | 192.168.10.0/24 | 1-10 |
| Yönetim | 20 | 192.168.20.0/24 | 11-20 |
| Misafir | 30 | 192.168.30.0/24 | — |
| MGMT | 99 | 192.168.99.0/24 | — |

## Key Configurations

- **RADIUS:** Centralized authentication for wireless users per SSID
- **TACACS+:** Device administration authentication for network equipment
- **ACL:** Extended ACLs permitting only necessary traffic per VLAN
- **Port Security:** MAC address restriction with violation shutdown
- **Syslog:** Centralized logging to 192.168.102.2
- **WLC:** Three SSIDs mapped to respective VLANs

## Files

| File | Description |
|------|-------------|
| `wireless-ACL-PortSecurity-Syslog-Radius-Tacacs+.pkt` | Main Packet Tracer file |

## How to Open

1. Download and install [Cisco Packet Tracer](https://www.netacad.com/courses/packet-tracer)
2. Open the `.pkt` file
3. Use Simulation Mode to test authentication workflows
