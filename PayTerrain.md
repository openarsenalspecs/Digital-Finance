# PayTerrain

**Every Freelancer, Every Region, One Map.**

PayTerrain is an open-source wage intelligence and regional compensation database designed to help businesses track, analyze, and compare the real wages paid to freelance workers.

PayTerrain provides a structured way to record compensation, calculate effective hourly rates, evaluate regional differences, apply cost-of-living and inflation adjustments, and compare actual compensation against regional and market benchmarks.

The platform is designed as a modular system. Core modules provide the essential wage, worker, regional, calculation, analytics, and data-management capabilities required by PayTerrain. Optional plugin modules extend the system with integrations, additional data sources, specialized analytics, reporting formats, and external services without requiring changes to the core platform.

## Core Objectives

- Track actual compensation paid to freelance workers.
- Calculate effective compensation based on hours and payments.
- Compare compensation across geographic regions.
- Account for regional cost-of-living differences.
- Support inflation-adjusted wage analysis.
- Compare actual compensation against benchmark data.
- Identify regional compensation disparities.
- Provide transparent and reproducible wage calculations.
- Maintain historical compensation records.
- Support business-level wage analysis without vendor lock-in.
- Provide an extensible architecture for additional data sources and integrations.

## Modular Architecture

PayTerrain is organized into independent modules with clearly defined responsibilities.

### Core Modules

Core modules contain the functionality required for the fundamental operation of PayTerrain.

### Plugin Modules

Plugin modules provide optional capabilities that can be installed, enabled, disabled, replaced, or developed independently from the core system.

This architecture allows organizations to deploy only the functionality they need while providing a framework for expanding PayTerrain without creating unnecessary dependencies within the core platform.

---

# Core Modules

## 1. Worker Module

The Worker Module manages the foundational records associated with freelance workers.

### Features

- Freelancer profiles
- Worker identifiers
- Professional roles
- Skills and specialties
- Experience classifications
- Worker location
- Primary work region
- Employment classification
- Historical worker records
- Worker status management
- Privacy-aware identifiers
- Relationship between workers and projects

The module is designed to separate worker identity data from compensation analytics where appropriate.

---

## 2. Compensation Module

The Compensation Module records the actual compensation paid to freelance workers.

### Features

- Payment records
- Gross compensation
- Payment dates
- Payment frequency
- Contract rates
- Project-based compensation
- Hourly compensation
- Fixed-fee compensation
- Milestone payments
- Bonuses and supplemental payments
- Currency tracking
- Compensation history
- Effective hourly rate calculations

The module provides the underlying transaction data used by PayTerrain's analytical systems.

---

## 3. Time & Work Module

The Time & Work Module records the amount of work associated with compensation.

### Features

- Hours worked
- Billable hours
- Non-billable hours
- Project hours
- Task hours
- Work periods
- Time-based compensation calculations
- Effective hourly wage calculations
- Compensation-to-time comparisons
- Historical work records

This module allows PayTerrain to distinguish between nominal contract rates and the actual compensation received relative to time worked.

---

## 4. Project & Contract Module

The Project & Contract Module connects workers, compensation, and work activity.

### Features

- Projects
- Contracts
- Contract types
- Project classifications
- Contract start and end dates
- Agreed rates
- Payment terms
- Project budgets
- Worker-project relationships
- Contract history
- Compensation associated with individual projects

---

## 5. Regional Data Module

The Regional Data Module provides the geographic framework used throughout PayTerrain.

### Features

- Countries
- States and provinces
- Counties
- Cities
- Metropolitan areas
- Postal regions
- Geographic identifiers
- Regional hierarchies
- Regional wage data
- Regional economic indicators
- Historical regional data
- Custom geographic regions

The regional model is designed to support different geographic structures rather than restricting PayTerrain to a single country's administrative system.

---

## 6. Cost of Living Module

The Cost of Living Module evaluates compensation relative to regional living costs.

### Features

- Regional cost-of-living indexes
- Housing cost indexes
- Transportation cost indexes
- Food cost indexes
- Utility cost indexes
- Healthcare cost indexes
- Composite regional indexes
- Regional purchasing-power comparisons
- Historical cost-of-living data
- Custom cost-of-living indexes

Users can compare nominal compensation against the economic conditions of the region where the freelancer works.

---

## 7. Inflation & Real Wage Module

The Inflation & Real Wage Module converts historical compensation into comparable purchasing-power values.

### Features

- Inflation indexes
- Historical inflation data
- Inflation-adjusted compensation
- Real wage calculations
- Nominal versus real wage comparisons
- Purchasing-power analysis
- Historical wage comparisons
- Configurable base periods

This module makes it possible to distinguish increases in nominal pay from actual increases in purchasing power.

---

## 8. Benchmark Module

The Benchmark Module provides comparative wage intelligence.

### Features

- Regional wage benchmarks
- Role-based benchmarks
- Skill-based benchmarks
- Experience-based benchmarks
- Industry benchmarks
- Hourly wage comparisons
- Project-rate comparisons
- Benchmark variance calculations
- Above-market compensation identification
- Below-market compensation identification
- Custom organizational benchmarks

Benchmark sources can be configured independently from the core compensation database.

---

## 9. Wage Calculation Module

The Wage Calculation Module provides standardized calculations across the platform.

### Features

- Effective hourly wage
- Gross wage calculations
- Regional wage adjustments
- Cost-of-living adjusted wages
- Inflation-adjusted wages
- Real purchasing-power calculations
- Benchmark variance
- Percentage differences
- Compensation trends
- Regional compensation differentials

Calculations should be deterministic, documented, and reproducible.

---

## 10. Analytics Module

The Analytics Module transforms PayTerrain data into actionable wage intelligence.

### Features

- Wage trend analysis
- Regional comparisons
- Worker-level analysis
- Role-level analysis
- Skill-level analysis
- Project-level analysis
- Compensation distributions
- Wage variance analysis
- Regional pay gaps
- Benchmark comparisons
- Historical comparisons
- Compensation growth analysis

---

## 11. Visualization Module

The Visualization Module provides graphical representations of compensation data.

### Features

- Regional wage maps
- Wage comparison charts
- Compensation trend charts
- Regional heat maps
- Wage distribution charts
- Benchmark comparison charts
- Cost-of-living comparisons
- Real versus nominal wage charts
- Interactive dashboards
- Filterable visualizations

---

## 12. Reporting Module

The Reporting Module produces structured compensation reports.

### Features

- Wage reports
- Regional compensation reports
- Benchmark reports
- Cost-of-living reports
- Real wage reports
- Historical compensation reports
- Executive summaries
- Custom report filters
- Scheduled reporting
- Data export

Supported export formats can include CSV, JSON, spreadsheet, and PDF through core functionality or plugins.

---

## 13. Data Management Module

The Data Management Module manages the integrity and lifecycle of PayTerrain data.

### Features

- Data import
- Data export
- Validation
- Duplicate detection
- Data normalization
- Historical records
- Data versioning
- Import logs
- Data quality checks
- Backup support
- Restore support
- Dataset metadata

---

## 14. API Module

The API Module provides programmatic access to PayTerrain.

### Features

- REST API
- Authentication
- Authorization
- Worker endpoints
- Compensation endpoints
- Project endpoints
- Regional data endpoints
- Benchmark endpoints
- Analytics endpoints
- Reporting endpoints
- Dataset endpoints
- API documentation

The API is designed to allow external applications to consume PayTerrain data without requiring direct database access.

---

## 15. Administration Module

The Administration Module manages system configuration and organizational controls.

### Features

- User management
- Role management
- Permissions
- Organization settings
- Regional configuration
- Benchmark configuration
- Dataset management
- Plugin management
- System configuration
- Audit logging

---

# Plugin Modules

Plugin modules extend PayTerrain without modifying the core architecture.

Plugins may be developed by the PayTerrain project, businesses, data providers, or the broader open-source community.

## Time Tracking Plugins

Optional integrations with external time-tracking platforms.

### Potential Features

- Import tracked hours
- Synchronize projects
- Synchronize workers
- Automatic compensation calculations
- Scheduled synchronization
- Import validation

---

## Payment Platform Plugins

Connect PayTerrain to external payment systems.

### Potential Features

- Payment imports
- Transaction reconciliation
- Payment status synchronization
- Currency conversion
- Payment history synchronization

---

## Wage Dataset Plugins

Allow external wage datasets to be integrated into PayTerrain.

### Potential Features

- Government wage datasets
- Regional labor statistics
- Industry datasets
- Professional wage surveys
- Community-contributed datasets
- Custom organizational datasets

Each dataset plugin should identify its source, methodology, geographic coverage, update frequency, and licensing requirements.

---

## Cost of Living Dataset Plugins

Provide additional regional economic data.

### Potential Features

- Housing indexes
- Transportation indexes
- Food indexes
- Utility indexes
- Regional purchasing-power indexes
- Historical cost-of-living datasets

---

## Inflation Data Plugins

Connect PayTerrain to external inflation datasets.

### Potential Features

- Consumer price indexes
- Regional inflation indexes
- Historical inflation data
- Automatic dataset updates
- Custom inflation indexes

---

## Currency Plugins

Provide international compensation support.

### Potential Features

- Currency conversion
- Historical exchange rates
- Multi-currency compensation
- Base-currency reporting
- Currency normalization

---

## Geographic Data Plugins

Extend PayTerrain's geographic capabilities.

### Potential Features

- Geographic boundaries
- Postal regions
- Metropolitan areas
- Census regions
- International geographic systems
- Geographic visualization data

---

## Mapping Plugins

Provide additional mapping functionality.

### Potential Features

- Interactive wage maps
- Regional overlays
- Geographic wage comparisons
- Cost-of-living map layers
- Benchmark map layers
- Custom geographic visualization

---

## Database Plugins

Allow organizations to integrate alternative database systems or external data stores.

### Potential Features

- Additional SQL databases
- Distributed databases
- Data warehouses
- Read-only external datasets
- Organizational data stores

---

## Reporting Plugins

Extend reporting and export capabilities.

### Potential Features

- Spreadsheet exports
- PDF reports
- Presentation exports
- Custom report templates
- Automated reports
- Organization-specific reports

---

## Notification Plugins

Provide alerts based on PayTerrain events and analytics.

### Potential Features

- Wage threshold alerts
- Benchmark variance alerts
- Dataset update notifications
- Report notifications
- Administrative notifications
- API event notifications

---

## Business Intelligence Plugins

Connect PayTerrain to external analytics systems.

### Potential Features

- Business intelligence dashboards
- Data warehouse synchronization
- Custom analytics pipelines
- External visualization systems
- Scheduled data exports

---

## AI & Analytics Plugins

Optional AI functionality can extend PayTerrain without making artificial intelligence a core dependency.

### Potential Features

- Wage trend analysis
- Compensation anomaly detection
- Regional compensation forecasting
- Dataset quality analysis
- Natural-language reporting
- Compensation pattern discovery
- Automated analytical summaries

AI plugins should remain optional and should not replace transparent underlying calculations.

---

# Data Architecture

PayTerrain uses a structured relational data model designed around the relationships between:

- Workers
- Organizations
- Projects
- Contracts
- Work records
- Compensation records
- Regions
- Economic datasets
- Benchmarks
- Calculations
- Reports
- Data sources
- Plugins

The architecture should maintain clear separation between source data, calculated values, external datasets, and analytical outputs.

---

# Data Provenance

PayTerrain is designed to make wage analysis traceable.

Each externally sourced dataset should maintain metadata describing:

- Source
- Publisher
- Dataset name
- Collection date
- Effective date
- Geographic coverage
- Methodology
- Update frequency
- License
- Version
- Transformation history

Calculated wage values should be traceable to the underlying compensation records and adjustment datasets used to produce them.

---

# Privacy & Data Protection

PayTerrain may contain sensitive compensation information and should provide privacy-conscious data handling.

### Features

- Role-based access controls
- Permission management
- Data minimization
- Configurable worker identifiers
- Audit logging
- Secure API access
- Dataset access controls
- Configurable retention policies
- Separation of identifying and analytical data where appropriate

Organizations are responsible for configuring and operating PayTerrain in accordance with applicable privacy and employment laws.

---

# Technology Stack

## Core Database

- PostgreSQL

## Backend

- Python
- FastAPI
- REST API

Alternative backend implementations may be supported through the modular architecture.

## Frontend

- React
- JavaScript or TypeScript
- Chart.js or Recharts
- Interactive dashboard components

## Data Analysis

- Python
- Pandas
- NumPy

## Deployment

- Docker
- Docker Compose
- Linux-compatible environments
- Self-hosted infrastructure

## Development Infrastructure

- Git
- GitLab
- Automated testing
- Continuous integration
- API documentation

---

# Open Data Architecture

PayTerrain is designed to support multiple wage and economic data sources rather than depending on a single provider.

Potential data sources may include:

- Government labor statistics
- Government economic datasets
- Regional cost-of-living datasets
- Inflation datasets
- Industry wage datasets
- Organization-provided datasets
- Community-contributed datasets

Every external dataset should retain appropriate source attribution and licensing information.

---

# Plugin Development

Plugins should interact with PayTerrain through documented interfaces rather than modifying core modules whenever possible.

A plugin should define:

- Plugin name
- Version
- Purpose
- Dependencies
- Data inputs
- Data outputs
- API interfaces
- Configuration requirements
- Permissions
- Data source information
- Licensing information

Plugins should fail independently where possible so that a disabled or unavailable plugin does not compromise core PayTerrain functionality.

---

# Extensibility

The modular architecture allows PayTerrain to expand into additional wage intelligence capabilities without requiring fundamental changes to the platform.

Potential future modules include:

- Industry-specific compensation analysis
- International freelance markets
- Contractor rate forecasting
- Compensation equity analysis
- Regional economic forecasting
- Workforce planning
- Compensation scenario modeling
- Organization-wide wage policy analysis

---

# Deployment Models

PayTerrain is designed to support multiple deployment models.

### Self-Hosted

Organizations can deploy PayTerrain on their own infrastructure and maintain complete control over their data.

### Private Organizational Deployment

Businesses can operate private PayTerrain installations for internal compensation analysis.

### Community Data Deployment

Organizations and communities can operate shared installations containing appropriately licensed and anonymized wage datasets.

### Development Deployment

Developers can run PayTerrain locally using containerized development environments.

---

# Project Principles

PayTerrain is built around several foundational principles:

- **Transparency:** Wage calculations should be understandable and traceable.
- **Regional Context:** Compensation should be evaluated in the context of geography.
- **Data Provenance:** External datasets should identify where their information originated.
- **Modularity:** Optional functionality should not unnecessarily burden the core platform.
- **Interoperability:** PayTerrain should work with external systems through documented interfaces.
- **Privacy:** Compensation information should be handled responsibly.
- **Vendor Independence:** Organizations should retain control over their data and deployment.
- **Open Source:** The platform should remain accessible for inspection, modification, and community development.
- **Reproducibility:** Analytical results should be based on documented calculations and identifiable data sources.

---

# Getting Started

PayTerrain is intended to be deployable in a self-hosted environment.

Initial development setup should include:

1. Clone the repository.
2. Install the required development dependencies.
3. Configure the application environment.
4. Initialize the PostgreSQL database.
5. Run database migrations.
6. Start the backend API.
7. Start the frontend application.
8. Enable required core modules.
9. Configure optional plugins as needed.

Detailed installation and development instructions should be maintained in the project documentation.

---

# Contributing

Contributions are welcome across the PayTerrain ecosystem, including:

- Core development
- Plugin development
- Database design
- Wage dataset integration
- Regional data
- Documentation
- Testing
- Data validation
- Analytics
- Visualization
- Security improvements
- Accessibility improvements

See `CONTRIBUTING.md` for contribution requirements and project guidelines.


---

# Project

**PayTerrain**

**Every Freelancer, Every Region, One Map.**

PayTerrain provides an open-source foundation for understanding freelance compensation through real wage tracking, regional comparison, economic adjustment, benchmark analysis, and transparent wage intelligence.

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
  - [https://roxanneardary.com/payterrain/](https://roxanneardary.com/payterrain/)

---

## License & Notice Requirements

PayTerrain is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.  
- PayTerrain specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a merge request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
