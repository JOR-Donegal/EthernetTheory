# Frame Size

There are complex issues like the size of the data payload in an Ethernet frame which must be considered. The idea of _jumbo frames_ is to make the payload the maximum size from an efficiency perspective. Decide if you plan to use jumbo frames and make sure everything in the path supports them. Don’t underestimate the complexity of getting this working and if you are mixing vendor equipment, beware! If you are implementing frames bigger than 1500 bytes on a backbone or across a WAN, you need to understand the _Maximum Transmission Unit_ (MTU) size your path can support. This is all also non-trivial and I have seen major contracts scuppered by inattention or a lack of understanding of the significance.

This quote from the [Ethernet Alliance](https://www.csd.uoc.gr/~hy435/material/EA-Ethernet%20Jumbo%20Frames%20v0%201.pdf):

“_It takes over 80,000 standard Ethernet frames per second to fill a 1 Gbps Ethernet pipe, consuming significant CPU cycles and overhead. Sending the same data with 9000-byte MTU Jumbo frames, only 14,000 frames need to be generated, with the reduction in header bytes freeing up 4 Mbps of bandwidth. For 10 Gbps Ethernet the maximum frame rate is 812,744 frames per second using the standard 1500-byte MTU, while with 9000-byte MTU Jumbo Frames the maximum frame rate is 138,581 frames per second._”&#x20;

You should also do some background reading on;

* TCP segmentation offload (TSO)
* Generic segmentation offload (GSO)
* Large receive offload (LRO)
