# FuturePathway
**Plan the Path. Fund the Future.**
- HTML Mirror:  [https://roxanneardary.com/futurepathway-specification/](https://roxanneardary.com/futurepathway-specification/)  

---
FuturePathway is an open source specification for deterministic education financing designed to connect educational opportunity with realistic career earning potential. The specification establishes transparent financing rules based on the annually updated average starting salary for a selected career field, while using AI assistance to help students identify viable career paths, educational programs, and schools that meet the financing requirements.

FuturePathway is built around the principle that **investing in the future means investing in youth**. Rather than using opaque lending models to determine how much educational debt a student can carry, FuturePathway establishes predictable qualification criteria that connect the total cost of education to the expected starting salary associated with the student's selected career field.

## Specification

FuturePathway defines a deterministic financing framework in which the maximum qualifying loan amount is calculated from the average starting salary for the selected career field.

The core financing calculation is:

**Maximum Qualifying Loan = Average Starting Salary × 3**

The average starting salary must be updated annually using defined and verifiable salary data.

The qualifying loan must be sufficient to cover the student's full qualifying tuition. If the maximum qualifying loan amount is less than the full qualifying tuition, the financing request is declined.

### Financing Terms

- **Interest Rate:** 4% fixed
- **Repayment Term:** 6 years
- **In-School Interest:** Interest does not grow while the student is enrolled in school
- **Salary Benchmark:** Annually updated average starting salary
- **Maximum Financing:** Three times the applicable average starting salary
- **Full Tuition Requirement:** The qualifying financing amount must cover the full qualifying tuition
- **Qualification:** Determined by transparent, reproducible rules
- **AI Role:** Assistance, prediction, discovery, and analysis
- **Decision Authority:** Deterministic qualification engine

FuturePathway does not use projected mid-career or peak-career earnings to increase the financing ceiling. The average starting salary is the authoritative income benchmark for the core qualification calculation.

## Design Principles

### Deterministic Financing

The financing rules are explicit and reproducible. The same inputs must produce the same qualification result.

### Starting Salary First

The financing ceiling is based on the average starting salary associated with the selected career field rather than an individual's projected future earnings.

### Full Education Funding

A qualifying loan must be capable of covering the student's full qualifying tuition. The specification does not create a partial financing obligation when the program cannot be fully financed under the defined limit.

### AI-Assisted, Not AI-Controlled

AI may assist with career forecasting, school discovery, program comparisons, and analysis. AI does not override the deterministic financing rules.

### Annual Data Updates

Salary benchmarks and other time-sensitive data are versioned and updated according to defined annual update procedures.

### Transparency

Inputs, data sources, calculations, rule versions, and relevant AI model information should be available for verification.

### Student-Centered Financing

The system is designed around creating viable educational and career pathways rather than maximizing the amount of debt issued.

### Open Source Interoperability

The specification is designed to support implementations by schools, financial institutions, governments, nonprofit organizations, and independent open source developers without requiring dependence on a single vendor.

## Modular Design

FuturePathway is organized as a modular specification so that the core financing framework remains stable while supporting optional implementations and integrations.

### Core Modules

#### 1. Core Specification Module

Defines the fundamental FuturePathway framework.

Features:

- Specification terminology
- Core principles
- Eligibility requirements
- Required data inputs
- Standard outputs
- Financing definitions
- Rule definitions
- Versioning requirements
- Interoperability requirements

#### 2. Salary Benchmark Module

Maintains the salary data used by the deterministic financing engine.

Features:

- Average starting salary by career field
- Annual salary updates
- Effective dates
- Salary-data source identification
- Historical salary records
- Salary-data versioning
- Field classification
- Geographic salary data support
- Data validation
- Reproducible salary calculations

The salary benchmark used for qualification must represent starting salary rather than established-career or peak-career earnings.

#### 3. Qualification Engine Module

Provides the deterministic financing decision system.

Features:

- Average starting salary calculation
- Three-year financing ceiling calculation
- Full-tuition comparison
- Qualification determination
- Decline determination
- Rule validation
- Reproducible calculations
- Qualification explanations
- Decision records
- Rule version tracking

The qualification engine must not allow an AI model to override the defined financing rules.

#### 4. Education Cost Module

Defines the costs used to determine whether a program can be fully financed.

Features:

- Tuition
- Mandatory fees
- Program duration
- Qualifying education costs
- Total qualifying program cost
- Cost verification
- Annual cost updates
- Program-level cost records
- Cost-data versioning

#### 5. Career Path Module

Defines the career information used to establish an educational pathway.

Features:

- Career field identification
- Career classifications
- Education-to-career relationships
- Entry-level career requirements
- Starting salary association
- Career pathway mapping
- Alternative career pathways
- Career progression information
- Career data versioning

#### 6. AI Career Assistant Module

Provides AI-assisted career analysis while preserving deterministic financing authority.

Features:

- Career pathway suggestions
- Career option discovery
- Education requirement analysis
- Career comparison
- Starting-salary information presentation
- Career-path explanations
- Predictive career modeling
- Confidence indicators
- Model assumptions
- Explainable recommendations

AI predictions may assist the student but cannot increase the maximum qualifying loan.

#### 7. School Discovery Module

Helps students locate schools and programs that satisfy the FuturePathway requirements.

Features:

- School discovery
- Program discovery
- Tuition comparison
- Career-program matching
- Financing-limit filtering
- Full-tuition qualification filtering
- Program duration comparison
- Location comparison
- School data verification
- Alternative program discovery

The module can work backward from a student's financing limit to identify educational programs that can be fully financed.

#### 8. Loan Terms Module

Defines the standard financing structure.

Features:

- 4% fixed interest
- Six-year repayment term
- In-school interest treatment
- Repayment schedule
- Principal calculation
- Interest calculation
- Payment calculation
- Amortization
- Loan status tracking
- Repayment milestones

#### 9. Data Provenance Module

Provides traceability for information used by the specification.

Features:

- Data source identification
- Source publication date
- Effective date
- Data version
- Calculation inputs
- Data transformation records
- Historical records
- Validation status
- Provenance tracking

#### 10. Audit Module

Creates an auditable record of financing qualification.

Features:

- Qualification history
- Input records
- Salary benchmark version
- Tuition data version
- Rule version
- AI model version
- Calculation results
- Approval or decline reason
- Reproducibility
- Audit records

#### 11. Governance Module

Defines how the specification and its data evolve.

Features:

- Annual salary updates
- Data-source requirements
- Rule versioning
- Specification versioning
- Model review
- Data validation
- Change management
- Governance records
- Implementation requirements

#### 12. API and Interoperability Module

Defines standardized interfaces for implementations.

Features:

- Qualification APIs
- Salary-data APIs
- School-data APIs
- Program-data APIs
- Career-data APIs
- Loan calculation APIs
- Standardized data structures
- Vendor-neutral interfaces
- Machine-readable outputs
- Integration support

## Optional Plugin Modules

Optional plugins extend FuturePathway without changing the core deterministic financing rules.

### Geographic Salary Plugin

Provides geographically specific starting-salary data.

Features:

- State-level salary data
- Regional salary data
- Metropolitan salary data
- Local labor-market data
- Geographic comparisons

### Scholarship Integration Plugin

Integrates scholarships and grants into education-cost calculations.

Features:

- Scholarship discovery
- Grant discovery
- Award tracking
- Tuition reduction calculations
- Remaining qualifying cost calculations

### Financial Aid Integration Plugin

Provides compatibility with external financial-aid systems.

Features:

- Financial-aid data integration
- Aid-package comparison
- Remaining tuition calculation
- Funding-source aggregation
- Eligibility-data exchange

### Workforce Data Plugin

Integrates employment and workforce datasets.

Features:

- Employment trends
- Occupation demand
- Labor-market indicators
- Career availability
- Regional workforce demand

### School Verification Plugin

Provides additional verification of educational institutions and programs.

Features:

- Accreditation information
- Program verification
- Tuition verification
- Program availability
- Institution status
- Data freshness monitoring

### Career Forecasting Plugin

Provides expanded predictive modeling capabilities.

Features:

- Career trajectory modeling
- Employment scenario modeling
- Industry trend analysis
- Geographic career projections
- Career transition analysis
- Model confidence reporting

Predictive outputs remain informational and cannot override the deterministic qualification engine.

### Student Pathway Planning Plugin

Provides expanded planning tools for students.

Features:

- Education pathway planning
- Career pathway visualization
- Program comparisons
- Cost comparisons
- Financing comparisons
- Alternative pathway discovery
- Completion planning

### Institution Integration Plugin

Allows schools and educational institutions to integrate FuturePathway into enrollment and financial planning systems.

Features:

- Program qualification checks
- Tuition verification
- Student pathway matching
- Financing eligibility checks
- Institutional reporting
- API integration

### Financial Institution Integration Plugin

Allows compatible financial institutions to implement FuturePathway financing.

Features:

- Loan origination integration
- Qualification verification
- Loan servicing integration
- Payment processing
- Repayment tracking
- Compliance reporting

### Analytics Plugin

Provides aggregated analytics without changing individual qualification rules.

Features:

- Program financing analysis
- Career-field analysis
- Education-cost trends
- Starting-salary trends
- Qualification statistics
- Program affordability analysis
- Aggregate reporting

## Core Decision Flow

FuturePathway implementations should follow a predictable sequence:

1. Identify the student's selected career field.
2. Retrieve the current average starting salary for that field.
3. Verify the salary-data version and effective date.
4. Calculate the three-year qualifying financing ceiling.
5. Identify the student's selected educational program.
6. Determine the full qualifying tuition.
7. Compare the full tuition against the financing ceiling.
8. Approve qualification when the financing ceiling covers the full qualifying tuition.
9. Decline qualification when the financing ceiling cannot cover the full qualifying tuition.
10. Provide the student with alternative qualifying education pathways when available.

## AI Decision Boundary

FuturePathway establishes a clear boundary between artificial intelligence and deterministic financial rules.

AI may:

- Recommend career fields
- Predict possible career pathways
- Identify educational programs
- Discover schools
- Compare programs
- Explain financing scenarios
- Identify alternative pathways
- Analyze available data

AI may not:

- Increase the financing ceiling
- Substitute a projected salary for the required starting salary
- Override the full-tuition requirement
- Approve a loan that fails the deterministic qualification rules
- Modify the interest rate
- Modify the repayment term
- Conceal the inputs used in a recommendation

## Example Qualification Model

A student selects a career field with an annually verified average starting salary of $50,000.

The three-year qualifying financing ceiling is $150,000.

If the student's qualifying educational program costs $140,000, the program meets the core financing requirement.

If the program costs $160,000, the program does not meet the core financing requirement and the financing request is declined.

The School Discovery Module may then identify alternative programs that meet the $150,000 financing ceiling.

## FuturePathway Philosophy

FuturePathway is designed around a simple principle:

**Investing in the future by investing in youth.**

Education financing should help students pursue viable career pathways without requiring them to assume an unpredictable level of debt. By establishing a transparent relationship between education cost and average starting salary, FuturePathway creates a deterministic framework for identifying educational opportunities that can be fully financed under defined terms.

The AI components enhance the student's ability to discover and evaluate opportunities, while the deterministic financing engine preserves consistency, transparency, and reproducibility.

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
  - [https://roxanneardary.com/futurepathway/](https://roxanneardary.com/futurepathway/)  

---

## License & Notice Requirements

FuturePathway is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.
By contributing to any Open Arsenal project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.
- FuturePathway specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.
  Any update that adds new contributors or modifies attribution should also update `notice.md`.
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
