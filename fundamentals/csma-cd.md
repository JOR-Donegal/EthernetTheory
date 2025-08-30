---
description: Carrier Sense Multiple Access with Collision Detection
---

# CSMA/CD

We have already discussed that with a shared medium, many devices contend for access. We need a protocol to police this contended access; Carrier Sense Multiple Access with Collision Detection or CSMA/CD. This protocol is still implemented fully, even on switched networks which perhaps don’t need it? We will cover switched networks in later notes.

When a device needs to transmit a frame, it first listens to see if the network is free. If the network is free, it issues a preamble, claiming the network. The preamble continues for long enough that every node on the network can detect the preamble and any collision. A collision occurs if a device tries to issue a preamble while another device has already started to issue one.

If a collision occurs, both nodes involved calculate a random time delay called exponential back-off. &#x20;

When a collision occurs;

1. Calculate _t_, the worst-case propagation time
2. _t_ = 51.2μS
3. After a collision (1) each station “backs off” either &#x30;_&#x74;_ or &#x31;_&#x74;_ and then retries
4. If another collision occurs (2) each station “backs off” either &#x30;_&#x74;_, &#x31;_&#x74;_, &#x32;_&#x74;_, &#x33;_&#x74;_ and then retries
5. If another collision occurs (3) each station “backs off” either &#x30;_&#x74;_, &#x31;_&#x74;_, &#x32;_&#x74;_, &#x33;_&#x74;_, &#x34;_&#x74;_, &#x35;_&#x74;_, &#x36;_&#x74;_, &#x37;_&#x74;_ and then retries
6. The chances of stations having a collision reduce exponentially.
