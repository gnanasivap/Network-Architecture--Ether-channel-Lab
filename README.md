# 🌐 Network Architecture – EtherChannel Lab | Cisco Packet Tracer

## 📌 Project Overview

This project focuses on understanding **EtherChannel technology** and its role in improving network performance, bandwidth, and redundancy using Cisco Packet Tracer.

EtherChannel allows multiple physical Ethernet links to be combined into a single logical connection between network devices.

This lab is part of my **CCNA Hands-on Networking Practice** to develop practical knowledge of switching technologies and network architecture.

## 🎯 Project Objectives

- Understand EtherChannel technology.
- Learn how multiple physical links form one logical connection.
- Explore Link Aggregation Control Protocol (LACP).
- Understand Port Aggregation Protocol (PAgP).
- Learn EtherChannel configuration concepts.
- Understand network redundancy and load balancing.
- Verify EtherChannel status using Cisco IOS commands.
- Improve network troubleshooting skills.

## 🖥️ Network Topology

The project focuses on EtherChannel connections in a switched network environment.

EtherChannel combines multiple physical Ethernet links into a single logical Port-Channel interface.

### Conceptual Network Diagram

```text
       Switch 1                 Switch 2
     +----------+             +----------+
     |          |---- Fa0/1 ---|          |
     |          |---- Fa0/2 ---|          |
     |          |---- Fa0/3 ---|          |
     +----------+             +----------+
             \                 /
              \---EtherChannel-/
```

The complete network topology is available in the Cisco Packet Tracer project file.

## 🛠️ Tools & Technologies

| Technology | Description |
|---|---|
| Cisco Packet Tracer | Network simulation |
| Cisco Switches | Layer 2 switching |
| EtherChannel | Link aggregation |
| LACP | IEEE-standard negotiation protocol |
| PAgP | Cisco-proprietary negotiation protocol |
| Cisco IOS CLI | Network configuration and verification |

## ⚙️ EtherChannel Configuration

The following are example configurations for learning EtherChannel. Actual interface numbers and protocols depend on the project.

### 1. Configure LACP EtherChannel

```bash
enable
configure terminal

interface range fa0/1 - 2
switchport mode trunk
channel-group 1 mode active
exit

interface port-channel 1
switchport mode trunk
exit
```

LACP uses the following modes:

- **Active:** Actively negotiates EtherChannel.
- **Passive:** Responds to LACP negotiation.

### 2. Configure PAgP EtherChannel

```bash
enable
configure terminal

interface range fa0/1 - 2
switchport mode trunk
channel-group 1 mode desirable
exit

interface port-channel 1
switchport mode trunk
exit
```

PAgP uses the following modes:

- **Desirable:** Actively negotiates EtherChannel.
- **Auto:** Responds to PAgP negotiation.

### 3. Configure Static EtherChannel

```bash
enable
configure terminal

interface range fa0/1 - 2
switchport mode trunk
channel-group 1 mode on
exit

interface port-channel 1
switchport mode trunk
exit
```

Static EtherChannel does not use LACP or PAgP negotiation.

**Note:** These configurations are alternative examples, not commands to apply together on the same interfaces. Both ends must use compatible configurations.

## 🔍 EtherChannel Verification Commands

### Check EtherChannel Summary

```bash
show etherchannel summary
```

### Check Port-Channel Information

```bash
show etherchannel port-channel
```

### Check EtherChannel Details

```bash
show etherchannel detail
```

### Verify Trunk Configuration

```bash
show interfaces trunk
```

### Verify Interface Status

```bash
show interfaces status
```

## 🔄 EtherChannel Protocol Comparison

| Feature | LACP | PAgP | Static |
|---|---|---|---|
| Protocol | IEEE 802.3ad / 802.1AX | Cisco Proprietary | No negotiation |
| Modes | Active / Passive | Desirable / Auto | On |
| Negotiation | Yes | Yes | No |
| Link Aggregation | Yes | Yes | Yes |

## 🚀 Benefits of EtherChannel

### 1. Increased Bandwidth

Multiple physical links can provide additional aggregate bandwidth between switches.

### 2. Network Redundancy

If one physical link fails, the remaining active links can continue carrying traffic.

### 3. Load Balancing

Network traffic can be distributed across the physical links using a hashing mechanism.

### 4. Improved Network Performance

EtherChannel improves link utilization and provides reliable network connectivity.

### 5. Spanning Tree Integration

Spanning Tree Protocol treats an EtherChannel bundle as a single logical interface.

## 🧪 Network Verification

The following checks can be performed to verify EtherChannel operation:

- [ ] Verify physical interface connections.
- [ ] Check EtherChannel configuration.
- [ ] Verify Port-Channel status.
- [ ] Confirm member interfaces are bundled.
- [ ] Verify trunk configuration.
- [ ] Test connectivity between network devices.
- [ ] Check network connectivity after a member link failure.

## 📚 Key Learnings

Through this project, I focused on understanding:

- EtherChannel technology and link aggregation.
- LACP and PAgP negotiation.
- Static EtherChannel configuration.
- Port-Channel interfaces.
- Network redundancy.
- Load balancing concepts.
- Switch-to-switch connectivity.
- Cisco IOS verification commands.
- Basic network troubleshooting.

## 📁 Project File

**Network Architecture- EtherChannel Lab.pkt**

Open this file using **Cisco Packet Tracer** to explore the network topology and configurations.

## 🚀 Skills Practiced

- Cisco Packet Tracer
- Cisco Switching
- EtherChannel
- LACP
- PAgP
- Link Aggregation
- Port-Channel Configuration
- Network Redundancy
- Network Architecture
- Cisco IOS CLI
- Network Troubleshooting

## 👨‍💻 CCNA Journey

This project is part of my ongoing **CCNA Journey** and hands-on networking practice.

As an aspiring Network Engineer, I am continuously improving my practical knowledge of networking technologies through Cisco Packet Tracer labs.

These hands-on projects help me strengthen my understanding of network configuration, switching technologies, network redundancy, and troubleshooting.

**Learning Networking One Lab at a Time! 🌐🚀**
