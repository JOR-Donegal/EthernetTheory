# Beacons

Each AP announces its existence by means of a beacon. A beacon frame from the AP is issued every 100ms and broadcasts the:

* ESSID/SSID supported
* The BSSID
* The supported link rates
* Any management frames

Beacons are not acknowledged by clients. When clients want to join a wireless network begin by creating a list of visible BSSIDs. The client will select a BSSID based on the presence of the correct SSID, signal strength, supported link rates, and other information.

When a client moves, it will experience a signal drop from the AP to which it is connected. The client should look for a BSSID which offers the required SSID as a better signal strength, this is roaming. This does not always work and clients which have not properly implemented roaming are referred to as sticky clients. As the stick client choice to continue communicating with an out of range AP, it can interfere with communications in other cells. This results in excessive Co-Channel Interference (CCI).
