# Tools Reference

## Free or Common Lab Tools

| Tool | Use in Course |
| --- | --- |
| Cisco Modeling Labs | Preferred Cisco virtual lab platform where available. |
| GNS3 | Advanced network emulation with supported images. |
| EVE-NG | Multi-vendor network emulation. |
| Cisco Packet Tracer | Conceptual and selected configuration labs. |
| Wireshark | Packet capture and protocol inspection. |
| PuTTY / Tera Term / Windows Terminal | Console and SSH access. |
| diagrams.net | Enterprise architecture and topology diagrams. |
| Text editor | Save running configurations, JSON samples, and troubleshooting notes. |

## Useful Cisco IOS Commands

```text
show running-config
show ip interface brief
show interfaces status
show vlan brief
show interfaces trunk
show spanning-tree
show etherchannel summary
show ip route
show ip protocols
show ip ospf neighbor
show ip eigrp neighbors
show bgp ipv4 unicast summary
show standby brief
show access-lists
show logging
show cdp neighbors detail
show lldp neighbors detail
ping
traceroute
copy running-config startup-config
```

## Enterprise Troubleshooting Flow

1. Define symptom and expected behavior.
2. Check physical and interface state.
3. Check VLAN, trunk, STP, and EtherChannel state.
4. Check IP addressing, gateway, and routing table.
5. Check routing protocol neighbors and advertisements.
6. Check ACLs, NAT, QoS, and security controls.
7. Check logs, telemetry, and recent changes.
8. Change one thing, verify, and document.
