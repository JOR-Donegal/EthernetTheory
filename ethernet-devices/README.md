# Ethernet Devices

By the 1990s Ethernet had emerged as the de-facto LAN standard standard for most applications.  It was cheap, simple, reasonably open and it worked well with low load and a low number of nodes.

Busy networks were rumoured to experience very low efficiency. There is a myth based on an early study that 37% is the peak load on shared Ethernet \[1]. Although many textbooks still state this, the empirical data does not back it up \[2]. There is a standard joke amongst engineers that Ethernet does not work in theory, but does in practice!

We did have other real problems though. Because the network was one _collision domain_, it was not scalable. _Binary Exponential Standoff_ is not effective once the number of nodes is greater than 200.

We fixed some of the problems of segment length by using repeaters. We fixed some of the issues of scale by using hubs. However, the aggregate available bandwidth was still 10 Mb/s and we were still sharing 10Mb/s half duplex amongst all the nodes. The bigger the networks got, the less bandwidth per node. This became our main problem. I will explain these terms and what they means in these notes.

This is not a history lesson!

You cannot understand Ethernet without understanding how the devices and practices evolved.

\[1] Robert M. Metcalfe and David R. Boggs, “Ethernet: Distributed Packet Switching for Local Computer Networks”. Communications of the ACM 19(7):395-404, July, 1976

\[2] Boggs, Mogul, and Kent, “Measured Capacity of an Ethernet: Myths and Reality”, Proceedings of the SIGCOMM ’88 Symposium on Communications Architectures and Protocols, ACM SIGCOMM, Stanford, California, August 1988
