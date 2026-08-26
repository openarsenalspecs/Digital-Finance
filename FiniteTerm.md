# FiniteTerm
**Financing You Can Model.**
- HTML Mirror:  [https://roxanneardary.com/finiteterm-specification/](https://roxanneardary.com/finiteterm-specification/)  

---

FiniteTerm is a modular, open source specification for deterministic financing across industries and products, excluding education. The specification provides a common financing framework where terms, calculations, qualification requirements, payment structures, lifecycle events, and settlement conditions can be explicitly defined, modeled, and audited.

FiniteTerm separates universal financing rules from industry and product-specific requirements. The Core Financing Module establishes the fundamental financing framework, while industry, product, and optional plugin modules extend the specification for specific applications without requiring changes to the core.

---

## Specification

FiniteTerm is designed around the principle that financing should be predictable and modelable. Given the same inputs, applicable modules, and defined rules, a compliant implementation should produce the same financing result.

The specification establishes a maximum financing term of 30 years. The financing term is also limited to 67% of the expected useful life of the financed product. The applicable interest rate is determined by the financier and applied through the defined financing calculations.

FiniteTerm supports both secured and unsecured financing and can incorporate affordability, cost of living, insurance, payment variation, cost escalation, portability, refinancing, and other requirements through modular components.

Education financing is specifically outside the scope of FiniteTerm.

## Modular Design

FiniteTerm uses a layered modular architecture.

### Core

The Core defines universal financing behavior that applies regardless of industry or product.

### Industry Modules

Industry Modules define requirements and characteristics specific to an industry.

Examples include:

- Automotive
- Real Estate
- Healthcare
- Energy
- Agriculture
- Construction
- Manufacturing
- Technology
- Telecommunications
- Transportation
- Consumer Goods
- Business Equipment
- Infrastructure
- Marine
- Aviation
- Recreation
- Hospitality
- Retail
- Professional Services

### Product Modules

Product Modules define financing characteristics for specific products or product classes within an industry.

Examples include:

- Automobiles
- Commercial Vehicles
- Solar Systems
- Battery Storage
- HVAC Systems
- Manufacturing Equipment
- Computers
- Servers
- Agricultural Equipment
- Medical Equipment
- Infrastructure Systems

New industries and products can be added without modifying the Core.

## Core Modules

### Core Financing Module

- Defines the universal financing framework
- Calculates principal
- Calculates interest
- Calculates financing charges
- Calculates payment amounts
- Supports payment frequencies
- Generates amortization schedules
- Tracks outstanding principal
- Tracks accrued interest
- Tracks fees and charges
- Calculates total financing cost
- Calculates remaining balances
- Calculates payoff amounts
- Defines financing states
- Defines financing lifecycle
- Records financing events
- Produces reproducible financing calculations

### Industry Module

- Defines industry-specific financing requirements
- Defines industry-specific asset characteristics
- Defines applicable industry rules
- Supports industry-specific qualification requirements
- Allows industries to be added independently of the Core
- Provides industry-specific inputs to the financing system

### Product Module

- Identifies the financed product
- Defines product characteristics
- Defines expected useful life
- Defines applicable product requirements
- Defines product-specific qualification requirements
- Provides product-specific financing inputs
- Supports individual products and product classes

### Product Life Expectancy Module

- Records expected useful life
- Determines maximum financing term
- Limits financing to 67% of expected useful life
- Enforces the 30-year absolute maximum
- Supports manufacturer-defined useful life
- Supports industry-defined useful life
- Supports independently established useful life
- Accounts for remaining useful life
- Prevents financing terms from exceeding defined lifecycle limits

### Interest Rate Module

- Allows the financier to establish the interest rate
- Records the applicable interest rate
- Applies the rate through defined financing formulas
- Supports fixed interest rates
- Supports variable interest rates where permitted
- Records applicable rate changes
- Maintains an auditable rate history
- Does not impose a universal interest rate

### Affordability Module

- Determines financing affordability
- Evaluates payment capacity
- Evaluates income
- Evaluates existing financial obligations
- Evaluates required expenses
- Evaluates available disposable income
- Supports affordability thresholds
- Produces deterministic affordability results
- Allows financiers to define applicable affordability rules
- Can be activated when required

### Cost of Living Module

- Evaluates required living expenses
- Accounts for household size
- Accounts for housing expenses
- Accounts for utilities
- Accounts for transportation
- Accounts for insurance
- Accounts for required household expenses
- Supports geographic cost-of-living data
- Calculates required minimum living costs
- Provides inputs to the Affordability Module
- Can be activated when required

### Secured Financing Module

- Defines secured financing arrangements
- Identifies collateral
- Verifies collateral ownership
- Records collateral value
- Calculates loan-to-value ratios
- Records security interests
- Defines collateral requirements
- Defines collateral insurance requirements
- Tracks collateral status
- Defines collateral release conditions
- Supports collateral substitution where permitted
- Defines predetermined default procedures

### Insurance Module

- Identifies required insurance
- Defines minimum coverage requirements
- Records insurance policies
- Verifies coverage
- Tracks policy expiration
- Tracks policy renewal
- Records insurance status
- Defines financing responses to coverage lapses
- Supports asset-specific insurance requirements
- Supports liability insurance requirements
- Supports collateral insurance requirements

### Payment Variation Module

- Supports predefined payment variations
- Supports fixed payments
- Supports increasing payments
- Supports decreasing payments
- Supports seasonal payments
- Supports milestone payments
- Supports revenue-based payments
- Supports predetermined irregular payment schedules
- Defines payment changes in advance
- Establishes rules governing payment changes
- Prevents arbitrary payment changes outside defined rules
- Models payment variations across the financing lifecycle

### Cost Escalation Module

- Models future changes in financing-related costs
- Accounts for insurance increases
- Accounts for maintenance increases
- Accounts for taxes
- Accounts for utilities
- Accounts for operating expenses
- Supports explicitly defined escalation assumptions
- Separates projected costs from guaranteed costs
- Models future affordability
- Supports cost escalation scenarios

### Asset Condition Module

- Records asset condition
- Records asset age
- Records usage
- Records mileage where applicable
- Records maintenance history
- Determines remaining useful life
- Adjusts applicable financing characteristics based on remaining life
- Supports used-asset financing
- Prevents new-asset assumptions from automatically applying to existing assets

### Residual Value Module

- Estimates expected value at financing maturity
- Records expected residual value
- Supports product-specific residual-value models
- Supports industry-specific valuation rules
- Supports end-of-term valuation
- Supports residual-value scenarios
- Provides inputs for financing and refinancing calculations

### Depreciation Module

- Records applicable depreciation methodology
- Calculates projected depreciation
- Models asset value over time
- Supports product-specific depreciation rules
- Supports industry-specific depreciation rules
- Provides asset-value projections
- Provides inputs to residual-value calculations

### Maintenance Module

- Defines required maintenance
- Records maintenance schedules
- Estimates maintenance costs
- Tracks maintenance events
- Tracks maintenance compliance
- Supports asset-specific maintenance requirements
- Supports industry-specific maintenance requirements
- Provides maintenance information for lifecycle modeling

### Revenue Module

- Supports financing tied to revenue-generating assets
- Records projected revenue
- Records actual revenue
- Supports revenue-based payments
- Supports payment percentage formulas
- Supports minimum payment requirements
- Supports maximum payment limits
- Models revenue variation
- Tracks revenue-related financing performance

### Guarantee Module

- Supports personal guarantees
- Supports corporate guarantees
- Supports third-party guarantees
- Records guarantee terms
- Records guarantor obligations
- Defines guarantee activation conditions
- Tracks guarantee status
- Defines guarantee termination conditions

### Refinancing Module

- Models existing financing
- Calculates remaining principal
- Calculates remaining financing costs
- Calculates early payoff requirements
- Models replacement financing
- Compares existing and replacement financing
- Calculates refinancing costs
- Calculates new payment obligations
- Calculates new financing terms
- Records refinancing events

### Early Payoff Module

- Calculates current payoff amount
- Calculates remaining principal
- Calculates applicable payoff fees
- Calculates interest avoided
- Calculates total savings
- Determines payoff date
- Updates financing status
- Produces an auditable payoff calculation

### Lifecycle Module

- Defines financing lifecycle states
- Supports proposed financing
- Supports qualified financing
- Supports approved financing
- Supports activated financing
- Supports performing financing
- Supports modified financing
- Supports delinquent financing
- Supports defaulted financing
- Supports recovery
- Supports completed financing
- Defines transitions between states
- Records lifecycle events

### Event Ledger Module

- Records financing events
- Records payments
- Records missed payments
- Records rate changes
- Records fees
- Records modifications
- Records collateral changes
- Records insurance changes
- Records refinancing
- Records default events
- Records settlement
- Maintains an auditable chronological history

### Explainability Module

- Explains financing calculations
- Identifies calculation inputs
- Identifies applicable rules
- Identifies applicable modules
- Identifies calculation versions
- Shows how payment amounts were determined
- Shows how financing terms were determined
- Shows how qualification results were determined
- Provides machine-readable calculation explanations
- Prevents unexplained financing outcomes

### Versioning Module

- Versions financing rules
- Versions industry modules
- Versions product modules
- Records the version used to create financing
- Preserves historical financing rules
- Prevents unauthorized silent changes
- Defines rules for permitted updates
- Maintains module compatibility

### Interoperability Module

- Defines standardized financing data
- Defines standardized financing fields
- Defines standardized calculation outputs
- Supports communication between financing systems
- Supports standardized financing records
- Enables integration with accounting systems
- Enables integration with financial management systems

### Portability Module

- Allows financing records to be transferred
- Preserves original financing terms
- Preserves payment history
- Preserves current balance
- Preserves applicable rules
- Preserves interest rate information
- Preserves collateral information
- Preserves modification history
- Preserves financing status
- Supports transfers between compatible systems
- Supports refinancing and financing-provider changes
- Prevents financing records from being locked to a single platform

### Comparison Module

- Standardizes financing offers
- Compares financing amounts
- Compares interest rates
- Compares terms
- Compares payment amounts
- Compares total financing costs
- Compares fees
- Compares collateral requirements
- Compares insurance requirements
- Compares early payoff conditions
- Produces standardized financing comparisons

### Marketplace Module

- Allows financiers to respond to standardized financing requests
- Allows multiple financing offers to be modeled
- Standardizes financing offer presentation
- Allows financing offers to be compared
- Separates financing rules from financier-specific pricing
- Allows financiers to compete using compatible financing structures

### Regulatory Rules Module

- Supports jurisdiction-specific rules
- Supports federal requirements
- Supports state requirements
- Supports local requirements
- Supports industry requirements
- Separates regulatory rules from the Core
- Allows jurisdiction-specific modules to be added
- Allows regulatory rules to be versioned
- Provides auditable records of applicable requirements

### Human Override Module

- Allows explicitly authorized exceptions
- Requires overrides to be recorded
- Identifies the authorizing person or entity
- Records the original deterministic result
- Records the modified result
- Records the reason for the override
- Records the applicable authority
- Records the date and time
- Preserves the original financing calculation
- Makes overrides auditable
- Prevents undocumented changes to financing outcomes
- Allows organizations to define which rules may or may not be overridden

### Dispute Module

- Records financing disputes
- Identifies disputed calculations
- Preserves the original financing state
- Preserves applicable rules
- Provides calculation history
- Provides event history
- Supports documented dispute resolution
- Records modifications resulting from resolution
- Maintains an auditable dispute record

### Security and Integrity Module

- Protects financing records
- Maintains data integrity
- Detects unauthorized changes
- Records changes to financial data
- Supports cryptographic verification where implemented
- Preserves calculation integrity
- Prevents silent modification of historical financing records

### Modeling Module

- Models financing before execution
- Calculates expected payments
- Calculates total financing costs
- Models asset lifecycle
- Models payment schedules
- Models cost escalation
- Models affordability
- Models refinancing
- Models early payoff
- Models adverse scenarios
- Models alternative financing structures
- Produces reproducible results from identical inputs and rules

### Settlement Module

- Determines when financing is complete
- Calculates final payment
- Calculates final balance
- Releases applicable collateral
- Terminates applicable guarantees
- Records final settlement
- Archives the financing record
- Preserves complete financing history
- Produces a final settlement record

---

## Optional Plugin Modules

FiniteTerm supports optional plugin modules that extend functionality without changing the Core specification.

### Scenario Analysis Plugin

- Creates alternative financing scenarios
- Models base-case outcomes
- Models favorable outcomes
- Models adverse outcomes
- Models early payoff
- Models refinancing
- Models asset sale
- Models payment changes
- Models cost changes
- Compares financing outcomes

### Stress Testing Plugin

- Tests financing against adverse conditions
- Models income reductions
- Models revenue reductions
- Models increased expenses
- Models increased insurance costs
- Models increased maintenance costs
- Models asset-value reductions
- Models financial shocks
- Measures financing resilience
- Identifies conditions that could impair affordability

### Inflation Modeling Plugin

- Models inflation
- Models future purchasing power
- Models real financing costs
- Models future operating expenses
- Models future income
- Models future maintenance costs
- Provides inflation-adjusted scenarios

### Tax Modeling Plugin

- Models applicable taxes
- Models property taxes
- Models transaction taxes
- Models recurring taxes
- Separates tax assumptions from financing calculations
- Provides tax-related financing scenarios

### Asset Valuation Plugin

- Provides asset valuation models
- Supports market-value inputs
- Supports replacement-cost inputs
- Supports industry valuation methodologies
- Supports valuation updates
- Provides valuation history
- Provides valuation inputs for secured financing

### Revenue Forecasting Plugin

- Models future revenue
- Supports historical revenue analysis
- Supports projected revenue
- Supports seasonal revenue
- Supports revenue growth assumptions
- Supports revenue decline scenarios
- Provides inputs to revenue-based financing

### Insurance Risk Plugin

- Evaluates insurance requirements
- Models insurance cost changes
- Evaluates coverage adequacy
- Models insurance availability
- Identifies coverage risks
- Integrates with the Insurance Module

### Maintenance Forecasting Plugin

- Projects maintenance requirements
- Projects maintenance costs
- Models maintenance schedules
- Models major replacement events
- Provides maintenance cost scenarios
- Integrates with the Maintenance Module

### Data Verification Plugin

- Verifies financing inputs
- Verifies product information
- Verifies asset information
- Verifies ownership information
- Verifies valuation information
- Verifies insurance information
- Records verification results

### Identity Verification Plugin

- Supports identity verification
- Supports entity verification
- Records verification status
- Provides verified identity inputs
- Integrates with applicable qualification modules

### AI Analysis Plugin

- Assists with financing analysis
- Identifies unusual financing conditions
- Detects potential calculation anomalies
- Assists with scenario generation
- Assists with data classification
- Provides analytical recommendations
- Does not independently modify deterministic financing rules
- Requires defined authorization for actions affecting financing outcomes

### Reporting Plugin

- Generates financing reports
- Generates amortization reports
- Generates cost reports
- Generates affordability reports
- Generates lifecycle reports
- Generates audit reports
- Generates comparison reports
- Generates settlement reports

### Notification Plugin

- Provides payment notifications
- Provides insurance notifications
- Provides maintenance notifications
- Provides financing status notifications
- Provides approaching maturity notifications
- Provides default-condition notifications
- Provides settlement notifications

### Integration Plugin

- Connects FiniteTerm to external financial systems
- Connects to accounting systems
- Connects to payment systems
- Connects to asset management systems
- Connects to insurance systems
- Connects to business management systems
- Supports standardized data exchange

## Fundamental Rules

1. Every financing arrangement must have a defined beginning and end.
2. No financing term may exceed 30 years.
3. The financing term may not exceed 67% of the financed product's expected useful life.
4. The financier determines the applicable interest rate.
5. Financing calculations must be reproducible from their defined inputs and rules.
6. Industry and product characteristics are defined through modular specifications.
7. Optional modules may be activated when applicable.
8. Exceptions must be explicitly recorded through the Human Override Module.
9. Financing records must remain portable between compatible implementations.
10. The complete financing lifecycle must be auditable.
11. Education financing is outside the scope of FiniteTerm.
12. New industries and products must be able to be added without modifying the Core.
13. Specialized modules must not silently alter universal Core rules.
14. Identical inputs and applicable rules should produce identical deterministic outputs.
15. Financing terms, costs, qualification requirements, and lifecycle conditions should be modelable before execution.

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
  - [https://roxanneardary.com/finiteterm/](https://roxanneardary.com/finiteterm/)  

---

## License & Notice Requirements

FiniteTerm is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.
By contributing to any Open Arsenal project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.
- FiniteTerm specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.
  Any update that adds new contributors or modifies attribution should also update `notice.md`.
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
