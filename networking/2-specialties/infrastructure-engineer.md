# Infrastructure Engineer

**Role:** designs and runs switching, routing, WAN, wireless and data center networks.
**Prerequisites:** [Fundamentals](../1-basics/fundamentals.md) and [CCNA](../1-basics/ccna.md).

## Skills, in order
1. VLANs, trunking, STP, EtherChannel
2. OSPF, then BGP
3. IPv6, QoS, HSRP/VRRP
4. WAN and overlays: MPLS basics, SD-WAN, VXLAN
5. Monitoring: SNMP, syslog, NetFlow
6. Structured troubleshooting

**Path at a glance:**
- Intermediate: FRR + Containerlab labs, then DevNet Sandbox for real Cisco platforms, with NetworkLessons for explanations.
- Advanced: Juniper Open Learning for a second vendor, ipspace.net for design thinking, INE for CCNP and CCIE depth.

## Resources
| Resource | Level | Cost | What it is | You will be able to |
|---|---|---|---|---|
| [FRRouting docs](https://docs.frrouting.org) with [Containerlab](https://containerlab.dev) | Intermediate | Free | Reference for FRR, an actively maintained open-source routing suite covering BGP, OSPF, IS-IS, BFD, VRRP and more. Pair it with a Containerlab topology. | Build and break OSPF and BGP labs on your own machine with no licences. |
| [Cisco DevNet Sandbox](https://developer.cisco.com/docs/sandbox/) | Intermediate | Free | Hosted Cisco labs. Always-on sandboxes are shared with restricted admin rights. Reservable ones are private with full admin access. Needs a free Cisco.com account and a VPN client. | Configure and inspect real or virtual Cisco platforms without buying hardware. |
| [Juniper Open Learning](https://www.juniper.net/us/en/training/open-learning) | Intermediate | Free training, discounted exam | Free self-paced Junos courses with a certification exam voucher at 75% off. | Configure Junos switching and routing and prepare for JNCIA. |
| [Cisco U. and Learning Network](https://learningnetwork.cisco.com) | Intermediate | Free + paid | Official CCNP study paths and community. | Follow an official CCNP-level study plan with peer support. |
| [NetworkLessons](https://networklessons.com) | Intermediate | Free + paid | Lessons with strong routing coverage, especially BGP. | Explain and configure BGP and other routing protocols. |
| [Packet Pushers](https://packetpushers.net) | Intermediate | Free | Podcasts and articles from working engineers. | Understand how the job and real designs work. |
| [CBT Nuggets](https://www.cbtnuggets.com) | Intermediate | Paid | Engaging CCNP-level video training. | Cover CCNP topics in a structured video format. |
| [ipspace.net](https://www.ipspace.net) | Advanced | Free blog + paid courses | Network design material by Ivan Pepelnjak. | Reason about network architecture and trade-offs. |
| [INE Learning](https://ine.com) | Advanced | Paid | Deep routing and CCNP/CCIE training. | Master advanced routing and prepare for expert-level exams. |

## Certifications
CCNA, then CCNP Enterprise. Juniper JNCIA-Junos is a low-cost second vendor.

## Project
Two-site lab: OSPF inside each site, BGP between them, redundant links, and documented failover tests. Build it in Containerlab with FRR.
