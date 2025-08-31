# Bridges

To fix the performance problems, we needed a device which would reduce the traffic on any network segment to only that traffic appropriate to that segment.

<figure><img src="../.gitbook/assets/image (3) (1) (1).png" alt=""><figcaption></figcaption></figure>

A bridge examines all the frames which propagate on a segment. It looks at the source MAC address in each frame and identifies which nodes are on which side of the bridge. It then records these in a MAC address table.

<table><thead><tr><th width="182">Device</th><th width="219.33333333333331">MAC</th><th>Port</th></tr></thead><tbody><tr><td>PC1</td><td>00 00 00 00 01</td><td>1</td></tr><tr><td>PC2</td><td>00 00 00 00 02</td><td>1</td></tr><tr><td>PC3</td><td>00 00 00 00 03</td><td>1</td></tr><tr><td>Server1</td><td>00 00 00 10 01</td><td>1</td></tr><tr><td>Server2</td><td>00 00 00 10 02</td><td>2</td></tr><tr><td>PC4</td><td>00 00 00 00 04</td><td>2</td></tr></tbody></table>

Whenever the bridge sees traffic now, it can decide whether it needs to forward it, and to which port. If the traffic is intended for a device on another segment, the bridge forwards it to that segment. If the frame is intended for a node on the same segment, the bridge drops the frame.

Traffic from PC1 to PC2 will not traverse the bridge; both nodes are on the same side.

Traffic from PC1 to Printer2 will traverse the bridge; the nodes are on different sides.

The advantage of this system is that we have the aggregate bandwidth of two links, 20 Mb/s available to us. If we had a third port on the bridge, we would have 30 Mb/s. We finally have a system which can scale and which allows us to build bigger networks, potentially without reducing performance.

Total available bandwidth = Segments \* 10Mb/s

When a bridge starts up, it does not have any entries in the MAC address table. When it sees a frame of data for a destination and it doesn’t know where to find the destination, it forwards the frame to every port, this is called _flooding_. It will receive a response from one port only and will update its MAC address table to match.

Each segment is a separate _collision domain_ but both segments are in the same _broadcast domain_.
