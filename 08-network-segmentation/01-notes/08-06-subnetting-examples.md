**# Subnetting Examples**



**## Example 1: Basic Subnetting (/24 → /26)**

**Given:**

**- IP Address: 192.168.1.0**

**- Default Subnet Mask: /24**

**We subnet to: /26**





\## Step 1: Identify Borrowed Bits



\- Original network bits = 24

\- New network bits = 26

\- Borrowed bits, n = 26 - 24 = 2

\- Total bits = 32

\- Host bits, h = 32 - 26 = 6

&#x20;



\## Step 2: Number of Subnets



Formula: Number of subnets = 2ⁿ = 2² = 4





\## Step 3: Number of Address and Number of Hosts per Subnet



Formula: Number of addresses per Subnet = 2ʰ =  2⁶ = 64 addresses per subnet



Formula: Number of hosts per Subnet = 2ʰ - 2  = 2⁶ - 2 = 62 hosts per Subnet





\## Step 4: Subnet/Address Ranges



Subnet mask in dotted binary: 11111111.11111111.11111111.11000000

Subnet mask in dotted decimal: 255.255.255.192

Block size = 256 − (value of the subnet mask in the changing octet) = 256 - 192 = 64



Thus, Subnet Ranges:

Subnet 1: 192.168.1.0   to 192.168.1.63    or, 192.168.1.0/26

Subnet 2: 192.168.1.64  to 192.168.1.127   or, 192.168.1.64/26

Subnet 3: 192.168.1.128 to 192.168.1.191   or, 192.168.1.128/26

Subnet 4: 192.168.1.192 to 192.168.1.255   or, 192.168.1.192/26



Address Range: 192.168.1.0 to 192.168.1.255





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





\## Step 1: Identify Borrowed Bits



\- Original network bits = 16

\- New network bits = 18

\- Borrowed bits, n = 18 - 16 = 2

\- Total bits = 32

\- Host bits, h = 32 - 18 = 14





\## Step 2: Number of Subnets



Formula: Number of subnets = 2ⁿ = 2² = 4





\## Step 3: Number of Address and Number of Hosts per Subnet



Formula: Number of addresses per Subnet = 2ʰ = 2¹⁴ = 16384 addresses per subnet



Formula: Number of hosts per Subnet = 2ʰ - 2 = 2¹⁴ - 2 = 16382 hosts per subnet





\## Step 4: Subnet/Address Ranges



Subnet mask in dotted binary: 11111111.11111111.11000000.00000000

Subnet mask in dotted decimal: 255.255.192.0



Block size = 256 − (value of the subnet mask in the changing octet) = 256 - 192 = 64



Thus, Subnet Ranges:

Subnet 1: 172.16.0.0   to 172.16.63.255    or, 172.16.0.0/18

Subnet 2: 172.16.64.0  to 172.16.127.255   or, 172.16.64.0/18

Subnet 3: 172.16.128.0 to 172.16.191.255   or, 172.16.128.0/18

Subnet 4: 172.16.192.0 to 172.16.255.255   or, 172.16.192.0/18



Address Range: 172.16.0.0 to 172.16.255.255





\## Step 5: Network, Broadcast, Host Range



Example:

For Subnet 1:

\- Network ID: 172.16.0.0

\- Broadcast ID: 172.16.63.255

\- Usable Hosts: 172.16.0.1 to 172.16.63.254



\---



\## Key Idea



Subnetting involves:

\- borrowing bits

\- calculating subnets

\- determining host ranges

\- identifying network and broadcast addresses

