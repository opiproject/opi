# OPI Scope Proposal

The following is a proposal from Intel on a future OPI Release.

# Proposed OPI Scope

1. OPI Provisioning & Lifecycle Specification (started [here](https://github.com/opiproject/opi-prov-life/blob/main/SPEC.md))
    - Ratified by OPI w/ version number & tracking
    - Ability for Intel to precisely describe what is supported / coming soon / unsupported
    - Longer term OPI should have a certification process within the lab

2. OPI APIs ratified by OPI w/ version number & tracking for the following:
    - [Port Config](https://github.com/opiproject/opi-api/issues/441): Ethernet port state, statistics, and configuration.
        - Current status: OpenConfig being developed based on interfaces
    - [Virtual Device Config](https://github.com/opiproject/opi-api/issues/442): Virtual port/disk add/del, statistics, configuration, SR-IOV config.
        - Current status: Custom OpenConfig developed 
    - Virtual L2 Learning:  Learn MACs on virtual ports, as well as associate IP addresses to MACs (ARP/ND).
        - Current status: Using P4Runtime directly in OVS
    - LACP Active-Active Link Redundancy: Support physical port multipath to multiple attached switches.
        - Current status: Using Linux Control Plane via netlink sockets
    - ECMP Active-Active Link Redundancy: Support physical port multipath to multiple attached routers.
        - Current status: Using Linux Control Plane running FRR via netlink sockets
    - OpenStack Security Groups: Support the creation/update/deletion of security groups at the boundaries of virtual L2 domains
        - Current status: Using P4Runtime directly
    - Kubernetes L3 Routing: Route between pods (local and remote), discover new endpoints, load balance across endpoints that share the same VIP, NAT in/out of virtual IPs.
        - Current Status: Using Calico Dataplane API
    - Kubernetes Policy: Create ACLs based on IP N-tuple (Source IP, Dest IP, Protocol, Source Port, Dest Ports, etc.). 
        - Current Status: Use Calico Dataplane API to implement Kubernetes Policy
    - EVPN Routing Gateway: Interconnect virtual L2/L3 domains using EVPN w/ dataplane in the IPU.
        - Current status: Programming API submitted [here](https://github.com/opiproject/opi-api/tree/main/network/evpn-gw).
    - Virtual Block Storage Initiator & Target: Support for virtual block storage initiator and target implemented in all software (SPDK) or IPU.
        - Current status: Using OPI Storage APIs common across implementations [here](https://github.com/opiproject/opi-api/tree/main/storage).
    - IPsec: Configuration of IPsec IKE stack to manage IPsec connections/tunnels.
        - Current status: Using OPI Security API common across implementations that configures strongSwan vici [here](https://github.com/opiproject/opi-api/tree/main/security).

3. OPI Maintained Codebases recognized by OPI as being aligned to OPI's specs, APIs, and processes for the following use cases:
    - **Virtualized Block Storage** found [here](https://github.com/opiproject/opi-intel-bridge) for Intel targets
    - **Virtualized L2 Switching, Policy & Load Balancing** using [OVS](https://openvswitch.org)/[OVN](https://ovn.org) found [here](https://github.com/ipdk-io/networking-recipe) for [IPDK](https://ipdk.io) compatible targets
    - **Kubernetes L3 Routing, Policy & Load Balancing** using [Calico](https://www.tigera.io/project-calico/) found [here](https://github.com/ipdk-io/k8s-infra-offload) for [IPDK](https://ipdk.io) compatible targets
    - **EVPN Gateway** using [FRR](https://frrouting.org/) found [here](https://github.com/opiproject/opi-evpn-bridge) for Intel targets
    - **Inline IPsec** using [strongSwan](https://www.strongswan.org/) found [here](https://github.com/ipdk-io/ipsec-recipe) for [IPDK](https://ipdk.io) targets

