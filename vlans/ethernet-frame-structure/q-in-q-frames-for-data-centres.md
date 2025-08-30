---
description: IEEE 802.1ad
---

# Q-in-Q frames for Data Centres

In a data centre environment, we may use more complex versions of trunking. Q-in-Q allows us to have an outer tag, which might be used by the operator of a multi-tenant data centre. The inner tag may then be used by each tenant, giving every tenant their own access to 4096 VLANs and giving the operator 4096 tenants. It’s not quite that simple, but you get the idea!

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>
