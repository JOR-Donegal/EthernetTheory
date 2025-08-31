# Switches

The next evolution in LAN design was to combine the wiring convenience of a hub with the scalability of a bridge and create a device called a network switch. A switch is a multi-port bridge which maintains a MAC address table with entries for every port.

<figure><img src="../.gitbook/assets/image (4) (1) (1).png" alt=""><figcaption></figcaption></figure>

The wiring interface is an RJ45 connector again, which has separate transmit and receive lines. Each connection to the switch has only one PC on it and is a single collision domain. Therefore, collisions can’t really occur and a 10Mb/s switch has 10Mb/s each way, 20 Mb/s in total available bandwidth per node.

We have provided a separate network segment for transmit and receive, for each node on the network. The performance increase was staggering. Modern office switches have ports from 100 Mb/s to 1Gb/s and in data centre environments, speeds of up to 100 Gb/s are common.

Switches look at ingress frames and store their MAC addresses in the MAC address table. They then make forwarding decisions to select the appropriate port for traffic which must egress.

Flooding works on a switch exactly as it did with a bridge. When a switch starts up, it does not have any entries in the MAC address table. When it sees a frame of data for a destination and it doesn’t know where to find the destination, it floods the frame to every port.

For a very small site with a single switch, we can use an unmanaged switch. This is a simple device which has fixed silicon allowing it to act as a switch.

For most sites, we specify a managed switch. This is a switch with an integrated computer. We can access this computer to configure, manage and monitor the switch.
