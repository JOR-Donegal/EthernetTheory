# Double Encapsulation

A client computer can connect to a switch and double encapsulate a frame. This switch will strip off the first encapsulation and then forward the frame. The second switch the frame reaches will remove the second encapsulation and forward the frame to a target VLAN. This attack is one way only.

By fixing client ports to be access only, this attack vector can be reduced. We also need to make sure that trunk connections use a dedicated unique VLAN ID, not the default of 1.
