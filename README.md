<div align="center">

# SAYANJALI BLOCKCHAIN

**Testnet Foundation — Early-Stage Layer-1 Infrastructure**

An independently engineered, open-source Layer-1 blockchain built from scratch in Python — now in its Testnet Foundation stage, with a native SYJ monetary protocol, Proof-of-Work consensus, and authenticated multi-node peer networking.

[![License: MIT](https://img.shields.io/badge/License-MIT-8B5CF6.svg)](LICENSE)
[![Status](https://img.shields.io/badge/status-testnet--foundation-4C6FFF.svg)]()
[![GitHub stars](https://img.shields.io/github/stars/SHalimoosavi/SAYANJALI-BLOCKCHAIN?style=social)](https://github.com/SHalimoosavi/SAYANJALI-BLOCKCHAIN/stargazers)
[![GitHub forks](https://img.shields.io/github/forks/SHalimoosavi/SAYANJALI-BLOCKCHAIN?style=social)](https://github.com/SHalimoosavi/SAYANJALI-BLOCKCHAIN/network/members)

[Website](https://shalimoosavi.github.io/syj-blockchain-web/) · [Blockchain Repository](https://github.com/SHalimoosavi/SAYANJALI-BLOCKCHAIN) · [Report an Issue](https://github.com/SHalimoosavi/SAYANJALI-BLOCKCHAIN/issues)

</div>

---

## Table of Contents

- [About](#about)
- [Current Status](#current-status)
- [Architecture](#architecture)
- [Core Technology](#core-technology)
- [The SYJ Native Asset](#the-syj-native-asset)
- [Ecosystem](#ecosystem)
- [Development Timeline](#development-timeline)
- [Roadmap](#roadmap)
- [Getting Started](#getting-started)
- [Contributing](#contributing)
- [Founder](#founder)
- [Disclaimer](#disclaimer)
- [License](#license)
- [Contact](#contact)

---

## About

**SAYANJALI BLOCKCHAIN** is an independently engineered blockchain network, progressing from its original MVP foundation into a **Testnet Foundation** stage. It is being built as the settlement and identity layer underneath the SAYANJALI NEXUS product ecosystem — a growing suite of AI tools, SaaS platforms, and automation products.

This is not a fork, a meme token, or a speculative side project. It is a from-scratch Layer-1 implementation: its own consensus, its own peer-to-peer networking, and its own native monetary protocol, developed and tested in the open.

> This project is under active, early-stage development. See [Disclaimer](#disclaimer) before relying on anything in this repository or its published materials.

## Current Status

**Stage: Testnet Foundation (Phase 3)**

| Metric | Result |
|---|---|
| Automated tests | 250 passed |
| Phase 2 tests | 244 passed |
| Focused Phase 3 / network / security suite | 29 passed |
| Multi-node testnet | 3 nodes verified (topology A ↔ B ↔ C) |
| Chain convergence | Verified |
| Work convergence | Verified |
| Balance convergence | Verified |
| Supply ceiling | Verified |

These are development and testnet verification metrics, not live-mainnet statistics. Three nodes verified in a lab testnet does not represent a public decentralized network.

### Phase 2 — completed

- Branch: `phase-2-completion`
- Verified commit: `d24e3b4612007be98680288e15e41d9565068acd` — *"feat: harden native SYJ monetary protocol"*
- 244 tests passed

Phase 2 hardened the native SYJ monetary protocol: deterministic integer-based monetary representation, maximum supply enforcement, supply-aware issuance, coinbase/reward validation, and monetary/state-transition validation — while preserving the existing P2P architecture rather than rebuilding it.

### Phase 3 — current (Testnet Foundation)

- **Node lifecycle** — explicit lifecycle states, clean startup/shutdown, FastAPI lifecycle integration, readiness/health state
- **Network maintenance** — background maintenance, controlled task lifecycle, task cleanup, peer maintenance
- **Peer health** — health tracking, failure counters, bounded exponential backoff, retry behavior
- **Bootstrap** — bootstrap peer registration, authenticated bootstrap communication
- **Peer discovery** — transitive peer-list discovery, multi-node topology formation
- **P2P protocol** — explicit message types, message-type validation, propagation validation
- **Observability** — propagation success/failure observability, expanded `/network/status`, improved `/health`

A real three-process testnet integration test (topology A ↔ B ↔ C) verified transitive peer discovery, authenticated links, transaction and block propagation, chain/work/balance convergence, SYJ supply verification, and existing network security controls — **250 tests passed**, focused Phase 3/network/security suite **29 tests passed**, real 3-node testnet **passed**.

## Architecture

```
Wallet → Transaction → Validation → Mempool → Mining/Consensus → Block
   → Propagation → Peer Network → Synchronization → Chain State
```

Node topology verified in the Phase 3 testnet:

```
Node A ↔ Node B ↔ Node C
```

## Core Technology

| Capability | Description |
|---|---|
| Native SYJ Protocol | Native asset accounting with deterministic monetary representation and enforced supply constraints |
| Proof-of-Work | Configurable PoW consensus with difficulty validation and accumulated-work chain selection |
| P2P Networking | Authenticated peer communication, propagation, discovery, and peer health management |
| Cryptographic Identity | Cryptographic node identity and authenticated communication |
| Chain Synchronization | Multi-node synchronization and work-based chain selection |
| Security | Replay protection, rate limiting, address validation, malformed-message rejection |
| Persistent Blockchain | Persistent chain and state storage |
| Developer API | FastAPI-based network and blockchain API |

Only capabilities actually implemented and tested are listed above. Future capabilities are labeled **Planned** in the [Roadmap](#roadmap).

## The SYJ Native Asset

SYJ is being designed as the native asset of the SAYANJALI BLOCKCHAIN, with a **protocol-level maximum supply of 720,000,000 SYJ**.

**Implemented protocol rules:**
- Deterministic, integer-based monetary representation
- Maximum supply enforcement at the protocol level
- Supply-aware issuance and coinbase/reward validation

**Future tokenomics (not yet published):** circulating supply, allocation, vesting, launch price, market capitalization, exchange listings, and investor/presale information. None of these have been determined or announced.

Intended (planned, not yet implemented) utility of SYJ includes AI subscriptions, SaaS licensing, marketplace payments, governance, premium API access, education platform access, developer services, enterprise automation, staking, and validator rewards.

## Ecosystem

SAYANJALI BLOCKCHAIN is being built as the settlement and identity layer underneath the SAYANJALI NEXUS product suite:

| Product | Description | Status |
|---|---|---|
| SYJ Utility Token | Economic and settlement layer for the network | Coming Soon |
| SYJ NexusIntel AI | AI intelligence platform for automation & insight | MVP |
| SYJ Mail Intelligence AI | AI-powered email triage, drafting & insight | MVP |
| SYJ Scholar AI | Offline-first AI study assistant | Open Source |
| SAYANJALI OSINT | Open intelligence tooling for research & security | Open Source |
| SYJ GST Recon | Automated GST reconciliation for businesses | MVP |
| FarmOwner | Digital infrastructure for farm ownership & operations | Coming Soon |
| Marketplace | On-chain marketplace across ecosystem products | Coming Soon |
| Wallet | Self-custody wallet for holding and using SYJ | Coming Soon |
| Exchange | Native venue for trading SYJ | Coming Soon |
| Launchpad | Launch platform for future ecosystem projects | Coming Soon |
| Identity | Portable on-chain identity across the ecosystem | Coming Soon |
| AI Cloud | Decentralized compute for ecosystem AI workloads | Coming Soon |

## Development Timeline

```
Foundation → Blockchain MVP → Phase 2 (Native SYJ Monetary Protocol)
   → Phase 3 (Testnet Foundation) → Multi-Node Testnet
   → Future: Validator Infrastructure → Future: Public Testnet → Future: Mainnet
```

## Roadmap

**Completed**
- Blockchain core, wallets, transactions
- Proof-of-Work, persistent storage, REST API, CLI
- P2P networking & authenticated peer communication
- Synchronization & security hardening
- Native SYJ monetary protocol & supply ceiling
- Three-node testnet verification

**Current — Testnet Foundation**
- Node lifecycle management
- Peer health & bootstrap
- Transitive peer discovery
- Propagation observability
- Synchronization reliability
- Ongoing multi-node testing

**Future — research & planned**
- Expanded public testnet
- Validator infrastructure
- Explorer & wallet applications
- Enhanced consensus research
- Smart-contract infrastructure
- Governance & ecosystem tooling
- Mainnet preparation

Roadmap items are targets, not commitments, and are subject to change.

## Getting Started

> The core network implementation is under active development. Setup instructions will be filled in as each component is released — this section will track the current state of the codebase.

```bash
# Clone the repository
git clone https://github.com/SHalimoosavi/SAYANJALI-BLOCKCHAIN.git
cd SAYANJALI-BLOCKCHAIN
```

## Contributing

Contributions are welcome as the project matures. Until a formal contribution guide is published:

1. Open an issue describing what you'd like to work on before submitting a large PR
2. Keep PRs focused and well-described
3. Follow the existing code style within each module

A full `CONTRIBUTING.md` will be added alongside the Developer SDK.

## Founder

**Syed Ali Hasan Moosavi**
Founder & Managing Director, SAYANJALI NEXUS PRIVATE LIMITED

Founder of SAYANJALI NEXUS, creator of the SAYANJALI BLOCKCHAIN vision, and lead architect responsible for product direction and core blockchain engineering.

> "SAYANJALI BLOCKCHAIN exists so that every product we ship shares one transparent, auditable foundation. It's early, it's open source, and we're building it in public — from MVP through Phase 2's monetary protocol to today's Testnet Foundation."

## Disclaimer

This repository and any associated documentation (including the website) are published for informational and development purposes only. Nothing here constitutes an offer or solicitation to buy or sell any security, token, or financial instrument, and nothing should be read as investment, legal, or tax advice.

SAYANJALI BLOCKCHAIN is under active development and is currently in its Testnet Foundation stage. No mainnet, public validator network, token generation event, or public sale has occurred as of this writing, and SYJ is not listed on any exchange. Roadmap items and described features are targets, not commitments, and are subject to change.

## License

Released under the [MIT License](LICENSE).

## Contact

- **Company:** SAYANJALI NEXUS PRIVATE LIMITED, Hyderabad, India
- **Email:** cto@sayanjalinexus.com
- **GitHub:** [@SHalimoosavi](https://github.com/SHalimoosavi)

---

<div align="center">
<sub>© 2026 SAYANJALI NEXUS PRIVATE LIMITED. All rights reserved.</sub>
</div>
