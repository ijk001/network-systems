**# Subnetting Basics**



\## What is Subnetting?

Subnetting is the process of dividing a network into smaller sub-networks (subnets).



It allows a large network to be split into multiple smaller and manageable networks.



\---



\## Why Subnetting is Needed

\- Improves network performance

\- Enhances security by isolating segments

\- Efficient use of IP addresses

\- Better network management



\---



\## Relationship with Classful Networks

In classful networking:

\- network and host portions are fixed

\- network portion always ends at the end of an octet



Subnetting allows:

\- modification of the default boundary

\- creation of multiple smaller networks from a single network

\- the network portion does not necessarily end at the end of an octet, rather it can extend into the next octet at the bit level



\---



\## How Subnetting Works

Subnetting works by borrowing bits from the host portion.



\- Some host bits are converted into network bits

\- This creates multiple smaller subnets



\---



\## Example

Original Network:

\- IP Address: 192.168.1.0

\- Default Subnet Mask: 255.255.255.0 (/24)



After Subnetting (/26):

New Subnet Mask: 255.255.255.192 (/26)



Explanation:

\- Original network bits: 24

\- New network bits: 26

\- Borrowed bits: 2



\---



\## Number of Subnets



Formula:

Number of subnets = 2ⁿ



Where: n = number of borrowed bits



Example:

2² = 4 subnets



\---



\## Number of Address and Number of Hosts per Subnet



Formula:

Total possible addresses per Subnet = 2ʰ



The first address is called the **Network ID**, which identifies the subnet.

The last address is called the **Broadcast ID**, which is used to send data to all devices in the subnet.



These two addresses are reserved and cannot be assigned to hosts.



Thus, Number of usable hosts per Subnet = 2ʰ − 2



Where: h = number of remaining host bits



Example:



6 host bits → 2⁶ = 64 total addresses



\- Network Address → first address

\- Broadcast Address → last address



Usable hosts = 64 − 2 = 62 hosts per Subnet



\---



\## Block Size: Block size determines the increment between subnet ranges.



Formula:

Block Size = 256 − (value of the subnet mask in the changing octet)



Example:

Subnet Mask: 255.255.255.192

Block Size = 256 − 192 = 64

This means subnets will increase in steps of 64: 0, 64, 128, 192



\---



\## Why Block Size Matters

\- Helps identify subnet ranges

\- Determines network and broadcast addresses

\- Simplifies subnet calculations



\---



\## Key Idea



Classful networking uses fixed boundaries.

👉 Subnetting introduces flexibility by allowing custom network boundaries.

