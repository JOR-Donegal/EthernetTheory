# Network Discovery

It can be quite a bit of work to understand the connections in a network. What switches are connected where, to what routers, with what devices? In a data centre, it is even more complex. You are working remotely on a server in a cabinet, but the server has six network connections, there are 32 servers in that cabinet, and it is in a row of 20 cabinets. Which cable is wrong?

Protocols have existed for some time that allows devices to identify each other and to exchange subsets of information.

Cisco Discovery Protocol (CDP) is one such standard. It is proprietary, but given Cisco’s market penetration, is probably the best known of the discovery protocols. CDP is on by default on all CISCO equipment except the firewall ranges like ASA. It is a layer 2 broadcast protocol; the information is propagated with an Ethernet address of all “1”s or FFFFFFFFFFFF. As this is a layer 2 protocol, you do not need to configure anything to make this work, not even an IP address.

Logical Link Discovery Protocol (LLDP) is the open standards equivalent of CDP and is the most appropriate protocol to use in a heterogeneous environment.
