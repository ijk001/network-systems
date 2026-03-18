# 08-05: Exercises

## Question

A network **10.0.0.0/24** is given.  
This network has to be divided using **VLSM** for the following requirements:

- LAN 1 → 60 hosts  
- LAN 2 → 30 hosts  
- LAN 3 → 12 hosts  
- LAN 4 → 6 hosts  

Based on this requirement, answer the following:

1. What is the required subnet size for each LAN?  
2. What prefix length will be used for each LAN?  
3. What subnet will be assigned to each LAN?  
4. What is the usable host range of each subnet?  
5. What unused address range remains after allocation?  

---

## Solution

### Step 1: Arrange host requirements in descending order

- LAN 1 → 60 hosts  
- LAN 2 → 30 hosts  
- LAN 3 → 12 hosts  
- LAN 4 → 6 hosts  

---

### Step 2: Find required subnet size for each LAN

Need to use:

Required addresses = hosts + 2

#### LAN 1
- Hosts needed = 60
- Required = 62
- Closest power of 2 = 64
- Prefix = /26

#### LAN 2
- Hosts needed = 30
- Required = 32
- Closest power of 2 = 32
- Prefix = /27

#### LAN 3
- Hosts needed = 12
- Required = 14
- Closest power of 2 = 16
- Prefix = /28

#### LAN 4
- Hosts needed = 6
- Required = 8
- Closest power of 2 = 8
- Prefix = /29

👉 **(1) Required subnet sizes:**
- LAN 1 → 64 addresses
- LAN 2 → 32 addresses
- LAN 3 → 16 addresses
- LAN 4 → 8 addresses

👉 **(2) Prefix lengths:**
- LAN 1 → /26
- LAN 2 → /27
- LAN 3 → /28
- LAN 4 → /29

---

### Step 3: Assign subnets

#### LAN 1
- Subnet = 10.0.0.0/26
- Address range = 10.0.0.0 to 10.0.0.63
- Usable host range = 10.0.0.1 to 10.0.0.62

#### LAN 2
- Subnet = 10.0.0.64/27
- Address range = 10.0.0.64 to 10.0.0.95
- Usable host range = 10.0.0.65 to 10.0.0.94

#### LAN 3
- Subnet = 10.0.0.96/28
- Address range = 10.0.0.96 to 10.0.0.111
- Usable host range = 10.0.0.97 to 10.0.0.110

#### LAN 4
- Subnet = 10.0.0.112/29
- Address range = 10.0.0.112 to 10.0.0.119
- Usable host range = 10.0.0.113 to 10.0.0.118

👉 **(3) Assigned subnets:**
- LAN 1 → 10.0.0.0/26
- LAN 2 → 10.0.0.64/27
- LAN 3 → 10.0.0.96/28
- LAN 4 → 10.0.0.112/29

---

### Step 4: Find unused address range

Remaining range:

- 10.0.0.120 to 10.0.0.255

👉 **(5) Unused address range = 10.0.0.120 to 10.0.0.255**

---

## Final Summary

1. Required subnet sizes:
   - LAN 1 → 64
   - LAN 2 → 32
   - LAN 3 → 16
   - LAN 4 → 8

2. Prefix lengths:
   - LAN 1 → /26
   - LAN 2 → /27
   - LAN 3 → /28
   - LAN 4 → /29

3. Assigned subnets:
   - LAN 1 → 10.0.0.0/26
   - LAN 2 → 10.0.0.64/27
   - LAN 3 → 10.0.0.96/28
   - LAN 4 → 10.0.0.112/29

4. Usable host ranges:
   - LAN 1 → 10.0.0.1 to 10.0.0.62
   - LAN 2 → 10.0.0.65 to 10.0.0.94
   - LAN 3 → 10.0.0.97 to 10.0.0.110
   - LAN 4 → 10.0.0.113 to 10.0.0.118

5. Unused address range:
   - 10.0.0.120 to 10.0.0.255