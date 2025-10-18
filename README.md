# UIU Enterprise Network Design using Packet Tracer

![GitHub contributors](https://img.shields.io/github/contributors/TashinParvez/UIU_Enterprise_Network_Design_PacketTracer)
![GitHub last commit](https://img.shields.io/github/last-commit/TashinParvez/UIU_Enterprise_Network_Design_PacketTracer)
![Visitor Count](https://visitor-badge.laobi.icu/badge?page_id=TashinParvez.UIU_Enterprise_Network_Design_PacketTracer)

## Overview

This repository contains the implementation of an **Enterprise Network** for United International University (UIU) using **Cisco Packet Tracer**. This project is a **Computer Network Lab assignment [CSE 3712]** that demonstrates the design, configuration, and testing of a functional enterprise network following real-world networking principles.

The network includes multiple routers, switches, and hosts, and demonstrates subnetting, routing, NAT, and DHCP functionalities.

---

## Project Features

The implemented network includes:

- **Hosts**: 30+ devices including PCs, laptops, and servers. At least 15 PCs are configured.
- **Routers and Switches**: 6 routers and 6 switches/hubs, connected in a realistic enterprise topology (not a linear setup).
- **Network Segmentation**: Two main networks:

  - Private Network
  - Public Network
  - NAT (Static/Dynamic) used for connectivity between the two.

- **Subnetting**: Custom subnets for efficient IP address management.
- **Routing**: Implemented using **RIP, OSPF, or static routing** to create routing tables on all routers.
- **DHCP**: Dynamically assigns IP addresses to all PCs in the network.
- **Testing**: Full connectivity verified by pinging all devices.

---

## Network Design

- Clean and organized layout in Packet Tracer.
- All devices are labeled with meaningful hostnames.
- Subnets and connections are clearly displayed for readability.

---

## IOS Commands Used

Example commands used in router configuration:

```bash
# Configure hostname
Router> enable
Router# configure terminal
Router(config)# hostname R1

# Configure interfaces
R1(config)# interface g0/0
R1(config-if)# ip address 192.168.1.1 255.255.255.0
R1(config-if)# no shutdown

# Enable RIP routing
R1(config)# router rip
R1(config-router)# version 2
R1(config-router)# network 192.168.1.0

# Configure NAT (example)
R1(config)# access-list 1 permit 192.168.1.0 0.0.0.255
R1(config)# ip nat inside source list 1 interface g0/1 overload

# Configure DHCP
R1(config)# ip dhcp pool UIU_PC
R1(dhcp-config)# network 192.168.1.0 255.255.255.0
R1(dhcp-config)# default-router 192.168.1.1
```

_Note: Full command list is available in the submitted report._

---

## Challenges Faced

- Designing a non-linear router topology that mimics real-world enterprise networks.
- Configuring NAT correctly between public and private networks.
- Subnetting efficiently to accommodate all hosts.
- Ensuring DHCP configuration does not overlap with static IPs.

---

## Files in Repository

- `UIU_Enterprise_Network_Design.pkt` – Cisco Packet Tracer file of the implemented network.
- `UIU_Network_Design_Report.pdf` – 1-3 page report detailing implementation, IOS commands, and learning outcomes.

---

## How to Open

1. Download and install **Cisco Packet Tracer** (Version 8.x recommended).
2. Open `UIU_Enterprise_Network_Design.pkt` to explore and test the network.

---

## Author

**Tashin** – CSE Student, UIU
This project is part of the **Computer Network Lab assignment**.

---

## 📞 Contact

For any questions, suggestions, or feedback, please feel free to reach out to the repository maintainer.

<p align="left">
  <a href="mailto:tashinparvez2002@gmail.com" target="blank">
    <img src="https://img.shields.io/badge/Email-0078D4?style=for-the-badge&logo=gmail&logoColor=white" alt="Tashin Parvez Email" />
  </a>
  <a href="https://linkedin.com/in/tashinparvez" target="blank">
    <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white" alt="Tashin Parvez LinkedIn" />
  </a>
  <a href="https://fb.com/tashin.parvez.5" target="blank">
    <img src="https://img.shields.io/badge/Facebook-1877F2?style=for-the-badge&logo=facebook&logoColor=white" alt="Tashin Parvez Facebook" />
  </a>
  <a href="https://tashinparvez.hashnode.dev/" target="blank">
    <img src="https://img.shields.io/badge/Hashnode-2962FF?style=for-the-badge&logo=hashnode&logoColor=white" alt="Tashin Parvez Hashnode" />
  </a>
</p>

Happy Learning! 🚀
