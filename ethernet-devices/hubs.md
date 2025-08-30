# Hubs

When twisted pair CAT3 phone wiring began to be used for data, we collapsed the backbone into a box called a _hub_. A hub is just a multi-port repeater with multiple phone type connectors called RJ45. This box was still a layer 1 device, it repeats electrical bits without understanding them. This changed the topology of our networks from bus to star and made networks cheaper and easier to implement and more reliable. The total available bandwidth was still 10Mb/s so our networks still didn’t scale very well.

<figure><img src="../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

This was still shared media, so the same problem of scaling applied; good for twenty nodes, not good for 200.
