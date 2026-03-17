**# Subnet Calculation Using Binary**



\## Why Use Binary in Subnetting?



Subnetting is fundamentally a binary operation.



\- IP addresses are stored in binary  

\- Subnet masks operate at the bit level  



Understanding binary makes subnetting:

\- more intuitive  

\- less error-prone 



\---



**## Example 1: Basic Subnetting**

**Given:**

**- IP Address: 192.168.1.0**

**- Default Subnet Mask: 255.255.255.0**

**We subnet to: 255.255.255.192**





\## Step 1: Identify Network and Host Bits



\- 1s → Network portion  

\- 0s → Host portion  



Before subnetting,

Subnet Mask: 255.255.255.0

Subnet Mask in binary: 11111111.11111111.11111111.00000000



After subnetting,

Subnet Mask: 255.255.255.192

Subnet Mask in binary: 11111111.11111111.11111111.11000000



Thus, now:

\- first 26 bits (1s) → network  

\- last 6 bits (0s) → host

&#x20;



\## Step 2: Number of Subnets



After subnetting, 2 more bits have been occupied by 1



Thus, Number of subnets = 2² = 4





\## Step 3: Number of Hosts per Subnet



After subnetting, number of remaining bits for 0 is 6



Thus,

Number of addresses per Subnet = 2⁶ = 64 addresses per subnet



Number of hosts per Subnet = 2⁶ - 2 = 62 hosts per Subnet





\## Step 4: Address/Subnet Ranges



IP Address: 192.168.1.0

IP Address in dotted binary: 11000000.10101000.00000001.00000000



Since, 1st 26 bits are for network,

Thus, 1st Address is = 11000000.10101000.00000001.00000000

and last Address is = 11000000.10101000.00000001.00111111 (keeping Network bits, i.e., 1st 26 bits unchanged)



In decimal Address Range is = 192.168.1.0 to 192.168.1.63



Since, Number of addresses per Subnet = 64

Thus, Subnet Ranges:

Subnet 1: 192.168.1.0   to 192.168.1.63    or, 192.168.1.0/26

Subnet 2: 192.168.1.64  to 192.168.1.127   or, 192.168.1.64/26

Subnet 3: 192.168.1.128 to 192.168.1.191   or, 192.168.1.128/26

Subnet 4: 192.168.1.192 to 192.168.1.255   or, 192.168.1.192/26





\## Step 5: Network, Broadcast, Host Range



Example:

For Subnet 1:

\- Network ID: 192.168.1.0

\- Broadcast ID: 192.168.1.63

\- Usable Hosts: 192.168.1.1 to 192.168.1.62



\---



**## Example 2: Subnetting a Class B Network (/16 → /18)**



**Given:**

**- IP Address: 172.16.0.0**

**- Default Subnet Mask: /16**

**We subnet to: /18**





\## Step 1: Identify Network and Host Bits



\- 1s → Network portion  

\- 0s → Host portion  



Before subnetting,  

Subnet Mask: 255.255.0.0  

Subnet Mask in binary: 11111111.11111111.00000000.00000000  



After subnetting,  

Subnet Mask: 255.255.192.0  

Subnet Mask in binary: 11111111.11111111.11000000.00000000  



Thus, now:

\- first 18 bits (1s) → network  

\- last 14 bits (0s) → host  





\## Step 2: Number of Subnets



After subnetting, 2 more bits have been occupied by 1  



Thus, Number of subnets = 2² = 4  





\## Step 3: Number of Hosts per Subnet



After subnetting, number of remaining bits for 0 is 14  



Thus,  

Number of addresses per subnet = 2¹⁴ = 16384 addresses per subnet  



Number of hosts per subnet = 2¹⁴ - 2 = 16382 hosts per subnet  





\## Step 4: Address/Subnet Ranges



IP Address: 172.16.0.0  

IP Address in dotted binary: 10101100.00010000.00000000.00000000  



Since, first 18 bits are for network,  

Thus, first address is = 10101100.00010000.00000000.00000000  

and last address is = 10101100.00010000.00111111.11111111  



In decimal, address range is = 172.16.0.0 to 172.16.63.255  



Since, number of addresses per subnet = 16384

But, In last octet the value 16383 Which is more than 255 is not Possible.

since, each octet contains 0 to 255, i.e., for total 256 numbers of 4th octet, number of cycles of 3rd Octet = 16384/256 = 64,

Again, since 3rd octet stared from 0, thus last cycle would start from 63.





Thus, Subnet Ranges:

Subnet 1: 172.16.0.0   to 172.16.63.255    or, 172.16.0.0/18

Subnet 2: 172.16.64.0  to 172.16.127.255   or, 172.16.64.0/18

Subnet 3: 172.16.128.0 to 172.16.191.255   or, 172.16.128.0/18

Subnet 4: 172.16.192.0 to 172.16.255.255   or, 172.16.192.0/18





\## Step 5: Network, Broadcast, Host Range



Example:

For Subnet 1:

\- Network ID: 172.16.0.0  

\- Broadcast ID: 172.16.63.255  

\- Usable Hosts: 172.16.0.1 to 172.16.63.254

