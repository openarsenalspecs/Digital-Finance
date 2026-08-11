# Vantor

**Make intent executable.**

Vantor is a deterministic capital routing system where all financial actions are explicitly defined by the user and executed through a strict, rule-validated pipeline. The system uses AI only as an instruction parser and never as a decision-maker.

---

## Overview

Vantor transforms user-defined financial intent into structured execution instructions. It ensures that every allocation, schedule, and transaction is:

- Explicitly defined by the user  
- Validated by a deterministic rule engine  
- Executed only through approved deposit-only rails  
- Fully auditable and replayable  

No financial inference, optimization, or autonomous decision-making is permitted.

---

## Core Architecture

Vantor is built as a modular system with strict separation of responsibilities:

- **Intent Layer** → User-defined allocation rules  
- **AI Parsing Layer** → Natural language to structured instruction compiler  
- **Rule Engine** → Validation and constraint enforcement  
- **Scheduling Engine** → Explicit-time execution control  
- **Execution Engine** → Deposit-only financial routing  
- **Connector Layer** → External financial integrations  
- **Audit Layer** → Immutable system logging  
- **Simulation Layer** → Safe testing environment  
- **Security Layer** → Access control and system integrity  
- **API Layer** → System interface  
- **UI Layer** → Optional visualization and management interface  

---

## Feature List

### 1. Intent Layer (User Definition Module)

- Fixed-dollar allocation definitions
- Percentage-based allocation rules
- Multi-destination fund splitting
- Multiple allocation profiles
- Profile activation/deactivation controls
- Explicit rule-based financial intent definition

---

### 2. AI Parsing Layer (Instruction Compiler Module)

- Natural language → structured financial instruction conversion
- Strict schema normalization
- Clarification requests for incomplete input
- Deterministic JSON output generation
- No advisory, optimization, or recommendation behavior
- Rejection of ambiguous financial intent

---

### 3. Rule Engine (Validation & Constraint Module)

- Schema validation for all allocation rules
- Enforcement of user-defined caps and constraints
- Destination account allowlist enforcement
- No-withdrawal policy enforcement
- Conflict detection between rules
- Deterministic rule resolution ordering
- Mandatory execution-time validation

---

### 4. Scheduling Engine (User-Specified Execution Module)

- Explicit timestamp-based execution (ISO 8601)
- User-defined recurring schedules with full boundaries
- Timezone-aware scheduling per rule or profile
- No inferred timing (e.g., “next Friday” is invalid unless fully defined)
- Strict rejection of incomplete or relative dates
- Batch execution at exact user-defined times

---

### 5. Execution Engine (Financial Routing Module)

- Deposit-only transaction execution
- Multi-rail support (bank, brokerage, wallet)
- Idempotent transaction processing
- Retry handling for failed executions
- Transaction lifecycle tracking (pending, confirmed, failed)
- Strict prohibition of withdrawals or fund re-routing

---

### 6. Connector Layer (Integration Module)

- Banking API integration (deposit rails only)
- Brokerage funding account support
- Optional crypto wallet deposit integration
- Scoped API key permissions (write-only where possible)
- Pluggable connector architecture
- Isolated provider integrations

---

### 7. Audit & Logging Module

- Immutable logs of all user instructions
- Pre-execution AI parsing records
- Validation decision logs (pass/fail with reasoning)
- Full transaction history tracking
- Exportable audit trails (JSON/CSV)
- Execution replay capability

---

### 8. Scheduling Engine (Execution Control)

- Strict user-defined execution timing enforcement
- No system-generated scheduling defaults
- Timezone enforcement per execution rule
- Batch execution of matching timestamps only
- Rejection of undefined or partial timing rules

---

### 9. Simulation & Sandbox Module

- Fully isolated financial simulation environment
- Rule conflict testing before activation
- Scenario-based allocation modeling
- Historical execution replay
- Debugging and step-through rule evaluation
- No real financial impact

---

### 10. Security & Permission Module

- System-wide no-withdrawal enforcement
- Role-based access control (user/admin/system)
- Scoped API key generation and rotation
- Optional execution approval gating
- Rate limiting for API endpoints
- Tamper-resistant configuration storage

---

### 11. API Layer

- REST/GraphQL support for rule management
- AI parsing endpoint (stateless compiler mode)
- Execution status and tracking endpoints
- Connector configuration APIs
- Audit log access endpoints
- Simulation endpoints
- Webhook event support

---

### 12. UI Layer (Optional)

- Rule builder interface
- Visual capital flow mapping
- Explicit schedule configuration tools
- Transaction history dashboard
- Sandbox simulation interface
- Connector management panel
- Audit log explorer

---

## System Principles

- AI translates intent only
- Rules validate structure only
- Execution follows explicit instructions only
- No inference, no optimization, no autonomy
- All transactions are deterministic and auditable

---

## Project Name Tagline

**Vantor — Make intent executable.**

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
  - [https://roxanneardary.com/vantor/](https://roxanneardary.com/vantor/)

---

## License & Notice Requirements

Vantor is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- Vantor specificiations are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.  
  Any update that adds new contributors or modifies attribution should also update `notice.md`.  
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.  
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.  
