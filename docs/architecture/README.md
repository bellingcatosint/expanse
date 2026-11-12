# Architecture Research

## Working concept: AHDN

**Autonomous Heterogeneous Decentralized Network (AHDN)** is the current working name for an architecture that aims to preserve useful communication and local services across changing network conditions.

AHDN is a research concept, not a deployed system or standard.

## Design objectives

- Continue useful local operation during loss of external Internet connectivity.
- Tolerate intermittent links and partial network partitions.
- Support more than one physical transport.
- Avoid a permanent central controller as a required component.
- Keep selected data and services available locally.
- Recover connectivity and reconcile delayed data when links return.
- Make security boundaries and trust assumptions explicit.

## Layer model

| Layer | Scope | Research questions |
|---|---|---|
| Computing infrastructure | Devices, routers, gateways, servers | Which nodes can host services or bridge segments? |
| Physical and link transports | Ethernet, Wi-Fi, radio, LoRa, satellite, cellular | What are the bandwidth, range, power, and availability constraints? |
| Transport and delivery | Streams, messages, buffering, DTN | How is data delivered when a continuous path does not exist? |
| Network and routing | Addressing, overlays, route selection | How are networks interconnected and routes recovered? |
| Local services | Messaging, repositories, discovery, documentation | Which functions remain useful while isolated? |

This table is a decomposition for research, not a claim that every technology maps neatly to one layer.

## Initial technology boundaries

- **Yggdrasil** provides an IPv6 overlay network. It does not, by itself, turn arbitrary non-IP radio links into compatible transports.
- **Reticulum** is designed to operate across diverse interface types. Its addressing and transport model differ from ordinary IP routing.
- **Babel** is an IP routing protocol. It is not a generic DTN protocol and does not automatically route over every radio or messaging system.
- **Meshtastic** provides LoRa-based messaging. It should not be treated as a transparent IP bearer without a separately demonstrated gateway design.
- **DTN / Bundle Protocol** addresses store-and-forward delivery under disrupted connectivity; it is not a replacement for all routing functions.
- **IPFS** distributes content by content identifiers. Availability still depends on reachable providers, caching, pinning, and replication strategy.
- **I2P** is a privacy-oriented overlay and should initially be evaluated as a separate subsystem.

## Integration rule

No integration should be described as complete merely because two components can be installed on the same device. A proposal must identify:

1. the interface between components;
2. addressing and identity mapping;
3. routing and forwarding responsibilities;
4. buffering and delivery semantics;
5. security and trust boundaries;
6. failure detection and recovery behaviour;
7. resource costs and operational constraints;
8. test cases and measurable acceptance criteria.

## First validation scenario

Build a small multi-segment testbed. Establish baseline local communication and service availability. Then introduce, one at a time and in combinations:

- external Internet loss;
- loss of selected links;
- loss of selected nodes;
- network partition;
- intermittent connectivity;
- movement of a mobile node between segments;
- delayed data delivery and later reconnection.

Measure service availability, message delivery success, delivery latency, convergence or recovery time, data consistency, bandwidth use, and energy consumption where relevant.

Every result must include test conditions and limitations. A successful laboratory demonstration does not establish resilience under every real-world threat model.
