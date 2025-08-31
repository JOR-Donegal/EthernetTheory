# Enterprise Network Design

As you could see, planning a network at 2.4 GHz is messy and I only covered the basics. You are so constrained by having to design a three cell network. There is another issue, a cell at a frequency will interfere with all adjacent cells using the same frequency. Its all complicated!

In reality, once there are more than 3 APs on a site, I can't really control the site in an optimal way. Something like a van pulling up out front will increase multi-path and degrade two adjacent APs on the same frequencies.&#x20;

Ideally, this would all happen automatically. With 5.8 GHz APs, some of this is automatic, some frequencies are required to operate Transmitter Power Control (TPC). Some APs will use Dynamic Frequency Selection (DFS) to find a quiet channel on which to operate.

In Enterprise design, we are more likely to use an Enterprise Wireless Controller. This is a single appliance which orchestrates large wireless networks. Each AP will connect to the controller via a specific protocol like Control And Provisioning of Wireless Access Points ([CAPWAP](https://datatracker.ietf.org/doc/html/rfc5415)). It may appears that a VPN exists between the controller and the AP. The AP can be frequency and power agile, adapting in real-time to changes in topology or the wireless environment. &#x20;

Once you have a view of multiple APs, you can add some functionality and identify the position of any Wi-Fi device (and its user)  \[1] using quadrilateration \[2].

You can also extract inventory information, security information, the list of functions is extensive. Do some background reading on the functionality in Cisco's Wireless LAN controllers.

\[1] Ferry, E., O'Raw, J. and Curran, K., 2015. A Context-Aware Mobility Indoor Positioning System. _International Journal of Adaptive, Resilient and Autonomic Systems (IJARAS)_, _6_(1), pp.25-47.

\[2] Kelsey, C., Laverty, D. and O'Raw, J., 2022, June. Multilateration Method for Locating GNSS Spoofing Attacks Affecting Substation Clocks. In _2022 33rd Irish Signals and Systems Conference (ISSC)_ (pp. 1-5). IEEE.
