# Explorer Capital

**Capital That Opens the World.**

Explorer Capital is a deterministic financing specification designed to provide purpose-specific capital for participants in an approved **World Expedition Program** curriculum.

The specification defines a fixed, transparent repayment model for loans of up to **$120,000**, using a two-year interest-free delay followed by a six-year repayment period. The model uses standard amortization to determine the total interest obligation, then redistributes that total interest equally across the repayment schedule so that every scheduled payment contains the same principal amount and the same interest amount.

Explorer Capital is not conventional declining-balance amortization. Standard amortization is used only to establish the total interest amount. The actual Explorer Capital repayment schedule uses equal principal and equal interest components.

## Purpose

Explorer Capital is designed to provide a predictable financial framework for individuals participating in an approved World Expedition Program curriculum.

The specification is intended to:

- Provide financing specifically connected to an approved World Expedition curriculum.
- Establish predictable repayment terms before loan origination.
- Provide a two-year interest-free delay.
- Calculate total interest using standard amortization.
- Redistribute the calculated total interest equally across the scheduled payments.
- Divide principal equally across the scheduled payments.
- Build principal equity at a constant rate.
- Allow principal prepayments without penalty.
- Eliminate future interest associated with eliminated payment periods.
- Allow complete early payoff by repayment of outstanding principal.
- Provide deterministic, reproducible calculations.
- Support independent implementations.
- Provide a modular foundation for financial, curriculum, compliance, and expedition management systems.

## Core Design Principles

### Deterministic Financing

Every loan must be reproducible from a defined set of inputs.

The same inputs must produce the same:

- Total interest
- Total repayment obligation
- Principal payment amount
- Interest payment amount
- Scheduled payment amount
- Payment count
- Payment dates
- Remaining principal
- Prepayment results
- Early payoff amount

No variable-rate calculation or discretionary interest calculation may be introduced into the core financing engine.

### Purpose-Specific Financing

Explorer Capital is not intended to function as a general-purpose lending specification.

Eligibility is tied to participation in an approved World Expedition Program curriculum.

The financing system must verify that the applicant has an approved curriculum before the loan can be originated.

### Equal Principal

The original principal is divided equally across the scheduled repayment period.

For the standard 72-month repayment term:

**Monthly Principal = Original Principal ÷ 72**

The principal component remains constant throughout the scheduled repayment period, subject to final currency reconciliation.

### Equal Interest

Explorer Capital first calculates what the total interest would be under standard amortization using the applicable principal, interest rate, and repayment term.

The resulting total interest is then divided equally across the scheduled repayment period.

**Monthly Interest = Standard Amortization Total Interest ÷ 72**

The actual Explorer Capital schedule does not use declining-balance interest.

### Equal Payment

The scheduled payment consists of:

**Equal Principal + Equal Interest**

Because both components are fixed, the scheduled payment is fixed.

The borrower therefore receives a predictable payment schedule while building principal equity at a constant rate.

## Core Modules

### Eligibility Module

The Eligibility Module determines whether an applicant satisfies the program requirement for Explorer Capital financing.

A qualifying applicant must have an **approved World Expedition Program curriculum**.

The module must verify:

- Applicant identity
- Approved curriculum status
- Curriculum approval authority
- Curriculum approval date
- Curriculum version
- Applicable expedition period
- Curriculum status
- Any required program eligibility conditions

The absence of an approved curriculum prevents loan origination.

**Core rule:**

**No Approved World Expedition Curriculum = No Explorer Capital Financing**

Curriculum approval establishes program eligibility but does not independently guarantee financial approval.

### Curriculum Verification Module

The Curriculum Verification Module maintains the relationship between the financing agreement and the approved World Expedition curriculum.

The module should support:

- Curriculum identification
- Curriculum versioning
- Curriculum approval records
- Curriculum status
- Curriculum provider
- Curriculum approval authority
- Participant enrollment
- Curriculum completion status
- Curriculum modification records

A general travel itinerary, personal educational plan, or independent expedition plan does not satisfy the approved curriculum requirement unless formally approved under the World Expedition Program.

### Loan Origination Module

The Loan Origination Module creates the deterministic loan record.

The standard inputs include:

- Original principal
- Interest rate
- Repayment term
- Deferral period
- Payment frequency
- Approved curriculum
- Borrower
- Origination date
- Repayment start date

The standard Explorer Capital parameters are:

| Parameter | Standard Value |
|---|---:|
| Maximum Principal | $120,000 |
| Annual Interest Rate | 5% |
| Deferral Period | 2 years |
| Repayment Period | 6 years |
| Scheduled Payments | 72 |
| Payment Frequency | Monthly |
| Interest During Deferral | $0 |
| Interest Method | Standard amortization calculation |
| Actual Payment Allocation | Equal principal and equal interest |

### Interest Calculation Module

The Interest Calculation Module establishes the total interest used by the Explorer Capital schedule.

The module first calculates the conventional amortized payment using:

**Principal:** Original loan principal

**Annual Rate:** 5%

**Monthly Rate:** 5% ÷ 12

**Term:** 72 months

The standard amortization payment is calculated using the conventional amortization formula.

The total conventional payments are then determined.

Total interest is:

**Total Interest = Conventional Monthly Payment × 72 − Original Principal**

This total interest becomes the Explorer Capital scheduled interest obligation.

The standard amortization schedule itself is not used as the actual repayment allocation.

### Interest Redistribution Module

After total interest has been established, the Interest Redistribution Module divides that amount equally across all scheduled payments.

**Monthly Interest = Total Interest ÷ 72**

Every scheduled payment therefore contains the same interest component.

The module must not:

- Recalculate interest against declining principal.
- Reduce monthly interest as principal declines.
- Compound interest.
- Accrue additional interest during the two-year delay.
- Add unpaid interest to principal.

### Principal Allocation Module

The Principal Allocation Module divides the original principal equally across the 72 scheduled payments.

**Monthly Principal = Original Principal ÷ 72**

The principal component remains constant.

The borrower therefore builds equity at a predictable rate.

For a $120,000 loan:

**$120,000 ÷ 72 = $1,666.666666...**

The implementation must maintain sufficient internal precision and apply final-payment reconciliation.

### Payment Calculation Module

The Payment Calculation Module combines the two equal components.

**Monthly Payment = Monthly Principal + Monthly Interest**

The payment amount is established before repayment begins.

The payment schedule must identify separately:

- Principal
- Interest
- Total payment
- Remaining principal
- Cumulative principal paid
- Cumulative interest paid
- Remaining scheduled interest
- Remaining payment count

### Two-Year Delay Module

Explorer Capital includes a 24-month interest-free delay.

During the delay:

- No payment is required under the standard schedule.
- No interest accumulates.
- No interest is capitalized.
- Principal does not increase.
- The repayment obligation does not grow because of the delay.

The 72-month repayment schedule begins after the two-year delay.

The two-year delay does not convert the loan into a 96-month interest-bearing loan.

### Repayment Schedule Module

The Repayment Schedule Module generates the complete schedule before repayment begins.

The schedule must include:

- Payment number
- Payment date
- Principal component
- Interest component
- Total payment
- Remaining principal
- Cumulative principal
- Cumulative interest
- Remaining scheduled interest

The complete schedule must be independently reproducible.

### Equity Accumulation Module

The Equity Accumulation Module tracks the constant reduction of principal.

Every standard payment reduces principal by the same amount.

The module must make it possible to determine:

- Principal repaid
- Principal remaining
- Percentage of original principal repaid
- Number of payment units completed
- Number of payment units remaining

The system must not use declining-balance interest to determine equity accumulation.

### Prepayment Module

Borrowers may make additional principal payments.

A qualifying principal prepayment:

- Reduces outstanding principal.
- Does not change the interest rate.
- Does not create additional interest.
- Does not create a prepayment penalty.
- Does not convert the loan to standard declining-balance amortization.
- Reduces the number of remaining payment units.
- Eliminates the interest associated with eliminated payment units.

### Payment Unit Module

Explorer Capital treats the scheduled repayment as deterministic payment units.

Each standard payment unit consists of:

**One equal principal component + one equal interest component**

A prepayment removes future payment units rather than changing the fundamental structure of the remaining payment units.

This means the benefit of prepayment is primarily a **shorter repayment period and reduced total interest**, rather than a reduced scheduled payment.

### Schedule Regeneration Module

When a principal prepayment occurs, the system regenerates the remaining schedule.

The regeneration process must:

- Apply the prepayment to principal.
- Determine the remaining principal.
- Determine the remaining payment units.
- Preserve the equal-component methodology.
- Remove eliminated payment units.
- Remove interest associated with eliminated payment units.
- Preserve the original interest methodology.
- Produce a new deterministic final payoff date.

The regenerated schedule must remain transparent and independently reproducible.

### Early Payoff Module

A borrower may completely repay the outstanding principal before the scheduled maturity date.

The complete early payoff amount is:

**Early Payoff Amount = Remaining Principal**

All future scheduled interest is eliminated.

Once the remaining principal reaches zero:

**Remaining Principal = $0**

**Remaining Interest Due = $0**

**Future Interest = $0**

**Loan Status = Paid in Full**

No future interest may survive complete repayment of principal.

### Interest Elimination Module

The Interest Elimination Module ensures that future interest associated with eliminated payment periods is removed from the borrower's obligation.

If a prepayment eliminates payment units, the interest assigned to those units is also eliminated.

This prevents borrowers from paying interest for repayment periods that no longer exist.

### Rounding and Reconciliation Module

The Rounding and Reconciliation Module handles currency precision.

Internal calculations must retain sufficient precision to prevent cumulative rounding errors.

The implementation must reconcile the final payment so that:

**Total Principal Repaid = Original Principal**

**Total Interest Paid ≤ Original Scheduled Interest**

**Final Loan Balance = $0.00**

For a complete scheduled repayment:

**Total Interest Paid = Calculated Total Interest**

For early repayment:

**Total Interest Paid = Interest Associated With Payment Units Actually Completed**

### Deterministic Audit Module

The Audit Module records the calculations used to create and modify every loan schedule.

The audit record should include:

- Original loan inputs
- Curriculum approval record
- Standard amortization calculation
- Calculated total interest
- Equal principal component
- Equal interest component
- Original payment schedule
- Prepayments
- Regenerated schedules
- Eliminated payment units
- Eliminated interest
- Early payoff
- Final reconciliation

Any change affecting the repayment schedule must produce an auditable calculation record.

### Transparency Module

The borrower must be able to view the complete financial structure.

The system should disclose:

- Original principal
- Interest rate
- Standard amortization payment used to establish total interest
- Total calculated interest
- Two-year interest-free delay
- Repayment start date
- Repayment end date
- Equal principal component
- Equal interest component
- Scheduled payment
- Remaining principal
- Remaining interest
- Prepayment effects
- Early payoff amount

The borrower must not need proprietary software to understand the financial obligation.

### Compliance Module

The Compliance Module is designed to support jurisdiction-specific implementation.

The core deterministic calculation must remain separate from jurisdictional rules.

Optional compliance implementations may address:

- Federal lending requirements
- State lending requirements
- Local requirements
- Consumer lending requirements
- Disclosure requirements
- Licensing requirements
- Usury limitations
- Recordkeeping requirements
- Data retention requirements
- Privacy requirements
- Electronic transaction requirements

The specification does not itself establish that an Explorer Capital implementation is legally authorized to make loans in any particular jurisdiction.

### Reporting Module

The Reporting Module provides financial and program reports.

Reports may include:

- Active loans
- Loans in deferral
- Loans in repayment
- Principal outstanding
- Interest paid
- Interest eliminated through prepayment
- Early payoff activity
- Curriculum eligibility
- Curriculum status
- Payment history
- Schedule changes
- Portfolio-level statistics

## Optional Plugin Modules

Optional plugins extend Explorer Capital without altering the deterministic core calculation.

### Jurisdiction Compliance Plugin

Provides configurable compliance rules for specific jurisdictions.

Potential functions include:

- State-specific loan rules
- Federal compliance rules
- Required disclosures
- Licensing checks
- Rate limitations
- Required notices
- Jurisdiction-specific documentation

### Loan Document Plugin

Generates loan documentation from the deterministic loan record.

Potential documents include:

- Loan agreement
- Repayment schedule
- Disclosure statement
- Prepayment statement
- Early payoff statement
- Payment history
- Final satisfaction statement

### Curriculum Management Plugin

Provides expanded curriculum management capabilities.

Potential functions include:

- Curriculum authoring
- Curriculum approval workflows
- Curriculum version control
- Instructor management
- Participant enrollment
- Curriculum milestones
- Completion verification

### Expedition Management Plugin

Connects financial records to expedition planning.

Potential functions include:

- Expedition planning
- Destination management
- Expedition milestones
- Travel phases
- Budget planning
- Completion tracking
- Expedition documentation

### Applicant Portal Plugin

Provides a participant-facing interface for:

- Application
- Curriculum verification
- Loan status
- Payment schedule
- Payment history
- Prepayment requests
- Early payoff requests
- Documents
- Notifications

### Payment Processing Plugin

Connects Explorer Capital to payment providers.

The plugin may process:

- Scheduled payments
- Principal prepayments
- Early payoff payments
- Payment confirmations
- Failed payments
- Refunds
- Reconciliation

The payment processing plugin must not alter the deterministic calculation rules.

### Accounting Plugin

Provides integration with accounting systems.

Potential functions include:

- Principal ledger
- Interest ledger
- Payment reconciliation
- Prepayment accounting
- Early payoff accounting
- Financial reporting
- General ledger integration

### Notification Plugin

Provides configurable notifications for:

- Repayment start
- Upcoming payments
- Payment receipts
- Prepayment confirmation
- Schedule regeneration
- Early payoff confirmation
- Curriculum status changes
- Required documentation

### Analytics Plugin

Provides nonessential analytical capabilities.

Potential functions include:

- Portfolio analytics
- Repayment performance
- Prepayment trends
- Early payoff rates
- Curriculum participation analytics
- Expedition financing analytics

Analytics must not modify loan calculations.

### Identity and Verification Plugin

Provides optional identity and eligibility verification.

Potential functions include:

- Identity verification
- Applicant verification
- Curriculum verification
- Program eligibility verification
- Document verification

### API Plugin

Provides programmatic access to Explorer Capital functionality.

The API may expose:

- Loan creation
- Loan calculations
- Schedule generation
- Curriculum verification
- Payment records
- Prepayment processing
- Early payoff calculations
- Reporting
- Audit records

The API must preserve the deterministic behavior of the core modules.

### Localization Plugin

Supports international deployment.

Potential functions include:

- Currency formats
- Date formats
- Language localization
- Regional documentation
- Local payment conventions

Localization must not change the underlying deterministic financing methodology unless a jurisdiction-specific implementation explicitly requires a different approved configuration.

## Core Calculation Model

Explorer Capital uses a two-stage calculation.

### Stage One: Standard Amortization Interest Calculation

The system first calculates the standard amortized monthly payment using:

- Original principal
- 5% annual interest
- Monthly compounding frequency for the standard amortization calculation
- 72 monthly payments

The standard amortization payment is:

**PMT = P × r × (1 + r)^n ÷ ((1 + r)^n − 1)**

Where:

- **P** = original principal
- **r** = monthly interest rate
- **n** = 72 payments

Total standard amortized interest is:

**Total Interest = (PMT × 72) − P**

### Stage Two: Equal Component Redistribution

The calculated total interest is divided equally across 72 payments.

**Equal Interest = Total Interest ÷ 72**

The original principal is divided equally across 72 payments.

**Equal Principal = P ÷ 72**

The actual Explorer Capital payment is:

**Explorer Capital Payment = Equal Principal + Equal Interest**

This creates a payment whose total amount corresponds to the conventional amortized payment while distributing principal and interest equally.

## Example Calculation

For the maximum $120,000 loan:

**Original Principal = $120,000**

**Annual Interest Rate = 5%**

**Monthly Rate = 0.05 ÷ 12**

**Repayment Term = 72 months**

The standard amortization calculation establishes the total interest obligation.

The resulting total interest is then divided equally across 72 payments.

The principal is also divided equally across 72 payments.

The resulting Explorer Capital payment therefore has:

- Equal principal every month
- Equal interest every month
- Equal total payment every month

The conventional amortization schedule is not used for actual payment allocation.

## Prepayment Model

The prepayment model is based on eliminating future payment units.

A principal prepayment reduces the remaining principal.

The system then determines how many future payment units are eliminated.

Each eliminated payment unit eliminates:

- Its principal component
- Its associated interest component
- Its scheduled payment

The borrower therefore pays the loan off sooner and pays less total interest.

The payment structure itself does not become a conventional declining-balance loan.

## Early Payoff Model

Complete early payoff requires only the remaining principal.

All future scheduled interest is eliminated.

This produces the fundamental rule:

**Paying principal early eliminates future interest.**

Explorer Capital does not charge future interest after the borrower has completely satisfied the remaining principal.

## Eligibility Model

Explorer Capital financing requires an approved World Expedition Program curriculum.

The eligibility relationship is:

**Approved Curriculum → Program Eligibility → Financial Underwriting → Loan Origination**

Curriculum approval and financial approval remain separate decisions.

## Security and Data Integrity

Implementations should protect:

- Applicant information
- Curriculum records
- Loan records
- Payment records
- Financial calculations
- Audit records
- Identity verification data

Core calculations should be immutable once a loan is originated, except through explicitly defined prepayment, schedule regeneration, reconciliation, or legally required modification processes.

Every modification must be auditable.

## Interoperability

Explorer Capital should be implementable independently of a specific financial institution, payment processor, curriculum platform, or software vendor.

The specification should support:

- Independent calculation engines
- REST APIs
- Structured data exchange
- Financial accounting integrations
- Curriculum management integrations
- Payment integrations
- Compliance integrations

No optional plugin may be required to understand or reproduce the core loan calculation.

## Human Review

Explorer Capital is designed for deterministic calculations, but deterministic calculations do not replace human judgment where human review is legally or operationally required.

Implementations should support human review for:

- Curriculum approval
- Financial underwriting
- Compliance decisions
- Exceptions
- Documentation
- Identity verification
- Disputes
- Schedule corrections

Any human modification to a deterministic loan must be recorded and auditable.

## Design Invariants

A compliant implementation must preserve the following invariants:

- Maximum original principal is $120,000.
- Standard interest rate is 5%.
- Standard repayment term is 72 months.
- Standard delay is 24 months.
- No interest accumulates during the two-year delay.
- Standard amortization determines the total scheduled interest.
- Actual repayment uses equal principal.
- Actual repayment uses equal interest.
- Actual scheduled payments are equal.
- Principal does not determine monthly interest.
- Interest does not compound.
- Prepayment reduces outstanding principal.
- Prepayment reduces the number of remaining payment units.
- Eliminated payment units eliminate their associated interest.
- Complete payoff eliminates all future interest.
- No prepayment penalty is permitted by the core model.
- The final principal balance must equal zero after complete repayment.
- The same inputs must produce the same calculations.

## Terminology

**Explorer Capital:** The deterministic financing specification and associated implementation framework.

**World Explorer:** A participant receiving financing under Explorer Capital.

[**World Expedition Program:**](https://gitlab.com/Roxanne_Ardary/world-expedition) The program under which an approved curriculum qualifies a participant for Explorer Capital eligibility.

**Approved Curriculum:** A World Expedition curriculum formally approved under the applicable program approval process.

**Standard Amortization:** The conventional amortization calculation used solely to establish the total interest obligation.

**Equal Component Repayment:** The Explorer Capital repayment methodology in which principal and interest are each distributed equally across scheduled payments.

**Payment Unit:** A scheduled repayment unit containing one equal principal component and one equal interest component.

**Principal Prepayment:** An additional payment applied to outstanding principal.

**Early Payoff:** Complete repayment of the remaining principal before the scheduled maturity date.

**Interest Elimination:** Cancellation of future interest associated with payment units eliminated through prepayment or early payoff.

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
  - [https://roxanneardary.com/explorer-capital/](https://roxanneardary.com/explorer-capital/)  

---

## License & Notice Requirements

Explorer Capital is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to any Open Arsenal project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.
- Explorer Capital specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
