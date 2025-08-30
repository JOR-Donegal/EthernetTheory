# Functionality

Modern networks are based on switches; but in many ways, switches are just multi-port bridges, so when we use the term bridge, think about it as a switch on a modern network.

When we start up a switch it does not forward traffic.

Initially each port on the switch is set to blocking mode.

When you plug in a cable, the port goes into listening mode and awaits traffic (default 15 seconds). In Packet Tracer, the port goes orange, real switches behave similarly. If the newly connected port carries BPDUs, the switch knows that a new switch has been connected. However, it is not forwarding traffic, so no loop occurs.

If there are no BPDUs received, the connection is not a switch and the port will go into a learning phase, identifying all the MAC addresses on this segment. During the learning phase, the bridge observes the source addresses on the frame received on each port and records these in the filtering database as dynamic entries. Bridges may also allow the administrator to insert static entries in this table, which will take priority. Dynamic entries have an ageing time, typically 300 seconds. If the source frame is not seen again on a port in that time, it ages-out and is removed from the filtering table. This is to allow for the movement or removal of nodes in a network.

After a period (default 15 seconds) in the learning phase, the port goes into forwarding mode, where it forwards frames and just works as we would expect. In this state, frames submitted to the bridge through a reception port. They are forwarded through to the port where the destination MAC address is located, the transmission port, assuming this port is also in a forwarding state. A frame will never be sent back out the port on which is was received. Every bridge will have a filtering database which identified where to forward the frame based on its destination MAC address. Frame will then be queued or buffered, awaiting an opportunity to be transmitted. If the destination address is not in the filtering database, the bridge has no way to know where to forward the frame to. In this case, it will flood the frame out every port.

When you plug a PC into a switch which has STP enabled, it may not come up for 30 seconds or more. STP is also this slow when a topology change occurs, e.g. when a switch is removed from the network or reset. This is just too slow. A newer protocol was standardized in 2001 called Rapid Spanning Tree (RSTP), which can respond much more quickly.
