# VLANS

In the early 1990s our networks were single segments of Ethernet, wired with coaxial cable. Users with the same needs were (hopefully!) located adjacent to each other. For example, we could run an Ethernet network through the payroll department, locating their server and printer on the same LAN. Somewhere else, marketing people could have their LAN, with their own servers and printers.

<figure><img src="../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

These simple LAN designs were functional and we ended up with a guiding rule as to how to divide them. _We grouped users into a LAN if they had similar requirements for access to applications, services and information at a similar security level_. This remains our rationale for separating users even to this day.

The problems with our traditional design was that the physical network determined where our users could be located. This is very inflexible and inconvenient.

As wiring changed to twisted pair (e.g. CAT5, 5e, 6) and we began to use switches, opportunities emerged to separate the logical design of a network from its physical design.
