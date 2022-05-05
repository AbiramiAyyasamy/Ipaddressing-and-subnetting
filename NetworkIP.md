## Understanding IP addresses

Every location or device on a network must be addressable. This means that it can be reached by referencing its designation under a predefined system of addresses. In the normal TCP/IP model of network layering, this is handled on a few different layers, but usually when we refer to an address on a network we are talking about an IP address.

IP addresses allow network resources to be reached through a network interface. If one computer wants to communicate with another computer, it can address the information to the remote computer’s IP address. Assuming that the two computers are on the same network, or that the different computers and devices in between can translate requests across networks, the computers should be able to reach each other and send information.

Each IP address must be unique on its own network. Networks can be isolated from one another, and they can be bridged and translated to provide access between distinct networks. A system called Network Address Translation, allows the addresses to be rewritten when packets traverse network borders to allow them to continue on to their correct destination. This allows the same IP address to be used on multiple, isolated networks while still allowing these to communicate with each other if configured correctly.
## IPV4

A typical IPv4 address looks something like this:

`192.168.0.5`

The lowest value in each octet is a 0, and the highest value is 255.

We can also express this in binary to get a better idea of how the four octets will look. We will separate each 4 bits by a space for readability and replace the dots with dashes:

`1100 0000 - 1010 1000 - 0000 0000 - 0000 0101`

Recognizing that these two formats represent the same number will be important for understanding concepts later on.

Although there are some other differences in the protocol and background functionality of IPv4 and IPv6, the most noticeable difference is the address space. IPv6 expresses addresses as an 128-bit number. To put that into perspective, this means that IPv6 has space for more than 7.9×1028 times the amount of addresses as IPv4.

## IPV6

To express this extended address range, IPv6 is generally written out as eight segments of four hexadecimal digits. Hexadecimal numbers represent the numbers 0–15 by using the digits 0–9, as well as the numbers a–f to express the higher values. A typical IPv6 address might look something like this:

1203:8fe0:fe80:b897:8990:8a7c:99bf:323d
You may also see these addresses written in a compact format. The rules of IPv6 allow you to remove any leading zeros from each octet, and to replace a single range of zeroed groups with a double colon (::).

For instance, if you have one group in an IPv6 address that looks like this:

...:00bc:...
You could instead just type:

...:bc:...
To demonstrate the second case, if you have a range in an IPv6 address with multiple groups as zeroes, like this:

...:18bc:0000:0000:0000:00ff:...
You could compact this like so (also removing the leading zeros of the group like we did above):

...:18bc::ff...
You can do this only once per address, or else the full address will be unable to be reconstructed.

While IPv6 is becoming more common every day, in this guide, we will be exploring the remaining concepts using IPv4 addresses because it is easier to discuss with a smaller address space.

