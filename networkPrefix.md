# Network Prefix Tag for CBOR

This document specifies a tag for Network Address Prefix in Concise Binary Object Representation (CBOR) [1].
Network Addresses Prefixes is either a IPv4 Address+SubnetMask or IPv6 Address+SubnetMask

    Tag: 261
    Data item: MAP (IPAddress + Mask Length)
    Semantics: Network Address Prefix (IPv4 or IPv6 Address + Mask Length) 
    Point of contact: Ravi R <ravir@employees.org>
    Description of semantics: https://github.com/toravir/CBOR-Tag-Specs/blob/master/networkPrefix.md

# Semantics

Tag 261 can be applied to a Map to indicate that the Map contains an IPv4/IPv6 Prefix.
Prefix is IP Address (v4 or v6) + Mask Length. The Map's length is set to 1 inorder to
indicate there is one network Prefix in the map.

The first item (aka key)  in  the  MAP is a byte string of IPv4 or IPv6 Address. 

The Second item (aka value) in the MAP is an unsigned integer indicating prefix length.

IP Address is stored in network byte order. There is no need for additional NetworkAddress Tag for
the first element (IPv4 or v6 Address).

# Examples
```
d90105 a1 4400000000 00    ==> IPv4 Prefix 0.0.0.0/0
d90105 a1 44c0a80064 1818  ==> IPv4 Prefix 192.168.0.100/24
```
# References

[1] C. Bormann, and P. Hoffman. "Concise Binary Object Representation (CBOR)". RFC 7049, October 2013.

# Author

Ravi R <ravir@employees.org>
