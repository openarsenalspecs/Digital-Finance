# FinAxis
**From Lending Idea to Compliance Framework.**
- HTML Mirror: [https://roxanneardary.com/finaxis-specification/](https://roxanneardary.com/finaxis-specification/)  

---

## Specification

FinAxis is an AI and LLM-ready, modular specification for building regulatory intelligence and compliance guidance systems for financial businesses engaged in lending. FinAxis is designed to help an upstart financial business understand applicable federal, state, and local laws, regulations, licensing requirements, disclosures, forms, lending restrictions, compliance obligations, and ongoing regulatory changes before and during the operation of a lending business.

FinAxis is designed as a decision-support and regulatory intelligence framework. It should provide source-verifiable information, identify unresolved questions, distinguish legal requirements from guidance and interpretation, and escalate matters requiring qualified legal or compliance review. FinAxis must not represent an AI system as a substitute for qualified legal counsel or regulatory authorities.

---

## Design Principles

FinAxis should follow these principles:

- Modular architecture
- Local-first operation
- Self-hosted deployment support
- Vendor-independent design
- AI and LLM compatibility
- Retrieval-first regulatory intelligence
- Authoritative source prioritization
- Jurisdiction-aware analysis
- Product-aware compliance analysis
- Source provenance
- Regulatory version tracking
- Effective date tracking
- Compliance date tracking
- Human-in-the-loop review
- Auditable decisions
- Extensible jurisdiction support
- Extensible financial product support
- Privacy-conscious data handling
- Clear separation between law, regulation, guidance, enforcement, and commentary
- Continuous regulatory change monitoring

---

## Core Modules

### Regulatory Intelligence Module

The Regulatory Intelligence Module provides the central framework for identifying and interpreting lending-related legal and regulatory requirements.

It should:

- Identify applicable statutes and regulations
- Map statutes to regulations
- Identify responsible regulatory agencies
- Track regulatory authorities
- Distinguish statutes from regulations
- Distinguish regulations from agency guidance
- Identify enforcement positions
- Identify relevant court decisions
- Track proposed rules
- Track final rules
- Track amendments
- Track rescinded or superseded requirements
- Track effective dates
- Track compliance dates
- Track source versions
- Maintain source provenance
- Identify conflicts or uncertainty between authorities
- Require verification against authoritative sources
- Provide source-linked regulatory responses

### Jurisdiction Module

The Jurisdiction Module determines which geographic jurisdictions may apply to a lending activity.

It should evaluate:

- Federal jurisdiction
- State jurisdiction
- County requirements where applicable
- Municipal requirements where applicable
- Tribal jurisdiction where applicable
- Borrower location
- Lender location
- Property location
- Transaction location
- Business location
- Interstate lending
- Multi-state lending
- Foreign transactions where applicable
- Jurisdiction-specific exemptions
- Choice-of-law considerations
- Licensing jurisdiction

The module should prevent the AI from assuming that the laws of the lender's location automatically govern every transaction.

### Financial Business Classification Module

The Financial Business Classification Module identifies the role and type of financial business involved in a transaction.

It should support classification of:

- Banks
- Credit unions
- Consumer lenders
- Business lenders
- Commercial lenders
- Mortgage lenders
- Mortgage brokers
- Finance companies
- Fintech lenders
- Marketplace lenders
- Peer-to-peer lending platforms
- Private lenders
- Hard-money lenders
- Auto lenders
- Student lenders
- Equipment financiers
- Invoice financiers
- Factoring companies
- Merchant cash advance providers
- Revenue-based financing providers
- Buy now, pay later providers
- Credit card issuers
- Loan servicers
- Debt buyers
- Debt collectors
- Loan brokers
- Lead generators
- Referral platforms
- Embedded-finance providers
- AI underwriting providers
- Technology providers
- Agents
- Assignees
- Loan purchasers
- Secondary-market participants

The module should identify whether an entity is acting as a creditor, broker, servicer, processor, marketer, technology provider, agent, assignee, purchaser, or other participant.

### Lending Product Classification Module

The Lending Product Classification Module determines the legal and functional characteristics of a proposed financial product.

It should support:

- Consumer loans
- Personal loans
- Business loans
- Commercial loans
- Mortgage loans
- Residential mortgages
- Commercial mortgages
- Home equity loans
- Home equity lines of credit
- Reverse mortgages
- Construction loans
- Bridge loans
- Hard-money loans
- Private mortgages
- Installment loans
- Small-dollar loans
- Secured loans
- Unsecured loans
- Lines of credit
- Credit cards
- Auto loans
- Equipment financing
- Student lending
- Debt consolidation loans
- Credit-builder loans
- Medical-purpose loans
- Invoice financing
- Factoring
- Merchant cash advances
- Revenue-based financing
- Buy now, pay later products
- Other emerging lending products

The module should evaluate the substance of a financial product rather than relying solely on the business's marketing terminology.

### Consumer Lending Module

The Consumer Lending Module provides compliance intelligence for credit primarily intended for personal, family, or household purposes.

It should address:

- Consumer applications
- Prequalification
- Underwriting
- Credit decisions
- Pricing
- Interest rates
- APR
- Fees
- Required disclosures
- Origination
- Funding
- Servicing
- Payment processing
- Delinquency
- Default
- Collections
- Charge-offs
- Repossession
- Foreclosure where applicable
- Credit reporting
- Consumer complaints
- Disputes
- Recordkeeping
- Regulatory reporting

### Personal Lending Advisory Module

The Personal Lending Advisory Module provides educational and compliance-aware guidance concerning personal lending.

It should support:

- Unsecured personal loans
- Secured personal loans
- Personal lines of credit
- Installment loans
- Debt consolidation loans
- Emergency loans
- Medical-purpose personal loans
- Home-improvement personal loans
- Auto-related personal loans
- Major-purchase personal loans
- Family and household loans
- Co-borrower considerations
- Cosigner considerations
- Personal guarantees
- Loans secured by personal property
- Loans secured by vehicles
- Loans secured by real estate
- Refinancing
- Loan modifications
- Credit-builder loans
- Small-dollar personal loans

The module should provide guidance concerning:

- Loan affordability
- Borrowing costs
- APR
- Interest rates
- Origination fees
- Application fees
- Prepayment provisions
- Late fees
- Default consequences
- Collateral risks
- Payment schedules
- Loan terms
- Total interest
- Total repayment
- Fixed versus variable rates
- Refinancing consequences
- Debt consolidation
- Alternatives to borrowing
- Personal loan risks

The module should distinguish mathematical affordability analysis from a lender's legal credit decision and should not represent financial guidance as individualized legal advice.

### Business and Commercial Lending Module

The Business and Commercial Lending Module provides compliance intelligence for financing intended primarily for business or commercial purposes.

It should support:

- Sole proprietors
- Partnerships
- LLCs
- Corporations
- Nonprofits
- Agricultural businesses
- Startups
- Established businesses
- Working capital loans
- Business lines of credit
- Business credit cards
- Equipment financing
- Commercial real estate
- Commercial mortgages
- Construction financing
- Invoice financing
- Factoring
- Revenue-based financing
- Merchant cash advances
- Business-purpose credit
- Guarantees
- Personal guarantees
- Business collateral
- UCC-related transactions
- Commercial collections

### Mortgage and Real Estate Lending Module

The Mortgage and Real Estate Lending Module provides specialized regulatory intelligence for lending secured by or related to real estate.

It should support:

- Residential mortgages
- Commercial mortgages
- Home equity loans
- Home equity lines of credit
- Reverse mortgages
- Construction loans
- Bridge loans
- Private mortgages
- Hard-money loans
- Mortgage brokerage
- Mortgage origination
- Mortgage servicing
- Appraisals
- Escrow
- Closing
- Foreclosure
- Loan modification
- Mortgage advertising
- Mortgage disclosures

### Licensing and Registration Module

The Licensing and Registration Module determines whether a financial business or individual may need authorization to conduct lending activities.

It should identify:

- Required licenses
- Required registrations
- State licensing
- Federal registration requirements
- Mortgage licensing
- Consumer finance licensing
- Broker licensing
- Individual licensing
- Company licensing
- License exemptions
- Foreign qualification
- Branch requirements
- Physical-presence requirements
- Surety bonds
- Net-worth requirements
- Responsible-person requirements
- Background checks
- Examination requirements
- Continuing education
- Renewal requirements
- Regulatory reporting
- Licensing fees
- Licensing authorities

### Interest Rate and Pricing Module

The Interest Rate and Pricing Module evaluates lending economics against applicable regulatory restrictions.

It should analyze:

- Interest rates
- APR
- Usury limits
- State interest-rate restrictions
- Federal interest-rate restrictions
- Fee limitations
- Origination fees
- Application fees
- Late fees
- Prepayment fees
- Default fees
- Service fees
- Product-specific pricing restrictions
- Loan-size restrictions
- Term restrictions
- Total-cost restrictions
- Rate advertising requirements

### Disclosure and Forms Module

The Disclosure and Forms Module identifies forms and disclosures that may be required for a lending transaction.

It should support:

- Applications
- Loan agreements
- Promissory notes
- Credit agreements
- Security agreements
- Guarantees
- Consumer disclosures
- Business disclosures
- Adverse-action notices
- Counteroffers
- Privacy notices
- Credit-report authorization
- Electronic-consent forms
- Payment authorization
- ACH authorization
- Servicing notices
- Default notices
- Collection notices
- Debt-validation notices
- State-specific disclosures
- Mortgage disclosures
- Closing documents
- Escrow documents
- Licensing applications
- Regulatory filings
- Annual reports
- Rescission notices
- Modification agreements
- Forbearance agreements
- Settlement agreements

The module should identify whether an item is required, conditionally required, optional, prohibited, or subject to jurisdiction-specific requirements.

### Credit Decision and Underwriting Module

The Credit Decision and Underwriting Module provides compliance guidance for evaluating applicants and making credit decisions.

It should address:

- Credit scoring
- Credit reports
- Alternative data
- Bank-account data
- Employment data
- Income data
- Automated underwriting
- AI underwriting
- Machine learning models
- Model governance
- Explainability
- Adverse-action reasons
- Fair lending
- Bias testing
- Human review
- Decision records
- Model validation
- Audit logs

### Advertising and Marketing Module

The Advertising and Marketing Module evaluates lending marketing practices.

It should address:

- Websites
- Landing pages
- Loan advertisements
- Social media
- Email marketing
- SMS marketing
- Affiliate marketing
- Lead-generation websites
- Referral programs
- Rate advertisements
- APR representations
- Fee representations
- Promotional offers
- Testimonials
- Claims of guaranteed approval
- Claims of no credit checks
- Claims concerning credit improvement
- AI-generated marketing
- Misleading or deceptive representations

### Privacy and Data Governance Module

The Privacy and Data Governance Module provides guidance concerning financial and consumer information used by lending businesses.

It should address:

- Consumer data
- Financial information
- Credit information
- Credit reports
- Bank-account information
- Social Security numbers
- Identity information
- Biometric information where applicable
- Data collection
- Data use
- Data sharing
- Data retention
- Data deletion
- Data security
- Third-party processors
- Vendor access
- Privacy notices
- Data breach obligations
- State privacy requirements
- Financial privacy requirements

### Servicing and Collections Module

The Servicing and Collections Module addresses obligations arising after loan origination.

It should support:

- Payment processing
- Account servicing
- Statements
- Payment allocation
- Late payments
- Grace periods
- Default
- Acceleration
- Collections
- Credit reporting
- Debt validation
- Communication restrictions
- Repossession
- Foreclosure
- Debt sale
- Charge-off
- Settlement
- Bankruptcy considerations
- Consumer complaints

### Compliance Management Module

The Compliance Management Module converts regulatory requirements into operational compliance processes.

It should support:

- Compliance policies
- Compliance procedures
- Control libraries
- Compliance checklists
- Risk assessments
- Compliance calendars
- Employee training requirements
- Vendor requirements
- Audit schedules
- Regulatory examination preparation
- Exception reporting
- Remediation plans
- Compliance attestations
- Compliance reviews
- Management reporting

### Regulatory Change Intelligence Module

The Regulatory Change Intelligence Module monitors changes that may affect lending operations.

It should track:

- New statutes
- Proposed regulations
- Final rules
- Amendments
- Rescissions
- Vacated rules
- Court decisions
- Agency guidance
- Enforcement actions
- State legislative changes
- State regulatory changes
- Licensing changes
- Effective dates
- Compliance dates

The module should identify how regulatory changes affect existing products, licenses, disclosures, forms, policies, procedures, and controls.

### Legal Source and Provenance Module

The Legal Source and Provenance Module establishes traceability for regulatory information used by the AI.

It should prioritize authoritative sources including:

- United States Code
- Code of Federal Regulations
- Federal Register
- Federal agency publications
- State statutes
- State administrative codes
- State regulator publications
- State attorney general publications
- Official court opinions
- Official licensing databases

The system should distinguish:

- Statutes
- Regulations
- Agency guidance
- Interpretive guidance
- Enforcement positions
- Court decisions
- Regulatory commentary
- Secondary sources

Every regulatory determination should retain source information, authority, jurisdiction, publication date, effective date, compliance date, verification date, and version information where available.

### Compliance Decision Module

The Compliance Decision Module combines information from the other core modules into a structured compliance analysis.

The analysis should follow a process such as:

Business Model → Business Classification → Product Classification → Borrower Classification → Transaction Characteristics → Jurisdiction → Applicable Laws → Licensing → Restrictions → Disclosures → Forms → Underwriting → Servicing → Collections → Recordkeeping → Ongoing Monitoring

The module should classify findings as:

- Applicable
- Not applicable
- Potentially applicable
- Exempt
- Requires additional facts
- Requires state-specific review
- Requires legal review
- Requires compliance review
- Prohibited
- License required
- Disclosure required
- Form required

### Human Review and Escalation Module

The Human Review and Escalation Module ensures that uncertain or high-risk issues are directed to qualified professionals.

It should:

- Identify unresolved legal questions
- Identify conflicting authorities
- Identify insufficient facts
- Flag high-risk transactions
- Flag uncertain exemptions
- Identify matters requiring qualified legal counsel
- Identify matters requiring compliance professionals
- Preserve the reason for escalation
- Record human determinations
- Record overrides
- Preserve review history

FinAxis should never fabricate legal certainty when available information is insufficient to establish a reliable conclusion.

### Audit and Evidence Module

The Audit and Evidence Module creates an auditable record of regulatory determinations.

It should record:

- User question
- Transaction facts
- Business characteristics
- Product characteristics
- Borrower characteristics
- Jurisdiction
- Assumptions
- Rules evaluated
- Sources consulted
- Source versions
- Effective dates
- Compliance dates
- Regulatory findings
- Compliance result
- Exceptions
- Human review
- Human overrides
- Reviewer
- Review date
- Supporting evidence
- Final determination

### Compliance Reporting Module

The Compliance Reporting Module should generate structured reports for financial businesses.

Reports may include:

- Regulatory applicability reports
- Licensing reports
- Product compliance reports
- State-by-state compliance reports
- Disclosure reports
- Forms reports
- Pricing compliance reports
- Underwriting compliance reports
- Advertising compliance reports
- Servicing compliance reports
- Collections compliance reports
- Privacy reports
- Regulatory change impact reports
- Compliance gap reports
- Risk reports
- Audit reports
- Examination preparation reports

---

## Optional Plugin Modules

Optional plugin modules may extend FinAxis without changing the core specification.

### State Regulatory Plugins

State-specific plugins may provide detailed regulatory datasets and workflows for individual states and territories.

Each state plugin may include:

- State statutes
- Administrative rules
- Licensing requirements
- State agencies
- State forms
- State disclosures
- State fee restrictions
- State interest-rate restrictions
- State exemptions
- State reporting requirements
- State enforcement information
- State regulatory updates

### Federal Agency Plugins

Federal agency plugins may connect FinAxis to authoritative federal regulatory sources.

Potential integrations may include:

- Consumer Financial Protection Bureau
- Federal Trade Commission
- Federal Reserve
- Office of the Comptroller of the Currency
- Federal Deposit Insurance Corporation
- National Credit Union Administration
- Securities and Exchange Commission
- Department of Housing and Urban Development
- Department of Justice
- Federal Housing Finance Agency
- Small Business Administration
- Other applicable federal agencies

### Regulatory Monitoring Plugins

Regulatory monitoring plugins may provide automated monitoring of:

- Federal Register updates
- State legislative updates
- State regulatory updates
- Agency announcements
- Enforcement actions
- Court decisions
- Licensing changes
- Regulatory guidance
- Compliance deadlines

### LLM Provider Plugins

LLM provider plugins may connect FinAxis to compatible AI models.

Plugins should support:

- Local LLMs
- Self-hosted models
- Cloud-based models
- Model selection
- Model routing
- Model-specific configuration
- Retrieval-augmented generation
- Structured outputs
- Model auditing

The core specification should not require a particular LLM provider.

### Document and Data Source Plugins

Optional plugins may provide connections to:

- Regulatory databases
- Government data sources
- Licensing databases
- Business registration systems
- Internal compliance databases
- Knowledge bases
- Document repositories
- Structured legal datasets

### Workflow Plugins

Workflow plugins may connect FinAxis to:

- Compliance management systems
- Case management systems
- Ticketing systems
- Task management systems
- Audit systems
- Business process automation
- Notification systems
- Reporting systems

### Identity and Access Plugins

Optional identity plugins may support:

- User authentication
- Role-based access control
- Compliance officer access
- Legal reviewer access
- Administrator access
- Audit-only access
- Organization-level permissions
- Multi-tenant access controls

### Notification Plugins

Notification plugins may provide:

- Regulatory change alerts
- Licensing expiration alerts
- Compliance deadline alerts
- Review requests
- Escalation notifications
- Audit notifications
- Risk alerts

### Analytics Plugins

Optional analytics plugins may provide:

- Compliance trend analysis
- Regulatory risk analysis
- Product risk scoring
- Licensing coverage analysis
- State coverage analysis
- Compliance gap analysis
- Regulatory change impact analysis
- Audit analytics

## AI Operating Requirements

AI implementations based on FinAxis should:

- Prefer authoritative retrieved sources over model memory
- Cite or identify sources used for regulatory conclusions
- Distinguish facts from assumptions
- Identify missing information
- Identify uncertainty
- Avoid unsupported legal conclusions
- Avoid fabricating statutes, regulations, cases, agencies, forms, or requirements
- Preserve regulatory source provenance
- Respect jurisdictional differences
- Track regulatory dates
- Provide structured reasoning summaries
- Support human review
- Preserve audit records
- Escalate matters requiring professional review

## Regulatory Knowledge Requirements

FinAxis implementations should maintain regulatory information in a structured and versioned format.

Each regulatory record should support, where available:

- Authority
- Jurisdiction
- Citation
- Title
- Subject
- Applicability
- Covered entities
- Covered products
- Requirements
- Exceptions
- Exemptions
- Required disclosures
- Required forms
- Licensing implications
- Penalties
- Effective date
- Compliance date
- Publication date
- Last verified date
- Source
- Source version
- Superseded authority
- Replacement authority

## Security and Privacy Requirements

FinAxis implementations should:

- Minimize collection of sensitive information
- Protect financial information
- Protect personally identifiable information
- Encrypt sensitive data where appropriate
- Provide access controls
- Maintain audit logs
- Support data retention policies
- Support data deletion policies
- Restrict unauthorized model access
- Prevent sensitive information from being unnecessarily transmitted to external AI providers
- Support local or self-hosted processing where appropriate
- Provide configurable data handling policies

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
  - [https://roxanneardary.com/finaxis/](https://roxanneardary.com/finaxis/)  

---

## License & Notice Requirements

FinAxis is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to any Open Arsenal project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.
- FinAxis specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.
  Any update that adds new contributors or modifies attribution should also update `notice.md`.
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
