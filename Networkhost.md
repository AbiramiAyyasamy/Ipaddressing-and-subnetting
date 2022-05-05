This is the second part in the “CIDR Addressing and Subnet Masking” series. This time we want to be able to create more subnets and add more hosts to the network. That was not something our original IP addressing scheme could give us i.e. 192.168.4.12/24. With 24-bits allocated for the network, like a Class C address, we can only build 1 subnet with 254 hosts (256 minus the subnet ID and broadcast ID).

This is the reason we implement a CIDR addressing scheme which will allow us to borrow bits from the third octet to create more subnets. That will then allow us to add more hosts to the network. Another term for this is “supernetting” or VLSM (Variable Length Subnet Masking).


Applying a new subnet mask of /20.
In binary, the IP address is written as:

11000000.10101000.00000100.00001100

We are now going to use CIDR notation for this example. In this scheme, we are actually just using a total of 20 bits for the network.

11111111.11111111.11110000.00000000

This will allow us to create more subnets. This is because from the third octet, we have a total of 4 bits for the subnet. We take the last significant bit, which has the binary position of 2⁴ or 16. This is our “magic number”. This means we have a total of 16 subnets on this network. In this example, since we are using CIDR notation, we will refer to the subnet ID as the network ID just for clarification.

Finding the Network ID
With a /20, our subnet mask is therefore:

255.255.240.0 -> 11111111.11111111.11110000.00000000

Once again, we will perform a logical AND between the given IP address and our subnet mask.

11111111.11111111.11110000.00000000
11000000.10101000.00000100.00001100

11000000.10101000.00000000.00000000

The network ID is 192.168.0.0.

Finding the Broadcast ID
Now we are looking for our broadcast ID. We must now reference the “magic number” because that determines our increments. Since we have 16, we must then subtract 1 as a rule and we get the following:

192.168.15.255

Once again, we turn on the wildcard bits that is the opposite of all zeroes, to all ones and we get 255.

Finding the IP Address Range
Now this is much different than the first example. This time we have subnets, which means more networks. We know that the total network to which the IP address 192.168.4.12/20 belongs to has a total of 16 subnets. We just take the network ID and add the first logical value allowed which is 1 and then take the broadcast ID and subtract 1 for the host (you cannot use 255 for a host address). The IP address range for this subnet is:

192.168.0.1–192.168.15.254

In this example it would be too time consuming to write down all the subnets and IP addresses, so we just use the network segment for the IP address given. That means the IP address range we have for the IP address in the example is just a segment of the greater network.

Finding Total Hosts
In order to find the total hosts, we must always subtract the IP address of the network ID and broadcast ID. Thus instead of 256, we have 254 hosts on each subnet. Since we have 16 subnets, we take that value and multiply the number of logical host IP addresses per subnet.

16 subnets * 254 host/subnet = 4,064 hosts

There are actually 4,096 addresses available in this network. That is because we have 12 bits allocated for the host space. 2¹² is equal to 4,096. In this case the only usable addresses for hosts is 4,064 after we exclude the network ID and broadcast ID from each subnet.

Putting It All Together
Based on the information we have gathered about 192.168.4.12/20, we can construct a table.
![host](https://user-images.githubusercontent.com/103209557/166890738-2248546f-c0e3-4604-8f86-046bc320b782.png)

