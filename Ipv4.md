## IPV4
IPv4 addresses are 32-bit numbers that are typically displayed in dotted decimal notation. A 32-bit address contains two primary parts: the network prefix and the host number. All hosts within a single network share the same network address. Each host also has an address that uniquely identifies it.

## IPv4 Classful Addressing

To provide flexibility in the number of addresses distributed to networks of different sizes, 4-octet (32-bit) IP addresses were originally divided into three different categories or classes: class A, class B, and class C. Each address class specifies a different number of bits for its network prefix and host number:

Class A network’s first octet begins with 0. The first octet identifies the network. Class A supports 127 networks, each with 16 million hosts.

Class B network’s first octet begins with 10. The first and second octets identify the network. Class B upports 16,000 networks, each with 65,000 hosts.

Class C network’s first octet begins with 110. The first three octets identify the network. Class C supports 2 million networks, each with 254 hosts.

Class D network’s first octet begins with 1110. Class D is reserved for multicast groups.

Class E network’s first octet begins with 1111. Class E is reserved for future use.

## IPv4 Dotted Decimal Notation

The 32-bit IPv4 addresses are most often expressed in dotted decimal notation, in which each octet (or byte) is treated as a separate number. Within an octet, the rightmost bit represents 20 (or 1), increasing to the left until the first bit in the octet is 27 (or 128). Following are IP addresses in binary format and their dotted decimal equivalents:

11010000 01100010 11000000 10101010 = 208.98.192.170
01110110 00001111 11110000 01010101 = 118.15.240.85
00110011 11001100 00111100 00111011 = 51.204.60.59
