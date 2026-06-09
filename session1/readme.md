# Computer Networks

# 1. Introduction to Computer Networks

## What is a Computer Network?

A Computer Network is a collection of two or more computing devices connected together through wired or wireless communication channels for the purpose of exchanging data, sharing resources, and enabling communication.

These devices may include computers, servers, smartphones, printers, routers, switches, IoT devices, and many others.

In modern computing, networking is one of the most fundamental technologies because almost every application relies on communication between multiple devices over a network.

### Real-Life Example

When you send a message through WhatsApp, your phone communicates with WhatsApp servers through the Internet. This communication happens through a computer network.

Similarly:

* Browsing websites
* Watching YouTube videos
* Online gaming
* Cloud storage
* Video conferencing

all depend on computer networks.

---

## Objectives of Networking

### 1. Resource Sharing

Multiple users can share resources such as:

* Printers
* Storage devices
* Internet connections
* Applications

Example:

Instead of buying a printer for every employee, an organization can connect one printer to the network and allow everyone to use it.

---

### 2. Communication

Networks enable communication between users.

Examples:

* Email
* Voice Calls
* Video Calls
* Instant Messaging

---

### 3. Data Exchange

Information can be exchanged quickly between devices.

Examples:

* File transfers
* Database synchronization
* Cloud backups

---

### 4. Internet Access

Networks provide access to the Internet and online services.

Examples:

* Web browsing
* Social media
* Online shopping

---

### 5. Centralized Management

Administrators can manage devices, users, and resources from a central location.

Benefits include:

* Better security
* Easier maintenance
* Simplified monitoring

---

# 2. Types of Computer Networks

Computer networks are categorized based on geographical coverage.

## PAN (Personal Area Network)

A Personal Area Network is the smallest type of network and typically covers a few meters around a user.

### Examples

* Bluetooth headset connected to mobile phone
* Smartwatch connected to smartphone
* Wireless keyboard connected to laptop

### Characteristics

* Very short range
* Low power consumption
* Usually wireless

---

## LAN (Local Area Network)

A Local Area Network connects devices within a limited geographical area such as a home, office, school, or building.

### Examples

* Home Wi-Fi network
* Office network
* School computer laboratory

### Characteristics

* High speed
* Low latency
* Privately owned

### Diagram

```text
PC1 ----\
PC2 ----- Switch ----- Router ----- Internet
PC3 ----/
```

---

## MAN (Metropolitan Area Network)

A Metropolitan Area Network spans an entire city or metropolitan region.

### Examples

* City-wide cable television network
* Municipal government network

### Characteristics

* Covers larger areas than LAN
* High-speed backbone connections

---

## WAN (Wide Area Network)

A Wide Area Network covers countries, continents, or even the entire world.

The Internet is the largest WAN in existence.

### Examples

* Internet
* Bank branch networks
* International corporate networks

### Characteristics

* Very large coverage
* Uses public and private infrastructure
* Higher latency than LAN

---

# 3. Network Topologies

A Network Topology defines how devices are arranged and connected.

## Bus Topology

All devices share a single communication cable.

### Advantages

* Simple
* Inexpensive

### Disadvantages

* Single cable failure affects entire network
* Difficult troubleshooting

---

## Star Topology

All devices connect to a central switch or hub.

### Advantages

* Easy to manage
* Easy fault detection
* Most commonly used

### Disadvantages

* Central device failure affects network

### Diagram

```text
       PC1
        |
PC2 -- Switch -- PC3
        |
       PC4
```

---

## Ring Topology

Devices form a circular chain.

Data travels around the ring.

### Advantages

* Predictable performance

### Disadvantages

* Failure may disrupt communication

---

## Mesh Topology

Every device connects to every other device.

### Advantages

* High reliability
* No single point of failure

### Disadvantages

* Expensive
* Complex

---

# 4. Networking Devices

Networking devices enable communication between computers and networks.

---

## Hub

A Hub is a basic networking device that broadcasts incoming data to every connected device.

### How It Works

Suppose PC1 sends data.

The hub forwards the data to:

* PC2
* PC3
* PC4

regardless of the intended recipient.

### Problems

* Wastes bandwidth
* Causes collisions
* Less secure

### OSI Layer

Layer 1 (Physical Layer)

---

## Switch

A Switch is an intelligent networking device used to connect devices within a Local Area Network.

Unlike a hub, a switch forwards data only to the intended destination.

### How It Works

The switch maintains a MAC Address Table.

When data arrives:

1. Switch reads destination MAC address.
2. Finds associated port.
3. Sends frame only to that port.

### Advantages

* Faster communication
* Reduced collisions
* Better security

### OSI Layer

Layer 2 (Data Link Layer)

---

## Router

A Router connects different networks and forwards packets between them.

It is responsible for determining the best path for data to travel.

### Functions

* Routing
* NAT
* DHCP
* Internet Connectivity

### Example

```text
Home Devices
      |
    Router
      |
      ISP
      |
   Internet
```

### OSI Layer

Layer 3 (Network Layer)

---

## Modem

A Modem converts signals between your ISP and home network.

### Purpose

Allows communication between:

* ISP infrastructure
* Home router

---

# 5. OSI Model

The Open Systems Interconnection (OSI) Model is a conceptual framework used to understand network communication.

It divides communication into seven layers.

| Layer | Name         |
| ----- | ------------ |
| 7     | Application  |
| 6     | Presentation |
| 5     | Session      |
| 4     | Transport    |
| 3     | Network      |
| 2     | Data Link    |
| 1     | Physical     |

The primary purpose of the OSI model is to simplify network design, troubleshooting, and protocol development.

---

## Layer 7 – Application Layer

The Application Layer is the closest layer to the end user.

It provides network services directly to applications.

### Examples

* HTTP
* HTTPS
* DNS
* FTP
* SMTP

### Responsibilities

* Web browsing
* Email
* File transfer
* Name resolution

---

## Layer 6 – Presentation Layer

Responsible for formatting and translating data.

### Responsibilities

* Encryption
* Compression
* Character Encoding

### Example

```text
ASCII ↔ Unicode
```

This layer ensures that data sent by one application can be correctly interpreted by another application.

---

## Layer 5 – Session Layer

Responsible for establishing, managing, and terminating communication sessions between devices.

### Responsibilities

* Session creation
* Session synchronization
* Session recovery

Example:

Video conferencing applications maintain sessions while users communicate.

---
# 5. OSI Model (Continued)

## Layer 4 – Transport Layer

Provides end-to-end communication between applications.

### Protocols

* TCP
* UDP

### Responsibilities

* Segmentation
* Flow Control
* Error Recovery
* Reliability

### Data Unit

```text
Segment
```

---

## Layer 3 – Network Layer

Responsible for routing packets between networks.

### Protocol

* IP

### Device

* Router

### Responsibilities

* Routing
* Logical Addressing

### Data Unit

```text
Packet
```

---

## Layer 2 – Data Link Layer

Provides communication between devices on the same network.

### Responsibilities

* Framing
* MAC Addressing
* Error Detection

### Device

* Switch

### Data Unit

```text
Frame
```

---

## Layer 1 – Physical Layer

Responsible for transmitting raw bits through cables or wireless signals.

### Examples

* Ethernet Cable
* Fiber Optic Cable
* Wi-Fi Signals

### Data Unit

```text
Bits
```

---

# 6. TCP/IP Model

The TCP/IP model is the practical networking model used on the Internet.

| TCP/IP Layer   | OSI Layers |
| -------------- | ---------- |
| Application    | 7, 6, 5    |
| Transport      | 4          |
| Internet       | 3          |
| Network Access | 2, 1       |

---

# 7. Data Encapsulation

As data moves down the OSI layers, headers are added.

```text
Data
 ↓
Segment
 ↓
Packet
 ↓
Frame
 ↓
Bits
```

This process is called **Encapsulation**.

---

# 8. IP Addressing

An IP Address uniquely identifies a device on a network.

## IPv4

32-bit address.

Example:

```text
192.168.1.10
```

## IPv6

128-bit address.

Example:

```text
2001:db8::1
```

### Public IP

Accessible over the Internet.

### Private IP

Used inside local networks.

Ranges:

```text
10.0.0.0 - 10.255.255.255
172.16.0.0 - 172.31.255.255
192.168.0.0 - 192.168.255.255
```

---

# 9. MAC Addressing

A MAC Address is the physical address of a network interface card.

Example:

```text
00:1A:2B:3C:4D:5E
```

### Characteristics

* 48-bit address
* Globally unique
* Assigned by manufacturer

Used for communication inside a LAN.

---

# 10. TCP vs UDP

| TCP                 | UDP            |
| ------------------- | -------------- |
| Reliable            | Unreliable     |
| Connection-Oriented | Connectionless |
| Ordered Delivery    | No Ordering    |
| Slower              | Faster         |

### TCP Uses

* HTTP
* HTTPS
* FTP

### UDP Uses

* Gaming
* Video Streaming
* DNS

---

# 11. DNS

DNS (Domain Name System) converts domain names into IP addresses.

Example:

```text
google.com
     ↓
142.x.x.x
```

Without DNS, users would need to remember IP addresses.

---

# 12. DHCP

DHCP (Dynamic Host Configuration Protocol) automatically assigns:

* IP Address
* Subnet Mask
* Default Gateway
* DNS Server

Usually handled by the router.

---

# 13. ARP

ARP (Address Resolution Protocol) converts:

```text
IP Address
     ↓
MAC Address
```

Used inside local networks.

---

# 14. HTTP and HTTPS

## HTTP

HyperText Transfer Protocol

### Methods

```http
GET
POST
PUT
DELETE
PATCH
```

### Port

```text
80
```

---

## HTTPS

HTTP running over TLS encryption.

### Port

```text
443
```

### Benefits

* Encryption
* Authentication
* Data Integrity

---

# 15. TLS / SSL

TLS secures communication between clients and servers.

### TLS Handshake

1. Client Hello
2. Server Hello
3. Certificate Exchange
4. Key Exchange
5. Secure Communication

Used by HTTPS.

---

# 16. Cryptography

## Symmetric Encryption

Uses the same key for encryption and decryption.

### Examples

* AES
* DES

### Advantage

* Fast

### Disadvantage

* Key Sharing Problem

---

## Asymmetric Encryption

Uses:

* Public Key
* Private Key

### Examples

* RSA
* ECC

### Advantage

* Secure Key Exchange

### Disadvantage

* Slower

---

# 17. Network Security

## Firewall

Monitors and filters network traffic.

### Types

* Hardware Firewall
* Software Firewall

---

## VPN

Virtual Private Network

Creates an encrypted tunnel between a client and a server.

Benefits:

* Privacy
* Security
* Remote Access

---

## NAT

Network Address Translation

Converts:

```text
Private IP
     ↓
Public IP
```

Performed by routers.

---

# 18. How the Internet Works

```text
Computer
   ↓
Switch
   ↓
Router
   ↓
ISP
   ↓
Internet Backbone
   ↓
Destination Server
```

Routers determine the best path for packets to reach their destination.

---

# 19. How Google Loads in Browser

### Step 1

User enters:

```text
https://www.google.com
```

### Step 2

DNS resolves the domain name to an IP address.

### Step 3

TCP Three-Way Handshake

```text
SYN
SYN-ACK
ACK
```

### Step 4

TLS Handshake establishes secure communication.

### Step 5

Browser sends HTTP request.

```http
GET /
Host: google.com
```

### Step 6

Google server sends response.

### Step 7

Browser renders:

* HTML
* CSS
* JavaScript

---

# 20. Remote Access Protocols

## SSH

Secure Shell

### Port

```text
22
```

### Example

```bash
ssh user@server-ip
```

### Features

* Secure
* Encrypted
* Remote Administration

---

## PuTTY

A popular SSH client used on Windows.

Supports:

* SSH
* Telnet
* Serial Connections

---

## Telnet

Remote access protocol.

### Port

```text
23
```

### Limitation

Not encrypted and considered insecure.

---

# Common Ports Cheat Sheet

| Service | Port |
| ------- | ---- |
| FTP     | 21   |
| SSH     | 22   |
| Telnet  | 23   |
| DNS     | 53   |
| HTTP    | 80   |
| HTTPS   | 443  |

---

