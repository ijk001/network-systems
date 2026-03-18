# 08-04: Exercises

## Question

A network **192.168.10.0/24** is given.  
This network has to be divided using **VLSM** for the following departments:

- Department A → 100 hosts  
- Department B → 50 hosts  
- Department C → 25 hosts  
- Department D → 10 hosts  

Based on this requirement, answer the following:

1. What is the required subnet size for each department?  
2. What prefix length will be used for each department?  
3. What subnet will be assigned to each department?  
4. What is the usable host range of each subnet?  
5. What unused address range remains after allocation?  

---

## Solution

### Step 1: Arrange host requirements in descending order

In VLSM, the largest requirement has to be allocated first.

- Department A → 100 hosts  
- Department B → 50 hosts  
- Department C → 25 hosts  
- Department D → 10 hosts  

---

### Step 2: Find required subnet size for each department

Need to use:

Required addresses = hosts + 2

#### Department A
- Hosts needed = 100
- Required = 100 + 2 = 102
- Closest power of 2 = 128
- Prefix = /25

#### Department B
- Hosts needed = 50
- Required = 50 + 2 = 52
- Closest power of 2 = 64
- Prefix = /26

#### Department C
- Hosts needed = 25
- Required = 25 + 2 = 27
- Closest power of 2 = 32
- Prefix = /27

#### Department D
- Hosts needed = 10
- Required = 10 + 2 = 12
- Closest power of 2 = 16
- Prefix = /28

👉 **(1) Required subnet sizes:**
- A → 128 addresses
- B → 64 addresses
- C → 32 addresses
- D → 16 addresses

👉 **(2) Prefix lengths:**
- A → /25
- B → /26
- C → /27
- D → /28

---

### Step 3: Assign subnets

Start from the beginning of 192.168.10.0/24 and assign sequentially.

#### Department A
- Subnet = 192.168.10.0/25
- Address range = 192.168.10.0 to 192.168.10.127
- Usable host range = 192.168.10.1 to 192.168.10.126

#### Department B
- Subnet = 192.168.10.128/26
- Address range = 192.168.10.128 to 192.168.10.191
- Usable host range = 192.168.10.129 to 192.168.10.190

#### Department C
- Subnet = 192.168.10.192/27
- Address range = 192.168.10.192 to 192.168.10.223
- Usable host range = 192.168.10.193 to 192.168.10.222

#### Department D
- Subnet = 192.168.10.224/28
- Address range = 192.168.10.224 to 192.168.10.239
- Usable host range = 192.168.10.225 to 192.168.10.238

👉 **(3) Assigned subnets:**
- A → 192.168.10.0/25
- B → 192.168.10.128/26
- C → 192.168.10.192/27
- D → 192.168.10.224/28

---

### Step 4: Find unused address range

After allocating Department D, the remaining range is:

- 192.168.10.240 to 192.168.10.255

👉 **(5) Unused address range = 192.168.10.240 to 192.168.10.255**

---

## Final Summary

1. Required subnet sizes:
   - A → 128
   - B → 64
   - C → 32
   - D → 16

2. Prefix lengths:
   - A → /25
   - B → /26
   - C → /27
   - D → /28

3. Assigned subnets:
   - A → 192.168.10.0/25
   - B → 192.168.10.128/26
   - C → 192.168.10.192/27
   - D → 192.168.10.224/28

4. Usable host ranges:
   - A → 192.168.10.1 to 192.168.10.126
   - B → 192.168.10.129 to 192.168.10.190
   - C → 192.168.10.193 to 192.168.10.222
   - D → 192.168.10.225 to 192.168.10.238

5. Unused address range:
   - 192.168.10.240 to 192.168.10.255

