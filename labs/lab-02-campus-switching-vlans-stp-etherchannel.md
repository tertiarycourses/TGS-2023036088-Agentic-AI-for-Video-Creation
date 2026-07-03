# Lab 02 - Campus Switching, VLANs, STP, and EtherChannel

## Objectives

- Configure enterprise VLANs and trunks.
- Verify STP behavior.
- Configure LACP EtherChannel.
- Troubleshoot Layer 2 faults.

## Steps

1. Build a three-switch campus topology.
2. Create user, voice, server, and management VLANs.
3. Assign access ports to the correct VLANs.
4. Configure trunks between switches.
5. Verify with `show interfaces trunk`.
6. Run `show spanning-tree`.
7. Identify root bridge, root ports, designated ports, and blocked ports.
8. Configure the intended root bridge priority.
9. Enable PortFast on access ports.
10. Discuss BPDU Guard and Root Guard.
11. Configure LACP EtherChannel between two switches.
12. Verify with `show etherchannel summary`.
13. Create and fix one Layer 2 fault.
14. Save final configurations.

## Validation

- VLANs and trunks are correct.
- Intended STP root bridge is active.
- EtherChannel is bundled.
- Troubleshooting notes include symptom, cause, and fix.

## Review Questions

1. Why is STP still important in switched networks?
2. What does LACP negotiate?
3. Why should PortFast be limited to access ports?
4. How can trunk mismatches affect reachability?
