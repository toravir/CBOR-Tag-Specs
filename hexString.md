# Hex String Tag for CBOR

This document specifies a tag for Hex String in Concise Binary Object Representation (CBOR) [1].

    Tag: 263
    Data item: byte string
    Semantics: Hexadecimal String
    Point of contact: Ravi R <ravir@employees.org>
    Description of semantics: https://github.com/toravir/CBOR-Tag-Specs/blob/master/hexString.md

# Semantics

Tag 263 can be applied to a byte string (major type 2) to indicate that the byte string is 
a hexadecimal string - any normal string is stored as hexadecimal string, but this tag means
that string is to be kept as hex format and does not mean anything to convert to ASCII or anything.

# References

[1] C. Bormann, and P. Hoffman. "Concise Binary Object Representation (CBOR)". RFC 7049, October 2013.

# Author

Ravi R <ravir@employees.org>
