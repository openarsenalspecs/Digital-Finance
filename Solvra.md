# Solvra

**A transparent engine for controlled amortization.**

Solvra is an open-source financial modeling specification and engine designed to provide transparent, deterministic loan modeling through controlled amortization rules. It introduces a structured approach to mortgage scenario analysis by applying a capped interest model, where the effective interest calculation period is limited to a maximum of 15 years and total interest is evenly distributed across the full life of the loan.

Unlike traditional amortization systems that create changing interest-to-principal payment curves, Solvra defines a predictable cost distribution framework. Loans can be modeled from 1 to 30 years while maintaining transparent payment calculations, consistent rules, and fully reproducible financial scenarios.

---

# Specification Overview

Solvra defines a modular architecture for building controlled amortization systems, affordability analysis tools, and financial scenario engines.

The specification separates required financial modeling capabilities into core modules while allowing optional extensions through plugin modules. Implementations may add additional functionality without altering the underlying Solvra calculation model.

---

# Core Modules

## 1. Controlled Amortization Core

The foundation of Solvra.

Responsibilities:

- Defines loan principal calculations
- Supports loan terms from 1 to 30 years
- Maintains deterministic payment calculations
- Generates complete amortization schedules
- Ensures consistent financial rule enforcement

---

## 2. Interest Cap Engine

Manages the Solvra interest limitation model.

Features:

- Implements the 15-year maximum effective interest window
- Prevents interest growth beyond the defined cap period
- Calculates total allowable interest exposure
- Maintains transparent interest calculation rules

Core rule:

- Loans shorter than 15 years use their actual term
- Loans longer than 15 years use the 15-year interest cap

---

## 3. Interest Distribution Engine

Controls how interest is allocated across the loan lifetime.

Features:

- Evenly distributes total interest across all payments
- Eliminates front-loaded interest structures
- Creates consistent monthly interest allocation
- Maintains predictable payment behavior

---

## 4. Payment Calculation Engine

Generates payment structures from defined loan parameters.

Features:

- Calculates monthly payment obligations
- Separates principal and interest allocation
- Supports variable loan terms
- Provides deterministic payment outputs

---

## 5. Scenario Simulation Core

Provides loan comparison and affordability modeling.

Features:

- Compares multiple loan terms
- Evaluates payment differences
- Models affordability scenarios
- Generates structured comparisons
- Supports financial planning workflows

---

## 6. Data & Reporting Core

Provides standardized outputs.

Features:

- Exportable amortization schedules
- Scenario reports
- Payment summaries
- Interest and principal breakdowns
- Machine-readable financial data formats

---

# Optional Plugin Modules

Solvra supports optional modules that extend functionality without modifying the core specification.

---

## AI Financial Advisor Plugin

Adds intelligent financial analysis.

Features:

- Natural language scenario explanations
- Payment optimization suggestions
- Loan comparison summaries
- Affordability insights

---

## Stress Testing Plugin

Adds financial resilience analysis.

Features:

- Interest rate variation testing
- Payment increase simulations
- Income change scenarios
- Long-term affordability modeling

---

## Refinancing Analysis Plugin

Provides refinancing simulations.

Features:

- Compare existing vs proposed loans
- Analyze payment changes
- Evaluate cost differences
- Model refinancing scenarios

---

## Real Estate Integration Plugin

Connects Solvra with property analysis systems.

Features:

- Property affordability calculations
- Purchase price modeling
- Down payment scenarios
- Closing cost analysis

---

## Tax & Expense Modeling Plugin

Adds additional ownership cost analysis.

Features:

- Property tax modeling
- Insurance projections
- Maintenance cost estimates
- Total ownership cost calculations

---

## Portfolio Analysis Plugin

Supports multiple-property scenarios.

Features:

- Multi-loan comparison
- Portfolio payment analysis
- Investment property modeling
- Long-term financial projections

---

# Design Principles

Solvra is built around:

## Transparency
All calculations are explicit, inspectable, and reproducible.

## Deterministic Modeling
Identical inputs always produce identical outputs.

## Modular Architecture
Core financial rules remain stable while optional capabilities can be added independently.

## Local-First Design
Implementations can operate without dependency on external financial services.

## Extensibility
Plugin modules allow organizations and developers to expand functionality without changing the core specification.

---

# Example Applications

Solvra can be used for:

- Mortgage affordability engines
- Loan comparison platforms
- Financial planning applications
- Real estate analysis systems
- Controlled lending simulations
- Educational financial modeling tools

---

## Technical Philosophy

Solvra is built on the principle of **deterministic financial modeling**:

- No stochastic assumptions
- No compounding-based payment shaping
- No hidden time-based yield expansion beyond defined caps

Every loan scenario produces a fully reproducible outcome based on explicit constraints.

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
  - [https://roxanneardary.com/solvra/](https://roxanneardary.com/solvra/)  

---

## License & Notice Requirements

Solvra is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to this project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.

---
