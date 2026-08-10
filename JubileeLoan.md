# JubileeLoan

**Less Interest. Less Uncertainty. A Defined End.**

JubileeLoan is a deterministic financing specification for refinancing qualifying school loans that have exceeded 15 years in repayment. The specification establishes a one-time interest charge equal to **1% of the total refinanced loan balance**, preserves the borrower's existing monthly payment, and limits the refinancing period to a maximum of 10 years.

JubileeLoan is designed to provide a predictable and finite path for long-term education debt. The refinancing terms are established at the beginning of the agreement and do not change based on income, credit score, market interest rates, servicing changes, or other discretionary factors. The borrower may voluntarily increase payments to accelerate repayment, but the loan originator may not require an increase to the scheduled payment solely because of the refinancing.

If the refinanced loan cannot be fully repaid within the maximum 10-year period, the remaining eligible balance must be declared a debt jubilee and permanently extinguished by the loan originator. The specification therefore creates a definitive terminal outcome rather than allowing the debt to continue indefinitely.

## Specification

JubileeLoan defines a standardized deterministic refinancing framework with the following core parameters:

- The qualifying school loan must have exceeded **15 years in repayment**.
- The refinanced loan receives a **1% interest charge based on the total refinanced loan balance**.
- The 1% interest charge is assessed as part of the refinancing and does not accrue annually.
- No additional annual interest is charged under the core specification.
- No interest compounding is permitted under the core specification.
- The borrower's **existing monthly payment remains the scheduled monthly payment** after refinancing.
- The borrower may voluntarily increase the payment at any time.
- The maximum refinancing period is **10 years or 120 months**.
- The refinancing period may not be extended beyond 10 years.
- No prepayment penalty may be imposed.
- If an eligible balance remains after 120 months, the remaining balance must be declared a **debt jubilee**.
- A debt jubilee permanently extinguishes the remaining eligible balance.
- Refinancing may not reset or restart the original 15-year repayment history.

## Deterministic Financing Model

JubileeLoan treats the existing school loan as the starting state and applies a fixed sequence of rules:

**Existing School Loan**  
→ **15+ Years in Repayment**  
→ **Eligibility Verification**  
→ **1% Total-Loan Interest Charge**  
→ **Existing Payment Preserved**  
→ **Maximum 10-Year Term**  
→ **Paid in Full or Debt Jubilee**

The specification is designed so that identical qualifying loan inputs produce the same refinancing terms and the same available terminal outcomes.

## Refinancing Terms

| Parameter | Specification |
|---|---|
| Qualification period | More than 15 years in repayment |
| Interest charge | 1% of the total refinanced loan balance |
| Interest calculation | One-time calculation at refinancing |
| Annual interest | None under the core specification |
| Interest compounding | Prohibited |
| Existing monthly payment | Preserved as the scheduled payment |
| Voluntary payment increase | Permitted |
| Maximum term | 10 years |
| Maximum repayment period | 120 months |
| Payment increase imposed by originator | Prohibited |
| Term extension | Prohibited |
| Prepayment penalty | Prohibited |
| Remaining balance at 120 months | Mandatory debt jubilee |

## One-Time Interest Charge

The JubileeLoan financing charge is calculated once when the loan is refinanced.

The charge is equal to:

**Interest Charge = Total Refinanced Loan Balance × 0.01**

The total obligation established at refinancing is:

**Total Refinanced Obligation = Total Refinanced Loan Balance + One-Time Interest Charge**

The 1% charge does not become an annual interest rate. It does not recur each year, compound, or increase during the repayment period.

For example, a qualifying loan with a refinanced balance of $50,000 would receive a one-time interest charge of $500, establishing a total refinancing obligation of $50,500.

## Payment Preservation

The borrower's existing monthly loan payment immediately before refinancing becomes the scheduled monthly payment under JubileeLoan.

The core rule is:

> **The borrower's existing monthly payment remains the same after refinancing unless the borrower voluntarily chooses to pay more.**

The loan originator may not increase the scheduled payment solely because the loan has been refinanced through JubileeLoan.

The borrower may voluntarily:

- Increase an individual payment.
- Increase recurring monthly payments.
- Make additional principal payments.
- Pay the loan off early.

Voluntary additional payments do not change the borrower's required scheduled payment and may allow the loan to reach a zero balance before the 10-year maximum.

## Maximum Term

JubileeLoan establishes an absolute maximum repayment period of **120 months**.

The loan originator may not extend the repayment period beyond 120 months through:

- Loan modifications
- Refinancing
- Forbearance
- Deferment
- Servicing transfers
- Re-amortization
- Capitalization
- Payment restructuring
- Administrative delays
- New repayment agreements

The original 15-year repayment history also cannot be reset by the refinancing.

## Debt Jubilee

The debt jubilee is the mandatory terminal mechanism of JubileeLoan.

At the end of the 120-month maximum period:

### Balance Is Zero

If the outstanding balance is $0, the loan is marked **SATISFIED** and the obligation is closed.

### Balance Remains

If an eligible balance remains after 120 months, the loan originator must declare the remaining balance a **debt jubilee** and permanently extinguish the remaining eligible debt.

The borrower cannot be required to:

- Continue making payments.
- Refinance the remaining balance.
- Extend the repayment term.
- Make a balloon payment.
- Enter another repayment agreement.
- Increase the scheduled payment.
- Restart the repayment period.

There is no indefinite repayment state under the core JubileeLoan specification.

## Core Modules

### 1. Eligibility Module

Determines whether a school loan qualifies for JubileeLoan refinancing.

The module verifies:

- Loan type
- Original loan information
- Repayment commencement date
- Total repayment duration
- Whether repayment has exceeded 15 years
- Current outstanding balance
- Previous refinancing history
- Required documentation

Eligibility must be determined using defined and reproducible criteria.

### 2. Loan Verification Module

Establishes the authoritative loan information used by the refinancing process.

The module records:

- Original principal
- Current principal balance
- Existing interest or charges
- Repayment start date
- Current monthly payment
- Payment history
- Loan status
- Previous refinancing or modification history

### 3. Refinancing Module

Converts a qualifying loan into a JubileeLoan agreement.

The module applies:

- The 1% total-loan interest charge
- The verified existing monthly payment
- The maximum 120-month term
- The prohibition on additional annual interest
- The prohibition on compounding
- The mandatory terminal debt-jubilee rule

### 4. Payment Preservation Module

Preserves the borrower's existing monthly payment as the scheduled payment.

The module ensures:

- Existing payment becomes the scheduled refinancing payment.
- The originator cannot require a higher scheduled payment.
- The borrower may voluntarily pay more.
- Additional payments may accelerate repayment.
- No prepayment penalty is permitted.

### 5. Interest Module

Calculates and records the one-time 1% interest charge.

The module must:

- Calculate 1% of the total refinanced loan balance.
- Apply the charge once at refinancing.
- Prevent annual recurrence.
- Prevent compounding.
- Prevent discretionary rate increases.
- Preserve the calculated charge throughout the refinancing period.

### 6. Term Limit Module

Enforces the 120-month maximum repayment period.

The module prevents:

- Term extensions
- Automatic renewals
- Re-amortization that extends maturity
- Refinancing that restarts the term
- Administrative actions that circumvent the maximum term

### 7. Voluntary Acceleration Module

Allows the borrower to voluntarily accelerate repayment.

The module supports:

- Increased monthly payments
- Additional principal payments
- Early payoff
- Irregular additional payments

Voluntary acceleration cannot create a new required payment amount for the borrower.

### 8. Debt Jubilee Module

Executes the mandatory final resolution when the 120-month period expires with an eligible remaining balance.

The module must:

- Determine whether a balance remains.
- Confirm expiration of the maximum term.
- Record the debt-jubilee event.
- Permanently extinguish the eligible remaining balance.
- Mark the loan as resolved.

### 9. Loan State Module

Maintains the deterministic state of each JubileeLoan agreement.

Supported states include:

- `UNQUALIFIED`
- `ELIGIBLE`
- `REFINANCED`
- `REPAYMENT`
- `SATISFIED`
- `JUBILEE`

State transitions must be based on defined conditions rather than discretionary servicing decisions.

### 10. Transparency Module

Maintains a reproducible record of the refinancing calculation and loan state.

The record should include:

- Original loan date
- Repayment commencement date
- Verified repayment duration
- Existing monthly payment
- Refinanced balance
- One-time 1% interest charge
- Total refinancing obligation
- Refinancing date
- Scheduled maturity date
- Payment history
- Voluntary additional payments
- Remaining balance
- Final resolution
- Jubilee date, when applicable

## Optional Plugin Modules

Optional plugins may extend JubileeLoan without changing the mandatory rules of the core specification.

### Income Verification Plugin

Provides optional verification of borrower income for administrative or reporting purposes.

Income verification must not be used to increase the required scheduled payment under the core specification.

### Loan Servicer Integration Plugin

Connects JubileeLoan with external loan servicing systems.

Supported functionality may include:

- Balance synchronization
- Payment synchronization
- Loan-status synchronization
- Payment-history imports
- Automated reporting

### Payment Processing Plugin

Provides integration with payment processors and financial institutions for scheduled and voluntary payments.

### Government Loan Integration Plugin

Provides adapters for participating government education-loan systems and databases.

### Private Loan Integration Plugin

Provides adapters for participating private education-loan systems.

### Verification and Audit Plugin

Provides independent verification of:

- Eligibility
- Repayment duration
- One-time interest calculation
- Payment preservation
- Remaining balance
- Term expiration
- Debt-jubilee execution

### Notification Plugin

Provides borrower notifications for:

- Qualification
- Refinancing approval
- Payment processing
- Remaining balance
- Approaching maturity
- Final loan satisfaction
- Debt jubilee

### Reporting Plugin

Generates aggregate reports for participating institutions without changing the deterministic rules of the core specification.

### API Integration Plugin

Provides standardized APIs for connecting JubileeLoan to financial institutions, loan servicers, education-financing platforms, and compatible systems.

### Identity and Authentication Plugin

Provides optional authentication and identity verification services for borrowers, loan originators, servicers, and administrators.

### Data Export Plugin

Provides standardized exports of loan records, payment histories, refinancing records, and final debt-resolution records.

## Plugin Requirements

Optional plugins must not alter the fundamental JubileeLoan rules.

A plugin must not:

- Increase the 1% total-loan interest charge.
- Convert the one-time charge into annual interest.
- Add compounding interest.
- Increase the required scheduled payment.
- Extend the maximum 10-year term.
- Remove the debt-jubilee requirement.
- Reset the original 15-year repayment history.
- Impose a prepayment penalty.
- Create an indefinite repayment state.
- Override deterministic core-module outcomes.

Plugins may provide additional functionality, integrations, interfaces, verification, or reporting while leaving the core specification unchanged.

## Deterministic Terminal Conditions

Every JubileeLoan agreement must eventually reach one of two final states.

### Satisfied

The outstanding balance reaches zero before or at the end of the maximum 120-month repayment period.

### Jubilee

The maximum 120-month repayment period expires while an eligible balance remains. The loan originator must declare the remaining eligible balance a debt jubilee and permanently extinguish it.

There is no permitted indefinite repayment state.

## Implementation Principles

JubileeLoan implementations should follow these principles:

- **Deterministic:** Identical inputs produce identical outcomes.
- **Transparent:** Core calculations and state transitions can be independently verified.
- **Finite:** The refinancing agreement has an absolute maximum duration.
- **Payment-preserving:** The borrower's existing payment becomes the scheduled refinancing payment.
- **Borrower-controlled acceleration:** Borrowers may voluntarily pay more.
- **Fixed financing charge:** The interest charge is exactly 1% of the total refinanced loan balance and is assessed once.
- **No compounding:** The 1% charge does not recur or compound.
- **Non-punitive:** No prepayment penalties or refinancing-based payment increases.
- **Terminal:** Every qualifying refinancing reaches satisfaction or mandatory debt jubilee.
- **Modular:** Optional integrations and services remain separate from the core specification.
- **Vendor-neutral:** The specification is not dependent on a particular lender, servicer, financial institution, or technology provider.

## Example Deterministic Flow

A borrower enters JubileeLoan with a qualifying school loan that has exceeded 15 years in repayment.

The loan has a verified outstanding balance of $50,000 and an existing monthly payment of $500.

JubileeLoan calculates a one-time interest charge of 1% of the refinanced balance:

**$50,000 × 1% = $500**

The total refinancing obligation becomes $50,500.

The borrower's existing $500 monthly payment remains the scheduled payment.

The borrower may continue paying $500 per month or voluntarily increase the payment to accelerate repayment.

The refinancing cannot be extended beyond 120 months.

If the balance reaches $0 before the end of the 120-month period, the loan is marked **SATISFIED**.

If an eligible balance remains when the 120-month period expires, the remaining balance is declared a **DEBT JUBILEE** and permanently extinguished.  

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
  - [https://roxanneardary.com/jubileeloan/](https://roxanneardary.com/jubileeloan/)  

---

## License & Notice Requirements

JubileeLoan is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.
By contributing to any Open Arsenal project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.
- JubileeLoan specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.
  Any update that adds new contributors or modifies attribution should also update `notice.md`.
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
