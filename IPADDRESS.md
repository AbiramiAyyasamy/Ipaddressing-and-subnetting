
## Perform a decimal to binary conversion (and vise versa).

* Convert Decimal IP address in Binary and Binary in Decimal

This tutorial explains how to convert a decimal IP address in binary IP address and a binary IP address in a decimal IP address step by step with examples. Learn the easiest method of converting a decimal IP address and subnet mask in binary IP address and subnet mask respectively.

An IP address and a subnet mask both collectively provide a numeric identity to an interface. Both addresses are always used together. Without subnet mask, an IP address is an ambiguous address and without IP address a subnet mask is just a number.

Both addresses are 32 bits in length. These bits are divided in four parts. Each part is known as Octet and contains 8 bits. Octets are separated by periods and written in a sequence.

In binary notation, all four octets are written in binary format.

Examples of IP address in binary notation are following: -

00001010.00001010.00001010.00001010

Examples of subnet mask in binary notation are following: -

11111111.00000000.00000000.00000000

In decimal notation, all four octets are written in decimal format. A decimal equivalent value of the bits is used in each octet.

Examples of IP address in decimal notation are following: -

10.10.10.10
172.168.1.1
192.168.1.1

Examples of subnet mask in decimal notation are following: -

255.0.0.0
255.255.0.0
255.255.255.0

## Understanding base value and position

Except the base value, binary system works exactly same as decimal system works. Base value is the digits which are used to build the numbers in both systems. In binary system, two digits (0 and 1) are used to build the numbers while in decimal system, ten digits (0,1,2,3,4,5,6,7,8,9) are used to build the numbers.

Since IP address and subnet mask both are built from 32 bits and these bits are divided in 4 octets, in order to convert these addresses in binary from decimal and vice versa, we only need to understand the numbers which can be built from an octet or 8 bits.

A bit can be either on or off. In binary system on bit is written as 1 and off bit is written as 0 in number. In decimal system if bit is on, its position value is added in number and if bit is off, its position value is skipped in number.

Following table lists the position value of each bit in an octet.
<pre class="terminal">
Bit position	1	2	3	4	5	6	7	8
Position value	128	64	32	16	8	4	2	1
</pre>

## Key points

Regardless which system we use to write the octet, it always contains all 8 bits. Bits are always written from left to right.

A number in which all 8 bits are off is written as 00000000 in binary system. Same number is written as 0 (0+0+0+0+0+0+0+0) in decimal system.

A number in which all 8 bits are on is written as 11111111 in binary system. Same number is written as 255 (128+64+32+16+8+4+2+1) in decimal system.

Let’s take an example. Convert a decimal number 117 in binary.

Given decimal number is 117

Calculation direction is Left to Right

Bit position	position value	Comparison	Operation in decimal	Value in decimal	Operation in 

Binary	Value in binary

1	128	128 is greater than 117	Skip	0	Off	0
2	64	0+64 = 64 is less than 117	Add	64	On	1
3	32	0+64+32 = 96 is less than 117	Add	32	On	1
4	16	0+64+32+16 = 112 is less than 117	Add	16	On	1
5	8	0+64+32+16+8 = 120 is greater than 117	Skip	0	Off	0
6	4	0+64+32+16+0+4 = 116 is less than 117	Add	4	On	1
7	2	0+64+32+16+0+4+2 = 118 is greater than 117	Skip	0	Off	0
8	1	0+64+32+16+0+4+0+1 = 117 is equivalent to 117	Add	1	On	1

To write the given number in decimal format, sum all the values of decimal field and write the result. In this example, it would be 0+64+32+16+0+4+0+1 = 117.

To write the given number in binary format, write all the values of binary field from left to right. In this example, it would be 11110101.
Converting binary number in decimal number
To convert a binary number in decimal number, sum the values of all on bits. Let’s take an example. Convert a binary number 10101010 in decimal number.

Given binary number is 10101010

Calculation direction is Left to Right

Bit position	1	2	3	4	5	6	7	8

position value	128	64	32	16	8	4	2	1

In binary	1	0	1	0	1	0	1	0

Bit status	On	Off	On	Off	On	Off	On	Off

If bit status is on, use position value in decimal	128	0	32	0	8	0	2	0
The binary number 10101010 is equal to the number 170 (128+0+32+0+8+0+2+0) in decimal system.

## Converting an IP address and subnet mask

As we know IP address and subnet mask both are built from 4 individual octets separated by periods. We can use above methods to convert all octets individually. Once all four octets are converted, we can merge them again separating by periods.
![convert-decimal-binary](https://user-images.githubusercontent.com/103209557/166885659-9dbebd7f-5cc2-4d5a-af4e-c6c36fae37f4.png)
