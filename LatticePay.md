# LatticePay

**Tools for Trade, Not Surveillance.**

LatticePay is an open-source, AGPL 3.0+ licensed payment infrastructure designed to give merchants, developers, and communities full control over how they transact. It is built as a **local-first, encrypted commerce protocol stack**, not a centralized payment processor or SaaS platform.

The goal is simple: enable commerce without surveillance, dependency, or data extraction.

---

## 🧭 What LatticePay Is

LatticePay is a **payment protocol and infrastructure layer** that enables:

- Merchant-owned payment systems
- Encrypted, local-first transaction processing
- Offline-capable commerce
- Federated or fully self-hosted deployments
- Modular integration with multiple payment rails

It is not a custodial system, and it does not act as a financial intermediary.

---

## 🚀 Feature List

### 🧱 Core Payment Features
- Accept payments via **tap, QR, invoice, and manual entry**
- Offline transaction creation, signing, and reconciliation
- Real-time and deferred settlement support
- Merchant-to-merchant payments
- Split payments and partial settlement handling
- Multi-device POS support per merchant

---

### 🔐 Privacy & Security Features
- End-to-end encrypted transactions by default
- Payload encryption performed on-device before transmission
- Forward-secret session key rotation
- No centralized transaction visibility layer
- No behavioral tracking or user profiling
- Optional pseudonymous or anonymous payment modes
- Cryptographic identity system (no mandatory accounts)

---

### 🌐 Network & Sync Features
- Peer-to-peer networking via libp2p
- Encrypted node-to-node communication channels
- Offline-first operation with automatic synchronization
- CRDT-based conflict resolution for distributed state
- Optional federated merchant clusters
- Resilient operation in low-connectivity environments

---

### 💾 Ledger & Accounting Features
- Append-only transaction ledger
- Deterministic reconciliation engine
- Local-first storage using PostgreSQL
- Hash-chained records for tamper-evidence (planned/optional)
- Exportable merchant-owned financial records
- Multi-device ledger synchronization

---

### 🖥️ POS & Merchant Tools
- Self-hosted POS system (no SaaS dependency)
- Touch-optimized POS interface for tablets and terminals
- Basic inventory tracking module (v1)
- Encrypted digital receipts
- Optional encrypted customer notes
- Multi-register support per merchant

---

### 🔌 Integration & Extensibility
- Modular payment rail plugin architecture
- Support for multiple settlement systems:
  - Card processors (via external adapters)
  - Bank transfer systems (ACH / SEPA equivalents)
  - Stablecoin / digital cash modules
  - Custom merchant-defined payment instruments
- REST + IPC APIs for integrations
- Webhook system for external business workflows
- Plugin SDK for third-party development

---

### 🧠 Developer Features
- Rust-based deterministic transaction engine
- Type-safe API boundaries
- RFC-driven protocol design
- Reproducible builds for auditability
- Local simulation mode for development
- Extensible module system for payment logic

---

### 🔧 Deployment Features
- Self-hosted single-merchant deployment
- Federated multi-merchant networks
- Air-gapped deployment support
- Docker and bare-metal installation support
- Runs on:
  - Linux servers
  - Desktop systems
  - Android POS devices
  - Embedded hardware (e.g., Raspberry Pi class systems)

---

### 📊 Financial Features
- Multi-currency support (via pluggable exchange layer)
- Split tender payments (multiple methods per transaction)
- Refund and reversal system with cryptographic linkage
- Optional recurring payments module
- Basic invoicing system (merchant-generated and encrypted)

---

## 🧩 System Guarantees (Design Principles)

- No centralized custody of funds or transaction data
- No forced identity system
- No surveillance-based analytics
- No data monetization layer
- No vendor lock-in
- Merchant retains full ownership of all transaction data
- Local-first operation is a core requirement, not a feature

---

## Specification Branding License (SBL)

### Standard
- Fully AGPL-3.0+ compliant system
- Copyleft enforced for network deployments
- Required attribution:
  - Roxanne Ardary
  - https://www.roxanneardary.com/

### Optional

- **Specification Branding License (SBL)**
  - Attribution-free commercial deployment
  - Pricing based on scale, usage, and deployment scope
  - [https://roxanneardary.com/latticepay/](https://roxanneardary.com/latticepay/)  

---

## 🧱 License & Notice Requirements

LatticePay is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- LatticePay specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
