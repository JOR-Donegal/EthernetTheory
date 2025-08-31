---
description: Logical Link Discovery Protocol
---

# LLDP

LLDP is the open standards equivalent of CDP and is the most appropriate protocol to use in a heterogeneous environment. For security and flexibility, it is probably better to only use LLDP and to switch off CDP.

We can set up LLDP locally on a per port basis. Generally, you can enable LLDP by typing **lldp run** and there may also be a per interface enabling option, normally **lldp transmit** and **lldp receive**.

In the same network as used previously, I disable CDP and enable LLDP. I then use the command

```
show lldp neighbors detail
```

<figure><img src="../.gitbook/assets/image (14).png" alt=""><figcaption></figcaption></figure>

LLDP is much more configurable and therefore secure. You can tailor which data is exchanged between devices. All data in LLDP is broken up into _Type Length Values_ (TLVs) and you can determine which TLVs are exchanged.&#x20;

We can set up LLDP globally.

<figure><img src="../.gitbook/assets/image (15).png" alt=""><figcaption></figcaption></figure>

I use LLDP during commissioning and again, disable it afterwards.
