# Algorithm

For every path through the tree, we need a path cost. The slower the link, the higher the cost. We will prefer to use the lowest cost path (fastest) between any two points.

At its simplest, there are four steps to the algorithm used in spanning tree.

1. We need all the switches in the network to elect a root. Decide on one switch which will be the root of the tree. The switches all exchange BPDUs to elect the root.

We will need to intervene on a real network. The algorithm picks the switch with the lowest MAC address as the root. This might not be the most powerful or central switch on a network. As it’s the lowest MAC address, it is often the oldest and most disreputable switch!

We will always select a central core switch to be root and this will be demonstrated in practical sessions.

<figure><img src="../.gitbook/assets/image (6) (1).png" alt=""><figcaption></figcaption></figure>

2. Each switch identifies the port which has the lowest cost to get to the root. This will be the root port of that switch (RP).

<figure><img src="../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

3. For each network segment, the port on a switch which offers the lowest cost to get to the root will be called the designated port (DP).

<figure><img src="../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

4. All other paths will now be disabled, there will only be one path between any segment and the root.

<figure><img src="../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

A network where all the switches have settled down into a stable topology is said to have converged.
