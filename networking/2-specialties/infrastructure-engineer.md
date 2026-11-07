# Infrastructure Engineer

## What this role does
Designs, builds, and keeps running the switching, routing, WAN, wireless, and data center networks that organizations depend on. It is the classic network engineer path and the best foundation for every other specialty.

## Prerequisites
Finish [fundamentals](../1-basics/fundamentals.md) and [CCNA](../1-basics/ccna.md). Basic Linux skills help a lot.

## Skills to learn, in order
1. Switching in depth: VLANs, trunking, STP/RSTP, EtherChannel
2. Routing: OSPF, then BGP (the big step up)
3. IPv6, QoS, and first-hop redundancy (HSRP/VRRP)
4. WAN and overlay concepts: MPLS basics, SD-WAN, VXLAN
5. Wireless and monitoring (SNMP, syslog, NetFlow)
6. Troubleshooting method: packet captures and structured diagnosis

## Resources
| Resource | Type | Level | Free/Paid | Notes |
|---|---|---|---|---|
| [Cisco Learning Network](https://learningnetwork.cisco.com) | Community/study groups | Intermediate | Free | Exam topics, forums, and study material for CCNP-level certs. |
| [Packet Pushers](https://packetpushers.net) | Podcasts/articles | Intermediate | Free | Real-world engineering discussions. Good for learning how the job works. |
| [ipspace.net](https://www.ipspace.net) | Blog + courses | Advanced | Free blog, paid courses | Ivan Pepelnjak's design material. Best source for architecture thinking. |
| [FRRouting](https://frrouting.org) + [Containerlab](https://containerlab.dev) | Lab setup | Intermediate | Free | Practice OSPF/BGP on your own Fedora machine without vendor licenses. |
| Juniper Day One books | Short guides | Intermediate | Free | Practical, hands-on guides. Good for seeing a second vendor's approach. |
| [NetworkLessons](https://networklessons.com) | Lessons | Intermediate | Free + paid | Strong explanations of routing protocols, especially BGP. |
| Wendell Odom, *CCNP Enterprise Core (ENCOR) Official Cert Guide* | Book | Intermediate | Paid | The standard text for the next certification level. |
| Jeff Doyle, *Routing TCP/IP, Vol. 1* | Book | Advanced | Paid | The deep reference on routing protocols. |

## Certifications
CCNA, then CCNP Enterprise (ENCOR plus one concentration exam). Verify current exam codes on Cisco's site. Juniper's JNCIA-Junos is a good low-cost vendor-diversity option.

## Project to build
A multi-site lab in Containerlab or GNS3: two sites with OSPF inside each, BGP between them, redundant uplinks, and documented failure tests (pull a link, show the failover).
