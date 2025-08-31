---
description: Multiple input multiple output
---

# MIMO

Older radio standards are relatively simple and use a single digital signal processor (DSP) to perform modulation to a single antenna. Spatial diversity allows these earlier standards to use a second antenna, where one antenna is better positioned to receive or transmit signals. In previous notes, I introduced multiple input multiple output (MIMO) wireless systems. In OSI model terms this is a physical layer configuration which allows both the transmitter and receiver choose multiple radio interfaces.

MIMO is defined by N x M:S where:

* N is the number of transmits RF chains.&#x20;
* M is number of receive RF chains.&#x20;
* S is the number of streams.

<figure><img src="../.gitbook/assets/image (17).png" alt=""><figcaption></figcaption></figure>

IEEE 802.11n onwards allows each AP and node to have multiple sub-transceivers, or chains, each of which can operate a separate radio stream. In some cases, a node may use a receive-only chain. The simplest system will be 1x1:1, a single transmit chain, single receive chain, and a single stream.

IEEE 802.11ax may have up to 8 RF chains, but radios with different chain counts can communicate without difficulty. Normally, only the AP will have all eight chains and the number of data streams does not need to equal the number of chains. The actual throughput of the system is dependent on the number of streams.

MIMO can take advantage of spatial diversity. Antennas spaced slightly can utilise different paths and have separate data streams and now for the first time, multipath as an advantage: this is spatial multiplexing. Beamforming is a technique where multiple antennas interfere constructively to create a directional signal of higher amplitude for a specific receive node and is included from IEEE 802.11n onwards. The transmitter can estimate the location of its intended receiver based on timing between antennae. In IEEE 802.11ax, the receive node participates, explicitly giving feedback as to its location. A later revision of IEEE 802.11ac allows for MU-MIMO, where the AP can transmit to multiple clients simultaneously, this is multi-user MIMO. Multiple RF chains allow an AP to transmit to 4 separate clients simultaneously, IEEE 802.11ax will allow for 8 clients.
