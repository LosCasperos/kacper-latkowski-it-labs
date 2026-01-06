Lab 1 – VLAN, Inter-VLAN Routing, DHCP, Basic Hardening

## Overview
This lab simulates a small enterprise access network with multiple VLANs, 
inter-VLAN routing using router-on-a-stick, centralized DHCP, and basic Layer 2 
and router hardening techniques.

The goal of this lab is to practice foundational switching and routing concepts 
commonly used in real-world network environments.

## Scope
- VLAN configuration
- Inter-VLAN routing (router-on-a-stick)
- DHCP server
- Basic device hardening

## Topology Summary
- Single Layer 2 switch with multiple access VLANs
- Router-on-a-stick used for inter-VLAN routing
- Trunk link (802.1Q) between switch and router
- End devices obtain IP configuration via DHCP

## Tools
- Cisco Packet Tracer

## Files
- Lab_1_VLAN+Inter-VLAN_Routing+DHCP.pkt – topology
- Lab1_Documentation.pdf – full documentation

## Verification
- Inter-VLAN connectivity verified using ICMP (ping)
- DHCP address assignment verified on router and end devices
- Configuration re-tested after security hardening

- ## Security Highlights
- Unused switch ports shut down and assigned to a parking VLAN
- Port security enabled on access ports (sticky MAC, restrict mode)
- DTP disabled on trunk interface
- Basic router hardening (password encryption, MOTD banner)

## Status
Completed – this lab serves as a foundation for future labs involving ACLs, 
management VLANs, and extended security configurations.
