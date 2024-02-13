---
title: "Understanding IP Addresses and Internet Protocols"
datePublished: Tue Feb 13 2024 10:23:50 GMT+0000 (Coordinated Universal Time)
cuid: clsk7typ9000x08l61grx4ded
slug: understanding-ip-addresses-and-internet-protocols
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1707819768041/a9d447ab-b7a4-40ed-8d36-2fff4c36c729.jpeg
tags: networking, cisco, computer-networking, ip-address

---

**IP Addresses**

An IP (Internet Protocol) address is a fundamental component of internet communication, used to pinpoint the geographical location of an address. In the realm of web operations services, IPv4 utilizes 32 bits for its addressing.

**IPv5 and the Transition to IPv6**

Contrary to its successors, IPv5 wasn't used for transmitting video data or streaming. Instead, it found its niche primarily within Apple's ecosystem, retaining the 32-bit structure. However, with the number of devices surpassing the (2^{32}) mark, the industry moved towards standardizing IPv6.

**IP Address Classes**

IP address classes, denoted by letters A, B, C, D, and E, delineate networks based on organizational size and purpose. Classes A, B, and C cater to different scales of network demands, while D is earmarked for multicasting and E is reserved for scientific endeavors.

**Historical Context**

During the Beginning stages of internet connectivity, access was confined to select organizations, setting the stage for the eventual expansion of network infrastructure.

**Network Allocation and Classification**

To maintain network integrity and separation, IP address ranges differ based on class classification. This classification is dictated by specific bit patterns:

* Class A: 0 as the first bit
    
* Class B: 10 as the first two bits
    
* Class C: 110 as the first three bits
    
* Class D: 1110 as the first four bits
    
* Class E: 1111 as the first four bits
    

**Calculating Possible Networks**

* Class A: (2^7) networks, excluding the 0th network.
    
* Class B: (2^{14}) networks.
    
* Class C: (2^{21}) networks, accounting for 3 reserved bits.
    
* Each class has a specific range of addresses defined by the number of bits used for the network portion.
    
* The remaining bits after network allocation determine the number of usable hosts per network.
    
* Class A: Largest networks (fewest), most hosts per network.
    
* Class B: Medium-sized networks, medium number of hosts.
    
* Class C: Smallest networks (most numerous), fewest hosts per network.
    

*Remember, the usable host range excludes the network address and broadcast address for each network.*

| **Class** | **Range** | **Network Bits** | **Usable Hosts per Network** | **Total Networks** |
| --- | --- | --- | --- | --- |
| A | 1.0.0.0 - 127.0.0.0 | 8 | 2^24 - 2 | 128 |
| B | 128.0.0.0 - 191.255.0.0 | 16 | 2^16 - 2 | 16,384 |
| C | 192.0.0.0 - 223.255.255.0 | 24 | 2^8 - 2 | 2,097,152 |

**Information Needed:**

* **IP address:** The address assigned to a specific device on the network.
    
* **Subnet mask:** A mask defining which bits in the IP address represent the network portion and which represent the host portion.
    

**Steps:**

1. **Identify the Network Address:**
    
    * Perform a **bitwise AND operation** between the IP address and the subnet mask. This operation retains only the bits that are "1" in both the address and the mask, effectively isolating the network portion.
        
    * The result of this operation represents the network address for the given IP address and subnet mask.
        
2. **Identify the Broadcast Address:**
    
    * **Invert the subnet mask** by replacing each "1" with a "0" and vice versa. This creates a mask with all host bits set to "1".
        
    * Perform a **bitwise OR operation** between the network address obtained in step 1 and the inverted subnet mask. This operation sets all host bits to "1", creating the broadcast address for the subnet.
        
3. **Identify the First Usable Host Address:**
    
    * Take the network address obtained in step 1.
        
    * Change the least significant host bit from "0" to "1". This sets the first host address within the subnet, excluding the network address itself.
        

| **\*\*Class** | **Network Bits** | **Host Bits** | **Subnet Mask** | **Example** |
| --- | --- | --- | --- | --- |
| A | 8 | 24 | 255.0.0.0 | 10.0.0.0 |
| B | 16 | 16 | 255.255.0.0 | 172.16.0.0 |
| C | 24 | 8 | 255.255.255.0 | 192.168.1.0 |

**Example:**

* IP address: 192.168.1.10
    
* Subnet mask: 255.255.255.0 (Class C network)
    

1. **Network Address:**
    
    * 192.168.1.10 (IP) AND 255.255.255.0 (mask) = 192.168.1.0
        
2. **Broadcast Address:**
    
    * Inverted mask: 0.0.0.255
        
    * 192.168.1.0 (network) OR 0.0.0.255 (inverted mask) = 192.168.1.255
        
3. **First Usable Host:**
    
    * Change the least significant bit of 192.168.1.0 to 1: 192.168.1.2
        

Therefore, for the given IP address and subnet mask:

* **Network address:** 192.168.1.0
    
* **Broadcast address:** 192.168.1.255
    
* **First usable host:** 192.168.1.2
    

### A simple trick to quickly find the network and broadcast addresses of an IP address based on its class.

1. **Determine the Class:**
    
    * Check the first few bits of the IP address to determine its class: A, B, C, D, or E.
        
2. **Find the Broadcast Address:**
    
    * For Class A, B, C, D, or E:
        
        * Replace all bits after the first 8, 16, 24, 32, or 32 bits (depending on the class) with "1". This forms the broadcast address.
            
3. **Find the Network Address:**
    
    * Replace all bits of the IP address with "0". This yields the network address.
        
4. **Find the First Host:**
    
    * Take the network address.
        
    * Change the least significant bit to "1". This gives you the first host address.
        

**Example:**

Let's take the IP address 192.168.1.10.

1. **Class Determination:**
    
    * Since the first octet (192) falls within the range of Class C (192.0.0.0 to 223.255.255.255), this IP address belongs to Class C.
        
2. **Broadcast Address:**
    
    * For Class C, replace all bits after the first 24 bits with "1".
        
    * Broadcast Address: 192.168.1.255
        
3. **Network Address:**
    
    * Replace all bits of the IP address with "0".
        
    * Network Address: 192.168.1.0
        
4. **First Host:**
    
    * Take the network address (192.168.1.0).
        
    * Change the least significant bit to "1".
        
    * First Host: 192.168.1.1
        

## Network Interface Card (NIC)

A NIC is a hardware component that enables your device to connect to a network. Understanding the logical structure of IP addresses within a specific subnet is essential for effective network management.