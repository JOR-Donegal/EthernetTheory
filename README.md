# Introduction

In previous notes I note that data communications can be abstracted as seven layers. These seven layers are described in various ways and the language used to describe them can be very inaccessible.&#x20;

The simplest way to describe layer two is that it is the layer which allows a computer on a network to talk to another computer on the same local area network (LAN). Layer two connections can also be used between directly connected devices in a wide area network (WAN), but let’s park that definition for now.&#x20;

The most common protocol used for layer two is Ethernet, it has been in development since the 1970s, it has been standardized since the early 1980s and it has been the dominant layer 2 technology since the late 1980s. Take some time to do a little background reading regarding it.&#x20;

Ethernet is rarely used on its own, even in communications between nodes on the same network. Higher level protocols are more useful and at the application layer, Ethernet is almost transparent; we use layer 3 and IP for communications, configuration and programming. Because of the long history, some of the terminology you need to know is complex and arcane. We need to cover some of this history to explain how Ethernet works and why.&#x20;

Data is exchanged at layer 2 in a _Protocol Data Unit_ (PDU) called a _frame_.

## What defines Ethernet?

The IEEE are the most significant professional body in the world of electronics, data communications and computing. Their 802-standard series was intended to cover all the technologies used for a LAN, or layer two network. Most of these technologies are now obsolete and we will not consider them.

Ethernet was standardized as the 802.3 family of standards. This now runs to many volumes! You have full access to these standards on-line through the library database.&#x20;

Feel free to download.
