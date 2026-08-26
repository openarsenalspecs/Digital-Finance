# Altius Capital OS Specification
**Make capital decisions computable.**
- HTML Mirror: [https://roxanneardary.com/altius-capital-os-specification/](https://roxanneardary.com/altius-capital-os-specification/)  

---

## Specification Overview

Altius Capital OS is a modular, jurisdiction-aware financial computation system designed to transform capital custody, taxation, regulatory requirements, liquidity requirements, risk parameters, and user-defined financial objectives into structured, deterministic, auditable decision models.

The system is designed around the principle that capital decisions should be computable. Financial rules are represented as structured, versioned data rather than embedded exclusively within prompts or AI models. The system combines deterministic financial computation with regulatory intelligence, constraint enforcement, simulation, optimization, scenario management, and an AI explanation layer.

Altius Capital OS is designed to support self-hosted, vendor-independent deployment and extensibility through optional plugin modules. The core system provides the foundational computation and regulatory architecture, while optional plugins can introduce additional jurisdictions, financial instruments, regulatory sources, optimization methods, data providers, and AI providers.

---

## Core Design Principles

- Rules are data, not prompts
- Capital decisions are computational outputs
- Regulatory sources are authoritative inputs
- Jurisdictions are modular
- Financial instruments are modular
- Constraints are executable
- Calculations are deterministic where possible
- Regulatory rules are versioned
- Effective dates are preserved
- Historical rules remain available for reproducibility
- Every material output is auditable
- Every strategy can be simulated
- Every scenario can be versioned
- AI is an explanation and interaction layer, not the source of regulatory authority
- User-defined constraints take precedence over optimization preferences
- System rules cannot be silently overridden by the AI layer
- The system is designed for privacy-conscious and self-hosted operation
- Core functionality remains independent of any specific financial institution, AI provider, or data vendor

---

## Core Modules

### Capital Computation Module

The Capital Computation Module provides the foundational computational layer for modeling capital.

Features include:

- Capital input processing
- Principal modeling
- Capital allocation
- Capital preservation analysis
- Cash flow modeling
- Income generation modeling
- Compound growth calculations
- Multi-period calculations
- Capital deployment modeling
- Reserve modeling
- Reinvestment modeling
- Distribution modeling
- Withdrawal modeling
- Deterministic calculation processing
- Calculation precision controls
- Calculation metadata
- Calculation versioning

The module must accept structured financial inputs and produce structured computational outputs that can be consumed by the other core modules.

### Custody Architecture Module

The Custody Architecture Module models how capital can be distributed across different custody structures.

Features include:

- Bank custody modeling
- FDIC-insured deposit modeling
- Multi-bank distribution
- Deposit concentration analysis
- Ownership category modeling
- Individual ownership structures
- Joint ownership structures
- Trust ownership structures
- Entity ownership structures
- Deposit exposure calculations
- Insured exposure calculations
- Uninsured exposure calculations
- Custodian concentration analysis
- Custody diversification
- Bank failure scenarios
- Custody-layer comparison
- Custody strategy generation

The module must distinguish between insurance coverage, government-backed securities, brokerage protections, and uninsured exposures.

### FDIC Insurance Module

The FDIC Insurance Module models applicable deposit insurance rules.

Features include:

- Insurance limit modeling
- Per-depositor analysis
- Per-bank analysis
- Ownership category analysis
- Coverage calculation
- Coverage gap identification
- Multi-bank coverage modeling
- Deposit category analysis
- Coverage scenario simulation
- Historical insurance rule versions
- Effective-date-aware insurance rules
- Source provenance
- Insurance constraint integration

The module must not represent FDIC insurance as applicable to financial products that do not qualify for FDIC deposit insurance.

### Treasury Instrument Module

The Treasury Instrument Module models U.S. Treasury securities and related capital structures.

Features include:

- Treasury bill modeling
- Treasury note modeling
- Treasury bond modeling
- Maturity modeling
- Coupon modeling
- Yield modeling
- Duration analysis
- Reinvestment modeling
- Treasury ladder construction
- Treasury income modeling
- Federal tax treatment integration
- State tax treatment integration
- Liquidity modeling
- Maturity matching
- Treasury allocation constraints
- Historical Treasury rule and rate data support

### Brokerage Custody Module

The Brokerage Custody Module models brokerage-based custody structures.

Features include:

- Brokerage account modeling
- Brokered CD modeling
- Multi-bank brokered CD allocation
- Brokerage sweep modeling
- Deposit sweep analysis
- Pass-through insurance modeling
- Brokerage concentration analysis
- Custodian diversification
- Maturity laddering
- Brokerage protection classification
- Custody risk analysis
- Brokerage scenario modeling

The module must distinguish brokerage protections from FDIC deposit insurance and must not treat the two systems as interchangeable.

### Financial Instrument Module

The Financial Instrument Module provides a standardized interface for supported financial instruments.

Supported instrument categories may include:

- Savings accounts
- Money market deposit accounts
- Certificates of deposit
- Brokered certificates of deposit
- Treasury bills
- Treasury notes
- Treasury bonds
- Government securities
- Other supported cash and fixed-income instruments

Each instrument definition may contain:

- Instrument type
- Issuer
- Custodian
- Yield
- Maturity
- Liquidity characteristics
- Tax characteristics
- Insurance characteristics
- Custody characteristics
- Risk characteristics
- Regulatory classifications
- Source data
- Effective dates
- Historical versions

### Federal Tax Module

The Federal Tax Module provides U.S. federal tax computation and rule integration.

Features include:

- IRS rule ingestion
- Federal income tax modeling
- Interest income treatment
- Dividend income treatment
- Capital gains treatment
- Income classification
- Tax bracket modeling
- Deduction modeling
- Credit modeling
- Reporting threshold modeling
- Tax-year modeling
- Effective-date tracking
- Historical tax-rule reconstruction
- Federal tax scenario analysis
- Tax impact calculations
- Tax drag calculations
- Tax-equivalent yield calculations

The module must maintain versioned federal tax rules and preserve source provenance for rules used in calculations.

### State Tax Code Module

The State Tax Code Module provides modular state-level tax modeling.

Features include:

- State tax jurisdiction registry
- State income tax modeling
- State tax brackets
- State deductions
- State credits
- State exemptions
- State income classifications
- Interest income treatment
- Treasury income treatment
- Capital gains treatment
- Federal conformity analysis
- Partial conformity analysis
- Nonconformity analysis
- State filing thresholds
- State tax-year versioning
- State effective-date tracking
- Historical state tax rules
- State tax scenario modeling
- State tax drag calculations

The architecture must support all U.S. states and applicable U.S. jurisdictions without requiring changes to the core computation engine.

### Jurisdiction Module

The Jurisdiction Module coordinates federal and state rules.

Features include:

- Jurisdiction identification
- Federal jurisdiction profiles
- State jurisdiction profiles
- Multi-state modeling
- Residency modeling
- Part-year residency modeling
- Tax domicile modeling
- Jurisdiction transitions
- Jurisdiction comparison
- Jurisdiction-specific rule resolution
- Historical jurisdiction states
- Effective-date-aware jurisdiction processing

The module must allow additional jurisdictions to be added without modifying core financial computation logic.

### Regulatory Intelligence Module

The Regulatory Intelligence Module manages regulatory information and converts authoritative source material into structured rules.

Features include:

- Regulatory source registration
- Official-source prioritization
- Regulatory document ingestion
- Regulatory document parsing
- Rule extraction
- Rule normalization
- Rule classification
- Rule validation
- Rule versioning
- Change detection
- Regulatory diff analysis
- Effective-date management
- Publication-date tracking
- Future-rule tracking
- Superseded-rule tracking
- Historical rule retention
- Regulatory source verification
- Source provenance
- Regulatory change alerts

Supported U.S. regulatory sources may include:

- Internal Revenue Service
- U.S. Treasury
- Federal Deposit Insurance Corporation
- Federal Register
- State departments of revenue
- State tax authorities
- State legislative sources

The system must prioritize authoritative sources and must preserve the source used to establish or update each rule.

### Rule Graph Module

The Rule Graph Module connects financial rules into a structured dependency graph.

Features include:

- Federal rule nodes
- State rule nodes
- Tax rule nodes
- FDIC rule nodes
- Treasury rule nodes
- Brokerage rule nodes
- Instrument rule nodes
- Ownership rule nodes
- Jurisdiction relationships
- Rule dependencies
- Rule precedence
- Rule conflicts
- Rule resolution
- Rule lineage
- Rule provenance
- Rule snapshots
- Effective-date resolution
- Historical rule resolution

The Rule Graph must function as the authoritative computational rule layer. The AI layer must not independently override or replace resolved rules.

### Rule Resolution Module

The Rule Resolution Module determines which rules apply to a specific calculation.

Features include:

- Jurisdiction-aware resolution
- Tax-year resolution
- Effective-date resolution
- Instrument-specific resolution
- Ownership-specific resolution
- Regulatory authority ranking
- Rule precedence
- Conflict identification
- Conflict resolution
- Historical rule selection
- Future rule selection
- Rule dependency resolution
- Resolution logging

Every resolved rule set must be identifiable by a version or snapshot reference.

### Effective Date Module

The Effective Date Module manages time-dependent financial and regulatory rules.

Features include:

- Publication dates
- Effective dates
- Expiration dates
- Tax-year applicability
- Future effective rules
- Historical rules
- Transition rules
- Overlapping rules
- Rule activation
- Rule deactivation
- Date-specific calculations
- Historical scenario reconstruction

### Yield Computation Module

The Yield Computation Module calculates and compares financial returns.

Features include:

- Gross yield
- Net yield
- Federal tax drag
- State tax drag
- Combined tax drag
- Inflation adjustment
- Real yield
- Effective annual yield
- Compound yield
- Yield-to-maturity modeling
- Reinvestment assumptions
- Tax-equivalent yield
- Instrument yield comparison
- Strategy yield comparison

### Liquidity Module

The Liquidity Module models accessibility of capital over time.

Features include:

- Immediate liquidity
- Short-term liquidity
- Medium-term liquidity
- Long-term allocation
- Custom liquidity periods
- 0 to 3 month modeling
- 3 to 12 month modeling
- 1 to 5 year modeling
- Withdrawal requirements
- Liquidity reserves
- Maturity matching
- Cash flow matching
- Liquidity stress testing
- Liquidity scoring
- Liquidity constraints

### Risk Module

The Risk Module models risks associated with proposed capital structures.

Features include:

- Custody risk
- Concentration risk
- Liquidity risk
- Interest-rate risk
- Duration risk
- Reinvestment risk
- Tax-policy risk
- Regulatory-change risk
- Counterparty exposure
- Uninsured exposure
- Scenario-specific risk
- Risk scoring
- Risk comparison
- Risk constraint integration

The system must clearly distinguish modeled risk from guaranteed outcomes.

### Constraint Builder Module

The Constraint Builder Module converts user-defined financial requirements into executable rules.

Features include:

- Constraint creation
- Constraint editing
- Constraint validation
- Hard constraints
- Soft constraints
- Weighted preferences
- Dollar-based constraints
- Percentage-based constraints
- Time-based constraints
- Jurisdiction-specific constraints
- Instrument-specific constraints
- Ownership-specific constraints
- Conditional constraints
- Compound constraints
- Constraint priorities
- Constraint conflicts
- Constraint violation reporting
- Constraint satisfaction analysis

Examples of supported constraint concepts include:

- Maximum exposure to a single bank
- Minimum insured capital
- Minimum Treasury allocation
- Maximum duration
- Minimum liquidity reserve
- Maximum tax exposure
- Maximum concentration
- Minimum diversification
- Custom user-defined requirements

### Constraint DSL Module

The Constraint DSL Module provides a machine-readable and human-readable representation of financial constraints.

Features include:

- Financial comparison operators
- Percentage conditions
- Dollar conditions
- Time conditions
- Instrument conditions
- Jurisdiction conditions
- Ownership conditions
- Compound conditions
- Conditional logic
- Constraint weighting
- Constraint priority
- Constraint validation
- DSL parsing
- DSL compilation
- DSL execution
- DSL error reporting

The DSL must translate user requirements into validated constraints without allowing natural-language ambiguity to silently alter a financial rule.

### Optimization Module

The Optimization Module searches for capital structures that satisfy defined objectives and constraints.

Features include:

- Yield optimization
- After-tax yield optimization
- Risk minimization
- Liquidity optimization
- Custody diversification
- Constraint-aware allocation
- Multi-objective optimization
- User-defined optimization priorities
- Strategy ranking
- Alternative strategy generation
- Sensitivity analysis
- Optimization feasibility testing
- Constraint-aware portfolio construction

The optimization engine must reject or clearly identify strategies that violate hard constraints.

### Strategy Module

The Strategy Module provides reusable capital allocation patterns.

Features include:

- Safety-first strategies
- Liquidity-first strategies
- Yield-focused strategies
- Tax-aware strategies
- Treasury-heavy strategies
- FDIC custody ladders
- CD ladders
- Hybrid custody structures
- Custom strategies
- Strategy templates
- Strategy scoring
- Strategy comparison
- Strategy versioning
- Strategy simulation

### Simulation Module

The Simulation Module evaluates capital structures under changing conditions.

Features include:

- Bank failure scenarios
- Multiple bank failure scenarios
- Interest-rate increases
- Interest-rate decreases
- Inflation changes
- Liquidity shocks
- Unexpected withdrawals
- Tax-law changes
- State relocation
- Residency changes
- Yield changes
- Reinvestment changes
- Custody changes
- Regulatory changes
- Multi-variable stress scenarios
- Multi-year simulations
- Historical simulations
- Forward-looking simulations based on user-defined assumptions

### Scenario Memory Module

The Scenario Memory Module provides persistent management of capital strategies and simulations.

Features include:

- Scenario creation
- Scenario storage
- Scenario retrieval
- Scenario cloning
- Scenario renaming
- Scenario archiving
- Scenario versioning
- Scenario comparison
- Scenario replay
- Scenario recalculation
- Historical-rule recalculation
- Current-rule recalculation
- Change tracking
- Constraint tracking
- Assumption tracking
- Rule snapshot tracking
- Scenario tagging
- Scenario search
- Scenario history

Each scenario must preserve the inputs, assumptions, constraints, rule snapshot, and calculation context required for reproducibility.

### Audit Module

The Audit Module records the computational history of system outputs.

Features include:

- Decision trace
- Rule provenance
- Rule-version recording
- Source recording
- Constraint evaluation logs
- Calculation trace
- Allocation trace
- Assumption tracking
- Input tracking
- Output tracking
- Scenario fingerprints
- Reproducibility hashes
- Audit reports
- Historical audit records
- Calculation verification

### Explainability Module

The Explainability Module translates deterministic system outputs into understandable explanations.

Features include:

- Allocation explanations
- Rule explanations
- Constraint explanations
- Tax explanations
- Yield explanations
- Risk explanations
- Liquidity explanations
- Strategy comparisons
- Scenario explanations
- Regulatory change explanations
- Calculation summaries
- Source references
- Assumption disclosure

The explanation layer must reflect the underlying computation and must not create unsupported financial, tax, legal, or regulatory conclusions.

### AI Interaction Module

The AI Interaction Module provides natural-language interaction with the system.

Features include:

- Natural-language financial queries
- Natural-language scenario creation
- Natural-language constraint creation
- Rule-grounded explanations
- Strategy comparison
- Scenario interpretation
- Calculation explanations
- Regulatory summaries
- User-intent translation
- Structured output generation
- Retrieval-grounded responses
- Citation-aware responses
- Confidence indicators
- Unsupported-claim detection
- Rule-source grounding

The AI must operate as an interface and explanation layer. It must not become the authoritative source for financial rules.

### Regulatory Monitoring Module

The Regulatory Monitoring Module monitors supported regulatory sources for changes.

Features include:

- Scheduled source checks
- Source health monitoring
- Regulatory change detection
- Tax rule change detection
- State tax change detection
- FDIC rule change detection
- Treasury change detection
- New rule detection
- Modified rule detection
- Superseded rule detection
- Effective-date alerts
- Pending-rule alerts
- Change summaries
- Rule graph update notifications

### Rebalancing Module

The Rebalancing Module evaluates existing strategies against current rules and conditions.

Features include:

- Rule-change rebalancing
- Yield-change rebalancing
- Tax-change rebalancing
- Liquidity-based rebalancing
- Concentration-based rebalancing
- Insurance-coverage rebalancing
- Constraint-based rebalancing
- Rebalancing recommendations
- Before-and-after comparison
- Rebalancing simulation
- User approval workflows

The system must not automatically execute financial transactions.

### Reporting Module

The Reporting Module produces structured financial analysis.

Features include:

- Capital allocation reports
- Custody reports
- Insurance coverage reports
- Tax impact reports
- After-tax yield reports
- Liquidity reports
- Risk reports
- Scenario reports
- Regulatory change reports
- Audit reports
- Strategy comparison reports
- Historical comparison reports
- Rule provenance reports
- Constraint compliance reports

### API Module

The API Module provides programmatic access to system capabilities.

Supported interfaces may include:

- Capital input
- Rule resolution
- Tax calculation
- Custody analysis
- Yield calculation
- Constraint management
- Simulation
- Optimization
- Scenario management
- Audit retrieval
- Explanation generation
- Regulatory ingestion
- Reporting

API responses must provide structured outputs and sufficient metadata to identify applicable rules, versions, assumptions, and calculation contexts.

### Security and Privacy Module

The Security and Privacy Module protects financial scenario data and system configuration.

Features include:

- Local-first deployment
- Self-hosted operation
- Encryption support
- Access controls
- Role-based permissions
- Scenario access controls
- Audit log protection
- Sensitive data minimization
- Configurable data retention
- Secure API authentication
- Secure module execution
- Configuration protection

### Reproducibility Module

The Reproducibility Module ensures that historical calculations can be reconstructed.

Features include:

- Versioned calculations
- Versioned regulatory rules
- Versioned tax codes
- Versioned scenarios
- Versioned constraints
- Versioned assumptions
- Historical replay
- Deterministic computation
- Calculation fingerprints
- Reproducible reports
- Rule snapshot preservation
- Source snapshot references

### Data Validation Module

The Data Validation Module validates financial and regulatory inputs before they enter computational processes.

Features include:

- Input validation
- Type validation
- Range validation
- Currency validation
- Date validation
- Jurisdiction validation
- Instrument validation
- Ownership validation
- Regulatory source validation
- Rule schema validation
- Constraint validation
- Missing-data detection
- Conflicting-data detection
- Invalid-data reporting

### Data Provenance Module

The Data Provenance Module tracks the origin and lifecycle of data used by the system.

Features include:

- Source identification
- Source authority classification
- Source timestamps
- Source versioning
- Rule provenance
- Financial data provenance
- Calculation provenance
- Transformation history
- Data lineage
- Provenance reporting

---

## Optional Plugin Modules

Optional plugins extend Altius Capital OS without changing the core architecture.

### Additional Jurisdiction Plugins

Optional jurisdiction modules may provide:

- Additional U.S. jurisdictions
- International tax systems
- Provincial tax systems
- Country-specific regulatory systems
- Residency systems
- Cross-border taxation
- International financial regulations

### Additional Financial Instrument Plugins

Optional instrument modules may support:

- Municipal securities
- Corporate bonds
- Government securities outside the U.S.
- Insurance products
- Annuity products
- Additional cash-equivalent instruments
- Additional fixed-income instruments
- User-defined instruments

Each optional instrument plugin must define its applicable tax, risk, liquidity, custody, regulatory, and yield characteristics.

### Advanced Optimization Plugins

Optional optimization plugins may provide:

- Linear programming
- Integer optimization
- Multi-objective optimization
- Stochastic optimization
- Monte Carlo optimization
- Constraint programming
- Genetic algorithms
- Custom optimization algorithms

### Advanced Simulation Plugins

Optional simulation plugins may provide:

- Monte Carlo simulation
- Probabilistic stress testing
- Macroeconomic scenarios
- Yield curve scenarios
- Inflation scenarios
- Banking-system stress scenarios
- Custom scenario generators

### Macro-Economic Plugin

An optional Macro-Economic Plugin may provide:

- Federal funds rate data
- Treasury yield curve data
- Inflation data
- CPI data
- Banking stress indicators
- Economic growth indicators
- Macroeconomic scenarios
- Historical macroeconomic datasets

### Market Data Plugins

Optional market data plugins may provide:

- Current yields
- Historical yields
- Treasury rates
- CD rates
- Deposit rates
- Market benchmarks
- Financial instrument pricing
- Historical market datasets

Market data must remain separate from authoritative regulatory rules.

### Regulatory Source Plugins

Optional regulatory source plugins may support:

- Additional government agencies
- State legislative sources
- International regulators
- Specialized regulatory authorities
- Industry-specific regulatory sources

Each source plugin must identify its authority, provenance, publication date, and applicable jurisdiction.

### AI Provider Plugins

Optional AI provider plugins may support:

- Local language models
- Self-hosted models
- Cloud AI providers
- Specialized financial language models
- Retrieval-augmented generation systems
- Custom inference engines

AI providers must not be permitted to silently replace the Rule Graph or deterministic computation engines.

### Identity and Ownership Plugins

Optional ownership plugins may expand:

- Individual ownership
- Joint ownership
- Trust ownership
- Business entities
- Estate structures
- Beneficiary structures
- Multi-entity capital relationships

### Notification Plugins

Optional notification plugins may provide:

- Email notifications
- Local notifications
- Web notifications
- Regulatory alerts
- Scenario alerts
- Liquidity alerts
- Maturity alerts
- Constraint violation alerts

### Integration Plugins

Optional integration plugins may connect Altius Capital OS with external systems for data import, reporting, or analysis.

External integrations must not receive authority to modify validated regulatory rules without explicit validation and versioning.

---

## System Integrity Requirements

All core modules must maintain separation between:

- Regulatory rules
- Financial data
- User assumptions
- User constraints
- Computational logic
- AI-generated explanations
- External market data
- Historical scenarios

No module may silently modify another module's authoritative data.

Financial rules must be versioned.

Regulatory rules must retain source provenance.

Calculations must retain the rule snapshot used to produce the result.

Scenarios must retain the assumptions and constraints used to produce the result.

Hard constraints must be enforced independently of the AI layer.

AI-generated explanations must remain subordinate to validated computational results.

Historical calculations must be reproducible whenever the required rule, data, and scenario versions remain available.

## AI Safety and Authority Boundaries

Altius Capital OS is a computational and analytical system.

The AI layer must:

- Explain system calculations
- Explain applicable rules
- Translate user intent into structured inputs
- Help construct scenarios
- Help construct constraints
- Compare system-generated strategies
- Identify missing information
- Identify potential conflicts
- Identify uncertainty

The AI layer must not:

- Invent regulatory requirements
- Override validated rules
- Modify hard constraints without authorization
- Represent assumptions as facts
- Represent simulations as guarantees
- Represent modeled outcomes as guaranteed returns
- Claim FDIC, Treasury, brokerage, tax, or regulatory protection when the applicable rule has not been established
- Execute transactions
- Take custody of funds

## Financial Decision Boundary

Altius Capital OS is designed to model financial structures and make capital decisions computable. It does not itself provide guarantees of investment performance, insurance coverage, tax outcomes, legal outcomes, or financial institution solvency.

Users remain responsible for validating financial decisions against current authoritative requirements and obtaining professional advice where appropriate.

## Open and Extensible Design

Altius Capital OS is designed as an open, modular financial computation framework.

The architecture must allow developers to add:

- New jurisdictions
- New tax systems
- New financial instruments
- New regulatory sources
- New optimization algorithms
- New simulation methods
- New AI providers
- New data providers
- New reporting systems
- New constraint types
- New scenario models

Extensions must preserve the core principles of modularity, versioning, provenance, auditability, reproducibility, and separation of authority.

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
  - [https://roxanneardary.com/altius-capital-os/](https://roxanneardary.com/altius-capital-os/)  

---


## License & Notice Requirements

Altius Capital OS is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- Altius Capital OS specificiations are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.  
  Any update that adds new contributors or modifies attribution should also update `notice.md`.
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.  
