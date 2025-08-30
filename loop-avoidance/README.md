# Loop Avoidance

Ethernet was designed as a simple layer 2 protocol and the designers never really considered that loops might be possible on a network. This is reasonable when you consider that Ethernet networks were originally single lengths of COAX.

But then bridges came along and the possibility existed that in a bridged network, we could have loops. Loops could be inadvertent; introduced into a network by mistake by means of one wrong cable patch. Loops can also be desirable; it might be that additional paths are created in a network topology for high availability, load balancing or redundancy. However, once frames of data circulate endlessly, our network will quickly saturate to 100%.

The protocol we use to mitigate this problem views the layer 2 network as a tree and identifies a topology such that there is only one path between any two nodes in the tree; this is a spanning tree.

We send _Bridge Protocol Data Units_ (BPDUs) between bridges. If a bridge emits a BPDU, other bridges respond. If there is no response, the other node is not a spanning tree capable bridge; it is probably a PC or an unmanaged switch.

Through the notes we may use the terms _bridge_ and _switch_ interchangeably!

The original [paper](https://dl.acm.org/doi/pdf/10.1145/318951.319004) which proposed the protocol was by Radia Perlman (c.1985) \[1] and is readily available on the internet. Obtain a copy now and read through it; you must admire someone who can summarise an algorithm as a poem!&#x20;

The original Digital Equipment Corporation (DEC) implementation may still exist in the wild!

The IEEE issues a standards-based version as IEEE 802.1D c. 1990 and this was superseded by Rapid Spanning Tree Protocol (RSTP) as IEEE 802.1W c.2004.



\[1] Perlman, R., 1985. An algorithm for distributed computation of a spanning tree in an extended LAN. _ACM SIGCOMM computer communication review_, _15_(4), pp.44-53.
