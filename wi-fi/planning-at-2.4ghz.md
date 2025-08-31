# Planning at 2.4GHz

One of the first things we do with wireless equipment, is tell it which country we are operating. Unfortunately, there are differences in channel availability and utilisation, from jurisdiction to jurisdiction. In earlier notes, I describe the 5 MHz channels available at 2.4 GHz.

Channels 12 and 13 are not available in the US and channel 14 is not available in Europe. But as always, it is more complicated than that. Each channel is 22 MHz wide. However, there is only 5 MHz between channels. If you are using channel 1, you overlap from 2.401 MHz to 2.423 MHz, you are interfering with all channels up to Channel 5. This is called adjacent channel interference (ACI).

Using 802.11 g or n, it may be possible to use Channels 1, 5, 9 and 11 with little overlap.

Even though there are 14 channels available, only 3 of them do not overlap with each other. The combination of 1, 6, and 11 is most commonly used.

If I am manually designing a 2.4 GHz radio network, I do it based on a cell network design with three frequencies.&#x20;

<figure><img src="../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

I manually ensure the maximum distance where an access point reuses a frequency channel. In practice this is only a partial mitigation. 2.4 GHz networks have good range and reasonable penetration through a house or business. When two or more APs are operating on the same channel, this results in co-channel interference (CCI). 2.4 GHz networks are horrible to plan, and the frequency band is extremely noisy. I live on a hill overlooking a plain and I can sniff 2.4 GHz beacons for perhaps 5 km. And they all interfere with my own use of those frequencies. If you have a single isolated AP, you could use wider channels. For instance, IEEE 802.11n allows for 40 MHz channels. In reality, apart from during channels, I should also be tuning power output. However, on any network above three APs, this becomes logistically infeasible. Such a network would really need to be controlled dynamically. For this reason, since the early 2000s, large wireless networks generally use a centralised controller.

The density of APs and the amount of overlap between adjacent APs depends on the application. For basic Wi-Fi coverage, we can have a low density. Where we need to be able to hand-off between APs for voice, we need a higher density.&#x20;

## Location

If we are doing positioning using multilateration, we need a greater density again. I have been working with indoor positioning since c. 2014 \[1] and outdoor location more recently \[2].

\[1] Ferry, E., O'Raw, J. and Curran, K., 2015. A Context-Aware Mobility Indoor Positioning System. _International Journal of Adaptive, Resilient and Autonomic Systems (IJARAS)_, _6_(1), pp.25-47.

\[2] Kelsey, C., Laverty, D. and O'Raw, J., 2022, June. Multilateration Method for Locating GNSS Spoofing Attacks Affecting Substation Clocks. In _2022 33rd Irish Signals and Systems Conference (ISSC)_ (pp. 1-5). IEEE.
