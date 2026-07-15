# Cisco-IPSec-Site-to-Site-VPN-Lab
# Cisco IPsec Site-to-Site VPN Lab

> A Cisco Packet Tracer project demonstrating the implementation of a secure Site-to-Site IPsec VPN between two branch offices over an untrusted ISP network.

---

## Project Overview

This project simulates two remote branch offices connected through an ISP using a secure IPsec Site-to-Site VPN.

The VPN encrypts all traffic exchanged between the internal LANs, ensuring confidentiality, integrity, and secure communication across the public network.

The lab was built entirely in Cisco Packet Tracer using Cisco IOS routers.

---

## Objectives

- Design a secure enterprise network
- Configure static routing
- Implement Site-to-Site IPsec VPN
- Configure IKE Phase 1 (ISAKMP)
- Configure IKE Phase 2 (IPsec)
- Configure Crypto Maps
- Protect LAN-to-LAN traffic
- Verify encrypted communication

---

## Network Topology

Two branch offices communicate securely through an ISP router.

```

```
             Branch Office A
        192.168.1.0/24
              |
             R1
              |
      200.165.50.0/24
              |
             ISP
              |
      200.165.40.0/24
              |
             R3
              |
        192.168.2.0/24
          Branch Office B
```

---

## Technologies Used

- Cisco Packet Tracer
- Cisco IOS
- IPsec VPN
- ISAKMP (IKE Phase 1)
- IPsec Transform Sets
- Crypto Maps
- ACLs
- Static Routing
- AES Encryption
- SHA Authentication

---

## Devices

| Device | Quantity |
|----------|----------|
| Cisco Routers | 3 |
| Cisco Switches | 2 |
| PCs | 4 |

---

## IP Addressing

| Device | Interface | IP Address |
|----------|------------|---------------|
| R1 | G0/0 | 200.165.50.1 |
| R1 | G0/1 | 192.168.1.1 |
| ISP | G0/0 | 200.165.50.2 |
| ISP | G0/1 | 200.165.40.2 |
| R3 | G0/1 | 200.165.40.1 |
| R3 | G0/0 | 192.168.2.1 |

---

## VPN Configuration

The VPN was configured using:

### Phase 1 (IKE)

- AES Encryption
- Pre-Shared Key Authentication
- Diffie-Hellman Group 5

### Phase 2 (IPsec)

- ESP-AES
- ESP-SHA-HMAC
- Perfect Forward Secrecy (PFS)

---

## Interesting Traffic

Traffic between the following networks is encrypted:

```

192.168.1.0/24

↓

192.168.2.0/24

```

---

## Verification

The VPN was successfully verified using:

- Successful ping between branch offices
- show crypto isakmp sa
- show crypto ipsec sa
- Packet counters increasing
- Encrypted packets
- Decrypted packets

---

## Skills Demonstrated

- Enterprise Network Design
- Secure VPN Deployment
- Cisco IOS Configuration
- Routing
- ACL Configuration
- Network Security
- IPsec
- IKE
- VPN Troubleshooting

---

## Screenshots

### Network Topology

![Topology](Images/topology.png)

---

### Successful Connectivity Test

![Ping](Images/ping-success.png)

---

### ISAKMP Security Association

![ISAKMP](Images/show-crypto-isakmp-sa.png)

---

### IPsec Security Association

![IPSEC](Images/show-crypto-ipsec-sa.png)

---

### Crypto Map Configuration

![CryptoMap](Images/crypto-map.png)

---

### Router Configuration

![RunningConfig](Images/show-run.png)

---

## Folder Structure

```

Cisco-IPSec-Site-to-Site-VPN-Lab
│
├── README.md
├── PacketTracer
├── Configurations
├── Images
├── Report
└── Docs

```

---

## Learning Outcomes

Through this project I gained hands-on experience with:

- Cisco VPN technologies
- Secure enterprise networking
- IPsec tunnel establishment
- Encryption and authentication
- VPN verification
- Cisco IOS troubleshooting

---

## Author

**Mohamed Ibrahim Shire**

SOC Analyst | Network Security | Digital Forensics

GitHub:
https://github.com/mohaShire12

LinkedIn:
https://linkedin.com/in/mohamed-ibrahim-shire-b64830234

