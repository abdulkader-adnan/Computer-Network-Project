# 🌐 Computer Network Project

This repository contains the documentation and network simulation file for a comprehensive enterprise network project. The project involves designing, implementing, and verifying a complex network topology that interconnects a main office, a branch office, and remote users.

## 🚀 Key Features

* **Network Design & Subnetting:**
    * Advanced `VLSM` (Variable Length Subnet Mask) design for multiple `VLANs` (e.g., `VLAN 5`, `15`, `35`, `45`, `55`, `65`, `75`, `130`).
    * Detailed IP addressing scheme for all network devices, servers, and hosts.

* **Layer 2 Configuration:**
    * `VLAN` creation and management across all switches.
    * Configuration of `802.1Q` trunking for inter-switch communication.
    * Implementation of `LACP EtherChannel` for link aggregation.
    * Inter-VLAN routing configured on Layer 3 switches.

* **Layer 3 Routing:**
    * **`OSPFv2`:** Implemented as the IGP for the main site (`Main-MLS`, `S-MLS`, `MIU-GW`).
    * **`EIGRP`:** Implemented as the IGP for other parts of the network (`N-MLS`, `R-MLS`, `MIU-GW`).
    * **Route Redistribution:** Configured on `MIU-GW` to connect the `OSPF` and `EIGRP` routing domains.
    * **Static & Default Routing:** Configured for `ISP` connectivity.

* **Network Services:**
    * **`DHCP Server`:** Provides dynamic IP addressing for multiple `VLANs`.
    * **`DHCP Relay`:** Configured on L3 switches (`Main-MLS`, `S-MLS`) to forward requests.
    * **`NAT`:** Includes `Static NAT` and `Dynamic NAT` with `PAT` (Port Address Translation).
    * **Servers:** Deployment of `DNS`, `Web (HTTP)`, `Email`, `NTP`, and `Syslog` servers.

* **Security:**
    * Basic device hardening (e.g., encrypted passwords, `secret` passwords).
    * Secure remote access via `SSH`.
    * **Site-to-Site `IPsec VPN`:** Configured to secure traffic between `MIU-GW` (Main) and `Branch-GW` (Branch).

* **Wireless:**
    * Configuration of a wireless home router with `WPA2 Personal` security.
