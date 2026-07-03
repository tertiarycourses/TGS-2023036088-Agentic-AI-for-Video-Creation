# Learner Guide - Cisco Certified Network Professional (CCNP) for ENCOR Training

## Course Overview

This learner guide supports hands-on CCNP ENCOR training for learners building enterprise networking skills. The course focuses on planning, configuring, operating, securing, troubleshooting, and automating enterprise networks.

The labs follow the main ENCOR capability areas:

1. Enterprise architecture.
2. Virtualization.
3. Infrastructure.
4. Network assurance.
5. Security.
6. Automation.

## Before You Start

### Recommended Lab Tools

Use one of the following:

- Cisco Modeling Labs.
- GNS3.
- EVE-NG.
- Cisco Packet Tracer for selected concepts.
- Physical Cisco routers, switches, and wireless lab equipment.

Some ENCOR features are platform-dependent. If a simulator does not support a command, document the concept, configuration intent, and verification equivalent.

### Lab Journal

For every lab, record:

- Topology diagram.
- Addressing and VLAN table.
- Routing protocol plan.
- Device names and roles.
- Configuration commands.
- Verification commands.
- Troubleshooting observations.
- Final saved configuration.

### Core Verification Commands

```text
show running-config
show ip interface brief
show interfaces status
show vlan brief
show interfaces trunk
show spanning-tree
show etherchannel summary
show ip route
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
```

## Learning Outcomes

By the end of the course, you should be able to:

1. Compare enterprise campus, WAN, cloud, and data center architecture patterns.
2. Explain virtualization concepts such as VRF, overlay, underlay, and tunneling.
3. Configure campus switching with VLANs, trunks, STP, and EtherChannel.
4. Configure Layer 3 switching with SVIs and routed ports.
5. Configure and verify OSPF and EIGRP concepts.
6. Explain BGP fundamentals and configure simple eBGP peering.
7. Explain FHRP and configure HSRP-style gateway redundancy where supported.
8. Configure NAT/PAT and explain QoS classification and marking.
9. Secure enterprise device access with management hardening, ACLs, and AAA concepts.
10. Explain enterprise wireless architecture, roaming, and WLAN security.
11. Use network assurance tools such as syslog, SNMP, NetFlow concepts, SPAN, and IP SLA.
12. Explain controller-based networking, REST APIs, JSON, and automation workflows.

## Course Flow

### Day 1

| Time | Activity |
| --- | --- |
| 09:00 | Course briefing, ENCOR scope, lab tools |
| 09:30 | Lab 01 - Enterprise Architecture, Virtualization, and Design |
| 13:00 | Lab 02 - Campus Switching, VLANs, STP, and EtherChannel |
| 16:00 | Review and configuration backup |

### Day 2

| Time | Activity |
| --- | --- |
| 09:00 | Day 1 recap |
| 09:30 | Lab 03 - Layer 3 Switching, OSPF, and EIGRP |
| 13:30 | Lab 04 - BGP Fundamentals, FHRP, NAT, and QoS |
| 16:30 | Routing verification and troubleshooting review |

### Day 3

| Time | Activity |
| --- | --- |
| 09:00 | Infrastructure recap |
| 09:30 | Lab 05 - Enterprise Security, ACLs, AAA, and Device Hardening |
| 13:30 | Lab 06 - Enterprise Wireless, WLC, Roaming, and Security |
| 16:30 | Security and wireless review |

### Day 4

| Time | Activity |
| --- | --- |
| 09:00 | Operations and assurance briefing |
| 09:30 | Lab 07 - Network Assurance, Telemetry, and Troubleshooting |
| 13:30 | Lab 08 - Automation, Controller-Based Networking, APIs, and Exam Review |
| 16:30 | Exam readiness checklist |

### Day 5

| Time | Activity |
| --- | --- |
| 09:00 | Integrated enterprise troubleshooting scenario |
| 11:00 | Learner lab remediation and instructor review |
| 13:00 | Practice assessment and discussion |
| 15:30 | Final configuration archive and study plan |

## Lab 01 Guide - Enterprise Architecture, Virtualization, and Design

### Objectives

- Compare enterprise architecture models.
- Explain campus, WAN, cloud, and data center roles.
- Understand virtualization and segmentation.
- Draft an enterprise topology.

### Steps

1. Draw two-tier and three-tier campus designs.
2. Identify access, distribution, and core responsibilities.
3. Add WAN edge, internet edge, data center, cloud, and branch components.
4. Compare traditional WAN, SD-WAN, and cloud connectivity at a high level.
5. Explain control plane, data plane, and management plane.
6. Explain VRF as routing table segmentation.
7. Explain overlay and underlay concepts.
8. Identify where redundancy is required in the design.
9. Create an addressing and VLAN naming convention.
10. Build a small enterprise topology in your lab tool.
11. Assign device names and roles.
12. Save the topology as the baseline for later labs.

### Deliverables

- Enterprise architecture diagram.
- Device role table.
- VLAN and addressing convention.
- Virtualization concept notes.

### Checkpoint

You can explain why enterprise networks separate access, distribution, core, edge, and services functions.

## Lab 02 Guide - Campus Switching, VLANs, STP, and EtherChannel

### Objectives

- Configure VLANs and trunks.
- Verify STP behavior.
- Configure EtherChannel.
- Troubleshoot Layer 2 issues.

### Steps

1. Build a three-switch campus topology.
2. Create user, voice, server, and management VLANs.
3. Assign access ports to VLANs.
4. Configure 802.1Q trunks between switches.
5. Verify trunk allowed VLANs and native VLAN.
6. Run `show spanning-tree` and identify root bridge and port roles.
7. Configure the intended root bridge priority.
8. Enable PortFast on access ports.
9. Discuss BPDU Guard and Root Guard use cases.
10. Configure LACP EtherChannel between distribution switches.
11. Verify with `show etherchannel summary`.
12. Create one Layer 2 fault and troubleshoot it.
13. Save the configuration.

### Deliverables

- VLAN table.
- Trunk and STP verification outputs.
- EtherChannel configuration.
- Layer 2 troubleshooting notes.

### Checkpoint

You can explain how STP and EtherChannel work together to provide loop prevention and bandwidth/resiliency.

## Lab 03 Guide - Layer 3 Switching, OSPF, and EIGRP

### Objectives

- Configure Layer 3 switching.
- Configure OSPF.
- Review EIGRP concepts.
- Verify routing decisions.

### Steps

1. Enable IP routing on a Layer 3 switch if supported.
2. Configure SVIs for campus VLAN gateways.
3. Configure routed ports between distribution and core devices.
4. Verify local inter-VLAN routing.
5. Configure OSPF area 0 on core and distribution links.
6. Set router IDs.
7. Use passive interfaces where appropriate.
8. Verify OSPF neighbors and routes.
9. Review DR/BDR behavior on broadcast segments.
10. Configure route summarization conceptually or in a supported topology.
11. Review EIGRP neighbor, metric, feasible successor, and summarization concepts.
12. Configure EIGRP if supported by your lab image.
13. Compare OSPF and EIGRP verification outputs.

### Deliverables

- Layer 3 switching configuration.
- OSPF neighbor and route outputs.
- EIGRP concept or configuration notes.
- Routing comparison table.

### Checkpoint

You can verify enterprise routing from access VLAN to routed core and explain why a route is chosen.

## Lab 04 Guide - BGP Fundamentals, FHRP, NAT, and QoS

### Objectives

- Configure basic eBGP peering.
- Explain first-hop redundancy.
- Configure NAT/PAT.
- Review QoS classification and marking.

### Steps

1. Build a small enterprise edge topology with two routers.
2. Configure a simple eBGP peering between enterprise and ISP routers.
3. Advertise one enterprise prefix.
4. Verify BGP summary and learned routes.
5. Configure default routing toward the internet edge.
6. Configure HSRP or review FHRP behavior if supported.
7. Verify active and standby gateway behavior.
8. Configure NAT/PAT for inside users.
9. Verify NAT translations.
10. Identify traffic classes for voice, video, business applications, and best effort.
11. Configure or document DSCP marking concepts.
12. Explain congestion management and policing/shaping at a high level.

### Deliverables

- BGP peering output.
- FHRP notes or configuration.
- NAT/PAT configuration.
- QoS classification table.

### Checkpoint

You can explain how enterprise edge routing, gateway redundancy, address translation, and QoS support resilient connectivity.

## Lab 05 Guide - Enterprise Security, ACLs, AAA, and Device Hardening

### Objectives

- Harden network device management.
- Apply ACLs.
- Explain AAA.
- Configure Layer 2 security controls.

### Steps

1. Review current device management settings.
2. Require SSH for remote access.
3. Configure local usernames and strong secrets.
4. Restrict VTY access with a management ACL.
5. Configure exec timeout and login banners.
6. Explain AAA and compare TACACS+ and RADIUS.
7. Configure a standard ACL and extended ACL in a lab scenario.
8. Verify ACL hit counts and traffic behavior.
9. Enable port security on selected access ports.
10. Review DHCP snooping and Dynamic ARP Inspection.
11. Configure DHCP snooping if supported.
12. Discuss control plane policing concepts.
13. Save security baseline configuration.

### Deliverables

- Device hardening checklist.
- ACL configuration and verification.
- AAA concept notes.
- Layer 2 security notes.

### Checkpoint

You can explain how management security, ACLs, AAA, and Layer 2 protections reduce enterprise risk.

## Lab 06 Guide - Enterprise Wireless, WLC, Roaming, and Security

### Objectives

- Explain enterprise wireless architecture.
- Review AP and WLC roles.
- Configure or document WLAN profiles.
- Understand roaming and security.

### Steps

1. Draw an enterprise wireless architecture.
2. Identify AP, WLC, CAPWAP, client, RADIUS, and switching roles.
3. Compare autonomous, lightweight, and cloud-managed AP models.
4. Define an SSID and VLAN mapping.
5. Review WPA2/WPA3, PSK, and 802.1X concepts.
6. Configure a WLAN profile if your lab tool supports it.
7. Review RF concepts: channel, band, interference, power, and coverage.
8. Explain Layer 2 and Layer 3 roaming at a high level.
9. Identify wireless troubleshooting data to collect.
10. Document a secure guest wireless design.

### Deliverables

- Wireless architecture diagram.
- WLAN profile notes.
- Security and roaming notes.
- Guest wireless design notes.

### Checkpoint

You can explain how WLCs, APs, SSIDs, VLANs, and security policies work together.

## Lab 07 Guide - Network Assurance, Telemetry, and Troubleshooting

### Objectives

- Configure and review operational logging.
- Use monitoring and telemetry concepts.
- Practise structured troubleshooting.
- Document evidence and fixes.

### Steps

1. Configure syslog or logging buffer.
2. Configure NTP or document the time source.
3. Review SNMP manager and agent concepts.
4. Review NetFlow/IPFIX concepts.
5. Configure SPAN or packet capture if supported.
6. Configure IP SLA tracking if supported.
7. Create a controlled fault in routing, VLANs, ACLs, or services.
8. Start with symptom and expected behavior.
9. Check Layer 1 and Layer 2 evidence.
10. Check routing, services, and security controls.
11. Fix one issue at a time.
12. Verify end-to-end reachability and log evidence.
13. Write a troubleshooting report.

### Deliverables

- Logging and assurance configuration notes.
- Monitoring concept table.
- Troubleshooting report.
- Verification outputs.

### Checkpoint

You can collect operational evidence and use it to solve enterprise network issues methodically.

## Lab 08 Guide - Automation, Controller-Based Networking, APIs, and Exam Review

### Objectives

- Explain controller-based networking.
- Understand REST APIs and JSON.
- Review automation tooling.
- Build an ENCOR exam readiness plan.

### Steps

1. Compare traditional device-by-device management with controller-based networking.
2. Identify control plane, data plane, and management plane in an SDN design.
3. Explain northbound and southbound APIs.
4. Review Cisco DNA Center or controller concepts.
5. Read a sample JSON object and identify keys, values, arrays, and nested objects.
6. Explain REST methods: GET, POST, PUT/PATCH, DELETE.
7. Review Ansible inventory, playbook, and idempotency concepts.
8. Review model-driven telemetry and configuration management concepts.
9. Identify which course labs map to each ENCOR domain.
10. Create a personal weak-topic list.
11. Write a 14-day study plan.
12. Archive all final configs and notes.

### Deliverables

- SDN/controller concept notes.
- JSON/API worksheet.
- Automation tool comparison.
- Personal ENCOR study plan.

### Checkpoint

You can explain how automation and controllers change enterprise network operations.

## Final Skills Checklist

Before finishing the course, confirm that you can:

- Explain enterprise architecture and virtualization concepts.
- Configure VLANs, trunks, STP, and EtherChannel.
- Configure Layer 3 switching.
- Configure and verify OSPF.
- Explain EIGRP and BGP fundamentals.
- Explain FHRP, NAT, and QoS.
- Secure management access and apply ACLs.
- Explain AAA and Layer 2 security.
- Explain enterprise wireless architecture.
- Use assurance tools and troubleshooting workflow.
- Explain REST APIs, JSON, controller-based networking, and automation basics.
