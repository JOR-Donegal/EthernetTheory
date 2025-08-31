# Ether Channel

As always, Cisco have their own way of doing things! They bought in their own channel bonding technology c. 1994, long before there were inter-operable standards. Originally, up to eight ports may be bonded, if these are 10 Gb/s, this implies the creation of an 80 Gb/s channel. There is some variation depending on hardware.

Traffic passes through a link depending on a proprietary hashing algorithm, which can use source or destination MAC addresses, IP addresses, or ports.

The failure of any individual link will result in its traffic been distributed amongst the remaining links.
