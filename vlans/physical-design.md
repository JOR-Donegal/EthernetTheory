# Physical Design

The physical design of a modern enterprise network is all about making sure we have;

* Adequate access connections at any wiring closet / floor distributor
* Aggregation of these connections if necessary
* Adequate redundant uplinks to the core

A detailed _physical diagram_ will show which ports are used and what communications medium (e.g. 1Gb/s CAT6 or OM3 MMF).

<figure><img src="../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

A physical LAN is difficult to reverse engineer using pings or other standard enumeration tools. Switches are (mostly) transparent to us.

We still need to group users based on requirements for access to applications, services and information at a similar security level. For this we need to look at the logical network design.
