\# What is Classful Networks?



Classful networking is an older method of IP address allocation where IP addresses are divided into fixed classes based on their first octet.



Each class defines:

\- the network portion

\- the host portion



\---



\## Why Classful Networks Were Used



\- Simple and easy to understand

\- Standardized network sizes

\- No need for subnet masks initially



\---



\## IP Address Classes



IPv4 addresses are divided into five classes:



\### Class A

\- Range: 1.0.0.0 to 126.255.255.255

\- Default Subnet Mask: 255.0.0.0 (/8)

\- Network bits: 8

\- Host bits: 24



\---



\### Class B

\- Range: 128.0.0.0 to 191.255.255.255

\- Default Subnet Mask: 255.255.0.0 (/16)

\- Network bits: 16

\- Host bits: 16



\---



\### Class C

\- Range: 192.0.0.0 to 223.255.255.255

\- Default Subnet Mask: 255.255.255.0 (/24)

\- Network bits: 24

\- Host bits: 8



\---



\### Class D

\- Range: 224.0.0.0 to 239.255.255.255

\- Used for multicast communication



\---



\### Class E

\- Range: 240.0.0.0 to 255.255.255.255

\- Reserved for experimental use



\---



\## Limitations of Classful Networking



\- Inefficient use of IP addresses

\- Fixed network sizes (too large or too small)

\- Lack of flexibility



\---



\## Transition to Modern Networking



Due to these limitations, classful networking was replaced by:

\- Classless Inter-Domain Routing (CIDR)

\- Subnetting



\---



\## Key Idea



Classful networks divide IP addresses into fixed classes,

while modern networking allows flexible allocation using subnetting and CIDR.

