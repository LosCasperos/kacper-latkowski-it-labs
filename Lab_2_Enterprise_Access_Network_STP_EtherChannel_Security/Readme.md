# Lab 2 – VLANs, STP, EtherChannel, Management VLAN, Layer 2 Security

## Overview
This lab simulates an enterprise-style access network with redundant switching, VLAN segmentation, spanning tree optimization, link aggregation, and Layer 2 security concepts.

The lab builds upon foundational VLAN and inter-VLAN routing knowledge and focuses on high availability, loop prevention, and management network separation, reflecting real-world campus access layer designs.

---

## Scope
- VLAN segmentation (user and management VLANs)
- Redundant access switches
- Spanning Tree Protocol (Rapid PVST+)
- EtherChannel (link aggregation)
- Management VLAN (VLAN 99)
- Inter-VLAN routing (Router-on-a-Stick)
- Basic switch and router hardening
- DHCP Snooping (tested and documented – disabled due to Packet Tracer limitations)

---

## Topology Summary
- Two access layer switches connected via EtherChannel
- Redundant trunk links with STP controlling loop-free topology
- Router-on-a-stick providing inter-VLAN routing and DHCP services
- Dedicated Management VLAN for switch management
- End devices placed in separate access VLANs

---

## Tools
- Cisco Packet Tracer

---

## Files
- **Lab_2_VLANs_STP_EtherChannel_Management_VLAN.pkt** – network topology  
- **Lab2_Documentation.pdf** – full step-by-step documentation with screenshots  
- **screenshots/** – directory containing all verification and troubleshooting screenshots  

---

## Verification
- Inter-VLAN connectivity verified using ICMP (ping)
- Management VLAN connectivity verified from access switches
- EtherChannel operational status verified
- STP root bridge and port roles verified
- DHCP address assignment verified after final configuration
- Full connectivity re-tested after security configuration

---

## Security & Design Highlights
- Management VLAN separated from user traffic
- Trunk ports explicitly configured (DTP disabled)
- Unused switch ports shut down and assigned to a parking VLAN
- EtherChannel used for redundancy and increased bandwidth
- Spanning Tree Protocol used to prevent Layer 2 loops

- DHCP Snooping was configured and tested but intentionally disabled due to
  Cisco Packet Tracer limitations when combined with EtherChannel and trunk links

---

## Troubleshooting Notes
During the lab, DHCP Snooping was configured and tested.
However, due to Cisco Packet Tracer limitations related to
EtherChannel and DHCP Snooping interaction, DHCP traffic was
incorrectly blocked despite correct configuration.

After analysis and validation, DHCP Snooping was intentionally
disabled to restore correct network operation. This behavior
and the decision-making process are fully documented in the
lab documentation.

---

## Status
**Completed** – this lab demonstrates enterprise access-layer
design principles and prepares the foundation for future labs
involving ACLs, dynamic routing, and advanced security mechanisms.
