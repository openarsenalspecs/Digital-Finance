# Paystead
**AI Assistance. Human Control.**
- HTML Mirror: [https://roxanneardary.com/paystead-specification/](https://roxanneardary.com/paystead-specification/)  

---

Paystead is an AGPL-3.0+ licensed, locally hosted financial operations specification designed to provide users with a unified interface for managing authorized financial accounts, banking activity, bills, payments, statements, checks, and AI-assisted financial tasks.

Paystead uses a modular architecture in which core financial capabilities are provided by core modules and institution-specific integrations are provided through individual bank, credit union, biller, payment, and financial-service modules. Each supported bank must have its own dedicated integration module so that institution-specific authentication, account access, transaction handling, bill payment, transfer capabilities, statement retrieval, and other supported functions remain isolated from the core system.

## Specification Goals

Paystead is designed to:

- Provide a locally hosted alternative to fragmented online banking interfaces.
- Give users one consistent interface for multiple authorized financial institutions.
- Allow users to view and manage accounts from different banks through the same interface.
- Download, process, and display financial statements in a readable user interface.
- Support PDF, CSV, OFX, QFX, QIF, image-based, and other supported financial formats.
- Use AI to assist with financial information processing and authorized financial tasks.
- Allow users to authorize AI agents to perform supported banking operations.
- Require appropriate user authorization before financial actions are executed.
- Provide bill discovery, bill management, and bill payment capabilities.
- Connect with companies that accept online bill payments through supported integrations.
- Create and manage checks for authorized checking accounts.
- Maintain financial records, transaction history, payment history, and check registers.
- Preserve source information and distinguish source data from AI-generated interpretations.
- Provide detailed audit records for financial and AI activity.
- Keep the user's financial data locally controlled wherever technically possible.
- Avoid dependence on a single bank, financial institution, vendor, or payment provider.
- Provide an extensible architecture for additional financial institutions and services.

---

## Core Principles

### Local First

Paystead should operate primarily within an environment controlled by the user. Local storage, processing, document management, AI processing, and financial records should not require unnecessary transmission to third-party services.

External services may be used when required for banking, payment, authentication, biller, financial data, or other supported integrations.

### User Financial Control

The user remains the authority over their financial accounts and financial decisions.

AI may recommend, prepare, retrieve, organize, analyze, or execute authorized tasks, but Paystead must maintain configurable permission boundaries and approval requirements.

### Human Approval

Money-moving actions should require explicit user approval by default unless the user has intentionally configured an appropriate automation rule.

The system must clearly distinguish between:

- Proposed actions
- User-approved actions
- Submitted actions
- Completed actions
- Failed actions
- Rejected actions
- Reversed actions

### Modular Design

Core financial functionality must remain independent of individual financial institutions.

Bank-specific behavior must be implemented through individual bank modules.

Biller-specific behavior must be implemented through individual biller modules.

Payment-network-specific behavior must be implemented through individual payment modules.

Additional capabilities may be implemented through optional plugin modules.

### Financial Data Provenance

Paystead must preserve the relationship between original financial information and information derived from processing or AI.

The system should distinguish between:

- Original source documents
- Extracted information
- Normalized financial records
- AI classifications
- AI interpretations
- User corrections
- User-created records

### Auditability

Significant financial operations and AI actions must be recorded in an auditable history.

The audit system should record sufficient information to determine what happened, when it happened, which account was involved, which module performed the operation, whether the user approved the operation, and what result was returned.

---

## Core Modules

### Account Management Module

The Account Management Module provides a unified representation of the user's authorized financial accounts.

It must support:

- Checking accounts.
- Savings accounts.
- Money market accounts.
- Credit card accounts.
- Loan accounts.
- Other supported financial account types.
- Account balances.
- Available balances where supported.
- Pending transactions.
- Posted transactions.
- Account identifiers.
- Account ownership information.
- Institution information.
- Account status.
- Account permissions.
- Account-specific capabilities.

The module must maintain the relationship between each local account record and its corresponding external financial institution account.

### Bank Integration Module Framework

The Bank Integration Module Framework defines the common interface that all bank modules must implement.

Every supported bank must have its own dedicated bank module.

A bank module must encapsulate institution-specific functionality rather than placing institution-specific logic inside the Paystead core.

Bank modules may provide:

- Authentication.
- Authorization.
- Account discovery.
- Account balances.
- Transaction retrieval.
- Transaction synchronization.
- Statement retrieval.
- Transfer functionality.
- Bill payment functionality.
- Check-related functionality.
- Payment status retrieval.
- Account information.
- Institution-specific security requirements.
- Institution-specific confirmation workflows.
- Institution-specific error handling.
- Institution-specific transaction rules.
- Institution-specific limits.
- Institution-specific API behavior.

Bank modules must expose their supported capabilities to the core system so Paystead does not attempt to execute unsupported operations.

### Individual Bank Modules

Each supported bank must be implemented as a separate module.

Examples may include:

- Bank A Module.
- Bank B Module.
- Bank C Module.
- Credit Union A Module.
- Credit Union B Module.

Each bank module must maintain its own:

- Authentication implementation.
- API integration.
- Supported account types.
- Supported transaction operations.
- Supported payment operations.
- Statement retrieval methods.
- Transfer methods.
- Bank-specific configuration.
- Error handling.
- Security requirements.
- Capability declarations.

The core system must not assume that all banks provide identical functionality.

If a bank does not support a particular operation, the bank module must report that capability as unavailable rather than attempting to emulate or bypass the institution's restrictions.

### Account Switching Module

The Account Switching Module allows users to move between financial institutions without changing the primary Paystead interface.

Users must be able to:

- Select a financial institution.
- Select an account.
- Switch between checking accounts.
- Switch between savings accounts.
- Switch between other supported accounts.
- View institution-specific capabilities.
- Perform supported operations through the selected institution's module.

The interface should remain consistent while institution-specific functionality is exposed only when supported.

### Transaction Management Module

The Transaction Management Module provides a unified transaction interface across supported financial institutions.

It must support:

- Transaction retrieval.
- Transaction synchronization.
- Transaction search.
- Transaction filtering.
- Transaction sorting.
- Transaction categorization.
- Transaction notes.
- Transaction attachments.
- Transaction status.
- Pending and posted transaction separation.
- Transaction reconciliation.
- Duplicate detection.
- Transaction history.
- Transaction provenance.

AI may assist with transaction categorization and interpretation, but users must be able to review and correct AI-generated classifications.

### Statement Management Module

The Statement Management Module manages financial statements obtained from banks and other supported financial institutions.

It must support:

- Statement downloads.
- Statement storage.
- Statement indexing.
- Statement search.
- Statement date ranges.
- Statement account association.
- Statement archival.
- Statement retrieval from supported bank modules.
- User-uploaded statements.

Statements must retain their original source files whenever technically possible.

### Statement Import Module

The Statement Import Module processes locally stored financial documents and structured financial files.

Supported formats should include:

- PDF.
- CSV.
- OFX.
- QFX.
- QIF.
- Common spreadsheet formats where appropriate.
- Image-based statements.
- Scanned statements.
- Additional formats through plugins.

The module must detect the input format and select an appropriate extraction method.

### Statement Transcription Module

The Statement Transcription Module converts financial statements into readable structured information.

It should support:

- PDF text extraction.
- Table extraction.
- OCR.
- Transaction recognition.
- Date recognition.
- Merchant recognition.
- Amount recognition.
- Debit and credit identification.
- Balance recognition.
- Statement period recognition.
- Account identification.
- Page and source references.
- Extraction confidence levels.

Extracted information must remain distinguishable from the original document.

### Financial Reconciliation Module

The Financial Reconciliation Module compares imported or extracted financial information against account records.

It should identify:

- Matching transactions.
- Potential duplicate transactions.
- Missing transactions.
- Amount discrepancies.
- Date discrepancies.
- Balance discrepancies.
- Unrecognized transactions.
- Statement-to-account inconsistencies.

Users must be able to approve, reject, or correct reconciliation suggestions.

### Financial Intelligence Module

The Financial Intelligence Module provides AI-assisted analysis of financial information.

It may assist with:

- Transaction classification.
- Merchant identification.
- Spending summaries.
- Recurring payment detection.
- Subscription identification.
- Bill identification.
- Unusual transaction detection.
- Statement summaries.
- Financial document interpretation.
- Account activity explanations.
- Reconciliation assistance.
- Payment preparation.
- Financial task planning.

AI-generated information must be clearly identified as AI-generated.

### AI Financial Agent Module

The AI Financial Agent Module allows users to issue natural-language financial commands.

Examples include:

- "Show me all transactions from this month."
- "Find my electric bill."
- "Download my latest statement."
- "Prepare my electric bill payment."
- "Create a check for this invoice."
- "Show me which bills are due this week."
- "Find recurring charges across all my banks."
- "Move $500 from my checking account to savings."

The agent must translate user requests into explicit actions and must verify required permissions before executing them.

### AI Authorization Module

The AI Authorization Module controls what the AI agent is permitted to do.

Permissions should be configurable by:

- Institution.
- Account.
- Operation.
- Payment type.
- Dollar amount.
- Biller.
- Frequency.
- Automation rule.
- User identity.

Examples of permissions include:

- Read account information.
- Download statements.
- Read transactions.
- Categorize transactions.
- Prepare payments.
- Submit payments.
- Create checks.
- Print checks.
- Initiate transfers.
- Execute recurring payments.

Sensitive financial operations must require appropriate authorization.

### AI Action Preview Module

Before executing sensitive financial operations, Paystead should present a human-readable action preview.

The preview should include:

- Account.
- Institution.
- Payee.
- Amount.
- Date.
- Payment method.
- Requested action.
- Destination.
- Expected processing date where available.
- Applicable fees where available.
- AI-generated reasoning or explanation where appropriate.
- Required authorization.

The user must be able to approve or reject the proposed action.

### Bill Management Module

The Bill Management Module provides centralized management of bills across financial institutions.

It should support:

- Biller identification.
- Biller account numbers.
- Due dates.
- Amounts due.
- Minimum payments.
- Recurring bills.
- Payment history.
- Payment methods.
- Payment status.
- Payment scheduling.
- Bill reminders.
- Bill documentation.
- Multiple payment sources.

### Biller Integration Module Framework

The Biller Integration Module Framework defines the common interface for connecting Paystead to companies that accept online payments.

Biller modules may provide:

- Account verification.
- Balance retrieval.
- Bill retrieval.
- Due-date retrieval.
- Payment submission.
- Payment confirmation.
- Payment status.
- Autopay information.
- Payment history.

Each supported biller should have its own dedicated module where direct integration is required.

### Individual Biller Modules

Each supported company that provides a direct online payment integration may have its own dedicated biller module.

Examples include modules for:

- Electric utilities.
- Water utilities.
- Internet providers.
- Telecommunications companies.
- Insurance companies.
- Credit card providers.
- Loan providers.
- Government payment services.
- Property-related service providers.
- Other participating billers.

Biller modules must only expose capabilities supported by the connected company.

### Bank Bill Pay Module

The Bank Bill Pay Module allows Paystead to use supported bank-provided bill payment functionality.

It should support:

- Payee selection.
- Payment amount.
- Payment date.
- Funding account.
- Payment scheduling.
- Payment cancellation where supported.
- Payment status.
- Confirmation records.

The module must respect the capabilities and restrictions of the selected bank module.

### Payment Management Module

The Payment Management Module provides a unified representation of payments.

It must track:

- Payment source.
- Payment destination.
- Payment amount.
- Payment date.
- Requested date.
- Processing date.
- Payment method.
- Payment status.
- Confirmation information.
- Cancellation status.
- Failure information.
- Related bill.
- Related account.
- Related audit record.

### Transfer Module

The Transfer Module provides transfers between authorized accounts where supported.

It should support:

- Internal transfers.
- External transfers where supported.
- Transfer scheduling.
- Transfer cancellation where supported.
- Transfer status.
- Transfer history.
- Transfer confirmation.

The module must not assume that every institution supports every transfer type.

### Check Creation Module

The Check Creation Module allows users to create checks for authorized checking accounts.

It must support:

- Checking account selection.
- Payer information.
- Financial institution information.
- Routing information.
- Account information.
- Check number management.
- Payee information.
- Check amount.
- Written amount.
- Date.
- Memo.
- Signature configuration where supported.
- Check layout.
- Check register integration.
- Check status tracking.
- Check printing.

The module must only create checks for checking accounts the user is authorized to operate.

Check generation must use the appropriate information associated with the selected checking account and must support applicable check formatting and banking requirements.

### Check Register Module

The Check Register Module maintains a record of created checks.

It should track:

- Check number.
- Account.
- Payee.
- Amount.
- Date.
- Memo.
- Creation status.
- Printing status.
- Issuance status.
- Clearing status.
- Void status.
- Related transaction.
- Related payment.
- Audit record.

### Payment Scheduling Module

The Payment Scheduling Module manages future financial actions.

It should support:

- One-time payments.
- Recurring payments.
- Scheduled transfers.
- Scheduled checks.
- Bill due dates.
- Payment reminders.
- User-defined automation rules.
- Payment approval requirements.

### Financial Calendar Module

The Financial Calendar Module provides a unified calendar for:

- Bills.
- Payment due dates.
- Scheduled payments.
- Scheduled transfers.
- Check dates.
- Statement periods.
- Account activity.
- Recurring transactions.

### Financial Search Module

The Financial Search Module provides unified search across the user's local financial records.

It should search:

- Accounts.
- Transactions.
- Statements.
- Bills.
- Payments.
- Checks.
- Payees.
- Financial documents.
- Audit records.

AI-assisted natural-language search may allow users to ask questions such as:

- "How much did I spend on utilities this year?"
- "Find every payment to this company."
- "Show me all checks over $500."
- "Which bills are due next week?"

### Financial Document Module

The Financial Document Module stores financial documents associated with accounts and transactions.

It should support:

- Statements.
- Invoices.
- Receipts.
- Payment confirmations.
- Check records.
- Tax documents.
- User-uploaded financial records.

Documents should be associated with relevant accounts, transactions, bills, or payments where possible.

### Notification Module

The Notification Module provides alerts for:

- Upcoming bills.
- Failed payments.
- Payment confirmations.
- Account synchronization failures.
- Unusual activity.
- Low balances.
- Statement availability.
- AI action requests.
- Approval requests.
- Authentication requirements.

### Audit Module

The Audit Module maintains a complete history of significant Paystead operations.

Audit records should include:

- Timestamp.
- User or agent identity.
- Account.
- Institution.
- Module.
- Requested operation.
- Authorization state.
- User approval.
- Action performed.
- Result.
- Error information.
- External confirmation.
- Related financial record.

Audit records should be protected against unauthorized modification.

### Security Module

The Security Module provides security controls for local financial data and connected financial services.

It should support:

- Encryption at rest.
- Secure credential storage.
- Session management.
- Access control.
- User authentication.
- Multi-factor authentication support.
- Permission management.
- Secure connector communication.
- Credential isolation.
- Sensitive-data redaction.
- Security event logging.

Paystead should minimize exposure of banking credentials to AI systems and should prefer tokenized or delegated authorization mechanisms when supported.

### Permission Module

The Permission Module controls access to financial capabilities.

Permissions should be granular enough to distinguish between:

- Viewing.
- Downloading.
- Creating.
- Preparing.
- Approving.
- Submitting.
- Modifying.
- Canceling.
- Printing.
- Automating.

### Automation Module

The Automation Module allows users to define rules for recurring financial tasks.

Automation rules may specify:

- Account.
- Biller.
- Payment type.
- Amount limits.
- Date limits.
- Frequency.
- Required approval.
- Allowed AI actions.

Automation must remain subject to the permissions defined by the user.

### Data Export Module

The Data Export Module allows users to export their financial records.

Supported exports may include:

- CSV.
- OFX.
- QFX.
- QIF.
- JSON.
- PDF reports.
- Other supported formats.

Exports should preserve transaction history and relevant provenance information where practical.

### Data Backup Module

The Data Backup Module provides secure backup and restoration of local financial information.

It should support:

- Encrypted backups.
- User-controlled backup destinations.
- Backup verification.
- Restore operations.
- Backup versioning.
- Selective restoration.

### Integration Capability Module

The Integration Capability Module allows the core system to determine which operations are supported by each connected institution.

Capabilities may include:

- Account access.
- Transactions.
- Statements.
- Bill pay.
- Transfers.
- Check services.
- Payment scheduling.
- Payment status.
- Document retrieval.

The interface must not present unsupported functions as available.

---

## Optional Plugin Modules

### Accounting Plugin

Provides integrations with accounting systems for:

- Transaction synchronization.
- Account reconciliation.
- Expense classification.
- Financial reporting.
- Journal entry assistance.

### Tax Plugin

Provides tax-related organization and reporting capabilities using locally stored financial information.

### Investment Plugin

Provides optional investment account integrations for:

- Holdings.
- Transactions.
- Balances.
- Investment statements.
- Portfolio reporting.

### Loan Management Plugin

Provides:

- Loan balances.
- Payment schedules.
- Interest information.
- Payment history.
- Loan document management.

### Credit Monitoring Plugin

Provides optional integrations for monitoring supported credit information.

### Payroll Plugin

Provides optional payroll integrations for supported users and organizations.

### Invoice Plugin

Provides:

- Invoice creation.
- Invoice tracking.
- Payment matching.
- Receivable management.

### Receipt Plugin

Provides receipt capture, OCR, classification, and transaction association.

### Mobile Plugin

Provides an optional mobile interface for users who want remote access to their locally hosted Paystead environment.

### Cloud Synchronization Plugin

Provides optional encrypted synchronization between user-controlled Paystead installations.

Cloud synchronization must remain optional and must not be required for the core system.

### Advanced AI Plugin

Provides optional advanced AI capabilities including:

- Financial planning.
- Scenario analysis.
- Cash-flow forecasting.
- Recurring expense analysis.
- Financial anomaly detection.
- Automated financial organization.

### Financial Advisor Plugin

Provides controlled access for authorized financial professionals.

The plugin must use explicit user permissions and must not provide unrestricted access to financial accounts.

### Household Management Plugin

Provides optional multi-user household functionality.

It may support:

- Shared accounts.
- Shared bills.
- Individual permissions.
- Household financial dashboards.
- Approval workflows.

### Business Finance Plugin

Provides optional business-oriented capabilities including:

- Business checking.
- Vendor payments.
- Business bills.
- Invoices.
- Expense management.
- Business financial reporting.

---

## Connector Standards

Paystead should use established financial data and payment standards wherever supported.

Potential standards and interfaces may include:

- OFX.
- Open Banking APIs.
- OAuth.
- Financial institution APIs.
- ACH-related interfaces.
- ISO 20022-compatible financial messaging where applicable.
- Institution-specific APIs.
- Biller-specific APIs.
- Other authorized financial data and payment interfaces.

Standards support must remain modular so the core system does not depend on a single financial interoperability standard.

## Authentication and Authorization

Paystead must support institution-specific authentication requirements.

Where supported, connectors should prefer:

- OAuth.
- Delegated authorization.
- Token-based authentication.
- Multi-factor authentication.
- Hardware security mechanisms.
- Short-lived authorization sessions.

Paystead must not attempt to circumvent security controls, authentication requirements, fraud controls, transaction limits, or access restrictions imposed by a financial institution.

Where a financial institution requires interactive user authentication, Paystead must provide a secure mechanism for the user to complete that authentication.

## AI Browser and Session Automation

Where institution-supported APIs are unavailable, an optional connector may provide user-authorized browser automation where legally and technically permitted.

Browser automation must:

- Operate only within an authorized user session.
- Respect authentication requirements.
- Respect institution security controls.
- Never attempt to bypass CAPTCHA or other security mechanisms.
- Never defeat multi-factor authentication.
- Never evade access controls.
- Require additional user interaction when required by the institution.
- Record significant actions in the audit system.

The AI agent must not be granted unrestricted control over the user's financial environment.

## AI Safety Controls

AI financial actions must be constrained by explicit permissions.

The system should provide:

- Read-only mode.
- Prepare-only mode.
- Approval-required mode.
- Limited automation mode.
- User-defined transaction limits.
- Biller-specific limits.
- Account-specific permissions.
- Emergency disable controls.

The user must be able to disable AI financial actions without disabling access to their financial records.

## Privacy

Paystead should minimize collection and transmission of financial information.

The system should:

- Process data locally whenever practical.
- Minimize external AI data transmission.
- Provide user control over external AI providers.
- Allow local AI models where practical.
- Encrypt sensitive information.
- Avoid unnecessary third-party analytics.
- Provide clear data retention controls.
- Provide financial data deletion capabilities.

## Error Handling

Financial operations must use explicit states and must never assume that an operation succeeded merely because a request was submitted.

The system should distinguish between:

- Requested.
- Pending.
- Submitted.
- Confirmed.
- Completed.
- Failed.
- Rejected.
- Canceled.
- Reversed.
- Unknown.

Unknown states must be clearly presented to the user and must not be represented as successful transactions.

## Reconciliation and Duplicate Protection

Paystead should prevent duplicate financial actions where technically possible.

Before submitting a payment, transfer, or other financial action, the system should check for:

- Existing matching actions.
- Recent submissions.
- Duplicate payment requests.
- Duplicate checks.
- Conflicting scheduled actions.

Where the system cannot determine whether an action has already occurred, it must notify the user rather than automatically repeating the operation.

## User Interface

The Paystead interface should provide a consistent experience across institutions.

Primary interface areas should include:

- Dashboard.
- Accounts.
- Transactions.
- Statements.
- Bills.
- Payments.
- Transfers.
- Checks.
- Documents.
- Calendar.
- AI Assistant.
- Audit History.
- Settings.

Institution-specific capabilities should be presented dynamically based on the selected bank module.

## Bank Module Independence

Each bank module must be independently maintainable.

Updating one bank module must not require changes to unrelated bank modules.

A bank module should be replaceable without changing the user's normalized financial records.

When a bank changes its API, authentication system, statement format, or supported capabilities, the affected bank module should be updated independently.

## Data Portability

Users must be able to export their financial information without being locked into Paystead.

The system should provide mechanisms for exporting:

- Accounts.
- Transactions.
- Statements.
- Bills.
- Payments.
- Checks.
- Documents.
- Audit records.
- User-created financial classifications.

## Extensibility

The specification should allow developers to create additional modules without modifying the core financial model.

New modules may include:

- New banks.
- New credit unions.
- New billers.
- New payment services.
- New financial data providers.
- New statement formats.
- New accounting systems.
- New AI providers.
- New local AI models.
- New financial tools.

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
  - [https://roxanneardary.com/paystead/](https://roxanneardary.com/paystead/)  

---

## License & Notice Requirements

Paystead is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to any Open Arsenal project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.
- Paystead specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
