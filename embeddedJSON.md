# Embedded JSON Tag for CBOR

This document specifies a tag for Embedding JSON Objects in Concise Binary Object Representation (CBOR) [1].

    Tag: 262
    Data item: byte string
    Semantics: Embedded JSON
    Point of contact: Ravi R <ravir@employees.org>
    Description of semantics: https://github.com/toravir/CBOR-Tag-Specs/blob/master/embeddedJSON.md

# Semantics

Tag 262 can be applied to a byte string (major type 2) to indicate that the byte string is 
a JSON Object. The length of the byte string indicates the content. 

# References

[1] C. Bormann, and P. Hoffman. "Concise Binary Object Representation (CBOR)". RFC 7049, October 2013.

# Author

Ravi R <ravir@employees.org>
