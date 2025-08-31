# Modulation

Different ways of using the radio spectrum have been experimented with throughout the history of Wi-Fi. Early versions of Wi-Fi used direct sequence spread spectrum (DSSS) and frequency hopping spread spectrum (FHSS) and these are still appropriate for low data rates (1-11Mbps).

Higher data throughput requires more sophisticated techniques. Higher bandwidths can be achieved using binary phase shift keying (BPSK), where a 180° phase change represents a bit. A transmission rate of one bit per symbol is achieved. With quadrature phase shift keying (QPSK), a 90° phase change can represent two bits, and a rate of two bits per symbol is achieved. These techniques were used by IEEE 802.11a and g.

For very high throughput, quadrature amplitude modulation (QAM) is used, the size of the constellation is dependent on the quality of the received signal. A constellation is created by having symbols at different phases and amplitudes. For example, 16QAM transmits 16 for bit symbols. IEEE 802.11ax uses 1024QAM.

As the technology has advanced, modulation schemes up to 32768QAM have entered into common usage, for example with ADSL. The bigger constellations all require high signal levels and very high signal to noise ratios.

## Orthogonal Frequency Division Multiplexing

There are better ways of using the radio spectrum than those that have described here. The term orthogonal means at right angles, or at 90°. In Orthogonal Frequency Division Multiplexing (OFDM), the spectrum is broken up into multiple sub carriers with a much slower symbol rate. Multiple carriers can have a guard interval between symbols, and this is affordable because there are multiple carriers.

This idea has been used in Wi-Fi technology from IEEE802.11a onwards.

## Orthogonal Frequency Division Multiple Access <a href="#hlk75251110" id="hlk75251110"></a>

Orthogonal Frequency Division Multiple Access (OFDMA) is a multi-user version of OFDM. Sub carriers are assigned by the AP to different nodes. When we began to work with outdoor wireless, and specifically with WiMAX IEEE802.16, it became obvious how powerful this technique was. This is also used in LTE mobile networks. From IEE 802.11ax onwards, this technology is utilised in Wi-Fi.

In OFDM, signals are still time division multiplexed, the AP deals with each client sequentially. With OFDMA, multiple clients can be dealt with simultaneously.
