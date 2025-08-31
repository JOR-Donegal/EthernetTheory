---
description: IEEE 802.1ac
---

# Ethernet Frame Structure

To support trunks/tagging, the IEEE decided to keep the existing Ethernet frame as much as possible. They added a 32-bit field in the middle!

<figure><img src="../../.gitbook/assets/image (4) (1).png" alt=""><figcaption></figcaption></figure>

The tag protocol identifier is set to 0x8100 to identify an IEEE 802.1ac frame.

The Priority Code Point (PCP) indicates the frame priority level

Drop Eligible (DE) indicates that the frame is eligible to be dropped in the presence of congestion

VLAN Identifier (VID) is a 12-bit field specifying the VLAN
