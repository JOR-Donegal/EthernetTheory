---
description: IEEE 802.1p
---

# Priority and Quality of Service

At the same time as the Ethernet frame was being modified for VLANs, there was a demand to also include flags for quality of service.IEEE P802.1p was responsible for adding Quality of Service (QoS) or class of service (CoS) fields to the Ethernet frame. The combined with VLAN requirements to create a new frame format called IEEE802.1ac.The quality of service bits are:

| PCP | Priority | Acronym | Traffic Types                      |
| --- | -------- | ------- | ---------------------------------- |
| 0   | 0        | BK      | Background                         |
| 1   | 1        | BE      | Best Effort                        |
| 2   | 2        | EE      | Excellent Effort                   |
| 3   | 3        | CA      | Critical Applications              |
| 4   | 4        | VI      | Video, < 100 ms latency and jitter |
| 5   | 5        | VO      | Voice, < 10 ms latency and jitter  |
| 6   | 6        | IC      | Internetwork Control               |
| 7   | 7        | NC      | Network Control                    |
