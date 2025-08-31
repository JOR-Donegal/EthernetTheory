# Link Aggregation

On a busy LAN one thing we can be sure of is that there is never enough bandwidth on the major uplinks. In the period 2000-2010, we outgrew gigabit links, but the costs of upgrading to 10 Gb was prohibitive. We used multiple uplinks and played tricks with Spanning Tree so there was some form of load balancing. We can have multiple path’s at layer 3, and there are ways we can share bandwidth. But in many cases what we really want is more bandwidth at layer 2.

Link aggregation is a technique which allows us to bond multiple ethernet connections, so they appear as a single, multiplexed, layer 2 path. A Link Aggregation Group (LAG) is the collective term for these links. There are a few different protocols in use, and different manufacturers have different names for the same things. There were originally many proprietary protocols, but now there are two protocols in most common use.

Consider a network with legacy Cisco 6513 switches. You could terminate >500 gigabit ethernet clients to such a switch, and its original cost may have been >€100k. And in many cases the reason you need to replace the switch is because it did not easily facilitate 10 Gb/s uplinks. When I first bought XENPAC 10 Gb/s technology, the price was equivalent to a 4 Wheel Drive SUV for each switch.

As an alternative, I could estimate the number of links I needed at 1 Gb/s and bond those links together. This was a much more scalable and economic solution. And as layer 2 is transparent to most network applications, these bonded links have no negative impact.

There is another modern application for bonding links. When I design a rack in a data centre, I use two 10GB/s Top of Rack (ToR) switches to terminate the workloads of each server. It is normal to bond these, the result is a 20GB/s link with redundancy.&#x20;
