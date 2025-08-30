# Repeaters

The simplest device we can use to extend the geographical range of a network is a _repeater_. One of the limiting factors on network segment length is that pulses become rounded and distorted as they propagate down a line. They also diminish in magnitude, becoming indistinguishable from noise. Since the earliest days of computing, we have had devices which took degraded signals in and regenerated them. These are layer 1 devices, they deal with physical bits, ones and zeros.

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

In early Ethernet networks, we extended the range of the network by joining multiple segments in this way. In 1996, Letterkenny campus' computer network consisted of four segments with a repeater between each. 800m of 10BASE2 network!

I have built industrial networks in the 1990s where we had multiple segments of 10BASE5, reaching over 1km.

Repeaters are long gone from Ethernet LANs, but we still use them in a range of applications. For example, long-haul data connections across countries and between continents use under-sea fibre optic cables. Every 90kms or so, there is an active repeater which takes the light pulses in, reshapes and retransmits them.
