---
description: Link Aggregation Control Protocol
---

# LACP

The IEEE standardized 802.3ad c.2000 and all equipment that I use can operate this standard. From 2008, this was superseded by IEEE 802.3AX.

LACP frames (LACPDUs) are sent with a multicast MAC address 01:80:C2:00:00:02 and a stay alive packet is sent periodically on each member of the link. Within the standard, devices on either side of a link can detect the posture of each other and can bring up as many links as are configured for LACP, or default to a single link is the connected device has not LACP enabled.

## Port Aggregation Protocol (PAGP)

This is a Cisco proprietary protocol and should not be used.

## Bonding

In Linux, it is possible to [bond](https://help.ubuntu.com/community/UbuntuBonding) several interfaces together to form an LACP link. This allows a single server to be inexpensively scaled and provided with resilient links.

## Teaming

In Microsoft operating systems, the same is true, but we call this [teaming](https://docs.microsoft.com/en-us/windows-server/networking/technologies/nic-teaming/nic-teaming).
