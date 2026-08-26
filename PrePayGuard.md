# PrePayGuard Specification
**Don't Let the Deadline Decide.**
- HTML Mirror:  [https://roxanneardary.com/prepayguard-specification/](https://roxanneardary.com/prepayguard-specification/)  

---

PrePayGuard is an open source AI specification for proactive payment coordination, payment timeliness, account balance protection, overdraft prevention, bounced-check protection, and human-controlled financial automation.

PrePayGuard is designed to identify payment obligations early, monitor bills and statements, establish safe payment timelines, coordinate funds across authorized accounts, provide advance warnings, and verify that payments are successfully completed.

The system is designed around two primary objectives:

- Ensure there is enough time to initiate and process every payment before it becomes late.
- Ensure there is enough money in the correct account to cover every payment without causing an overdraft, bounced check, or other funding failure.

## Purpose

PrePayGuard moves payment management from reactive reminders to proactive payment coordination.

The system should continuously determine:

- What payments are coming due.
- Whether the required bill or statement has arrived.
- Whether the amount and due date are known.
- Whether the information has been verified.
- Which authorized account should fund the payment.
- Whether sufficient funds will exist when the payment occurs.
- Whether sufficient processing time remains.
- Whether user approval is required.
- When action must occur.
- Whether the payment was actually initiated.
- Whether the payment was successfully completed.
- Whether any failure requires immediate recovery.

The system should identify problems while there is still enough time and financial flexibility to resolve them.

## Design Principles

- Advance warning is preferred over last-minute notification.
- The system must work backward from the actual payment due date.
- Payment processing time must be treated as part of the payment deadline.
- Account funding must be evaluated before payment execution.
- Current balance must not automatically be treated as unrestricted available funds.
- Outstanding checks must be treated as future financial commitments.
- Expected deposits must not be treated as guaranteed funds.
- Missing statements must become actionable exceptions.
- AI-generated financial information must remain distinguishable from verified information.
- Consequential financial actions must require appropriate human authorization.
- Users must remain in control of their money and payment policies.
- The system must fail safely rather than silently.
- Important financial decisions should be explainable.
- Important financial events should be auditable.
- Local-first operation should be supported.
- Vendor lock-in should not be required.
- External integrations should be modular and replaceable.
- The system must not knowingly create an overdraft or bounced check without applicable user authorization.
- The system must not wait until the due date to determine whether a payment can safely be completed.

---

## Core Modules

### Payment Obligation Module

The Payment Obligation Module maintains the canonical record for every recurring and one-time payment obligation.

The module should track:

- Creditor
- Merchant
- Service provider
- Account
- Invoice
- Statement
- Invoice number
- Statement number
- Billing frequency
- Billing cycle
- Statement closing date
- Expected statement date
- Statement availability date
- Invoice date
- Payment due date
- Minimum payment
- Statement balance
- Current balance
- Payment amount
- Currency
- Payment method
- Preferred payment account
- Backup payment account
- Processing time
- Safe payment initiation date
- User approval deadline
- Warning thresholds
- Payment status
- Payment confirmation
- Recurrence rules
- Source documents
- Source emails
- Confidence level
- Verification status
- User approval status
- Audit history

The system must distinguish between:

- Expected amount
- AI-extracted amount
- Source-confirmed amount
- User-entered amount
- User-approved amount
- Payment amount
- Actually paid amount
- Creditor-confirmed amount

### Universal Bill and Statement Ingestion Module

The Universal Bill and Statement Ingestion Module provides format-independent ingestion of financial documents.

Supported inputs may include:

- PDF
- Scanned PDF
- Photograph
- Screenshot
- Image
- HTML
- Plain text
- CSV
- Spreadsheet
- Digital invoice
- Electronic statement
- Receipt
- Email attachment
- Downloaded document
- Local file
- Connected document storage
- Connected creditor portal
- User-entered information
- Financial API data

The module should support:

- OCR
- Document classification
- Table extraction
- Entity extraction
- Date recognition
- Currency recognition
- Invoice recognition
- Statement recognition
- Recurring-obligation recognition
- Payment-instruction recognition
- Confidence scoring

Original source material should be retained or referenced whenever practical.

Every extracted financial field should be traceable to its source.

### Email Bill Intelligence Module

The Email Bill Intelligence Module monitors authorized email sources for payment-related communications.

It should detect:

- New bills
- New statements
- Invoices
- Payment reminders
- Due-date notices
- Past-due notices
- Payment confirmations
- Failed payments
- Returned payments
- Autopay notifications
- Billing-cycle notifications
- Rate changes
- Amount changes
- Due-date changes
- Payment-method changes
- New creditors
- Account changes
- Missing statements
- Statement availability notifications

The module should distinguish actionable financial messages from informational messages.

Relevant emails should be associated with existing obligations whenever possible.

New obligations should be created only when the system has sufficient evidence or obtains appropriate human confirmation.

### Statement Cycle Intelligence Module

The Statement Cycle Intelligence Module learns recurring billing and statement patterns.

It should track:

- Historical closing dates
- Historical statement arrival dates
- Historical due dates
- Typical statement availability windows
- Billing-cycle frequency
- Deviations from historical patterns

If a statement normally closes on the 24th and normally arrives within three days, the system should establish a monitoring window around that cycle.

For example:

- Statement closing date: 24th
- Expected statement window: 24th through 27th
- Missing-statement checkpoint: 27th
- Payment due date: configured creditor due date
- Safe payment initiation date: calculated backward from the due date

If the expected statement is missing, the system should ask the user whether the statement was received.

The system must distinguish learned expectations from confirmed facts.

### Financial Data Extraction Module

The Financial Data Extraction Module identifies financial information from bills, statements, invoices, and related communications.

It should extract:

- Creditor
- Account identifier
- Invoice number
- Statement number
- Statement date
- Closing date
- Due date
- Amount due
- Minimum payment
- Statement balance
- Current balance
- Previous balance
- Fees
- Interest
- Taxes
- Credits
- Payment instructions
- Payment method
- Payment address
- Electronic payment information

Each extracted field should include:

- Source
- Extraction method
- Confidence
- Verification status

Conflicting or uncertain values must be presented for human review.

### AI-Assisted Data Entry Module

The AI may prepare financial records from extracted information.

It may:

- Populate bill records
- Populate statement records
- Enter amounts
- Enter due dates
- Enter creditor information
- Enter invoice numbers
- Enter statement numbers
- Create recurring payment records
- Update existing payment records

The system must clearly identify AI-generated entries.

Human-in-the-loop approval should be available before consequential financial information becomes authoritative.

### Payment Timeline Engine

The Payment Timeline Engine determines when action must occur.

The engine should calculate:

- Creditor due date
- Processing deadline
- Safe payment initiation date
- User review deadline
- User approval deadline
- Statement availability deadline
- Funding deadline
- Transfer deadline
- Confirmation checkpoint
- Recovery deadline

Conceptually:

Safe Payment Initiation Date = Creditor Due Date - Processing Time - Safety Buffer

User Approval Deadline = Safe Payment Initiation Date - User Review Time

The actual calculation should account for:

- Payment method
- ACH processing
- Electronic transfers
- Card payments
- Check delivery
- Bank processing
- Weekends
- Holidays
- Bank cutoff times
- Transfer processing
- User review time
- Failure recovery time

The system must not assume that initiating a payment on the creditor's due date is safe.

### Advance Warning Module

The Advance Warning Module provides progressively earlier and more urgent notifications.

Warning states may include:

- Payment awareness
- Statement expected
- Statement received
- Statement missing
- Amount awaiting verification
- Account awaiting selection
- Payment preparation required
- Approval required
- Payment deadline approaching
- Payment initiation deadline
- Payment processing
- Confirmation required
- Payment failed
- Recovery required
- Potentially late

Warning intervals should be configurable.

The system should provide enough warning for the user to correct problems rather than merely notifying the user when a problem has already become urgent.

### Bank Account Coordination Module

The Bank Account Coordination Module coordinates payment obligations with authorized financial accounts.

The system should maintain account profiles containing:

- User-defined account name
- Institution
- Account type
- Limited account identifier
- Permitted payment types
- Permitted creditors
- Preferred use
- Backup status
- Protected minimum balance
- Authorization status
- Applicable account rules

When no approved account is available, the system must ask the user which authorized account should be used.

The system must not infer permission to use an account solely because it was previously used.

### Account Rules Module

Users should be able to define rules such as:

- Always use a specific account for a creditor.
- Use a preferred account unless insufficient funds exist.
- Ask before using a backup account.
- Never use a specific account for a particular payment.
- Require approval for payments above a specified amount.
- Require approval when a payment amount changes.
- Require approval for a new creditor.
- Require approval for a new payment account.
- Maintain a minimum account reserve.
- Never automatically initiate payments.
- Permit automatic payment execution only within defined limits.

Rules must be explicit, reviewable, auditable, and revocable.

### Balance Intelligence Module

The Balance Intelligence Module monitors financial resources against future obligations.

It should account for:

- Current balance
- Available balance
- Pending transactions
- Scheduled payments
- Automatic payments
- Outstanding checks
- Expected withdrawals
- Expected deposits
- Pending transfers
- Protected reserves
- Committed funds

The system must distinguish between current balance and projected available balance.

Conceptually:

Projected Balance = Available Funds + Confirmed Incoming Funds - Committed Payments - Expected Withdrawals

Uncertain incoming funds should be treated conservatively.

### Protected Minimum Balance Module

Users should be able to establish protected reserves for accounts.

A reserve may be:

- Fixed dollar amount
- Percentage of balance
- Account-specific
- Temporary
- Recurring
- Rule-based

The system should treat the protected amount as unavailable for ordinary payment distribution unless the user explicitly authorizes an override.

The system should warn before a payment would violate the protected reserve.

### Never Overdraft Module

The Never Overdraft Module is a core financial safety component.

Its objective is to prevent:

- Overdrafts
- Insufficient-funds events
- Returned electronic payments
- Returned checks
- Bounced checks
- Payment failures caused by insufficient funds

The module should continuously calculate projected account balances.

It should detect risks caused by:

- Upcoming payments
- Multiple payments
- Outstanding checks
- Pending transactions
- Unexpected withdrawals
- Delayed deposits
- Delayed transfers
- Payment timing collisions
- Protected reserves

The system should warn while corrective action is still possible.

It must not knowingly initiate a payment that will cause an account to become overdrawn without applicable user authorization.

### Check Protection Module

The Check Protection Module tracks checks that have been written but have not yet cleared.

Each check may include:

- Check number
- Payee
- Amount
- Date written
- Account
- Expected clearing date
- Actual clearing date
- Status
- Source
- User confirmation

Outstanding checks must be treated as future financial commitments.

The system should include outstanding checks in projected account balances.

It should detect when an outstanding check could conflict with another scheduled payment.

If check status is uncertain, the system should ask the user whether the check should continue to be treated as outstanding.

### Payment Distribution Module

The Payment Distribution Module coordinates multiple obligations across multiple accounts.

It should calculate:

- Payment account
- Payment amount
- Payment date
- Resulting balance
- Protected reserve
- Funding requirement
- Transfer requirement
- Payment collision
- Alternative account availability

The system should identify when an account has sufficient total funds but insufficient funds for its assigned obligations.

Total household or organizational funds must not automatically be treated as interchangeable.

### Payment Collision Module

The Payment Collision Module identifies multiple financial commitments competing for the same funds.

It should detect:

- Multiple payments on the same date
- Multiple payments within the same processing period
- Checks competing with electronic payments
- Automatic payments competing with manual payments
- Transfers competing with outgoing payments
- Payments exceeding available funds
- Payments violating protected reserves

The system should consolidate related conflicts into an actionable funding warning.

### Payment Priority Module

Users may establish payment priorities.

Possible categories include:

- Housing
- Utilities
- Insurance
- Taxes
- Debt
- Payroll
- Business obligations
- Essential services
- Discretionary services
- Subscriptions

The system must not independently determine payment priorities without an applicable user rule.

When a funding shortage occurs and no rule determines the appropriate action, the system should present the user with available choices and their projected consequences.

### Inter-Account Transfer Module

The Inter-Account Transfer Module coordinates authorized transfers between accounts.

It should determine:

- Source account
- Destination account
- Transfer amount
- Transfer initiation date
- Expected arrival date
- Processing buffer
- Resulting balances
- Protected reserves
- Downstream payment effects

The system must account for:

- Processing time
- Weekends
- Holidays
- Bank cutoff times
- Transfer type

The system should warn when a transfer must occur by a specific date to preserve payment safety.

### Deposit Coordination Module

The Deposit Coordination Module monitors expected incoming funds where authorized.

Possible deposit types include:

- Payroll
- Recurring income
- Pension
- Government payment
- Transfers
- Other user-defined deposits

Expected deposits must remain distinguishable from confirmed deposits.

The system should not rely on an unconfirmed deposit as the sole basis for authorizing a payment that could otherwise fail.

If an expected deposit does not arrive, the system should immediately recalculate payment and balance risk.

### Payment Preparation Module

The Payment Preparation Module prepares a payment without necessarily executing it.

A payment-ready record should include:

- Creditor
- Amount
- Due date
- Safe initiation date
- Payment account
- Payment method
- Reference information
- Funding status
- User authorization
- Risk status

The system must distinguish:

- Prepared
- Approved
- Scheduled
- Initiated
- Processing
- Completed
- Confirmed
- Failed

### Human-in-the-Loop Module

Human approval is a foundational component.

The system should request user input when:

- A new bill is detected.
- A new creditor is detected.
- A new account is proposed.
- A payment amount is uncertain.
- A payment amount materially changes.
- A due date is uncertain.
- A payment method changes.
- A payment account changes.
- A payment exceeds a user-defined threshold.
- A backup account is required.
- A funding conflict occurs.
- A payment timeline becomes unsafe.
- AI confidence is low.
- Conflicting source information exists.

The user should be able to approve:

- Amount
- Due date
- Payment account
- Payment method
- Payment date
- Transfer
- Recurrence rule
- Automation policy

Approval events must be recorded.

### Payment Execution Module

Payment execution should be an optional module separate from the core intelligence system.

It may integrate with:

- Banks
- Credit unions
- Bill-pay systems
- Payment processors
- Creditor portals
- ACH providers
- Authorized electronic payment systems

Execution modules must respect the user's authorization policies.

The core specification must remain functional without direct payment execution.

### Payment Confirmation Module

The Payment Confirmation Module verifies that a payment actually occurred.

Confirmation sources may include:

- Bank transactions
- Creditor confirmations
- Payment processors
- Email confirmations
- Receipts
- Transaction identifiers
- User confirmation

A payment must not be classified as confirmed merely because it was scheduled.

### Failed Payment Recovery Module

The system should detect:

- Insufficient funds
- Returned payments
- Rejected payments
- Invalid payment information
- Expired payment methods
- Creditor-side failures
- Failed transfers
- Missing confirmations

After a failure, the system must recalculate the remaining time available for recovery.

It should identify:

- Alternative authorized accounts
- Alternative payment methods
- Transfer opportunities
- Remaining processing time
- Recovery deadlines

The system should escalate when the remaining recovery window becomes limited.

### Duplicate Payment Protection Module

The system should identify potential duplicate payments by comparing:

- Creditor
- Invoice number
- Statement number
- Amount
- Due date
- Payment date
- Payment account
- Transaction identifier
- Payment history

Potential duplicate payments should require human review unless an applicable automation rule exists.

### Change Detection Module

The Change Detection Module compares current financial documents against historical information.

It should detect:

- Amount changes
- Due-date changes
- Minimum-payment changes
- New fees
- Interest changes
- Billing-cycle changes
- Payment-method changes
- Account changes
- Creditor changes
- New recurring charges
- Discontinued charges
- Unusual charges

Material changes should trigger user review.

### Financial Forecasting Module

The Financial Forecasting Module provides forward-looking financial visibility.

It may forecast:

- Upcoming payment obligations
- Projected account balances
- Funding shortages
- Protected reserve violations
- Payment collisions
- Transfer requirements
- Expected deposits
- Periods of increased payment risk

Predictions must remain distinguishable from confirmed financial information.

### Exception Management Module

The system must explicitly manage unresolved conditions.

Exceptions may include:

- Missing statement
- Missing invoice
- Unreadable document
- Conflicting amount
- Conflicting due date
- Unknown creditor
- Unknown account
- Unknown payment method
- Unexpected charge
- Unexpected withdrawal
- Missing deposit
- Failed transfer
- Missing payment confirmation
- Insufficient funds
- Overdraft risk
- Bounced-check risk
- Duplicate payment risk
- Insufficient processing time

Exceptions must never be silently converted into assumptions.

### Explainability Module

The AI should explain why it has generated a recommendation, warning, or request.

Explanations should identify:

- Relevant facts
- Source documents
- Source emails
- User rules
- Calculated deadlines
- Processing assumptions
- Balance assumptions
- Confidence levels
- Projected consequences

Example:

Your statement normally closes on the 24th and arrives within three days. This month's statement has not been detected. Your payment is due on the 18th and the selected payment method requires processing time. Please confirm whether the statement has been received so the payment timeline can be maintained.

### Rules and Policy Module

Users should be able to configure:

- Warning periods
- Processing buffers
- Safety buffers
- Protected reserves
- Approval thresholds
- Account preferences
- Creditor rules
- Payment priorities
- Notification channels
- Escalation rules
- Automation permissions
- Statement monitoring windows
- Transfer rules
- Duplicate-payment rules
- Recovery rules

Policies must be reviewable and revocable.

### Automation Control Module

The system should support multiple automation levels:

- Notification only
- Analysis only
- Preparation only
- Approval required
- Limited automation
- Fully authorized automation within explicit user-defined limits

Automation policies should support:

- Maximum payment amount
- Permitted creditors
- Permitted accounts
- Permitted payment methods
- Required balance reserves
- Timing restrictions
- Frequency restrictions
- Approval requirements

Automation scope must never silently expand.

### Notification Module

The Notification Module should support replaceable notification channels.

Possible channels include:

- Application notifications
- Email
- SMS
- Push notifications
- Desktop notifications
- Calendar notifications
- Voice notifications

Notifications should clearly communicate:

- What requires attention
- Amount
- Due date
- Safe payment date
- Funding status
- Required action
- Risk
- Consequence of inaction

### Escalation Module

The Escalation Module increases urgency when required actions remain unresolved.

Possible escalation states include:

- Awareness
- Attention
- Action Required
- Urgent
- Critical

Escalation should occur when:

- Statements are missing
- Amounts remain unverified
- Accounts remain unselected
- Payments remain unapproved
- Funding becomes insufficient
- Transfers have not occurred
- Payment confirmations are missing
- A payment has failed
- Recovery time is decreasing
- A payment may become late

### Calendar Module

The Calendar Module may create:

- Statement expectation events
- Statement verification events
- Payment preparation events
- Approval deadlines
- Transfer deadlines
- Payment initiation deadlines
- Confirmation checkpoints

Calendar events should update automatically when payment timelines change.

### Audit and Provenance Module

The system should maintain an auditable history of significant events.

Audit events should identify:

- Source
- Timestamp
- Extracted information
- AI interpretation
- Confidence
- User modification
- User approval
- Account selection
- Payment preparation
- Payment scheduling
- Payment execution
- Payment confirmation
- Failure
- Recovery action
- Policy changes

Every financial field should maintain provenance whenever practical.

### Security Module

The Security Module should protect:

- Bank connections
- Email connections
- Payment credentials
- API tokens
- Financial documents
- Payment instructions
- User approvals
- Audit records

Security controls should include:

- Encryption
- Strong authentication
- Least-privilege access
- Credential isolation
- Tokenized account references
- Secure secrets management
- Redacted logs
- Permission boundaries

Raw financial credentials should never be stored in ordinary payment records.

### Privacy Module

The Privacy Module should support:

- Local processing
- Local document storage
- Local AI inference
- User-controlled retention
- User-controlled deletion
- Minimal third-party data exposure
- Explicit external-service authorization
- Separation of financial credentials from payment intelligence

The system should clearly identify information that leaves the local environment.

### Local-First Module

The system should support local-first operation.

Local functionality may include:

- Document processing
- OCR
- AI inference
- Payment timeline calculations
- Balance calculations
- Audit records
- Notification management
- Financial-data storage

Cloud services should be optional wherever practical.

### Interoperability Module

The system should support replaceable adapters for:

- Banks
- Credit unions
- Email providers
- Payment processors
- Bill-pay providers
- Creditor portals
- OCR engines
- AI models
- Databases
- Notification providers
- Calendar providers
- Document storage providers

No individual vendor should be required by the core specification.

---

## Optional Plugin Modules

Optional functionality should be implemented as replaceable plugins rather than requirements of the core system.

### Automatic Payment Plugin

Provides authorized automatic payment execution.

The plugin should respect:

- User authorization
- Payment limits
- Creditor restrictions
- Account restrictions
- Protected reserves
- Timing rules
- Approval requirements

### Automatic Transfer Plugin

Provides authorized automated transfers between accounts under explicit user-defined rules.

### Bank Balance Plugin

Connects to authorized financial institutions to retrieve:

- Balances
- Available balances
- Pending transactions
- Cleared transactions
- Deposits
- Withdrawals
- Transfers
- Check clearing information

### Email Provider Plugin

Connects to supported email providers for bill and statement monitoring.

### OCR Plugin

Provides specialized document and image recognition.

### AI Model Plugin

Allows implementations to use interchangeable AI models.

### Calendar Plugin

Connects to external calendar services.

### Notification Plugin

Provides additional notification channels.

### Credit Card Plugin

Provides specialized credit card statement, balance, due-date, and payment intelligence.

### Utility Bill Plugin

Provides specialized handling of variable utility bills and recurring utility statements.

### Subscription Monitoring Plugin

Identifies recurring subscriptions and detects changes in recurring charges.

### Invoice Management Plugin

Provides advanced invoice processing for individuals, businesses, contractors, and organizations.

### Business Finance Plugin

Provides separate business payment profiles, accounts, obligations, permissions, and approval workflows.

### Multi-User Approval Plugin

Supports multiple authorized users with different approval and account permissions.

### Cash Flow Forecasting Plugin

Provides advanced forecasting of income, expenses, payment obligations, and account balances.

### Income Monitoring Plugin

Monitors authorized expected income and deposit schedules.

### Voice Assistant Plugin

Provides voice-based payment notifications and user interactions.

### Local AI Plugin

Provides local language models and local document-processing models.

### Advanced Financial Agent Plugin

Provides additional autonomous coordination while remaining constrained by explicit user policies, account permissions, financial limits, and human approval requirements.

### Financial Anomaly Detection Plugin

Detects unusual financial activity, unexpected charges, unexpected withdrawals, and deviations from historical patterns.

### Accounting Integration Plugin

Connects PrePayGuard with accounting systems and financial recordkeeping platforms.

### Tax Payment Plugin

Provides specialized tracking of tax obligations, payment deadlines, estimated payments, and funding requirements.

### Insurance Payment Plugin

Provides specialized monitoring of insurance premiums, renewal dates, statements, and payment requirements.

### Loan Payment Plugin

Provides specialized monitoring of loans, payment schedules, interest, principal, and payment deadlines.

---

## Payment State Model

Payment obligations should support explicit machine-readable states:

- Identified
- Awaiting Statement
- Statement Received
- Amount Extracted
- Awaiting Verification
- Verified
- Awaiting Account Selection
- Awaiting Approval
- Prepared
- Approved
- Scheduled
- Initiated
- Processing
- Completed
- Confirmed
- Failed
- Returned
- Canceled
- Exception
- Potentially Late

The system must never represent a payment as confirmed solely because it was prepared or scheduled.

## Account Risk States

Accounts should support explicit risk states:

- Funded
- Funded With Reserve Risk
- Funding Required
- Transfer Required
- Payment Collision
- Overdraft Risk
- Bounced Check Risk
- Payment Failure Risk
- Unknown Balance
- Reconciliation Required
- Critical

Risk states should drive notifications and escalation.

## Financial Safety Invariants

The implementation should enforce the following principles:

- Do not knowingly initiate a payment that will cause an overdraft.
- Do not knowingly cause an account to violate its protected reserve without authorization.
- Do not knowingly cause an outstanding check to bounce.
- Do not treat expected deposits as guaranteed funds.
- Do not treat current balance as unrestricted available funds.
- Do not treat a scheduled payment as completed.
- Do not treat AI extraction as human-approved financial information.
- Do not assume a missing statement has the same amount as a previous statement.
- Do not silently change a payment account.
- Do not silently change a payment amount.
- Do not silently delay a payment.
- Do not silently cancel a payment.
- Do not silently transfer funds.
- Do not silently override user financial policies.
- Do not knowingly create a payment collision.
- Do not wait until the due date to identify payment risk.
- Do not represent uncertain financial information as confirmed information.

## Funding Shortage Workflow

When projected funds are insufficient, the system should:

- Identify the shortage.
- Identify affected obligations.
- Identify the date on which the shortage occurs.
- Calculate the amount required.
- Identify authorized alternative accounts.
- Identify possible transfers.
- Calculate whether transfers can arrive in time.
- Identify user-approved payment priorities.
- Present available options.
- Explain the projected consequence of each option.
- Request human direction when required.
- Recalculate payment and balance safety after the decision.

## Payment Timeline Model

Every obligation should maintain a complete lifecycle:

Statement Expected

↓

Statement Received

↓

Information Extracted

↓

Information Verified

↓

Payment Account Confirmed

↓

Funding Confirmed

↓

Payment Prepared

↓

User Approval

↓

Safe Payment Initiation Deadline

↓

Payment Initiated

↓

Payment Processing

↓

Payment Confirmed

↓

Obligation Closed

The system should continuously monitor every stage.

## User Action Center

The system should provide a centralized queue for actions requiring human attention.

Actions may include:

- Review extracted amount
- Confirm due date
- Confirm statement
- Select payment account
- Approve payment
- Approve transfer
- Resolve missing statement
- Resolve conflicting information
- Review unexpected charge
- Resolve funding shortage
- Confirm outstanding check
- Review failed payment
- Confirm payment completion
- Approve automation rule

## Financial Safety Dashboard

The dashboard should provide a consolidated view of:

- Payments due soon
- Safe payment deadlines
- Statements expected
- Statements missing
- Payments awaiting approval
- Payments prepared
- Payments scheduled
- Payments processing
- Payments awaiting confirmation
- Account balances
- Projected balances
- Protected reserves
- Outstanding checks
- Pending transfers
- Expected deposits
- Funding shortages
- Overdraft risks
- Bounced-check risks
- Payment collisions
- Failed payments
- Critical exceptions

The highest-risk items should be displayed first.

## AI Agent Architecture

The AI agent should operate as a coordinator and guardian rather than an unrestricted financial actor.

The agent may:

- Observe
- Read
- Extract
- Classify
- Compare
- Calculate
- Forecast
- Warn
- Ask
- Prepare
- Coordinate
- Recommend
- Monitor
- Escalate
- Confirm

The agent may only perform consequential financial actions when the applicable user authorization and policy permit the action.

## Human Financial Authority

The user remains the final authority over:

- Payment amounts
- Payment accounts
- Transfers
- Payment execution
- Protected reserves
- Payment priorities
- Automation policies
- Financial exceptions

The AI should provide information, timing intelligence, recommendations, warnings, and preparation while preserving human authority.

## Core Objective

PrePayGuard should provide enough:

- Time
- Information
- Funding
- Account coordination
- Warning
- Verification
- Recovery opportunity

for every payment to be safely completed on time.

The system should protect against both major payment failures:

**Late Payment**

A payment is not initiated or processed in sufficient time.

**Funding Failure**

A payment causes or contributes to an overdraft, bounced check, returned payment, or other insufficient-funds event.

## Primary Principle

**Don't Let the Deadline Decide.**

PrePayGuard should identify the obligation before it becomes urgent, identify the information before it becomes necessary, identify the funding requirement before the payment is attempted, identify the correct account before funds need to move, and identify failures while there is still enough time to recover.

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
  - [https://roxanneardary.com/prepayguard/](https://roxanneardary.com/prepayguard/)  

---

## License & Notice Requirements

PrePayGuard is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to any Open Arsenal project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.
- PrePayGuard specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
