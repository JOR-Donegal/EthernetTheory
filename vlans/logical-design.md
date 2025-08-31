# Logical Design

A logical diagram of the network shows it in the original terms in which we wanted it, divided up into LANs based on requirements.

We see the logical LAN as an IP packet would see it. We know;

* Its name, which should be descriptive!
* Its VLAN tag ID
* Its associated IP address range

Its gateway address. There may be more than one router but we need a clear indication of the gateway IP.

<figure><img src="../.gitbook/assets/image (2) (1).png" alt=""><figcaption></figcaption></figure>

In the diagram, router 12 uses the last octet .12 in every subnet. This is typical, however, many network designers always put their routers on .1 or .254.  If there is a consistent pattern, all are valid.

Typically, we will route at the aggregation layer and/or the core.

In a real network, any of the VLANs above can be assigned to any port on any switch. So how do we achieve this?
