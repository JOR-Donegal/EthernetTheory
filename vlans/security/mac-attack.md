# MAC Attack

The MAC or CAM tables in a switch have a limited size. When this table is filled, any frame for a destination address not in the CAM table floods to all ports, essentially becoming a hub.&#x20;

The MACOF tool (part of the DSNIFF suite) implements this attack.

Most vendors will have a mitigation strategy, on CISCO equipment, check the **port-security** commands.
