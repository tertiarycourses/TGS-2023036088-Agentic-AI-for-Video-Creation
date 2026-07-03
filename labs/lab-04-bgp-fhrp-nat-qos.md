# Lab 04 - BGP Fundamentals, FHRP, NAT, and QoS

## Objectives

- Configure basic eBGP.
- Explain first-hop redundancy.
- Configure NAT/PAT.
- Review QoS classification and marking.

## Steps

1. Build a small enterprise edge and ISP topology.
2. Configure IPv4 addressing.
3. Configure an eBGP neighbor between enterprise and ISP routers.
4. Advertise one enterprise prefix.
5. Verify with `show bgp ipv4 unicast summary`.
6. Verify learned routes.
7. Configure or review HSRP/VRRP behavior for default gateway redundancy.
8. Test active gateway behavior where supported.
9. Configure NAT overload for inside users.
10. Verify NAT translations.
11. Identify voice, video, business, and best-effort traffic classes.
12. Document DSCP marking and queuing concepts.
13. Save configurations and notes.

## Validation

- BGP peering reaches established state where supported.
- NAT translations appear.
- FHRP behavior is explained.
- QoS table maps traffic class to treatment.

## Review Questions

1. Why is BGP used at enterprise edges?
2. What problem does FHRP solve?
3. What is NAT overload?
4. Why does QoS classify traffic?
