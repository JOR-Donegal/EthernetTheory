# Contention

In previous notes I described contention mechanisms used by Ethernet. Carrier Sense Multiple Access with Collision Detection (CSMA/CD) works on wired shared Ethernet media. In the same broadcast domain, there is no case where a station can emit a preamble, without it being visible to every other station in the same broadcast domain.

Wireless networks are little different. Firstly, if wireless is half duplex, and the station cannot transmit and receive at the same time, then it can hardly detect a collision. In previous notes, I discussed the difference in power levels between transmit and receive. Any distant signal will be dwarfed by the transmit power of any node simultaneously transmitting and receiving.

Secondly, the visibility of all stations on wireless network to each other is not guaranteed. For example, I might be able to see an AP at maximum range, another laptop may be able to see the same AP at maximum range, but we cannot see each other. This is called the hidden node problem.

Networks use Carrier Sense Multiple Access with Collision Avoidance (CSMA/CA). A node which wishes to transmit listens to ensure no other notice transmitting. If the network is quiet, the packet will be entirely transmitted. The sending node then waits for an acknowledgement from the AP. If such an acknowledgement does not arrive, the sending node assumes a collision has occurred. It then uses binary exponential backoff to wait for a random period before retransmitting.

The standards also allow for semaphore between the AP and the sending node. A node could send a request to send (RTS) packet to the AP. The AP could respond with a clear to send (CTS) packet to the single note, guaranteeing a clear channel. However, the overhead of this semaphore would be significant, especially where packets are small.

We know this the 2.4 GHz band is very noisy. To determine whether a node is active, we need a power threshold. The noise floor can be assumed to be c.-100dBm with 20 MHz channels. Any signal 3dB be greater than this will be assumed to be above the threshold. The threshold is dependent on frequency and wireless standard used.
