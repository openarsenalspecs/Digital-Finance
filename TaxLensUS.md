# TaxLensUS
**Give small business the insight big corporations use.**
- HTML Mirror:  [https://roxanneardary.com/taxlensus-specification/](https://roxanneardary.com/taxlensus-specification/)  

---

## Purpose

TaxLensUS is an open-source, AI-driven U.S. tax intelligence and policy impact analysis system designed to ingest publicly available corporate tax and financial disclosures, identify and analyze the tax provisions reflected in those disclosures, track changes in U.S. tax policy, and evaluate how those changes may have helped or hurt small businesses.

TaxLensUS is designed as a research, education, transparency, and financial intelligence platform. The system converts complex tax disclosures and tax policy changes into structured, traceable information that can be analyzed by artificial intelligence and presented in understandable reports.

The system is intended to help small business owners improve their financial IQ by learning how the U.S. tax system works, understanding how tax provisions affect businesses, identifying legally available tax planning opportunities to investigate, and understanding how tax policy can create advantages or disadvantages between large and small businesses.

## Design Principles

- Open-source architecture
- Modular system design
- Local-first operation where practical
- Self-hosted deployment support
- Vendor-neutral architecture
- Public-data-first methodology
- Evidence-based analysis
- Source traceability
- Reproducible research
- Versioned data
- Versioned tax policy
- Human-in-the-loop review
- Explicit uncertainty
- Confidence scoring
- Separation of facts from inference
- Separation of tax education from professional tax advice
- No unsupported causal claims
- No fabricated tax provisions or filing information
- Extensible ingestion architecture
- Replaceable AI models
- Replaceable data providers
- API-accessible intelligence

---

## Core Modules

### Corporate Filing Intelligence Module

The Corporate Filing Intelligence Module shall ingest and process publicly available U.S. corporate financial and tax disclosures.

Features:

- SEC EDGAR integration
- Public filing discovery
- 10-K ingestion
- 10-Q ingestion
- Applicable SEC filing type support
- Filing metadata extraction
- Filing date extraction
- Fiscal year identification
- Company identification
- CIK identification
- Ticker identification where available
- XBRL ingestion
- HTML filing ingestion
- Filing document normalization
- Filing version tracking
- Filing source preservation
- Filing provenance tracking
- Tax-related section identification
- Income tax footnote identification
- ASC 740 disclosure identification
- Tax reconciliation identification
- Deferred tax disclosure identification
- Tax jurisdiction disclosure identification
- Tax credit disclosure identification
- Tax benefit disclosure identification
- Tax-loss disclosure identification
- Uncertain tax position disclosure identification
- Tax contingency disclosure identification
- One-time tax adjustment identification
- Tax reform adjustment identification

The module shall preserve the relationship between extracted information and its originating filing.

### Tax Data Extraction Module

The Tax Data Extraction Module shall convert corporate tax disclosures into normalized, machine-readable tax records.

Features:

- Effective tax rate extraction
- Statutory tax rate extraction
- Current tax expense extraction
- Deferred tax expense extraction
- Federal tax extraction where disclosed
- State tax extraction where disclosed
- Foreign tax extraction where disclosed
- Deferred tax asset extraction
- Deferred tax liability extraction
- Valuation allowance extraction
- Tax credit extraction
- Tax credit carryforward extraction
- Tax-loss carryforward extraction
- Deduction identification
- Tax provision identification
- Tax-rate reconciliation extraction
- Permanent difference identification
- Temporary difference identification
- Foreign tax rate impact identification
- State tax rate impact identification
- Tax reform impact identification
- Tax benefit identification
- Tax expense adjustment identification
- Tax terminology normalization
- Unit normalization
- Currency normalization
- Fiscal-period normalization
- Data validation
- Extraction confidence scoring

The module shall distinguish between directly reported values, calculated values, and AI-inferred values.

### Corporate Tax Profile Module

The Corporate Tax Profile Module shall create longitudinal tax profiles for companies based on available public disclosures.

Features:

- Corporate tax history
- Effective tax rate history
- Statutory tax rate history
- Current tax expense history
- Deferred tax history
- Tax credit history
- Tax-loss history
- Tax jurisdiction history
- Tax reconciliation history
- Tax provision history
- Tax policy exposure
- Reported tax strategy signals
- Significant tax change detection
- Year-over-year comparisons
- Multi-year trend analysis
- Industry comparisons
- Company comparisons
- Policy-period comparisons
- Filing-to-filing comparisons

Each profile shall maintain links to the underlying evidence.

### U.S. Tax Code Intelligence Module

The U.S. Tax Code Intelligence Module shall maintain a structured and versioned representation of relevant U.S. tax provisions.

Features:

- Internal Revenue Code provision tracking
- Tax section identification
- Tax subsection identification
- Tax provision descriptions
- Tax provision effective dates
- Tax provision expiration dates
- Tax provision phase-ins
- Tax provision phase-outs
- Historical provision versions
- Tax rate changes
- Deduction changes
- Credit changes
- Depreciation changes
- Amortization changes
- Business income provisions
- Corporate tax provisions
- Pass-through provisions
- Small business provisions
- Research and development provisions
- Investment provisions
- Loss utilization provisions
- State tax provision references where supported
- Related regulatory references
- Related IRS guidance references
- Related Treasury guidance references

The module shall preserve historical versions so that analysis can determine which rules were applicable during a particular period.

### Tax Policy Timeline Module

The Tax Policy Timeline Module shall maintain a chronological record of U.S. tax policy changes.

Features:

- Legislative event tracking
- Tax reform tracking
- Tax provision amendments
- Tax provision replacements
- Tax rate changes
- Effective-date tracking
- Expiration-date tracking
- Phase-in tracking
- Phase-out tracking
- IRS guidance tracking
- Treasury guidance tracking
- Policy event descriptions
- Policy event relationships
- Pre-policy periods
- Post-policy periods
- Policy comparison periods
- Policy impact windows

The system shall allow policy events to be associated with specific tax provisions and applicable business categories.

### Tax Policy Knowledge Graph Module

The Tax Policy Knowledge Graph Module shall connect companies, filings, tax provisions, policy events, industries, jurisdictions, and economic indicators.

Entities may include:

- Companies
- Corporate filings
- Tax provisions
- Tax sections
- Legislation
- Regulations
- IRS guidance
- Treasury guidance
- Policy events
- Industries
- Economic indicators
- Small business indicators
- Geographic jurisdictions
- Tax years
- Fiscal periods
- Impact assessments
- Evidence sources

Relationships may include:

- Applies to
- Reported in
- Changed by
- Amended by
- Replaced by
- Effective during
- Associated with
- Impacts
- Correlates with
- Precedes
- Follows
- Observed in
- Supported by
- Contradicted by
- Relevant to

The graph shall support historical and temporal relationships.

### Small Business Data Module

The Small Business Data Module shall integrate public datasets that can provide evidence about small business conditions and outcomes.

Potential data sources include:

- Small Business Administration datasets
- U.S. Census Bureau datasets
- Federal Reserve datasets
- Small business credit surveys
- Small business employment data
- Business formation data
- Business closure data
- Business lending data
- Wage data
- Investment data
- Industry-level economic data
- Government economic reports
- Other legally usable public datasets

The module shall record source, publication date, measurement period, geographic scope, business-size definitions, methodology, and applicable limitations.

### Small Business Impact Analysis Module

The Small Business Impact Analysis Module shall evaluate whether tax policy changes appear to have helped, hurt, or produced mixed effects for small businesses.

Potential impact classifications:

- Likely beneficial
- Moderately beneficial
- Neutral
- Mixed
- Moderately negative
- Likely negative
- Insufficient evidence

The module shall analyze potential effects on:

- Tax burden
- Cash flow
- Business investment
- Business formation
- Business closures
- Employment
- Wages
- Financing
- Credit availability
- Operating costs
- Consumer demand
- Supplier costs
- Market competition
- Market concentration
- Capital access
- Investment incentives
- Large-business competitive advantages
- Small-business competitive advantages

The system shall distinguish observed small business indicators from inferred policy effects.

### Policy Impact Inference Module

The Policy Impact Inference Module shall evaluate relationships between tax policy changes, corporate tax behavior, and small business indicators.

Features:

- Pre-policy baseline creation
- Post-policy comparison
- Time-series analysis
- Trend analysis
- Correlation analysis
- Comparative analysis
- Sector analysis
- Geographic analysis
- Company-size analysis
- Policy sensitivity analysis
- Anomaly detection
- Structural change detection
- Mechanism identification
- Confounding-factor identification
- Alternative explanation analysis
- Evidence weighting
- Confidence scoring
- Contradictory evidence detection
- Insufficient evidence detection

The module shall not treat correlation as proof of causation.

### AI Analysis Module

The AI Analysis Module shall analyze structured and source-linked data to produce explanations and findings.

Features:

- Retrieval-augmented analysis
- Filing interpretation
- Tax provision interpretation
- Policy interpretation
- Comparative analysis
- Trend interpretation
- Evidence synthesis
- Tax terminology explanation
- Small business impact interpretation
- Financial education assistance
- Natural-language question answering
- Structured finding generation
- Confidence assessment
- Uncertainty identification
- Contradiction detection
- Unsupported claim detection
- Source-grounded responses

The AI shall clearly distinguish:

- Reported facts
- Calculated results
- Statistical observations
- AI interpretations
- Hypotheses
- Potential causal mechanisms
- Areas requiring professional review

### Financial IQ Education Module

The Financial IQ Education Module shall help small business owners understand tax concepts and financial consequences without requiring them to become tax professionals.

Features:

- Plain-language tax explanations
- Tax terminology explanations
- Tax provision explanations
- Deduction education
- Credit education
- Depreciation education
- Amortization education
- Tax timing education
- Business structure education
- Tax incentive education
- Cash-flow implications
- Effective tax rate education
- Tax planning concept education
- Policy change education
- Corporate tax strategy education
- Large-business versus small-business comparisons
- Interactive questions
- Follow-up explanations
- Source-linked educational material

The module shall prioritize education and understanding rather than providing unsupported individualized tax conclusions.

### Legal Tax Planning Intelligence Module

The Legal Tax Planning Intelligence Module shall identify tax provisions and planning concepts that users may wish to investigate for lawful tax optimization.

Potential findings may include:

- Potentially applicable deductions
- Potentially applicable credits
- Depreciation opportunities
- Amortization opportunities
- Research and development incentives
- Investment incentives
- Loss utilization concepts
- Timing considerations
- Business expense categories
- Entity-structure considerations
- Federal tax considerations
- State tax considerations
- Tax incentive programs

The system shall use language such as:

- May apply
- Worth investigating
- Potential opportunity
- Requires eligibility review
- Requires documentation
- Discuss with a qualified tax professional

The system shall not recommend illegal concealment, falsification, evasion, or fraudulent reporting.

### Report Generation Module

The Report Generation Module shall create structured reports from analyzed evidence.

Reports may contain:

- Executive summary
- Policy summary
- Relevant tax provisions
- Policy change timeline
- Corporate filing findings
- Corporate tax behavior changes
- Small business indicators
- Economic indicators
- Potential transmission mechanisms
- Supporting evidence
- Contradictory evidence
- Confounding factors
- Alternative explanations
- Impact classification
- Confidence score
- Data limitations
- Methodology
- Source references
- Evidence provenance
- Areas requiring additional research

Reports shall clearly separate evidence from interpretation.

### Evidence & Provenance Module

The Evidence & Provenance Module shall maintain traceability between every significant finding and its source.

Features:

- Source identification
- Source URL preservation
- Filing accession identification
- Filing date preservation
- Publication date preservation
- Tax-year identification
- Dataset identification
- Extracted text references
- Source document references
- Data lineage
- Transformation history
- Analysis versioning
- Model versioning
- Report versioning
- Evidence confidence
- Provenance records
- Audit trails

### Data Quality Module

The Data Quality Module shall validate incoming and processed information.

Features:

- Schema validation
- Filing validation
- Duplicate detection
- Missing-data detection
- Type validation
- Unit validation
- Currency validation
- Date validation
- Fiscal-period validation
- Cross-source consistency checks
- Historical consistency checks
- Extraction quality scoring
- Source integrity checks
- Anomaly detection
- Data quality reporting

### Search & Discovery Module

The Search & Discovery Module shall provide structured and natural-language discovery across the TaxLensUS knowledge base.

Features:

- Company search
- Filing search
- Tax provision search
- Policy search
- Industry search
- Geographic search
- Tax-year search
- Keyword search
- Semantic search
- Natural-language search
- Evidence search
- Report search
- Cross-company search
- Cross-industry search
- Policy-event discovery

Example queries:

- How did corporate effective tax rates change after a specific tax reform?
- Which tax provisions appear most frequently in this industry?
- Which companies reported significant tax changes after a specific policy became effective?
- What evidence suggests that a tax policy helped or hurt small businesses?
- What changed in corporate tax disclosures after a policy change?
- Which tax incentives should a small business owner investigate?

### Comparative Analysis Module

The Comparative Analysis Module shall allow users to compare tax and policy effects across entities and periods.

Features:

- Company versus company
- Industry versus industry
- Year versus year
- Pre-policy versus post-policy
- Policy versus policy
- Sector comparisons
- Geographic comparisons
- Tax provision comparisons
- Corporate versus small business indicators
- Historical comparisons
- Tax burden comparisons
- Effective tax rate comparisons

### Visualization Module

The Visualization Module shall present structured findings through interactive visualizations.

Potential visualizations include:

- Effective tax rate trends
- Tax expense trends
- Deferred tax trends
- Tax provision timelines
- Policy timelines
- Company tax profiles
- Industry comparisons
- Small business impact indicators
- Policy impact scorecards
- Evidence timelines
- Geographic comparisons
- Tax provision relationships
- Corporate response trends

### API Module

The API Module shall provide programmatic access to TaxLensUS intelligence.

Potential endpoints shall support:

- Company profiles
- Corporate filings
- Tax records
- Tax provisions
- Policy events
- Economic indicators
- Small business indicators
- Impact assessments
- Reports
- Evidence
- Provenance
- Search
- Dataset exports

Supported data formats may include:

- JSON
- CSV
- Parquet
- JSON-LD

### Reproducibility Module

The Reproducibility Module shall preserve the information necessary to reproduce analytical results.

Features:

- Dataset versioning
- Source versioning
- Tax policy versioning
- Analysis versioning
- Model versioning
- Prompt or analysis specification versioning where applicable
- Pipeline versioning
- Report versioning
- Transformation metadata
- Analysis metadata
- Reproducible workflows
- Audit records

---

## Optional Plugin Modules

### Additional Filing Source Plugin

Provides support for additional publicly available financial and regulatory filing sources beyond the core SEC ingestion system.

Capabilities:

- Additional filing providers
- Additional regulatory databases
- Source-specific parsers
- Source-specific metadata
- Source-specific provenance
- Source normalization

### State Tax Intelligence Plugin

Extends TaxLensUS into state and local tax analysis.

Capabilities:

- State tax code tracking
- State corporate tax rates
- State deductions
- State credits
- State policy changes
- State filing references where publicly available
- State small business indicators
- State-by-state comparisons
- Geographic policy impact analysis

### Small Business Tax Form Education Plugin

Provides educational analysis of publicly documented small business tax forms and instructions.

Capabilities:

- Form education
- Instruction analysis
- Provision mapping
- Eligibility education
- Deduction education
- Credit education
- Filing-period comparisons
- Tax terminology explanations

### Tax Professional Review Plugin

Provides workflows for professional review of AI-generated findings.

Capabilities:

- Human review queues
- Finding approval
- Finding rejection
- Annotation
- Correction
- Evidence review
- Confidence adjustment
- Review history
- Expert feedback

### Advanced Causal Inference Plugin

Provides additional statistical methodologies for policy impact research.

Capabilities:

- Difference-in-differences analysis
- Event-study analysis
- Regression analysis
- Synthetic control methodologies
- Matching methodologies
- Sensitivity analysis
- Robustness testing
- Confounder analysis

Results shall clearly identify methodology, assumptions, limitations, and uncertainty.

### Economic Research Plugin

Expands economic data analysis.

Capabilities:

- Additional government datasets
- Economic indicators
- Labor market indicators
- Inflation indicators
- Interest rate indicators
- Credit conditions
- Business formation
- Business closure
- Investment activity
- Industry indicators

### Local Business Impact Plugin

Provides geographically focused small business analysis.

Capabilities:

- County-level indicators
- City-level indicators where available
- State comparisons
- Local economic indicators
- Local tax policy
- Local business conditions
- Geographic policy impact reports

### Advanced AI Model Plugin

Allows deployment of alternative AI models.

Capabilities:

- Local language models
- Hosted language models
- Specialized financial models
- Specialized document models
- Model selection
- Model comparison
- Model versioning
- Model performance evaluation

### Vector Search Plugin

Provides semantic retrieval across filings, policies, reports, and evidence.

Capabilities:

- Document embeddings
- Filing embeddings
- Tax provision embeddings
- Policy embeddings
- Semantic retrieval
- Similarity search
- Evidence retrieval
- Retrieval ranking

### Knowledge Graph Provider Plugin

Allows alternative graph database implementations.

Capabilities:

- Graph database adapters
- Entity synchronization
- Relationship synchronization
- Graph querying
- Historical relationship storage
- Policy relationship analysis

### Dashboard Plugin

Provides an optional web-based user interface.

Capabilities:

- Company dashboards
- Tax policy dashboards
- Small business impact dashboards
- Search interfaces
- Report interfaces
- Visualization interfaces
- Evidence inspection
- Source inspection

### Notification Plugin

Provides optional alerts for significant changes.

Capabilities:

- New filing alerts
- Tax policy change alerts
- Corporate tax change alerts
- Industry trend alerts
- Small business indicator alerts
- Report availability alerts
- Custom search alerts

### Research Export Plugin

Provides advanced research data exports.

Capabilities:

- Research datasets
- Bulk exports
- CSV exports
- JSON exports
- Parquet exports
- JSON-LD exports
- Research metadata
- Provenance packages
- Reproducibility packages

---

## AI Finding Classification

Every substantive AI finding should be classified according to the type of evidence supporting it.

### Observed

Information directly reported by a source.

### Calculated

Information mathematically derived from reported data.

### Correlated

A statistical relationship identified between variables.

### Inferred

An interpretation supported by available evidence but not directly stated by a source.

### Hypothesized

A possible explanation requiring additional evidence.

### Causal

A causal conclusion supported by an appropriate causal methodology and sufficient evidence.

The system shall not label a finding causal solely because two variables changed at the same time.

---

## Impact Assessment Framework

TaxLensUS shall evaluate policy impacts using multiple dimensions.

### Direct Tax Effect

The estimated or reported effect of a policy on applicable tax liabilities, credits, deductions, or other tax provisions.

### Corporate Response

Changes observed in corporate tax disclosures following policy implementation.

### Market Transmission

Potential mechanisms through which corporate tax changes may affect markets and smaller competitors.

### Small Business Indicators

Changes in measurable small business conditions following a policy event.

### Confounding Factors

Other events or economic conditions that could explain observed changes.

### Evidence Strength

The amount, quality, consistency, and directness of supporting evidence.

### Confidence

A structured assessment of confidence based on evidence quality, data coverage, methodological strength, and uncertainty.

---

## Small Business Impact Report

A Small Business Impact Report should contain:

- Policy being evaluated
- Applicable tax provisions
- Policy effective dates
- Analysis period
- Corporate filing evidence
- Corporate tax behavior changes
- Small business indicators
- Economic indicators
- Potential benefits
- Potential costs
- Competitive effects
- Financing effects
- Investment effects
- Employment effects
- Potential transmission mechanisms
- Confounding factors
- Contradictory evidence
- Evidence limitations
- Impact classification
- Confidence level
- Supporting sources
- Methodology
- Areas requiring additional research

---

## Financial IQ Workflow

TaxLensUS shall support a learning workflow in which a small business owner can:

- Ask a question about a tax provision
- Receive a plain-language explanation
- Review the underlying tax authority
- Examine how the provision has affected businesses
- Review relevant corporate disclosures
- Compare historical policy periods
- Identify potentially relevant deductions or credits
- Review eligibility considerations
- Examine potential financial effects
- Identify questions to discuss with a tax professional
- Track changes in the applicable tax policy

The objective is to help business owners understand the tax system well enough to make better-informed financial decisions.

---

## Legal Tax Optimization Boundary

TaxLensUS shall support lawful tax planning education and analysis.

The system may identify:

- Legal deductions
- Legal credits
- Tax incentives
- Timing strategies
- Depreciation methods
- Amortization concepts
- Business structure considerations
- Loss utilization concepts
- Research and development incentives
- Investment incentives
- State and federal tax considerations

The system shall not assist with:

- Tax evasion
- Concealment of taxable income
- Falsification of records
- Fraudulent deductions
- Fabricated transactions
- Destruction or concealment of evidence
- False tax reporting
- Circumvention of tax laws through illegal means

## Data Governance

Each data source shall maintain metadata describing:

- Source name
- Source type
- Source location
- Publication date
- Retrieval date
- Coverage period
- Geographic scope
- Entity scope
- Data format
- Licensing or usage conditions
- Processing method
- Transformation history
- Known limitations

The system shall distinguish between source data and TaxLensUS-generated analysis.

## AI Safety and Reliability

AI-generated findings shall:

- Cite supporting evidence
- Identify uncertainty
- Avoid unsupported claims
- Avoid fabricated citations
- Avoid fabricated tax provisions
- Identify conflicting evidence
- Identify missing information
- Preserve source context
- Provide confidence levels
- Distinguish facts from interpretations
- Avoid presenting tax advice as professional advice
- Avoid presenting legal conclusions without appropriate authority
- Allow human review

## Privacy

TaxLensUS shall prioritize publicly available information.

The core system shall not require:

- Private corporate tax returns
- Individual tax returns
- Confidential IRS records
- Non-public taxpayer information

Any user-provided private information shall be handled separately from the public research dataset and shall not be incorporated into public datasets without appropriate authorization.

## Transparency Requirements

The system shall make its analytical methodology inspectable.

Documentation should identify:

- Data sources
- Data acquisition methods
- Extraction methods
- Tax provision mappings
- Policy mappings
- Statistical methodologies
- Impact assessment methodology
- Confidence methodology
- AI model information where applicable
- Major assumptions
- Known limitations
- Dataset versions
- Analysis versions
- Report versions

## Extensibility

TaxLensUS shall support modular replacement or extension of:

- Data sources
- Filing parsers
- Tax code datasets
- Policy datasets
- Economic datasets
- Storage systems
- Graph databases
- Vector databases
- AI models
- Statistical analysis engines
- Report generators
- APIs
- User interfaces
- Visualization systems

Core functionality shall not depend unnecessarily on a single vendor or proprietary service.

## Deployment

TaxLensUS should support:

- Local deployment
- Self-hosted deployment
- Server deployment
- Containerized deployment
- API-only deployment
- Research deployment
- Web application deployment
- Optional cloud deployment

Network-deployed versions shall comply with the project's AGPL-3.0+ licensing requirements.

## Research and Public Interest Use

TaxLensUS is intended to support:

- Small business financial education
- Tax policy research
- Economic research
- Corporate tax transparency
- Journalism
- Academic research
- Government policy analysis
- Financial analysis
- Public-interest research
- Open-source financial intelligence

The system is designed to make complex tax and economic information more understandable, searchable, and independently verifiable.

## Limitations

TaxLensUS shall explicitly acknowledge that:

- Most private corporate tax returns are not publicly available
- SEC disclosures do not represent complete corporate tax returns
- Public economic indicators are proxies for many small business outcomes
- Corporate disclosures may omit relevant information
- Tax disclosures can differ between companies
- Tax policy can interact with numerous non-tax economic conditions
- Correlation does not establish causation
- AI interpretation can contain errors
- Tax law changes over time
- Eligibility for tax provisions depends on individual circumstances
- Professional tax advice may be required
- Data availability varies by period and jurisdiction

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
  - [https://roxanneardary.com/taxlensus/](https://roxanneardary.com/taxlensus/)

---

## License & Notice Requirements

TaxLensUS is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- TaxLensUS specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.  
  Any update that adds new contributors or modifies attribution should also update `notice.md`.
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
