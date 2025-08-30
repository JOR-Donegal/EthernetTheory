---
description: IEEE 802.1q
---

# Trunk/Tagged Ports

To logically separate broadcast domains on a network, the concept of VLANs were introduced. These allowed us to separate out groups of ports on one switch and connect them to groups of ports on other switches in the network, all at layer 2. Each VLAN looks like an independent Ethernet network but it can span the entire enterprise. _VLANs decouple physical network topology from logical network topology._

Just to keep things completely confusing, Cisco calls a connection where VLANs are transacted a trunk. Everyone else uses the term trunk to describe aggregating links together, e.g. aggregating two 1 Gb/s links between switches to make a 2Gb/s Link Aggregation Group (LAG). When anyone other than Cisco talks about VLANs between switches, they use the term _tagging_.

Completely confusing!

<figure><img src="../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

VLANs can be static, assigning switch ports to a VLAN. This is the most typical configuration we see. However, VLANs assignment can be automatic;

* By MAC addresses&#x20;
* By IP Addresses
* By User

This approach is reasonably secure and VLANs have been the basis for enterprise network design for much of the past 20 years.

However, to get a VLAN on one switch to talk to a VLAN on another switch, we need a trunked connection between the switches. A trunked connection carries the packets for multiple VLANs through a port on a default VLAN (normally VLAN 1). Each trunked packet has a VLAN ID based on the IEEE802.1q standard. Ethernet did not have any spare fields in its header so the IEEE802.1q standard modified the Ethernet frame and added these tags. Only trunk/tagged links between switches use these modified Ethernet frames.

The standard supports 4096 VLANs.

The port used for trunking is itself be in a VLAN. It can therefore pass tagged or untagged traffic. The untagged VLAN the port is in is called the native VLAN. Unexpected results and security issues may arise! It is best practice to make the native VLAN reserved and otherwise unused. If a switch receives untagged frames on a trunked switch port, they are assumed to be part of the VLAN that is designated on the switch port as the native VLAN.  Frames which egress a switch port on the native VLAN are not tagged.

VLANs were standardized as _IEEE802.1Q_
