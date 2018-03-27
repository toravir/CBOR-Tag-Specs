# Network Address Tag for CBOR

This document specifies a tag for Network Addresses in Concise Binary Object Representation (CBOR) [1].
Network Addresses include IPv4 Address, IPv6 Address and MAC Address.

    Tag: 260
    Data item: byte string
    Semantics: Network Address (IPv4 or IPv6 or MAC Address)
    Point of contact: Ravi R <ravir@employees.org>
    Description of semantics: https://github.com/toravir/CBOR-Tag-Specs/blob/master/networkAddr.md

# Semantics

Tag 260 can be applied to a byte string (major type 2) to indicate that the byte string is 
IPv4 or IPv6 or MAC Address. The length of the byte string indicates the content. 
If the length is
 4 bytes => IPv4 Address
16 bytes => IPv6 Address
 6 bytes => MAC  Address

The addresses are stored in binary values in network byte order.

# Examples

190103 44c00a0a01     --> IPv4 address 192.10.10.1
190103 460123456789ab --> MAC address 01:23:45:67:89:ab
190103 5420010db885a3000000008a2e03707334 --> IPv6 address 2001:db8:85a3::8a2e:370:7334

# References

[1] C. Bormann, and P. Hoffman. "Concise Binary Object Representation (CBOR)". RFC 7049, October 2013.

# Author

Ravi R <ravir@employees.org>
