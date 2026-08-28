# CashOps
**Earn More From Cash Without Losing Control of It.**
- HTML Mirror:  [https://roxanneardary.com/cashops-specification/](https://roxanneardary.com/cashops-specification/)  

---

## Specification

**CashOps** is a modular AI personal finance optimization specification designed to help individuals earn more from available cash without losing control of it. CashOps continuously evaluates where money should be held, when it should move, how much liquidity must remain available, whether obligations should be funded or prepaid, and where eligible cash can earn appropriate risk-free or principal-protected yield.

## Purpose

CashOps transforms personal cash management into continuous financial operations. Instead of treating account balances as passive cash, CashOps evaluates every dollar according to its purpose, timing, liquidity requirements, obligations, potential yield, and user-defined financial policies.

The system is designed to optimize cash allocation while prioritizing payment certainty, liquidity, principal protection, user control, privacy, security, explainability, and long-term financial objectives.

## Design Principles

- Modular architecture
- AI-assisted financial optimization
- Dollar-level financial allocation
- Continuous cash optimization
- Payment-aware money movement
- Prepayment-aware financial planning
- Risk-free or appropriately protected yield optimization
- Deterministic safety controls
- Human-in-the-loop governance
- User-defined financial policies
- Local-first operation where practical
- Privacy-preserving architecture
- Vendor-neutral financial infrastructure
- Explainable recommendations
- Auditable financial decisions
- Fail-safe operation
- Separation of intelligence from execution
- No optimization action may compromise a protected financial obligation

## Core Operating Model

CashOps continuously evaluates:

- Where is every dollar?
- What is every dollar for?
- When will every dollar be needed?
- How much must remain liquid?
- Can available cash safely earn more while waiting?
- Should money move?
- Where should it move?
- When should it move?
- When must it return?
- Should an obligation be prepaid?
- What are the costs and risks of moving the money?
- Does the action comply with the user's financial policies?
- Does the action support long-term financial objectives?

CashOps shall optimize only after these conditions have been evaluated.

---

## Core Modules

### Financial State Module

The Financial State Module maintains the current representation of the user's financial position.

Features:

- Track connected financial accounts.
- Track account balances.
- Track available balances.
- Track pending balances.
- Track reserved funds.
- Track committed funds.
- Track restricted funds.
- Track account ownership.
- Track account-specific rules.
- Track account requirements.
- Track interest rates.
- Track yields.
- Track fees.
- Track minimum balances.
- Track withdrawal restrictions.
- Track settlement characteristics.
- Distinguish immediately available funds from funds subject to settlement or withdrawal restrictions.
- Identify idle cash.
- Identify underutilized cash.
- Maintain historical financial states.
- Maintain provenance for financial state information.

### Dollar Allocation Module

The Dollar Allocation Module assigns a financial purpose and position to available funds.

Features:

- Assign a purpose to every available dollar.
- Classify funds according to current obligations.
- Classify funds according to future obligations.
- Identify immediate liquidity requirements.
- Identify obligation reserves.
- Identify emergency reserves.
- Identify funds available for yield optimization.
- Identify funds suitable for prepayment.
- Identify funds designated for financial goals.
- Identify funds designated for long-term wealth.
- Identify funds designated for continuity objectives.
- Continuously reassess dollar allocation states.
- Prevent committed funds from being treated as available funds.
- Maintain an auditable allocation state.

### Cash Flow Forecasting Module

The Cash Flow Forecasting Module predicts future financial conditions.

Features:

- Forecast expected income.
- Forecast recurring income.
- Forecast recurring expenses.
- Forecast known bills.
- Forecast subscriptions.
- Forecast debt payments.
- Forecast taxes.
- Forecast periodic obligations.
- Forecast irregular expenses.
- Incorporate user-defined future expenses.
- Calculate projected account balances.
- Calculate projected cash surpluses.
- Calculate projected cash shortfalls.
- Calculate when funds become available.
- Calculate when funds will be required.
- Model multiple cash flow scenarios.
- Update forecasts as new financial information becomes available.
- Identify changes that materially affect projected liquidity.

### Obligation Management Module

The Obligation Management Module maintains the user's financial obligations and their associated requirements.

Features:

- Discover financial obligations.
- Track one-time obligations.
- Track recurring obligations.
- Track scheduled obligations.
- Track payment amounts.
- Track payment due dates.
- Track expected payment dates.
- Track payment accounts.
- Track payment frequency.
- Track payment windows.
- Track payment priority.
- Track payment status.
- Track upcoming payment clusters.
- Track changes in payment amounts.
- Track changes in payment dates.
- Associate obligations with required funding accounts.
- Calculate future funding requirements.

### Liquidity Module

The Liquidity Module determines how much money must remain accessible.

Features:

- Calculate dynamic liquidity requirements.
- Maintain minimum cash balances.
- Maintain payment reserves.
- Maintain emergency reserves.
- Maintain settlement buffers.
- Maintain obligation-specific liquidity.
- Calculate excess liquidity.
- Identify funds available for temporary allocation.
- Recalculate liquidity requirements continuously.
- Increase liquidity requirements when uncertainty increases.
- Reduce liquidity requirements when obligations are satisfied.
- Support account-specific liquidity policies.
- Support user-defined liquidity thresholds.
- Support conservative, balanced, and aggressive liquidity policies.

### Yield Optimization Module

The Yield Optimization Module identifies opportunities to improve the productive return of eligible cash.

Features:

- Identify eligible risk-free destinations.
- Identify appropriately protected cash destinations.
- Compare available yields.
- Compare liquidity characteristics.
- Compare maturity periods.
- Compare withdrawal restrictions.
- Compare minimum balance requirements.
- Compare fees.
- Compare expected net yield.
- Calculate incremental yield.
- Calculate opportunity cost of idle cash.
- Calculate expected yield over a defined holding period.
- Account for transfer costs.
- Account for settlement requirements.
- Account for liquidity requirements.
- Account for payment timing.
- Account for configured tax considerations.
- Distinguish principal protection from investment performance.
- Require explicit classification of protection characteristics.
- Avoid selecting a destination solely because it has the highest nominal yield.

### Money Movement Module

The Money Movement Module determines whether, when, where, and how much money should move.

Features:

- Recommend when money should move.
- Recommend where money should move.
- Recommend how much money should move.
- Recommend when money should return.
- Calculate transfer lead times.
- Calculate settlement requirements.
- Sequence multiple movements.
- Coordinate movements with payment schedules.
- Coordinate movements with prepayment decisions.
- Consolidate compatible movements.
- Minimize unnecessary transfers.
- Minimize transfer fees.
- Minimize operational friction.
- Support cash sweeps.
- Support automated movements within user-defined policies.
- Maintain complete movement provenance.
- Recalculate movement recommendations when financial conditions change.

### PrePayGuard Integration Module

The PrePayGuard Integration Module provides payment assurance, payment timing protection, prepayment analysis, and obligation safety.

Features:

- Integrate PrePayGuard as a core financial protection layer.
- Discover financial obligations.
- Maintain a bill and obligation calendar.
- Track payment deadlines.
- Track payment amounts.
- Track payment accounts.
- Track payment schedules.
- Track recurring payment patterns.
- Track payment status.
- Determine payment readiness.
- Calculate required payment balances.
- Calculate payment reserves.
- Calculate payment buffers.
- Calculate minimum safe balances.
- Verify available funds before payment.
- Verify expected funds at payment execution time.
- Calculate payment safety windows.
- Calculate transfer lead times.
- Calculate settlement lead times.
- Account for weekends.
- Account for banking holidays.
- Account for transfer delays.
- Account for settlement uncertainty.
- Establish return-to-account deadlines.
- Prevent optimization actions from jeopardizing payments.
- Prevent transfers that could cause insufficient funds.
- Prevent allocations that could create payment timing risk.
- Suspend optimization when payment information is stale or uncertain.
- Identify payment timing conflicts.
- Identify competing obligations.
- Identify liquidity gaps.
- Calculate payment risk.
- Assign confidence levels to payment-readiness decisions.
- Prioritize mandatory obligations.
- Prioritize time-sensitive obligations.
- Sequence payment funding.
- Recommend when an obligation should be funded.
- Recommend how much should be funded.
- Recommend which account should fund an obligation.
- Recommend when funds should return to a payment account.
- Pre-fund future obligations when appropriate.
- Maintain obligation-specific reserves.
- Maintain aggregate payment reserves.
- Detect underfunded obligations.
- Identify obligations that may be prepaid.
- Compare prepayment benefits against continued cash yield.
- Calculate potential interest savings where applicable.
- Calculate potential early-payment benefits.
- Calculate potential fees or penalties.
- Determine whether prepayment improves the user's financial position.
- Determine the optimal prepayment date.
- Determine the optimal prepayment amount.
- Monitor scheduled payments.
- Monitor pending payments.
- Monitor completed payments.
- Monitor failed payments.
- Monitor delayed payments.
- Monitor rejected payments.
- Monitor duplicate payments.
- Monitor unexpected payments.
- Monitor payment amount changes.
- Monitor payment account changes.
- Confirm successful settlement where supported.
- Detect unusual payment amounts.
- Detect unusual payment frequency.
- Detect duplicate obligations.
- Detect unexpected recurring payments.
- Detect missing expected payments.
- Detect anomalous payment timing.
- Handle failed transfers.
- Handle delayed transfers.
- Handle failed payments.
- Handle insufficient funds.
- Handle unavailable accounts.
- Handle stale financial information.
- Handle unexpected obligations.
- Recalculate affected optimization strategies.
- Provide recovery recommendations.

PrePayGuard shall provide deterministic payment-safety states including:

- SAFE_TO_MOVE
- SAFE_TO_MOVE_WITH_RETURN_DATE
- SAFE_TO_PREPAY
- SAFE_TO_HOLD
- SAFE_TO_ALLOCATE
- WAIT
- PAYMENT_RISK
- INSUFFICIENT_LIQUIDITY
- TRANSFER_UNCERTAIN
- PAYMENT_DATA_STALE
- HUMAN_APPROVAL_REQUIRED

CashOps shall not execute an optimization action that conflicts with a protected PrePayGuard state.  

[https://roxanneardary.com/prepayguard/](https://roxanneardary.com/prepayguard/)  

### Nexa Integration Module

The Nexa Integration Module provides long-term financial continuity and strategic financial objectives.

Features:

- Integrate Nexa as the long-term financial continuity layer.
- Incorporate long-term financial objectives into tactical cash decisions.
- Distinguish short-term liquidity from long-term financial purpose.
- Preserve funds designated for long-term objectives.
- Support wealth-preservation policies.
- Support continuity objectives.
- Support future-generation allocations.
- Support estate-related objectives where configured.
- Prevent short-term yield optimization from overriding long-term policies.
- Incorporate long-term consequences into allocation decisions.
- Maintain separation between tactical optimization and strategic financial continuity.

[https://roxanneardary.com/nexa/](https://roxanneardary.com/nexa/)  

### Soluna Finance OS Integration Module

The Soluna Finance OS Integration Module provides financial orchestration and execution infrastructure.

Features:

- Integrate with Soluna Finance OS.
- Use Soluna-compatible financial account abstractions.
- Support financial orchestration.
- Support insured liquidity strategies where applicable.
- Provide CashOps recommendations to the Soluna execution layer.
- Separate optimization logic from execution infrastructure.
- Support multiple financial institutions.
- Support multiple execution providers.
- Avoid dependency on a single financial institution.
- Coordinate account allocation through Soluna.
- Permit Soluna to execute authorized CashOps strategies.
- Maintain separation between decision-making and execution.
- Preserve user-defined authorization boundaries.

[https://roxanneardary.com/soluna-finance-os/](https://roxanneardary.com/soluna-finance-os/)  

### Financial Policy Module

The Financial Policy Module allows users to define the rules under which CashOps operates.

Features:

- Define minimum cash balances.
- Define minimum liquidity.
- Define maximum transfer amounts.
- Define approved destinations.
- Define prohibited destinations.
- Define minimum yield thresholds.
- Define minimum expected-benefit thresholds.
- Define payment buffers.
- Define emergency reserves.
- Define prepayment rules.
- Define automation permissions.
- Define human approval requirements.
- Define acceptable holding periods.
- Define risk-free asset requirements.
- Define account-specific rules.
- Define financial goal priorities.
- Apply policies consistently across recommendations and execution.

### Decision Engine Module

The Decision Engine Module evaluates competing financial actions and determines the most appropriate action within defined constraints.

The optimization objective shall be:

**Maximize expected safe financial return subject to financial safety, liquidity, payment, policy, and long-term objective constraints.**

Features:

- Evaluate competing financial actions.
- Rank potential actions.
- Calculate expected benefits.
- Calculate expected costs.
- Calculate incremental yield.
- Calculate opportunity cost.
- Calculate timing risk.
- Calculate liquidity exposure.
- Calculate payment exposure.
- Evaluate prepayment opportunities.
- Evaluate alternative money movement dates.
- Evaluate alternative allocation amounts.
- Evaluate alternative destinations.
- Apply user-defined policies.
- Apply PrePayGuard constraints.
- Apply Nexa strategic constraints.
- Apply Soluna execution constraints.
- Reject actions that violate hard constraints.
- Produce explainable recommendations.
- Identify assumptions.
- Identify uncertainties.
- Assign confidence levels.

### AI Agent Module

The AI Agent Module coordinates specialized financial intelligence.

Supported agents may include:

- Cash Flow Agent
- Obligation Agent
- Payment Agent
- Prepayment Agent
- Liquidity Agent
- Yield Agent
- Money Movement Agent
- Financial Policy Agent
- Scenario Agent
- Monitoring Agent
- Explanation Agent
- Nexa Continuity Agent
- Soluna Orchestration Agent

AI agents shall provide analysis and recommendations to the controlled Decision Engine.

Individual agents shall not independently bypass deterministic financial safety rules, payment protection rules, liquidity requirements, or user-defined restrictions.

### Scenario Analysis Module

The Scenario Analysis Module evaluates potential financial conditions before actions are taken.

Features:

- Model alternative movement dates.
- Model alternative allocation amounts.
- Model alternative yield destinations.
- Model prepayment versus continued yield.
- Model unexpected expenses.
- Model delayed income.
- Model delayed transfers.
- Model changes in interest rates.
- Model changes in payment timing.
- Model emergency conditions.
- Compare competing financial strategies.
- Estimate expected yield.
- Estimate liquidity exposure.
- Estimate payment exposure.
- Identify the safest strategy that meets user objectives.

### Financial Opportunity Module

The Financial Opportunity Module identifies opportunities to improve financial efficiency.

Features:

- Detect idle cash.
- Detect low-yield balances.
- Detect higher-yield alternatives.
- Detect expiring promotional rates.
- Detect cash sweep opportunities.
- Detect laddering opportunities.
- Detect prepayment opportunities.
- Detect early-payment discounts.
- Detect unnecessary account fees.
- Detect unnecessary transfer fees.
- Detect inefficient account allocations.
- Detect opportunities to consolidate movements.
- Detect opportunities to improve financial efficiency without increasing permitted risk.

### Fee Optimization Module

The Fee Optimization Module incorporates financial costs into optimization decisions.

Features:

- Detect account fees.
- Detect transfer fees.
- Detect maintenance fees.
- Detect minimum-balance penalties.
- Calculate fee impact on yield.
- Identify avoidable costs.
- Incorporate fees into movement decisions.
- Incorporate fees into prepayment decisions.
- Incorporate fees into account allocation decisions.

### Tax-Aware Module

The Tax-Aware Module incorporates configured tax considerations into financial optimization.

Features:

- Track configured tax considerations.
- Estimate after-tax yield where sufficient information is available.
- Compare gross and estimated net yield.
- Distinguish taxable and tax-advantaged accounts.
- Incorporate user-provided tax policies.
- Support tax-aware allocation calculations.
- Avoid unsupported tax determinations.
- Support integration with optional tax optimization modules.

### Goal Allocation Module

The Goal Allocation Module coordinates available cash with defined financial objectives.

Features:

- Define financial goals.
- Assign target amounts.
- Assign target dates.
- Allocate funds toward goals.
- Track goal progress.
- Protect goal-designated funds.
- Incorporate goal timing into cash flow forecasts.
- Incorporate goals into yield optimization.
- Recalculate allocations when goals change.

### Debt Coordination Module

The Debt Coordination Module incorporates debt obligations into cash optimization.

Features:

- Track debt obligations.
- Track required payments.
- Track debt interest rates.
- Preserve required debt-payment liquidity.
- Compare debt costs against available cash yields.
- Identify potential debt prepayment opportunities.
- Compare debt prepayment against risk-free yield.
- Support user-defined debt optimization policies.

### Emergency Mode Module

The Emergency Mode Module protects financial stability when normal optimization conditions are disrupted.

Features:

- Detect projected liquidity emergencies.
- Detect projected payment shortfalls.
- Suspend discretionary optimization.
- Increase required liquidity reserves.
- Prevent nonessential transfers.
- Prioritize upcoming obligations.
- Return eligible funds to liquid accounts where appropriate.
- Notify the user of projected shortfalls.
- Provide recovery recommendations.
- Resume normal optimization after defined safety conditions are restored.

### Monitoring Module

The Monitoring Module continuously observes financial conditions.

Features:

- Monitor account balances.
- Monitor transactions.
- Monitor obligations.
- Monitor payment status.
- Monitor transfer status.
- Monitor settlement status.
- Monitor yields.
- Monitor liquidity requirements.
- Monitor financial policies.
- Monitor execution outcomes.
- Detect material deviations from expected conditions.
- Trigger reoptimization when material conditions change.

### Notification Module

The Notification Module communicates material financial conditions and recommendations.

Features:

- Notify users of meaningful yield opportunities.
- Notify users of upcoming obligations.
- Notify users of payment-risk conditions.
- Notify users when cash becomes available for optimization.
- Notify users when funds should return to a payment account.
- Notify users of prepayment opportunities.
- Notify users of failed or delayed transfers.
- Notify users of failed payments.
- Notify users of material yield changes.
- Notify users when emergency mode activates.
- Support configurable notification thresholds.

### Explainability Module

The Explainability Module makes financial recommendations understandable and reviewable.

Every material recommendation should explain:

- What money should move.
- How much should move.
- Where it should move.
- When it should move.
- When it should return.
- Why the movement is recommended.
- Which obligations were evaluated.
- Which liquidity requirements were evaluated.
- Whether prepayment was considered.
- What additional yield is expected.
- What fees were considered.
- What risks were identified.
- Which user policies were applied.
- Which assumptions were used.
- What conditions could change the recommendation.

### Audit and Provenance Module

The Audit and Provenance Module records the history of financial decisions and actions.

Features:

- Record financial state changes.
- Record obligation discovery.
- Record payment calculations.
- Record payment-safety determinations.
- Record prepayment evaluations.
- Record yield calculations.
- Record liquidity calculations.
- Record recommendations.
- Record policy evaluations.
- Record approvals.
- Record execution requests.
- Record execution results.
- Record failed actions.
- Record rejected actions.
- Record user overrides.
- Record modules involved in each decision.
- Preserve recommendation provenance.
- Support independent review of financial decisions.

### Security Module

The Security Module protects financial information and execution authority.

Features:

- Encrypt sensitive financial information.
- Apply least-privilege access controls.
- Separate read permissions from execution permissions.
- Separate account access from transaction authority.
- Require explicit authorization for financial connections.
- Support authorization revocation.
- Protect financial credentials and tokens.
- Prevent unauthorized module access.
- Log security events.
- Support secure secrets management.
- Fail closed when authorization cannot be verified.

### Privacy Module

The Privacy Module minimizes unnecessary exposure of financial information.

Features:

- Support local financial data processing where practical.
- Minimize unnecessary transmission of financial data.
- Support encrypted local financial records.
- Support user-controlled financial data storage.
- Support configurable data retention.
- Support privacy-preserving integrations.
- Avoid unnecessary centralized financial data storage.
- Separate financial identity from optimization logic where practical.

### Reliability Module

The Reliability Module ensures that CashOps behaves safely when financial information or infrastructure becomes unreliable.

Features:

- Detect stale account data.
- Detect missing transactions.
- Detect conflicting balances.
- Detect delayed transactions.
- Detect failed transfers.
- Detect unavailable financial institutions.
- Detect incomplete payment information.
- Suspend optimization when critical information is unreliable.
- Avoid acting on stale forecasts.
- Provide graceful degradation.
- Maintain deterministic fallback behavior.
- Preserve user control during service failures.

### Autonomy and Human Control Module

The Autonomy and Human Control Module defines how much authority CashOps has to act.

#### Advisory Mode

- Provide recommendations only.
- Do not initiate financial movement automatically.

#### Supervised Mode

- Prepare financial movements.
- Require user approval before execution.

#### Policy-Automated Mode

- Execute actions that satisfy predefined user policies.
- Require approval for actions outside authorized policy boundaries.

#### Emergency Mode

- Suspend discretionary optimization.
- Protect liquidity.
- Protect upcoming obligations.
- Prioritize payment readiness.
- Prevent unnecessary financial movements.

Features:

- Allow users to pause automation.
- Allow users to override recommendations.
- Allow users to establish permanent restrictions.
- Allow users to establish temporary restrictions.
- Record the policy responsible for automated actions.
- Require appropriate authorization for high-impact actions.

### Rule-Based Safety Module

The Rule-Based Safety Module separates deterministic financial safety from AI reasoning.

Features:

- Evaluate hard constraints before execution.
- Prevent AI recommendations from bypassing payment rules.
- Prevent AI recommendations from bypassing liquidity requirements.
- Prevent AI recommendations from bypassing user policies.
- Prevent unsupported assumptions from triggering financial movement.
- Detect stale financial information.
- Fail safely when required information is unavailable.
- Suspend automated optimization when safety cannot be established.

---

## Optional Plugin Modules

CashOps shall support optional plugin modules that extend functionality without requiring changes to the core financial optimization architecture.

### Investment Coordination Plugin

- Coordinate cash optimization with investment allocations.
- Identify cash that should remain outside investment portfolios.
- Coordinate investment schedules with liquidity requirements.
- Distinguish investment assets from immediately available cash.
- Prevent investment allocations from being incorrectly treated as liquid reserves.

### Treasury Management Plugin

- Support advanced personal treasury management.
- Support cash ladders.
- Support maturity scheduling.
- Support liquidity planning.
- Support larger-scale household treasury operations.
- Coordinate multiple cash instruments.

### Household Finance Plugin

- Coordinate authorized household finances.
- Track shared obligations.
- Maintain individual ownership boundaries.
- Support shared financial policies.
- Support shared financial goals.
- Coordinate household liquidity.

### Business Finance Plugin

- Separate business and personal cash operations.
- Track business obligations.
- Track payroll reserves.
- Track business tax reserves.
- Optimize business cash independently.
- Maintain business-specific policies.

### Subscription Optimization Plugin

- Identify recurring subscriptions.
- Detect duplicate services.
- Identify potentially unused subscriptions.
- Track recurring cost changes.
- Calculate potential savings.
- Incorporate recurring savings into cash flow forecasts.

### Financial Education Plugin

- Explain financial concepts.
- Explain yield calculations.
- Explain liquidity.
- Explain payment timing.
- Explain prepayment tradeoffs.
- Explain financial optimization decisions.

### Simulation Plugin

- Test financial policies before activation.
- Simulate cash flow scenarios.
- Simulate yield strategies.
- Simulate prepayment strategies.
- Simulate payment disruptions.
- Simulate emergency conditions.
- Compare historical and hypothetical strategies.

### Financial Institution Plugin

- Connect supported financial institutions.
- Normalize account information.
- Normalize transaction information.
- Provide account-specific capabilities.
- Provide transfer capabilities.
- Maintain provider-specific integration boundaries.

### Yield Data Plugin

- Retrieve eligible yield information.
- Monitor changes in available rates.
- Normalize yield data.
- Track effective dates.
- Track maturity requirements.
- Track liquidity characteristics.
- Provide yield information to the Yield Optimization Module.

### Calendar Plugin

- Synchronize financial obligations with authorized calendars.
- Track payment dates.
- Track financial events.
- Track recurring obligations.
- Provide scheduling information to the Obligation Management Module.

### Tax Optimization Plugin

- Provide advanced tax-aware calculations.
- Compare after-tax financial outcomes.
- Coordinate tax reserves.
- Coordinate tax-related obligations.
- Provide configurable tax policies.

### Estate and Continuity Plugin

- Extend Nexa continuity capabilities.
- Coordinate designated long-term assets.
- Track continuity objectives.
- Support estate-related financial policies.
- Protect designated continuity funds from short-term optimization.

---

## Integration Architecture

CashOps shall maintain clear boundaries between intelligence, safety, strategy, orchestration, and execution.

**CashOps** provides personal financial optimization intelligence.

**PrePayGuard** provides obligation discovery, payment readiness, payment timing, prepayment analysis, payment protection, payment monitoring, and payment-risk controls.

**Nexa** provides long-term financial continuity and strategic financial objectives.

**Soluna Finance OS** provides financial orchestration and execution infrastructure.

The integrated model is:

Financial Data → CashOps Intelligence → PrePayGuard Validation → Nexa Strategic Constraints → User Policy Authorization → Soluna Orchestration → Authorized Execution

## Optimization Hierarchy

CashOps shall prioritize financial objectives in the following order:

- Fulfill mandatory obligations.
- Preserve required liquidity.
- Preserve principal according to user policy.
- Protect payment timing.
- Protect emergency reserves.
- Evaluate advantageous prepayment.
- Optimize risk-free or appropriately protected yield.
- Minimize fees and financial friction.
- Optimize taxes where configured.
- Advance short-term financial goals.
- Advance long-term financial objectives.
- Continuously reassess the financial state.

Incremental yield shall never automatically take priority over payment certainty or a protected liquidity requirement.

## Optimization Lifecycle

CashOps shall support the following operational lifecycle:

**Receive → Identify → Forecast → Reserve → Evaluate → Optimize → Validate → Move → Monitor → Reassess**

For obligations:

**Identify → Forecast → Fund → Evaluate Prepayment → Protect → Pay → Confirm → Reallocate**

For idle cash:

**Identify → Verify Liquidity → Compare Yield → Check Obligations → Check Prepayment → Validate With PrePayGuard → Allocate → Monitor → Reoptimize**

## Financial Decision Requirements

Before recommending or executing a material financial action, CashOps should determine:

- Current financial state.
- Current available balance.
- Purpose of the funds.
- Upcoming obligations.
- Required liquidity.
- Payment reserve requirements.
- Prepayment opportunities.
- Available yield opportunities.
- Transfer requirements.
- Settlement requirements.
- Fees.
- User policies.
- Long-term financial objectives.
- Relevant risks.
- Relevant uncertainties.
- Expected financial benefit.

## Execution Principle

**AI recommends. Deterministic rules validate. PrePayGuard protects. User policies authorize. Soluna orchestrates. Financial infrastructure executes.**

No AI-generated recommendation shall independently override:

- A payment-safety rule.
- A liquidity requirement.
- A principal-protection requirement.
- A user-defined restriction.
- A financial policy.
- A protected long-term objective.
- An execution authorization requirement.

## Vendor Neutrality

CashOps shall avoid unnecessary dependency on any single financial institution, financial product, data provider, execution provider, or technology vendor.

The specification should support:

- Multiple financial institutions.
- Multiple account types.
- Multiple financial data providers.
- Multiple execution providers.
- Modular yield data sources.
- Interchangeable plugins.
- User-controlled financial data.
- Provider-independent financial state representation.

## Local-First Design

Where practical, CashOps should support local-first financial intelligence.

The architecture should minimize unnecessary transmission of:

- Account information.
- Transaction information.
- Financial identities.
- Financial policies.
- Financial goals.
- Cash-flow history.
- Financial decision history.

Financial information should remain under user control wherever practical.

## Fail-Safe Requirements

CashOps shall fail safely when:

- Financial data is stale.
- Required financial data is unavailable.
- Account balances cannot be verified.
- Payment timing cannot be established.
- Transfer timing is uncertain.
- Settlement status is unknown.
- An obligation cannot be properly identified.
- A user policy cannot be evaluated.
- A required authorization cannot be verified.
- A financial institution is unavailable.
- A safety constraint cannot be evaluated.

When safety cannot be established, CashOps shall prefer waiting, preserving liquidity, or requesting human review over executing an uncertain financial movement.

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
  - [https://roxanneardary.com/cashops/](https://roxanneardary.com/cashops/)  

---

## License & Notice Requirements

CashOps is released under the **GNU Affero General Public License v3.0 or later (AGPL-3.0+)**.   
By contributing to any Open Arsenal project, you agree that your contributions will also be released under this license.

Please note the following:

- All contributions must comply with the **AGPL-3.0+** terms.  
- Under **Section 7** of the license, all redistributions, forks, and derivative works must preserve attribution to:  
  **Roxanne Ardary** and **[roxanneardary.com](https://www.roxanneardary.com/)**.
- CashOps specifications are free to use with attribution. A Specification Branding License can be negotiated upon request.
- The project's **notice.md** file tracks attribution requirements and contributor acknowledgments.   
  Any update that adds new contributors or modifies attribution should also update `notice.md`. 
- When submitting a pull request, ensure that any new files maintain the attribution headers where applicable.
- Network-deployed versions of this software must also remain fully AGPL-3.0+ compliant, including exposure of source code modifications when applicable under the license.

For full legal details, please refer to the AGPL-3.0+ license and the project's `notice.md` file.
