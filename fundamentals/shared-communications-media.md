# Shared Communications Media

Early Ethernet networks were small, with tens of devices per network, I worked on networks like these from the late 1980s until the mid-1990s, but they still exist out there.&#x20;

Layer 1 (the physical link) was a single cable interconnecting all the devices on the network. If a device wanted to transmit, it had to do so when the network was free and not in use by any other node.

<figure><img src="../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

To detect if the bus was free, each device listens for traffic and only attempts to transmit if no other node is doing so. If the network is free, the node which wants to transmit sends out a jamming signal or preamble, so every other node knows that it needs to use the bus.

The preamble needs to be long enough that it can reach every node on the bus before real data is transmitted. For an Ethernet network, that signal is 64 bits long. The actual algorithm for transmission is called _Carrier Senses Multiple Access with Collision Detection_ or CSMA/CD.

Every node on this shared bus can “hear” all traffic, making security non-existent. On reception of a frame, the node examines the destination address to determine whether the packet is for it or not. If not, it discards the packet.

Only one node can transmit at a time, so a conversation requires two devices to transmit alternately. This is called _half-duplex_, also called simplex. If a device can transmit and receive at the same time, this kind of network is called _full duplex_.
