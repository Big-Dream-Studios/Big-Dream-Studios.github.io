# STUN Detection

There are two methods in the STUNDetection class.


## ** GetPublicEndpoint **

* `BOFA.STUN.STUNDetection.GetPublicEndpoint(UdpClient)`

Requires a UdpClient and will return the public IP address for that client, returns null if failed.

-----------------

## ** GetNATType **

* `BOFA.STUN.STUNDetection.GetNATType(UdpClient)`

Requires a UdpClient and will return a `BOFA.STUN.Models.NATType` depending on the UdpClient's determined NAT Type.
