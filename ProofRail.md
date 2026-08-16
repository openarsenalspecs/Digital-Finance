# ProofRail
**Every transaction verified before it moves.**
- HTML Mirror:  [https://roxanneardary.com/proofrail-specification/](https://roxanneardary.com/proofrail-specification/)

---

## Specification

ProofRail is an open-source financial infrastructure protocol for fast, verifiable, programmable, privacy-aware, and resilient movement of value.

ProofRail is designed as a modular financial rail that combines real-time payment processing, cryptographic verification, intelligent risk controls, programmable transactions, settlement, identity, compliance, interoperability, and financial automation.

The system is designed to provide an open-source alternative to conventional payment infrastructure while remaining capable of interoperating with existing financial networks.

## Mission

ProofRail aims to establish a new standard for financial infrastructure based on:

- Proof before payment
- Verification before settlement
- Real-time processing
- Transaction certainty
- Programmable value
- Privacy-preserving identity
- Intelligent fraud prevention
- Transparent auditing
- Interoperability
- Resilience
- Open-source infrastructure

The central principle is:

**Proof-Powered Finance**

## Design Principles

### Proof First

ProofRail verifies the conditions necessary for a transaction before allowing value to move.

### Trust by Design

Trust is established through verifiable identity, transaction history, authorization, proofs, risk analysis, and network integrity rather than assumed from incomplete information.

### Real-Time by Default

Transactions should be processed continuously rather than depending on traditional batch windows whenever the selected settlement method supports real-time processing.

### Security by Default

Security controls are integrated into the protocol rather than added as an afterthought.

### Privacy by Design

ProofRail should minimize unnecessary disclosure of personal and financial information while supporting legitimate verification and compliance requirements.

### Programmable Value

Payments can contain conditions, rules, schedules, permissions, splits, escrow instructions, and other executable financial logic.

### Human Control

Automation and AI systems must operate within clearly defined permissions, limits, policies, and human override mechanisms.

### Interoperability

ProofRail should work with existing payment networks, financial institutions, digital assets, currencies, and future settlement systems.

### Auditability

Transactions and protocol decisions should produce verifiable records without requiring unnecessary disclosure of private information.

### Resilience

The system should continue operating safely through network interruptions, service failures, degraded connectivity, and other operational disruptions.

## Core Modules

### Transaction Core

The Transaction Core manages the complete lifecycle of a ProofRail transaction.

Capabilities include:

- Transaction creation
- Transaction validation
- Transaction authorization
- Transaction state management
- Transaction identifiers
- Idempotency
- Replay protection
- Duplicate detection
- Transaction expiration
- Transaction cancellation where permitted
- Transaction lifecycle events
- Atomic transaction processing
- Multi-party transactions
- Transaction batching where appropriate
- Transaction metadata management

The Transaction Core must maintain deterministic transaction behavior and prevent unauthorized changes to transaction state.

### Proof Core

The Proof Core establishes the verification foundation of ProofRail.

Capabilities include:

- Proof-of-funds
- Proof-of-identity
- Proof-of-authorization
- Proof-of-intent
- Proof-of-payment
- Proof-of-settlement
- Proof-of-delivery
- Cryptographic signatures
- Cryptographic receipts
- Proof validation
- Proof expiration
- Proof revocation
- Proof chaining
- Selective disclosure
- Zero-knowledge verification support

Proofs must be independently verifiable and tied to the transaction conditions they establish.

### Settlement Core

The Settlement Core manages the movement and finalization of value.

Capabilities include:

- Real-time settlement
- Settlement authorization
- Settlement finality
- Settlement state management
- Atomic settlement
- Settlement reconciliation
- Settlement confirmations
- Settlement failure handling
- Settlement recovery
- Internal ledger settlement
- External rail settlement
- Liquidity-aware settlement

The settlement system must distinguish clearly between authorized, pending, settled, failed, reversed, disputed, and finalized transactions.

### Ledger Core

The Ledger Core provides the authoritative transaction record.

Capabilities include:

- Account balances
- Transaction records
- Double-entry accounting
- Ledger integrity
- Balance conservation
- Cryptographic record verification
- Transaction history
- Ledger replication
- Reconciliation
- Audit records
- Historical state verification

Ledger operations must preserve financial integrity and prevent unauthorized balance creation, destruction, or modification.

### Account Core

The Account Core manages financial accounts and account relationships.

Capabilities include:

- Account creation
- Account verification
- Account status
- Account permissions
- Account limits
- Account relationships
- Multiple account types
- Subaccounts
- Escrow accounts
- Programmable accounts
- Account recovery
- Account suspension
- Account closure

Accounts must have clearly defined ownership, authorization, and operational states.

### Identity Core

The Identity Core provides privacy-aware identity and entity verification.

Capabilities include:

- Individual identity verification
- Business identity verification
- Institutional verification
- Credential management
- Credential expiration
- Credential revocation
- Selective disclosure
- Zero-knowledge credentials
- Portable identity credentials
- Verified payment identities
- Identity recovery
- Identity authorization

ProofRail should support different verification levels based on transaction requirements and applicable legal obligations.

### Authorization Core

The Authorization Core determines whether a transaction or financial operation is permitted.

Capabilities include:

- User authorization
- Account authorization
- Delegated authorization
- Multi-signature authorization
- Role-based permissions
- Policy-based permissions
- Transaction limits
- Spending controls
- Approval workflows
- Time-based authorization
- Emergency controls
- Human approval requirements

Authorization must be evaluated before financial operations are finalized.

### Intent Core

The Intent Core validates that a transaction represents an authorized and understood action.

Capabilities include:

- Payment intent creation
- Intent signatures
- Recipient confirmation
- Amount confirmation
- Context verification
- First-time recipient warnings
- High-risk transaction confirmation
- User confirmation workflows
- Intent expiration
- Intent cancellation

The Intent Core should help prevent accidental payments, manipulated payment instructions, and social engineering attacks.

### Risk Core

The Risk Core evaluates transaction risk before and during financial operations.

Capabilities include:

- Real-time risk scoring
- Transaction anomaly detection
- Behavioral analysis
- Account risk analysis
- Recipient risk analysis
- Device and session signals
- Network risk signals
- Fraud pattern detection
- Velocity analysis
- Geographic anomaly detection
- Risk thresholds
- Adaptive transaction controls

Risk decisions may result in:

- Allow
- Monitor
- Warn
- Require additional verification
- Require human approval
- Delay
- Reject
- Freeze

Risk systems must be explainable enough for appropriate review and must avoid treating automated scores as infallible.

### Reputation Core

The Reputation Core provides longitudinal trust signals.

Capabilities include:

- Transaction reliability
- Payment success history
- Dispute history
- Verification history
- Account age
- Network behavior
- Fraud history
- Reliability indicators
- Validator reputation
- Service reputation

Reputation information must be designed to reduce abuse, avoid unjustified exclusion, and prevent a single opaque score from becoming an uncontrolled financial gatekeeper.

### Routing Core

The Routing Core determines how transactions should reach their destination.

Capabilities include:

- Internal ProofRail routing
- ACH routing
- Real-time payment routing
- Wire routing
- Bank transfer routing
- Digital asset routing
- Cross-border routing
- Local payout routing
- Cost optimization
- Speed optimization
- Risk optimization
- Settlement optimization
- User preference optimization
- Automatic fallback routing

Routing decisions should consider availability, cost, speed, settlement characteristics, risk, currency, jurisdiction, and user-defined preferences.

### Liquidity Core

The Liquidity Core manages available settlement liquidity.

Capabilities include:

- Liquidity monitoring
- Liquidity forecasting
- Liquidity allocation
- Settlement liquidity management
- Internal netting
- Reserve monitoring
- Liquidity thresholds
- Liquidity alerts
- Cross-rail liquidity coordination
- Predictive liquidity management

Liquidity operations must maintain transparent accounting and clearly distinguish available liquidity from committed or restricted funds.

### Currency Core

The Currency Core provides support for multiple currencies and forms of value.

Capabilities include:

- Currency representation
- Currency conversion
- Exchange rate management
- FX quote generation
- FX execution
- Multi-currency accounts
- Currency settlement
- Exchange rate validation
- Rate expiration
- Currency precision controls

The architecture should allow additional currencies and settlement instruments without redesigning the transaction protocol.

### Programmability Core

The Programmability Core allows transactions and accounts to operate according to defined rules.

Capabilities include:

- Conditional payments
- Scheduled payments
- Recurring payments
- Milestone payments
- Payment splitting
- Payment limits
- Conditional release
- Time locks
- Automated refunds
- Automated allocations
- Rule-based accounts
- Event-triggered transactions

Programmable financial logic must operate within explicit permissions and cannot bypass core security, authorization, or compliance controls.

### Escrow Core

The Escrow Core provides native conditional custody and release mechanisms.

Capabilities include:

- Escrow creation
- Escrow funding
- Conditional release
- Partial release
- Milestone release
- Refund rules
- Time-based release
- Multi-party approval
- Dispute holds
- Escrow expiration
- Escrow reconciliation

Escrow rules must be established before funds become subject to the associated conditions.

### Atomic Transaction Core

The Atomic Transaction Core supports coordinated multi-party value movement.

Capabilities include:

- All-or-nothing settlement
- Multi-party transfers
- Automatic payment splitting
- Fee allocation
- Tax allocation
- Commission allocation
- Escrow allocation
- Conditional multi-party settlement

Atomic operations must ensure that defined transaction groups cannot settle partially unless partial settlement has been explicitly authorized.

### Dispute Core

The Dispute Core manages payment disputes and transaction challenges.

Capabilities include:

- Dispute initiation
- Dispute windows
- Evidence submission
- Evidence verification
- Transaction holds
- Escrow protection
- Resolution workflows
- Arbitration support
- Human review
- Automated evidence analysis
- Resolution records
- Appeal processes

Dispute mechanisms must preserve transaction evidence and clearly distinguish between disputes, reversals, refunds, and fraud investigations.

### Compliance Core

The Compliance Core provides configurable controls for applicable legal and regulatory requirements.

Capabilities include:

- Transaction monitoring
- Identity requirements
- Sanctions screening integrations
- Jurisdiction rules
- Transaction thresholds
- Record retention
- Reporting workflows
- Compliance alerts
- Policy enforcement
- Regulatory audit support

Compliance functionality should be configurable by jurisdiction and deployment rather than hard-coded into every transaction path.

### Privacy Core

The Privacy Core protects sensitive financial and identity information.

Capabilities include:

- Data minimization
- Encryption
- Selective disclosure
- Privacy-preserving credentials
- Zero-knowledge verification
- Access controls
- Data retention controls
- Consent management
- Private transaction metadata
- Audit access controls

Privacy protections must coexist with legally required verification, reporting, and audit capabilities.

### Security Core

The Security Core provides system-wide security controls.

Capabilities include:

- Cryptographic key management
- Authentication
- Authorization
- Secure sessions
- Rate limiting
- Replay protection
- Tamper detection
- Intrusion detection
- Security event monitoring
- Secret management
- Secure recovery
- Emergency controls
- Security audit logging

Security-sensitive operations must use explicit authorization and verifiable state transitions.

### Audit Core

The Audit Core creates verifiable records of financial and protocol activity.

Capabilities include:

- Cryptographic receipts
- Transaction audit trails
- State transition records
- Administrative audit logs
- Security event records
- Compliance records
- Reconciliation records
- Verifiable transaction histories
- Exportable audit data

Audit records should provide sufficient evidence to verify system behavior without unnecessarily exposing private information.

### Reconciliation Core

The Reconciliation Core ensures that internal records agree with external settlement sources.

Capabilities include:

- Account reconciliation
- Settlement reconciliation
- External rail reconciliation
- Balance verification
- Exception detection
- Missing transaction detection
- Duplicate transaction detection
- Settlement mismatch detection
- Automated reconciliation
- Manual reconciliation workflows

### Resilience Core

The Resilience Core provides safe operation during infrastructure failures.

Capabilities include:

- Transaction queues
- Retry policies
- Idempotent recovery
- Network interruption handling
- Service failover
- Data replication
- Recovery procedures
- Degraded operation
- Low-bandwidth operation
- Offline transaction preparation
- Synchronization after reconnection

Offline functionality must not allow unauthorized creation or double spending of value.

### Observability Core

The Observability Core provides operational visibility.

Capabilities include:

- Transaction metrics
- Settlement metrics
- Latency measurements
- Validator health
- Network health
- Error monitoring
- Security events
- Risk events
- Liquidity metrics
- Service health
- Audit events
- Operational dashboards

Observability data should be separated from sensitive transaction data whenever possible.

### AI Intelligence Core

The AI Intelligence Core provides optional intelligent decision support within controlled boundaries.

Capabilities include:

- Fraud detection
- Anomaly detection
- Risk analysis
- Payment routing optimization
- Cash flow forecasting
- Financial pattern analysis
- Transaction classification
- Evidence analysis
- Compliance assistance
- User assistance
- Predictive liquidity analysis

AI systems must not independently override core authorization, settlement, security, or user-control requirements.

### Payment Agent Core

The Payment Agent Core enables authorized automated financial agents.

Capabilities include:

- User-defined payment rules
- Spending limits
- Authorized recipients
- Scheduled actions
- Approval thresholds
- Agent permissions
- Agent identity
- Agent activity logs
- Human override
- Emergency suspension

Agents must operate within explicit authorization boundaries and maintain complete records of actions taken.

### Semantic Payment Core

The Semantic Payment Core translates human-readable financial intent into structured transaction instructions.

Capabilities include:

- Natural-language payment requests
- Intent extraction
- Recipient identification
- Amount extraction
- Condition extraction
- Schedule extraction
- Payment confirmation
- Ambiguity detection
- Risk-aware clarification

Semantic interpretation must never silently execute an ambiguous or materially different transaction.

### Invoice Core

The Invoice Core connects financial obligations directly to payment execution.

Capabilities include:

- Invoice creation
- Invoice verification
- Recipient verification
- Payment requests
- Payment status
- Automated reconciliation
- Partial payments
- Installments
- Conditional invoices
- Recurring invoices
- Payment receipts

### Tax Core

The Tax Core provides transaction classification and tax-related financial tooling.

Capabilities include:

- Transaction categorization
- Tax metadata
- Tax allocation
- Reporting data
- Tax event identification
- Exportable records
- Jurisdiction-aware rules
- Accounting integration

The Tax Core should provide financial information and automation without assuming that automated classifications constitute legal or tax advice.

### Financial Automation Core

The Financial Automation Core manages recurring and rule-based financial operations.

Capabilities include:

- Automated bill payments
- Savings allocations
- Scheduled transfers
- Balance thresholds
- Budget rules
- Recurring obligations
- Cash flow rules
- Automatic reconciliation
- Financial alerts

Automation must remain subject to user-defined limits and authorization.

### Payment Identity Core

The Payment Identity Core provides human-readable payment addresses.

Supported identifiers may include:

- `name@proofrail`
- `business@proofrail`
- Domain-based payment identities
- Verified organization identities
- Application-specific payment identities

Payment identities must resolve through verifiable records and protect against impersonation and unauthorized changes.

### Interoperability Core

The Interoperability Core allows ProofRail to communicate with external financial systems.

Capabilities include:

- Banking integrations
- Payment network integrations
- ACH integrations
- Real-time payment integrations
- Wire integrations
- Digital asset integrations
- Accounting integrations
- Identity provider integrations
- Compliance provider integrations
- External settlement systems
- API interoperability
- Standardized transaction messaging

## Optional Plugin Modules

ProofRail supports optional plugins that extend functionality without unnecessarily increasing the complexity of the core protocol.

Plugins must use documented interfaces and must not bypass core security, authorization, settlement integrity, or audit requirements.

### Risk Intelligence Plugin

Provides advanced external risk models, specialized fraud models, behavioral analytics, and additional transaction intelligence.

### AI Routing Plugin

Provides advanced machine-learning models for selecting settlement routes based on speed, cost, liquidity, reliability, risk, and user preferences.

### Fraud Intelligence Plugin

Provides external fraud intelligence, network signals, scam pattern detection, account reputation signals, and specialized fraud analysis.

### Identity Provider Plugin

Connects ProofRail to external identity verification providers and credential systems.

### Compliance Provider Plugin

Connects ProofRail to external compliance, sanctions, screening, monitoring, and reporting services.

### Banking Connector Plugin

Connects ProofRail to participating financial institutions and banking APIs.

### ACH Connector Plugin

Provides compatibility with ACH infrastructure during transitional and multi-rail deployments.

### Real-Time Payment Connector Plugin

Provides connectivity to supported real-time payment networks.

### Wire Connector Plugin

Provides compatibility with traditional wire systems for high-value or specialized settlement.

### Digital Asset Connector Plugin

Provides controlled interoperability with supported digital asset networks and tokenized settlement systems.

### FX Provider Plugin

Connects ProofRail to external foreign exchange providers and liquidity sources.

### Accounting Plugin

Connects transaction records with accounting and bookkeeping systems.

### Payroll Plugin

Provides payroll workflows, scheduled compensation, employee payment processing, and payroll reconciliation.

### Marketplace Plugin

Provides marketplace payment splitting, escrow, seller settlement, refunds, commissions, and platform fees.

### Subscription Plugin

Provides recurring billing, subscription payments, payment retries, account lifecycle rules, and automated reconciliation.

### Real Estate Plugin

Provides transaction workflows for deposits, escrow, commissions, taxes, settlement distributions, and other real estate payment requirements.

### Legal Agreement Plugin

Connects programmable payment conditions with structured agreements, obligations, signatures, and jurisdiction-aware workflows.

### Arbitration Plugin

Provides specialized dispute resolution and arbitration workflows.

### Insurance Plugin

Provides optional transaction protection and fraud coverage integrations.

### Reputation Provider Plugin

Connects ProofRail with external reputation and verification services while preserving user privacy and authorization requirements.

### Notification Plugin

Provides email, SMS, push, webhook, and other transaction notification capabilities.

### Analytics Plugin

Provides advanced financial analytics, reporting, visualization, forecasting, and operational intelligence.

### Tax Reporting Plugin

Provides jurisdiction-specific tax reporting and export capabilities.

### AI Financial Assistant Plugin

Provides user-facing financial assistance, analysis, recommendations, and controlled automation.

### Offline Payment Plugin

Provides additional low-bandwidth and disconnected operation capabilities where the deployment can safely support them.

### Developer SDK Plugin

Provides language-specific SDKs, libraries, testing tools, simulators, and integration helpers.

## Smart Routing

ProofRail should select an appropriate settlement path based on transaction requirements.

Routing decisions may evaluate:

- Settlement speed
- Transaction cost
- Transaction value
- Risk
- Finality
- Liquidity
- Currency
- Geographic location
- Jurisdiction
- Network availability
- User preferences
- Recipient requirements
- Compliance requirements

ProofRail should support automatic fallback when the preferred settlement path is unavailable, provided the fallback remains authorized and meets transaction requirements.

## Trust Model

ProofRail establishes trust through multiple independent signals rather than relying on a single trust score.

Trust signals may include:

- Verified identity
- Verified account ownership
- Proof-of-funds
- Proof-of-intent
- Transaction history
- Payment reliability
- Dispute history
- Risk analysis
- Network reputation
- Validator integrity
- Credential status

Trust decisions should remain explainable, reviewable, and subject to appropriate controls.

## Transaction Lifecycle

A typical ProofRail transaction should progress through defined states:

- Created
- Identified
- Verified
- Authorized
- Risk Evaluated
- Approved
- Routed
- Funded
- Settling
- Settled
- Confirmed
- Reconciled
- Completed

Alternative states may include:

- Rejected
- Expired
- Cancelled
- Failed
- Reversed
- Disputed
- Frozen
- Refunded

Every state transition should be authorized, recorded, and auditable.

## Programmable Payment Model

ProofRail supports financial conditions such as:

- Pay when a milestone is verified
- Release escrow after approval
- Pay a specified recipient on a schedule
- Split funds among multiple recipients
- Refund funds after an expiration period
- Require multiple approvals
- Require proof of delivery
- Require proof of service completion
- Enforce transaction limits
- Trigger payments from verified events

Programmable conditions must remain deterministic where financial finality depends upon them.

## Multi-Party Settlement

ProofRail supports transactions involving multiple participants.

A transaction may distribute funds among:

- Sellers
- Buyers
- Contractors
- Employees
- Agents
- Governments
- Tax authorities
- Marketplaces
- Service providers
- Escrow participants
- Other authorized recipients

Atomic settlement should ensure that defined distributions occur according to the transaction's approved allocation rules.

## Privacy Model

ProofRail should provide users and institutions with control over financial information.

Privacy mechanisms include:

- Data minimization
- Encryption
- Selective disclosure
- Zero-knowledge proofs
- Permissioned access
- Credential-based verification
- Transaction metadata protection
- Audit access controls

Privacy must not be implemented in a way that prevents legitimate security, compliance, or legal obligations from being fulfilled.

## Security Model

ProofRail security should protect:

- Funds
- Accounts
- Identity
- Credentials
- Transactions
- Proofs
- Settlement
- Validators
- Network communications
- Audit records
- Private data

Security controls should include:

- Strong cryptography
- Secure key management
- Authentication
- Authorization
- Replay protection
- Rate limiting
- Fraud monitoring
- Tamper detection
- Secure recovery
- Operational monitoring
- Incident response

## Governance

ProofRail uses transparent, maintainer-led governance.

Governance should prioritize:

- Financial integrity
- Security
- Reliability
- Interoperability
- Privacy
- Open-source participation
- Technical transparency
- Long-term sustainability

Protocol changes should be documented, reviewed, tested, and communicated before production adoption.

## Compatibility

ProofRail should support interoperability with existing and emerging financial systems.

The protocol should be capable of acting as:

- A native settlement network
- A payment orchestration layer
- A multi-rail routing system
- A programmable payment layer
- A verification layer
- A financial intelligence layer
- An interoperability layer

This allows adoption without requiring immediate replacement of existing financial infrastructure.

## Performance Requirements

ProofRail should target:

- Real-time transaction processing
- Low settlement latency
- High transaction throughput
- Deterministic transaction processing
- Efficient proof verification
- Horizontal scalability
- Fault tolerance
- Continuous availability
- Efficient reconciliation

Performance improvements must not compromise financial correctness, security, privacy, or auditability.

## Reliability Requirements

The protocol should maintain:

- Balance integrity
- Transaction uniqueness
- Settlement consistency
- Proof integrity
- Authorization integrity
- Ledger consistency
- Idempotent recovery
- Reconciliation accuracy
- Auditability

Failures must produce controlled and recoverable states rather than ambiguous financial outcomes.

## Developer Experience

ProofRail should provide:

- Documented APIs
- Protocol specifications
- SDKs
- Client libraries
- Testing tools
- Transaction simulators
- Local development environments
- Integration examples
- Plugin interfaces
- Webhooks
- Event streams
- Versioned protocol interfaces

Developers should be able to integrate ProofRail without needing to understand every internal subsystem.

## Testing and Verification

ProofRail should maintain comprehensive testing across:

- Unit tests
- Integration tests
- End-to-end tests
- Security tests
- Cryptographic tests
- Invariance tests
- Failure recovery tests
- Load tests
- Performance tests
- Interoperability tests
- Reconciliation tests
- Privacy tests
- Compliance tests

Financially significant protocol changes require additional verification before release.

## Observability

ProofRail deployments should provide appropriate operational visibility through:

- Metrics
- Logs
- Events
- Alerts
- Health checks
- Transaction tracing
- Settlement monitoring
- Validator monitoring
- Risk monitoring
- Security monitoring
- Liquidity monitoring

Sensitive financial and identity information must not be unnecessarily exposed through observability systems.

## Disaster Recovery

ProofRail should support controlled recovery from:

- Node failure
- Database failure
- Network interruption
- Service failure
- Key compromise
- Infrastructure loss
- External settlement failure
- Data corruption

Recovery mechanisms must preserve financial state and prevent duplicate settlement.

## Open-Source Model

ProofRail is developed as open-source financial infrastructure.

The project should encourage:

- Public technical specifications
- Community contributions
- Transparent issue tracking
- Auditable changes
- Interoperable implementations
- Independent security review
- Extensible modules
- Open developer tooling

The protocol should avoid unnecessary vendor lock-in.

## Vision

ProofRail is intended to establish a new generation of financial infrastructure in which:

- Money moves quickly
- Transactions are verified before execution
- Identity can be proven without unnecessary disclosure
- Funds can be proven before settlement
- Intent can be verified before authorization
- Risk can be evaluated before value moves
- Payments can be programmed
- Settlement can be atomic
- Transactions can be audited
- Financial systems can interoperate
- Users retain meaningful control
- Infrastructure remains open-source

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
  - [https://roxanneardary.com/proofrail/](https://roxanneardary.com/proofrail/)

---

# License & Notice Requirements

ProofRail is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.
- ProofRail specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.  
