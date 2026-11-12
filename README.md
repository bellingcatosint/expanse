# EXPANSE
## Autonomous Decentralized Networks

**EXPANSE** is an open research and development initiative focused on resilient, autonomous, heterogeneous and decentralized communication infrastructure.

Its central research question is:

> How can a community network remain useful when external Internet connectivity, individual nodes, or entire communication links become unavailable?

EXPANSE investigates architectures that combine multiple physical transports, independent routing and delivery mechanisms, distributed data, and locally available digital services. The goal is not to assume that any single technology can solve the problem, but to test how different components can cooperate—and where their boundaries and failure modes lie.

## Research status

EXPANSE is a research initiative. **Autonomous Heterogeneous Decentralized Network (AHDN)** is a working architectural concept, not a finished product, formal standard, or claim of demonstrated capability.

Design proposals and technical statements must be labelled according to their evidence:

- **Confirmed** — supported by reproducible tests or authoritative technical documentation.
- **Experimental** — observed in a defined experiment, with its conditions recorded.
- **Hypothesis** — a proposition that still requires testing.
- **Unverified** — a claim for which sufficient evidence has not yet been obtained.
- **Refuted** — contradicted by reliable evidence or reproducible testing.

## Research areas

1. **Self-healing networks** — resilience to node, link, and topology changes.
2. **Delay-tolerant networking (DTN)** — store-carry-forward delivery across intermittent or disconnected links.
3. **Heterogeneous mesh transport** — cooperation between Wi-Fi, Ethernet, radio, LoRa, satellite, cellular, and other transports.
4. **Autonomous routing** — route discovery, adaptation, and recovery without a permanent central controller.
5. **Privacy-preserving infrastructure** — reducing unnecessary trust, metadata exposure, and single points of control.
6. **Persistent edge services** — keeping essential local services and data available during isolation.

## Technologies under investigation

The initial technology landscape includes:

- **Yggdrasil** — an IPv6-based encrypted overlay network.
- **Reticulum** — a cryptography-based networking stack designed to operate over diverse physical and link-layer transports.
- **Babel** — a loop-avoiding distance-vector routing protocol for IP networks.
- **DTN / Bundle Protocol** — mechanisms for communication where continuous end-to-end connectivity cannot be assumed.
- **Meshtastic** — an open-source LoRa-based mesh communication system.
- **IPFS** — content-addressed data distribution and retrieval.
- **I2P** — an anonymous overlay network, considered as a separate privacy-oriented research track.

These technologies operate at different layers and are not assumed to be directly interchangeable or plug-compatible. Integration proposals must specify interfaces, addressing, routing, transport assumptions, security boundaries, and failure behaviour.

## Initial architectural model

The working AHDN model separates the system into layers:

1. **Computing infrastructure** — devices, routers, gateways, servers, and mobile nodes.
2. **Physical and link transports** — wired and wireless links, radio, LoRa, satellite, and other available channels.
3. **Transport and delivery** — reliable streams where available, message delivery, buffering, and DTN mechanisms.
4. **Network and routing** — addressing, overlays, route selection, and interconnection between network segments.
5. **Local digital services** — messaging, documentation, data repositories, service discovery, and other community infrastructure.

This is a research model. Its boundaries and interfaces will be revised as experiments produce evidence.

## Initial experimental question

Can a small multi-segment network continue providing useful local communication and access to selected data after losing its external Internet connection and some of its nodes or links—and can it synchronize again when connectivity returns?

A first testbed may include:

- several network segments and approximately ten nodes;
- at least two different transport types;
- local services and a distributed data repository;
- controlled loss of Internet access;
- node and link failures;
- a mobile node moving between segments;
- delayed data transfer and later synchronization.

Experiments should record topology, configuration, software versions, test conditions, observed results, failure modes, and limitations. Results must be reproducible wherever practical.

## Repository structure

```text
.
├── README.md
├── README.uk.md
├── CONTRIBUTING.md
├── SECURITY.md
├── docs/
│   ├── architecture/
│   └── research-methodology/
├── research/
│   ├── self-healing/
│   ├── dtn/
│   ├── heterogeneous-transport/
│   ├── autonomous-routing/
│   ├── privacy/
│   └── edge-services/
└── experiments/
    ├── testbed/
    └── results/
```

Directories and documents will be added as the research programme develops.

## How to contribute

Researchers, network engineers, radio enthusiasts, developers, infrastructure operators, and technical writers are welcome to contribute.

Start with [CONTRIBUTING.md](CONTRIBUTING.md). Contributions should distinguish documented capabilities from assumptions, cite primary technical sources where possible, and include enough detail for independent review.

## Project principles

- Evidence before claims.
- Explicit separation of facts, hypotheses, and experimental observations.
- No dependence on a single vendor, transport, operator, or platform by design.
- Security and privacy considered from the beginning.
- Reproducible tests and openly documented limitations.
- Prefer interoperable open technologies and standards.
- No claim of resilience without a defined threat model and test conditions.

## Licence

No software or documentation licence has been selected yet. Until a licence is added, the repository contents remain subject to applicable copyright law; public visibility does not itself grant permission to reuse them.

## Project identity

**EXPANSE — Autonomous Decentralized Networks**  
Research initiative within the Black Roses / Project Expanse effort.
