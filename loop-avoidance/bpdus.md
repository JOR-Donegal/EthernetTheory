---
description: Bridge Protocol Data Units
---

# BPDUs

Several types of BPDU exist to transfer information through a bridged network. I captured these using Wireshark in GNS3.

### Configuration BPDUs

<figure><img src="../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

This PDU holds the following fields of data.

1\.      The Protocol Identifier is encoded in Octets 1 and 2. It takes the value 0000 0000 0000 0000.

2\.      The Protocol Version Identifier is encoded in Octet 3. It takes the value 0000 0000 for STP and 0000 0010 for RSTP.

3\.      The BPDU Type is encoded in Octet 4. This field takes the value 0000 0000 for STP and 0000 0010 for RSTP. This denotes a Configuration BPDU.

4\.      Octet 5 contains flags which differ per version between STP and RSTP.

5\.      The Root Identifier is encoded in Octets 6 through 13.

6\.      The Root Path Cost is encoded in Octets 14 through 17.

7\.      The Bridge Identifier is encoded in Octets 18 through 25.

8\.      The Port Identifier is encoded in Octets 26 and 27.

9\.      The Message Age timer value is encoded in Octets 28 and 29.

10\.   The Max Age timer value is encoded in Octets 30 and 31.

11\.   The Hello Time timer value is encoded in Octets 32 and 33.

12\.   The Forward Delay timer value is encoded in Octets 34 and 35.

13\.   RSTP has an extra Octet 36 which is not currently used and is set to 0000 0000.

### Topology Change Notification BPDUs

1\.      The Protocol Identifier is encoded in Octets 1 and 2. It takes the value 0000 0000 0000 0000.

2\.      The Protocol Version Identifier is encoded in Octet 3. It takes the value 0000 0000.

3\.      The BPDU Type is encoded in Octet 4. This field takes the value 1000 0000 (where bit 8 is shown at the left of the sequence). This denotes a Topology Change Notification BPDU.

The root bridge sends a Hello Message periodically based on the HELLO\_TIME setting. Each designated bridge sends a hello message to the LAN for which it is designated. Thus only one bridge per LAN should ever egress hello frames.

The Ethernet address 01:80:C2:00:00:00 is used and the message includes;

* The transmitting bridge ID
* The ID of the root bridge
* The length of the best path to the root
* A local link identifier
* A timer value called MAX\_AGE; if no hello messages are received for MAX\_AGE the tree will be recomputed.

Each bridge uses the information in the configuration BPDU to calculate the best path from itself to the root bridge.
