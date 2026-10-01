# CMPG325 - Tshepe Haulage Network
*Student:* MC-56
*Project:* Enterprise Network Design

## Overview
This repository contains the full network design for Tshepe Haulage company.

## VLANs
- VLAN 10 Management: 192.168.10.0/24
- VLAN 20 Sales: 192.168.20.0/24
- VLAN 30 Server-Farm: 192.168.30.0/24
- VLAN 40 Logistics: 192.168.40.0/24

## Devices
- SW1-Tshepe: L2 Switch with VLANs and trunk
- R1-Tshepe: Router-on-a-stick + DHCP + NAT
- ISP-Router: Internet simulation (8.8.8.8)

## Structure
- Configurations/ - Router and Switch configs
- All other folders contain documentation

## Key Fix
- Fixed err-disabled port Fa0/21 for Server connection
