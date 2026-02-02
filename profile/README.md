# Drasil 🌳

**Bitcoin-Native Data Ownership Platform**

[![Website](https://img.shields.io/badge/Website-drasil.co-orange)](https://drasil.co)
[![Citrea](https://img.shields.io/badge/Built%20on-Citrea-purple)](https://citrea.xyz)
[![License](https://img.shields.io/badge/License-MIT-blue)](LICENSE)

> *Own your data. Control your privacy. Monetize your value.*

Drasil is a comprehensive data ownership platform that gives users complete control over their personal data while enabling trusted third parties to create and validate authoritative records. Built on [Citrea](https://citrea.xyz), Bitcoin's first ZK rollup.

---

## 🎯 Mission

Transform the data economy from institutional ownership to user sovereignty. Drasil combines the security of Bitcoin with zero-knowledge privacy to create the first truly user-owned data platform.

**Core Value Proposition**: "Your data, your control, your value" - Users own their data cryptographically, decide who accesses it, and profit when it's valuable to others.

---

## ✨ Key Features

### 🔐 Bitcoin-Native Data Ownership
- Cryptographic ownership proofs anchored to Bitcoin
- No institutional control or vendor lock-in
- Permanent, censorship-resistant records

### 🛡️ Zero-Knowledge Privacy
- Selective disclosure - prove attributes without revealing identity
- Anonymous discovery for professional networking
- Client-side encryption (AES-256-GCM + ECIES)

### 💰 Data Monetization
- Subscription-based data sharing
- Users earn from their valuable data
- 10-15% platform commission (vs 100% taken by Big Tech)

### 🔑 Three-Tier Authentication
| Tier | Best For | Key Feature |
|------|----------|-------------|
| **Anonymous Trial** | New users | Device-based identity, no registration |
| **Managed Account** | Mainstream users | Email/password, gasless transactions |
| **Self-Custody** | Web3 natives | Full key control, maximum sovereignty |

### 📱 Use Cases
- **Contact Management** - Multi-profile sharing with automatic sync
- **Medical Records** - Patient-owned health data with doctor validation
- **Financial Data** - Monetize spending patterns privately
- **Professional Credentials** - Cryptographically-verified career history

---

## 🚀 Quick Start

### Prerequisites
- [Nix](https://nixos.org/download.html) (for development environment)
- Node.js 18+ (for smart contract development)
- Rust 1.70+ (for CLI development)

### Clone & Setup
```bash
# Clone the repository
git clone https://github.com/drasil/drasil.git
cd drasil

# Enter development shell
nix develop

# Build CLI
cd drasil-cli && cargo build --release
```

### Run Demo
```bash
# Quick demo (no services required)
./examples/demo_workflow.sh

# With local blockchain (Hardhat + IPFS)
./examples/start_local_services.sh
./examples/demo_workflow.sh --network hardhat
./examples/stop_local_services.sh
```

---

## 📦 Project Structure

```
drasil/
├── drasil-cli/         # Rust CLI for contact management
├── drasil-contracts/   # Solidity smart contracts
├── recrypt-rs/         # Proxy Re-Encryption library
└── docs/               # Documentation (PRD, architecture, FAQ)
```

### Documentation
All documentation is maintained in the `docs/` directory:
- **[Product Requirements](https://github.com/drasil/drasil/blob/main/docs/drasil-prd.md)** - Complete PRD with user journeys
- **[Technical Architecture](https://github.com/drasil/drasil/blob/main/docs/drasil-arch.md)** - Architecture, 8 problem solutions, encryption, deployment
- **[FAQ](https://github.com/drasil/drasil/blob/main/docs/drasil-faq.md)** - Common questions and blockchain justifications

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────────────────┐
│  User Layer (Mobile/Web/CLI)                                │
└───────────────────────┬─────────────────────────────────────┘
                        ↓
┌─────────────────────────────────────────────────────────────┐
│  Client Layer                                               │
│  • Encryption (AES-256-GCM)                                 │
│  • PRE (Proxy Re-Encryption)                                │
│  • Bitcoin signatures                                       │
│  • IPFS integration                                         │
└───────────────────────┬─────────────────────────────────────┘
                        ↓
┌─────────────────────────────────────────────────────────────┐
│  Smart Contract Layer (Citrea)                              │
│  • DrasilRegistry (central coordinator)                     │
│  • Element/Profile/Sharing/Discovery modules                │
│  • Access control & ownership                               │
└───────────────────────┬─────────────────────────────────────┘
                        ↓
┌─────────────────────────────────────────────────────────────┐
│  Bitcoin Layer (Settlement)                                 │
│  • Proof-of-Work security                                   │
│  • Immutable ownership records                              │
└─────────────────────────────────────────────────────────────┘
```

### Key Technologies
- **Blockchain**: Citrea (Bitcoin ZK rollup)
- **Smart Contracts**: Solidity 0.8.28, modular architecture
- **Privacy**: Proxy Re-Encryption (PRE), Zero-Knowledge proofs
- **Storage**: IPFS for encrypted data
- **Cryptography**: AES-256-GCM, ECIES, ECDSA (secp256k1)

---

## 🧪 Testing

All components include comprehensive test coverage:

```bash
# Smart contract tests
cd drasil-contracts
npm test

# CLI tests
cd drasil-cli
cargo test

# BDD scenarios
npm run test:bdd  # 155+ passing scenarios
```

---

## 📊 Project Stats

| Metric | Value |
|--------|-------|
| **Test Coverage** | 93.3% (166/178 scenarios) |
| **Contract Size** | All modules <24KB ✅ |
| **Gas Efficiency** | ~70% savings with batch operations |
| **Network** | Citrea Testnet (Chain ID: 5115) |

---

## 🌐 Community

- **Website**: [https://drasil.co](https://drasil.co)

---

## 🙏 Acknowledgments

- [Citrea](https://citrea.xyz) - Bitcoin's first ZK rollup
- [recrypt-rs](https://github.com/IronCoreLabs/recrypt-rs) - Proxy Re-Encryption library
- [Hardhat](https://hardhat.org) - Ethereum development environment
- [Alloy](https://github.com/alloy-rs/alloy) - Rust Ethereum tooling

---

<div align="center">

**Built with ❤️ in Curaçao**

[Website](https://drasil.co) • [Documentation](https://github.com/drasil/drasil) • [Twitter](https://twitter.com/drasil)

</div>
