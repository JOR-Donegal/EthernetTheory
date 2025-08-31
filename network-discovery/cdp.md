---
description: Cisco Discovery Protocol
---

# CDP

We can look at CDP on any network with Cisco equipment. Consider the following simple network in GNS3.

<figure><img src="../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

I add the following configuration on both switches to ensure CDP is on.

```
Switch22#conf t
Switch22#(conf) cdp enable
Switch22#exit
```

I can now detect any switches which are directly connected at Layer 2, using the command:

```
show cdp neighbors
```

<figure><img src="../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

And I can extract more using the **detail** option.

<figure><img src="../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

I extracted the following frame from GNS3 on Switch21.

<figure><img src="../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

This detail is available to anyone sniffing on a connected subnet! What a security vulnerability to assist anyone enumerating the network.

We leave CDP on briefly for configuration or for topology mapping when commissioning.&#x20;

It is common to disable CDP by using the command **no cdp run** as a global command or **no cdp enable** on an individual interface.

Some technicians will leave CDP on for trunk ports and switch it off on access ports. This helps debugging from the console but reduces the ability of clients to abuse it.&#x20;
