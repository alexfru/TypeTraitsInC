The presentation slides and the sample code (TBD) demonstrate how to implement
type traits in C somewhat similar to those that can be implemented in C++ with
templates. This is achieved through construction of "self-descriptive types".

The technique lets the programmer write more generic C code that is still type-
aware and abstract away and hide most of the type-specific machinery while also
making coding less error-prone.

As an example of the technique the presentation shows how one can greatly
simplify handling of byte order (AKA endianness) conversions by introducing
types like little_endian_uint32_t and big_endian_uint16_t and just 2 macros
(EGET() and ESET()) that the programmer has to use to achive the goal as opposed
to using the following battery of similarly looking and easy-to-confuse macros:
htonl(), ntohl(), htons() and ntohs().
